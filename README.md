[![Gitter](https://badges.gitter.im/dot-config/community.svg)](https://gitter.im/dot-config/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

# Use .config to store your project configs

The goal of dot-config is to promote standardization of `.config` folder
for storing project specific tool configurations.

By using a subfolder you will help **decluttering project root folder**
and **isolating configuration** from other project files.

Use of `.config` is based on long standing [XDG](https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html)
standard which promoted the use of `~/.config` for keeping **user settings**.
We only extended the concept to project repositories.

## Projects already supporting .config at repository level

- [molecule](https://molecule.readthedocs.io/en/latest/)
