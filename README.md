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

## MacOs Customization (Experimental)

---

I have included some costumization, this however could break your System use it with care. By default these lines are commented out.

- Removing all dock items
- Persistently Showing all hidden files and folders in Finder
- Setting dock icon size to 36
- Only showing items in dock that are currently open

## Contributing

---

Edit the `setup` file.
Document in the `README.md` file.
Update the `CHANGELOG`.
Follow shell style guidelines by using [ShellCheck] and [Syntastic].

```sh
brew install shellcheck
```

[shellcheck]: http://www.shellcheck.net/about.html
[syntastic]: https://github.com/scrooloose/syntastic

### Testing your changes

Test your changes by running the script on a fresh install of macOS.
You can use the free and open source emulator [UTM].

Tip: Make a fresh virtual machine with the installation of macOS completed and
your user created and first launch complete. Then duplicate that machine to test
the script each time on a fresh install thats ready to go.

[utm]: https://mac.getutm.app
