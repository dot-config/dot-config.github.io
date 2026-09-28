# Let your tool find its config in `.config/`

Help projects keep their root directories clear by automatically discovering
your tool’s configuration in `.config/`. Keep your existing file format and
configuration locations—just support one more place to look.

The proposal is a shared directory convention. Each tool implements its own
lookup, so users can organize tool settings without adding custom paths to every
command, editor and CI integration.

The name is inspired by XDG’s user configuration directory, `~/.config/`.
Project-local `.config/` is independent of user settings and is not part of the
[XDG specification](https://specifications.freedesktop.org/basedir/latest/).

## Explore the proposal

- [Guidance for tool authors](https://dot-config.github.io/#authors)
- [Tools with automatic discovery](https://dot-config.github.io/#tools)
- [Questions and rationale](https://dot-config.github.io/#faq)

## Contribute

See [CONTRIBUTING.md](CONTRIBUTING.md) for local preview instructions using mise
and Jekyll, and guidance on updating the website. Tool entries live in
[`_data/tools.yml`](_data/tools.yml); the site generates the table and language
filters from that list.

To suggest a tool or discuss the proposal,
[open an issue](https://github.com/dot-config/dot-config.github.io/issues).
