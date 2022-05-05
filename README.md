# shopify-setup

My personal Shopify theme development setup

## Use below snippets to install tools for Shopify development on Debian/Ubuntu based distros

### Install basic tools
  
```sh
sudo apt install git curl zsh
sh -c "$(curl -fsSL  https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh )"
```

Set zsh as default and restart your session.

### Install themekit (for Shopify 1.0 themes)

```sh
curl -s https://shopify.github.io/themekit/scripts/install.py | sudo python
```

You can install python using below command if required.

```sh
sudo apt install python
```

### Install nvm to setup node

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash 
```

Check successful install using `nvm -v`. If you are not able to use nvm or get error for nvm not found, open `.zshrc` file using `code ~/.zshrc` and paste below lines at the end.

```sh
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

You can find latest version and install guide for `nvm` form [here](https://github.com/nvm-sh/nvm) 

### Install latest lts node version and set as default using nvm

```sh
nvm install --lts
nvm alias default node
```

### Install ruby and shopify-cli using ruby gem

```sh
sudo apt-get install ruby-full
sudo gem install shopify-cli
```
