# .dotfiles for Termux

Forked from [jooray](https://github.com/jooray/dotfiles), modified to work for [termux](https://github.com/termux/termux-app)

# Installation

**Warning:** If you want to give these dotfiles a try, you should first fork this repository, review the code, and remove things you don’t want or need. Don’t blindly use my settings unless you know what that entails. Use at your own risk!

### Using Git and the bootstrap script

You can clone the repository wherever you want. (I like to keep it in `~/Termux-dotfiles`) The bootstrapper script will pull in the latest version and copy the files to your home folder.

```bash
git clone https://github.com/dominee/Termux-dotfiles.git && cd dotfiles && source bootstrap.sh
```

To update, `cd` into your local `dotfiles` repository and then:

```bash
source bootstrap.sh
```

Alternatively, to update while avoiding the confirmation prompt:

```bash
set -- -f; source bootstrap.sh
```

### Git-free install

To install these dotfiles without Git:

```bash
cd; curl -#L https://github.com/dominee/Termux-dotfiles/tarball/master | tar -xzv --strip-components 1 --exclude={README.md,bootstrap.sh,LICENSE-MIT.txt}
```

To update later on, just run that command again.

### Specify the `$PATH`

If `~/.path` exists, it will be sourced along with the other files, before any feature testing takes place.

Here’s an example `~/.path` file that adds `/usr/local/bin` to the `$PATH`:

```bash
export PATH="/usr/local/bin:$PATH"
```

### Apt setup

Simple installer for APT packages that use this dotfiles, and that make your life easier ;]

```bash
./apt.sh
```


### Add custom commands without creating a new fork

If `~/.extra` exists, it will be sourced along with the other files. You can use this to add a few custom commands without the need to fork this entire repository, or to add commands you don’t want to commit to a public repository.

My `~/.extra` looks something like this:

```bash
alias moo='fortune | cowsay'
```

You could also use `~/.extra` to override settings, functions and aliases.
You can also use `~/.gitconfig.local` and `~/.vimrc.local`.

## Feedback

Suggestions/improvements [welcome](https://github.com/dominee/Termux-dotfiles/issues)!


## Thanks to…
* [Juraj Bednar](https://juraj.bednar.sk/) and his [dotfiles repository](https://github.com/jooray/dotfiles) 
* [Termux](https://termux.com/) / [termux=app repository](https://github.com/termux/termux-app) for a great Android terminal emulator and Linux environment
* all the authors and contributors from all the dotfiles projects
* you =]
