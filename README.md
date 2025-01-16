# Laus

Laus is a command-line tool to make it faster and more pleasant to work with [`launchd`](https://en.wikipedia.org/wiki/Launchd) by saving you from having to remember and retype long commands full of boilerplate. This is particularly useful when creating and testing new agents.

It helps to be at least marginally familiar with the `launchctl` grammar. Laus is a quality of life improvement for people frustrated with the ergonomics of running `launchctl` commands but it doesn’t replace it—every Laus action calls `launchctl` under the hood.

## Installation

Install with [Homebrew](https://brew.sh):

```shell
brew install vitorgalvao/tiny-scripts/laus
```

Alternatively, download the executable at the root of this repository and call it directly.

## Usage

```
Shortcuts for launchctl actions.

Usage:
  laus <action> <plist>
  laus <action> <bid>
  laus <action>

Actions:
  Long Name   Alias   Argument   Description
  ------------------------------------------
  bootstrap   s       plist      Load user job.
  bootout     o       plist      Unload user job.
  kickstart   k       plist      Run user job now.
  reload      r       plist      Run, in order: bootout, boostrap.
  rekick      rk      plist      Run, in order: bootout, bootstrap, kickstart.
  disable     di      bid        Disable user service (do not load on boot).
  enable      en      bid        Enable user service (activate on boot even if unloaded previously).
  status      st      none       Print disabled services.
  help        h       none       Show this help.

Options:
  -h, --help   Show this help.
```

## License

3-Clause BSD
