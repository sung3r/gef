# GDB Enhanced Features (a.k.a. GEF)

<p align="center">
  <img src="https://i.imgur.com/v3PUqPx.png" alt="logo"/>
</p>

`GEF` (pronounced ʤɛf - "Jeff") is a set of commands for x86/64, ARM, MIPS, PowerPC and SPARC to assist exploit developers and reverse-engineers when using old school GDB. It provides additional features to GDB using the Python API to assist during the process of dynamic analysis and exploit development. Application developers will also benefit from it, as GEF lifts a great part of regular GDB obscurity, avoiding repeating traditional commands, or bringing out the relevant information from the debugging runtime.

![gef-context](https://i.imgur.com/E3EuQPs.png)


## Instant Setup ##

Simply make sure you have [GDB 7.7 or higher](https://www.gnu.org/s/gdb) compiled with Python3 bindings, then:

```bash
# via the install script
$ wget -q -O- https://github.com/hugsy/gef/raw/master/scripts/gef.sh | sh

# manually
$ wget -O ~/.gdbinit-gef.py -q https://github.com/hugsy/gef/raw/master/gef.py
$ echo source ~/.gdbinit-gef.py >> ~/.gdbinit
```

Then just start playing:

```bash
$ gdb -q /path/to/my/bin
gef➤  gef help
```

_Note_: As of January 2020, GEF doesn't officially support Python 2 any longer, due to Python 2 becoming officially deprecated.
If you really need GDB+Python2, use [`gef-legacy`](https://github.com/hugsy/gef-legacy) instead.


## Highlights ##

A few of `GEF` features include:

  * **One** single GDB script.
  * Entirely **OS Agnostic**, **NO** dependencies: `GEF` is battery-included and is installable in 2 seconds (unlike [PwnDBG](https://github.com/pwndbg/pwndbg)).
  * **Fast** limiting the number of dependencies and optimizing code to make the
    commands as fast as possible (unlike _PwnDBG_).
  * Provides a great variety of commands to drastically change your experience in     GDB.
  * **Easily** extendable to create other commands by providing more comprehensible
    layout to GDB Python API.
  * Works consistently on both Python2 and Python3.
  * Built around an architecture abstraction layer, so all commands work in any
    GDB-supported architecture such as x86-32/64, ARMv5/6/7, AARCH64, SPARC, MIPS,
    PowerPC, etc. (unlike [PEDA](https://github.com/longld/peda))
  * Suited for real-life apps debugging, exploit development, just as much as
    CTF (unlike _PEDA_ or _PwnDBG_)

Check out the [Screenshot page](docs/screenshots.md) for more.

Or [try it online](https://demo.gef.blah.cat) (user:`gef`/password:`gef-demo`)


## Documentation ##

Unlike other GDB plugins, GEF has an extensive and up-to-date [documentation](https://gef.readthedocs.io/). Users are recommended to refer to it as it may help them in their attempts to use GEF. In particular, new users should navigate through it (see the [FAQ](https://gef.readthedocs.io/en/master/faq/) for common installation problems), and the problem persists, try to reach out for help on the IRC channel or submit an issue.


## Current status ##


| Documentation | License | Compatibility | Test validation |
|--|--|--|--|
| [![ReadTheDocs](https://readthedocs.org/projects/gef/badge/?version=master)](https://gef.readthedocs.org/en/master/) |  [![MIT](https://img.shields.io/packagist/l/doctrine/orm.svg?maxAge=2592000?style=plastic)](https://github.com/hugsy/gef/blob/master/LICENSE) | [![Python 3](https://img.shields.io/badge/Python-3-green.svg)](https://github.com/hugsy/gef/) | [![CircleCI status](https://circleci.com/gh/hugsy/gef/tree/master.svg?style=shield)](https://circleci.com/gh/hugsy/gef/tree/master) |


## Community ##

| IRC | Gitter | Slack | Discord |
|--|--|--|--|
| [![IRC](https://img.shields.io/badge/freenode-%23%23gef-yellowgreen.svg)](https://webchat.freenode.net/?channels=##gef) | [![Gitter](https://badges.gitter.im/gdb-gef/community.svg)](https://gitter.im/gdb-gef/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge) | [![Slack](https://img.shields.io/badge/Slack-GDB--GEF-blueviolet)](https://gdb-gef.slack.com) | [![Slack](https://img.shields.io/badge/Discord-GDB--GEF-yellow)](https://discordapp.com/channels/705160148813086841/705160148813086843) | 

## Contribute ##

To get involved, refer to the [Contribution documentation](https://gef.readthedocs.io/en/master/#contribution) and the [guidelines](https://github.com/hugsy/gef/blob/dev/.github/CONTRIBUTING.md) to start.

And special thanks to [Pedro "TheZakMan" Araujo](https://thezakman.tumblr.com/) for the logo!.


## Happy Hacking ##
