# Terminal Velocity 3

Terminal Velocity 3 is a TUI application for managing plain-text notes.
It combines finding and creating notes in a single minimal interface and
delegates the note-taking itself to your `$EDITOR`.

![Terminal Velocity 3 Screencast](./tv3.gif)

The interface concept is taken from [Notational
Velocity](http://notational.net/).

This is an active fork of
[terminal-velocity-notes/terminal_velocity](https://github.com/terminal-velocity-notes/terminal_velocity)
and a port from Legacy Python to **Python 3**.

## Installation

### User site installation

This installs to `~/.local/`.  It doesn't need root privileges and keeps
your system-wide Python installation clean.  If you want to install
system-wide, drop the `--user` flag and prepend `sudo -H` to `pip3`.

```bash
git clone https://github.com/alperyilmaz/tv3
cd tv3
pip3 install --user .
cd ..
rm -rf tv3
```

### Installation in a Python virtual environment

The code currently depends on Urwid version 1.1.1 and isn't (yet) fully
compatible with more recent versions.  If you have other stuff depending
on a more recent Urwid in the same Python environment, you will get a
dependency conflict, because Python doesn't support multiple versions of
a package in the same environment.

The solution is to install TV3 in its own virtual Python environment and
symlink it to `~/.local/bin/` (or any other directory in your `$PATH`).
If you are a pythonista and familiar with the command line you probably
know how to do this.  Otherwise just follow these instructions.

```bash
bash
sudo -H pip3 install virtualenv
git clone https://github.com/alperyilmaz/tv3 ~/.tv3
cd ~/.tv3
virtualenv -p python3 env
env/bin/activate
pip3 install .
deactivate
mkdir -p ~/.local/bin/
ln -s ~/.tv3/env/bin/tv3 ~/.local/bin/
exit
```
