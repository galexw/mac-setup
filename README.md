# zsh

The Z shell (also known as `zsh`) is a Unix shell that is built on top of `bash`
and that, since macOS 10.15 Catalina, is the **default** shell for macOS.
Since it has many with additional features, _if you have a version of macOS older than Catalina_,
it's recommended to use `zsh` over `bash`. In this case it's also highly recommended to install a framework with
`zsh` as it makes dealing with configuration, plugins and themes a lot nicer.

We've also included an `env.sh` file where we store our aliases, exports, path
changes etc. We put this in a separate file to not pollute our main
configuration file too much. This file is found in the bottom of this page.

Install `zsh` using Homebrew:

```sh
brew install zsh
```

Now you should install a framework, we recommend to use [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh)
or [Prezto](https://github.com/sorin-ionescu/prezto). **Note that you should
pick one of them, not use both.**

The configuration file for `zsh` is called `.zshrc` and lives in your home
folder (`~/.zshrc`).

## Oh My Zsh

[Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh) is an open source,
community-driven framework for managing your `zsh` configuration. It comes
with a bunch of features out of the box and improves your terminal experience.

Install Oh My Zsh:

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

The installation script should set `zsh` to your default shell, but if it
doesn't you can do it manually:

```sh
chsh -s $(which zsh)
```

### Configuration

The out-of-the-box configuration is usable but you probably want to customise
it to suit your needs. The [Official Wiki](https://github.com/robbyrussell/oh-my-zsh/wiki)
contains a lot of useful information if you want to deep dive into what you
can do with Oh My Zsh, but we'll cover the basics here.

To apply the changes you make you need to either **start new shell instance**
or run:

```sh
source ~/.zshrc
```

#### Plugins

Add plugins to your shell by adding the name of the plugin to the `plugin`
array in your `.zshrc`.

```sh
plugins=(git colored-man-pages colorize pip python brew macos)
```

You'll find a list of all plugins on the [Oh My Zsh Wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins).
Note that adding plugins can cause your shell startup time to increase.

##### zsh-syntax-highlighting

The Syntax Highlighting plugin adds beautiful colors to the commands you are typing.

Clone the zsh-syntax-highlighting plugin’s repo and copy it to the “Oh My ZSH” plugins directory.

```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

##### zsh-autosuggestions

This plugin auto suggests any of the previous commands. Pretty handy! To select the completion, simply press → key.

Clone the zsh-autosuggestions plugin’s repo and copy it to the “Oh My ZSH” plugins directory.

```sh
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

##### Enforce Changes

To apply the changes you make you need to either **start new shell instance**
or run:

```sh
source ~/.zshrc
```
