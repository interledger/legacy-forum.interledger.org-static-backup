# Interledger Forum static archive

This repository contains a read-only static export of the Interledger Forum generated from the Discourse database backup captured on 2026-10-15.

The site was produced using the open-source tool at https://github.com/nolosb/discourse-static-archive. The generated archive is designed to be static-hosted on Netlify or any other web server that can serve plain HTML, CSS, and JavaScript files.

## Source backup

The original backup used to generate this archive was captured on 2026-10-15.

Backup folder: https://drive.google.com/drive/folders/1uFmazrg9Y1VsRqPXol8vjp-2JcD6Jys4

## Privacy and access restrictions

This archive intentionally contains only public, visible forum content. Direct messages and other private conversations are excluded from the generated site.

## Generated output

The generated static site lives in the `dist/` directory. Netlify is configured to publish from this directory via `netlify.toml`.

## Local testing

To test the site locally:

```bash
python3 -m http.server 8000 -d dist
```

Then open:

- http://127.0.0.1:8000/

## Search

The site includes a static, client-side search index generated with Pagefind. The index is stored under `dist/pagefind` and is served as part of the static site.

## Repository structure

```text
.
├── README.md
├── netlify.toml
├── dist/
│   ├── index.html
│   ├── pagefind/
│   └── ...
└── tmp/
    └── source backup archive(s)
```

## Notes

- This is a read-only archive; no forum backend is required to host it.
- The content is static, which makes it easy to deploy to Netlify, GitHub Pages, or a simple static web server.
