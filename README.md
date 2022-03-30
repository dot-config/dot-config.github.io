# Use .config to store your project configs

[![Gitter](https://badges.gitter.im/dot-config/community.svg)](https://gitter.im/dot-config/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

The goal of dot-config is to promote standardization of `.config` folder
for storing project specific tool configurations.

By using a subfolder you will help **decluttering project root folder**
and **isolating configuration** from other project files.

Use of `.config` is based on long standing [XDG](https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html)
standard which promoted the use of `~/.config` for keeping **user settings**.
We only extended the concept to project repositories.

![social-preview](https://repository-images.githubusercontent.com/449231631/31bc5be9-e2e4-409b-9b0e-f7bce50dfd7a)

## Tools already supporting .config at repository level

- [ansible-lint](https://github.com/ansible/ansible-lint)
- [doc8](https://github.com/PyCQA/doc8)
- [molecule](https://github.com/ansible-community/molecule)

## Q&A

### Do we really need yet another standard?

Dot-config is **not a new standard**, is just an extension of XDG one, one
that covers for projects directories in addition to user home directories.
