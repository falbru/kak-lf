# Kakoune lf

kakoune-lf is plugin for [Kakoune] text editor. It integrates [lf] file manager
as sidebar file browser.

![screenshot](screen.png)

## Installation

You have to have lf executable in PATH.

### Dependencies

**Only last stable versions of Kakoune and lf are supported**

- [lf][lf] file manager

### Installation

1. Install Kakoune plugin. Any of the following methods will do

- use [plug.kak] plugin manager
- load `lf.kak` from your kakrc: `source path/to/lf.kak`
- put `lf.kak` in your autoloads directory `~/.config/kak/autoload/`

## Usage

### Kakoune commands

- Open/close lf with `:lf` command.

- `:lf-follow` opens directory containing current buffer (or Kakoune's CWD if
buffer is not existing file) in runing lf instance

- `:lf-sync-cwd` opens Kakoune CWD in runing lf instance

### lf keys

- up / down <kbd>j</kbd> <kbd>k</kbd>
- parent directory <kbd>h</kbd>
- open file under cursor (and selected files if any) in Kakoune <kbd>l</kbd>
- select file <kbd>space</kbd>
- unselect all files <kbd>u</kbd>
- enter command <kbd>:</kbd>
- quit <kbd>q</kbd>

See lf documentation for more.

### lf commands

- `:lf-sync-cwd` change Kakoune's CWD to currently open directory

## Kakoune options

- `lf_follow` option to enable/disable changing lf path on Kakoune buffer change.
- `lf_openables` list of regexes that has to match mimetype of file opened from lf.
  This prevents opening binary files by accident.
