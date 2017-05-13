# Dotfiles: Wrapped

This is my docker wrappers. I use docker **A LOT**, for everything, I am really impressed by [Jess Frazelle](https://github.com/jessfraz/dotfiles/blob/master/.dockerfunc) docker functions.

I usually work with docker-compose'd environment I need a way to simply run things with the same stack without writing very long command lines, so here is my take on that matter.

## Installation

### 1. Get the code

You can install this repository using either one of these method:

#### Using bootstrap script
    bash <(curl -sL https://raw.githubusercontent.com/aegypius/dotfiles-wrapped/master/bootstrap.bash)

#### Using homeshick

These dotfiles requires an additional castle to properly run:

```shell
homesick clone aegypius/dotfiles-docker
homesick clone aegypius/dotfiles-wrapped
```

### 2. Inject it in your environment

Then you need to update your `.bashrc` with the following code:

```shell
# Source everything in ~/bashrc.d {{{
if [ -d ~/.bashrc.d ]; then
  for script in ~/.bashrc.d/*; do
    test -f $script && source $script;
  done;
fi
# }}}
```

### See Also

  - [aegypius/dotfiles](https://github.com/aegypius/dotfiles-docker): My personal dotfiles canonical repository
  - [aegypius/dotfiles-docker](https://github.com/aegypius/dotfiles-docker): Docker helpers functions
