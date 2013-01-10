shanes's dotfiles
==================
Focusing on Coffee-Script/Javascript Development

My fork of [@mjsrusso](http://github.com/mjrusso)'s dotfiles. ([Inspiration](http://zachholman.com/2010/08/dotfiles-are-meant-to-be-forked/))

installation
------------

    git clone git://github.com/shanejonas/dotfiles ~/.dotfiles
    cd ~/.dotfiles
    rake install
    vim +BundleInstall +qall

my setup
--------
- Vim +vundle +powerline +vim-coffee-script +syntastic +supertab
- Zsh +oh-my-zsh

Bonus: Emacs +evil-mode (vim-bindings) for the adventurous


additions
--------
###Adding syntax highlighting to zsh
* clone this repository into the
  [oh-my-zsh](http://github.com/robbyrussell/oh-my-zsh) plugins
directory (create it if its not there):

        cd ~/.oh-my-zsh/custom/plugins
        git clone git://github.com/zsh-users/zsh-syntax-highlighting.git

* Activate the plugin in `~/.zshrc` (in **last** position):

        plugins=( [plugins...] zsh-syntax-highlighting)

* Source `~/.zshrc`  to take changes into account:
    
        source ~/.zshrc

notes
-----

- **bin/**: Anything in `bin/` will be added to your `$PATH` and be made
  available everywhere.

- **topic/\*.sh**: Any files ending in `.sh` get loaded into your environment.

- **topic/\*.symlink**: Any files ending in `*.symlink` get symlinked into
  your `$HOME`. (These files get symlinked when you run `rake install`.)

  - symlinks can be generated in cases where these standard **topic/\*.symlink**
  symlink rules do not apply; see the `:install` task of the `Rakefile` for details.

- **.localrc**: Create a file called `.localrc` to store any data that you do
  not want committed to the git repository (secrets, etc.).

system
------

OS X, with the [Homebrew package manager](http://mxcl.github.com/homebrew/).

thanks
------

These dotfiles are heavily based on [Zach Holman's dotfiles](https://github.com/holman/dotfiles).

Also includes code from the following dotfiles:

- [Mathias Bynens](https://github.com/mathiasbynens/dotfiles)
- [Andrew Sardone](https://github.com/andrewsardone/dotfiles)
