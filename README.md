# PythonMusic — documentation site

Source for **[pythonmusic.org](https://pythonmusic.org)**, the documentation and
example site for [PythonMusic](https://github.com/CreativePython/PythonMusic) — a
Python environment for making algorithmic music and visuals.

The library itself lives in a separate repository. This one holds only the site:
prose, the API reference, example programs, and audiovisual assets.

## What's here

| Path | Contents |
| --- | --- |
| `docs/` | All site content. `api/` is the API reference, `examples/` the chapter examples, `articles/` the longer writeups. |
| `docs/examples/_snippets/` | The example programs themselves (`.py`). Pulled into the example pages and bundled into a downloadable archive at build time. |
| `mkdocs.yml` | Site config and the full navigation tree. |
| `overrides/` | Theme customizations and three MkDocs hooks (see below). |

The API reference is **hand-maintained**. It was originally generated from the
library's docstrings, but is now edited directly. Any time a function signature
changes in the library, the matching page under `docs/api/` needs to be updated.

## Building the site locally

The docs build does not import PythonMusic, so you don't need the library
installed — just the site toolchain:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r docs/requirements.txt

mkdocs serve      # live preview at http://127.0.0.1:8000
mkdocs build      # render to site/
```

Two things are cached once per process and won't refresh during `serve`:
the examples archive and the release version/date. If you edit a file in
`_snippets/` or publish a new release, **restart `mkdocs serve`** to see the
change. `mkdocs build` always starts fresh.

### The hooks in `overrides/`

- `navtools.py` — nav rules shared by the mega-menu and the left sidebar. Marks
  each section's "Overview" page and handles divider entries.
- `zip_examples.py` — bundles `docs/examples/_snippets/` into
  `examples/PythonMusic_Examples.zip` at build time, so the download link always
  matches the current examples and no archive is committed.
- `release_info.py` — replaces `%%version%%` and `%%date%%` on any page with the
  latest release from the library repo, so the download page never quotes a
  stale version by hand. If GitHub can't be reached the build still succeeds and
  leaves the placeholders alone.

## Deploying

Pushing to `main` builds the site and publishes it to GitHub Pages
automatically (`.github/workflows/deploy-docs.yml`). You can also trigger a
rebuild from the Actions tab with the **Run workflow** button — useful for
picking up a new release without changing any content.

`docs/CNAME` holds the custom domain and is copied into the published site.

## License

This repository is deliberately split, because the writing and the example
programs are meant to be used in different ways.

**Prose, images, and audio — [CC-BY-NC-SA-4.0](LICENSE).** Share and adapt them, 
but only for non-commercial purposes, as long as you give credit and license 
your adaptations under the same terms.

**Example programs in `docs/examples/_snippets/` — [CC-BY-NC-SA-4.0](LICENSE).** 
Share and adapt them, but only for non-commercial purposes, as long as you 
give credit and license your adaptations under the same terms.

The PythonMusic library is licensed separately in its
[own repository](https://github.com/CreativePython/PythonMusic).

When attribution is required, please credit:

> PythonMusic documentation, by Bill Manaris, Taj Ballinger, and Marge Marshall
> — https://pythonmusic.org
