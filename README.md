dorarep dotfiles
===================

Requirements
------------

Set zsh as your login shell:

    chsh -s $(which zsh)

Install
-------

Install [rcm](https://github.com/thoughtbot/rcm):

    brew tap thoughtbot/formulae
    brew install rcm

Install the dotfiles:

    env RCRC=$HOME/dotfiles/rcrc rcup

After the initial installation, you can run `rcup` without the one-time variable
`RCRC` being set (`rcup` will symlink the repo's `rcrc` to `~/.rcrc` for future
runs of `rcup`).

This command will create symlinks for config files in your home directory.
Setting the `RCRC` environment variable tells `rcup` to use standard
configuration options:

* Exclude the `README.md` and `LICENSE` files, which are part of
  the `dotfiles` repository but do not need to be symlinked in.
* Give precedence to personal overrides which by default are placed in
  `~/dotfiles-local`
* Please configure the `rcrc` file if you'd like to make personal
  overrides in a different directory

Update
------

From time to time you should pull down any updates to these dotfiles, and run

    rcup

to link any new files and install new vim plugins. **Note** You _must_ run
`rcup` after pulling to ensure that all files in plugins are properly installed,
but you can safely run `rcup` multiple times so update early and update often!

License
-------

License
MIT. see LICENSE.md file.
