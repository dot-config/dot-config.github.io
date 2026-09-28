# Updating the website

Jekyll renders YAML tool entries into HTML and CSS. The published site needs no
JavaScript. Language filters use radio buttons and CSS `:has()`; older browsers
show every tool and hide the controls. Printing includes all tools.

## Local preview

Ruby is managed by mise and pinned in `.config/mise.toml`:

```sh
mise install
mise exec -- bundle install
mise exec -- bundle exec jekyll serve --livereload
```

Open <http://localhost:4000/>. Changes to data, HTML and CSS rebuild automatically.
Restart the server after editing `_config.yml`. Opening `index.html` directly
will not render the Liquid templates.

## Editing content

- Edit tool entries in `_data/tools.yml`.
- Edit page copy in `index.html`.
- Edit the table and filter templates in `_includes/`.
- Edit page styles in `assets/styles.css` and filter rules in `assets/filters.css`.
- Edit the favicon in `assets/favicon.svg`.

The table, language controls, counts and matching CSS update from the tool data.
Each entry contains a name, languages, description, paths and upstream reference.
Use `reference_label: Source` for implementation links, or `Docs` for documentation.
Add an optional `note` for qualifications such as version or scope restrictions.

Include implementation languages and supported formats or ecosystems. For example,
rumdl belongs to Rust, Markdown and Cross-language. Do not tag a language solely
because it is a config format. Reuse existing labels when possible.

Verify project-local discovery in upstream documentation or source. Accepting an
arbitrary configuration path through a flag alone does not qualify. Configuration
libraries belong in the maintainer guidance, separate from the tool list.

## Checking changes

```sh
mise exec -- bundle exec jekyll build --strict_front_matter
pre-commit run --all-files
```

Check desktop and mobile layouts, keyboard navigation, language filters and FAQ
disclosures in the local preview. The filters should work with JavaScript disabled.
The preview server injects a live-reload script; the published site has no scripts.
