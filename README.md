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

The code is upgraded to newer version of Urwid (2.1.2) so it should be easily installed via pip or conda. 

The earlier code had a misfortunate naming of a local module as "notebook" which messes with jupyter installations. That is fixed, the module is renamed to tv_notebook.
