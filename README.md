Setup script for Mac Books with a focus on web development in Angular.

This project is inspired by the wonderful people over at https://github.com/thoughtbot/laptop

It can be run multiple times on the same machine safely.
It installs, upgrades, or skips packages
based on what is already installed on the machine.

## Install

---

Download the script:

```sh
curl --remote-name https://raw.githubusercontent.com/nephi5/setup-script/main/setup
```

Review the script (avoid running scripts you haven't read!):

```sh
less setup
```

Execute the downloaded script:

```sh
sh setup 2>&1 | tee ~/setup-script.log
```

Optionally, review the log:

```sh
less ~/setup-script.log
```

## Debugging

---

Your last setup-script run will be saved to `~/setup-script.log`.
Read through it to see if you can debug the issue yourself.

## What it sets up

---

macOS tools:

- [Homebrew] for managing operating system libraries.

[homebrew]: http://brew.sh/

Unix tools:

- [Universal Ctags] for indexing files for vim tab completion
- [Git] for version control
- [OpenSSL] for Transport Layer Security (TLS)
- [RCM] for managing company and personal dotfiles
- [The Silver Searcher] for finding things in files
- [Tmux] for saving project state and switching between projects
- [Watchman] for watching for filesystem events
- [Zsh] as your shell

[universal ctags]: https://ctags.io/
[git]: https://git-scm.com/
[openssl]: https://www.openssl.org/
[rcm]: https://github.com/thoughtbot/rcm
[the silver searcher]: https://github.com/ggreer/the_silver_searcher
[tmux]: http://tmux.github.io/
[watchman]: https://facebook.github.io/watchman/
[zsh]: http://www.zsh.org/

GitHub tools:

- [GitHub CLI] for interacting with the GitHub API

[github cli]: https://cli.github.com/

## MacOs Customization

---

If you'd like to modify the look and feel of MacOs and change some of it's system settings you can run the `mac-customization` script.

Download the script:

```sh
curl --remote-name https://raw.githubusercontent.com/nephi5/setup-script/main/mac-customization
```

Execute the script:

```sh
sh mac-customization 2>&1 | tee ~/mac-customization.log
```

Check the file to make sure that the changes that are being made suit your needs.
