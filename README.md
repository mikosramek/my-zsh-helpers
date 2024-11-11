# My ZSH config

## Requirements

- [brew](https://brew.sh/)
- [oh-my-zsh](https://ohmyz.sh/#install)

## Theme

```shell
ZSH_THEME="half-life"
```

## Plugins

```shell
plugins=(git zsh-syntax-highlighting)
```

### zsh-syntax-highlighting

- [install guide](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)

```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

## aliases

```shell
# zsh config
alias _config="code /Users/xxx/.zshrc"
alias _refresh="source /Users/xxx/.zshrc"

# quick routes
alias _work="cd ~/Documents/work"

# git shorthands
alias gpo="git push origin"
alias branch="git checkout -b"

# others
alias running="netstat -vanp tcp | grep '*.'"
alias _ngrok="ngrok http --domain=<xxx> https://localhost:xxxx"
```

## functions

\_webpify ([install cwebp](https://www.npmjs.com/package/cwebp))

```shell
function _webpify ()  {
    cwebp -q 80 "$1" -o "$1.webp"
}
```
