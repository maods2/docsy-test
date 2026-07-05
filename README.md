# Docsy Test Site

A [Docsy](https://docsy.dev) documentation site for testing deployment to [GitHub Pages](https://pages.github.com/).

**Live site:** https://maods2.github.io/docsy-test/

## Features

- Docsy theme via Hugo Modules
- Dummy documentation pages
- Blog section with 12 posts and pagination (5 per page)
- GitHub Actions workflow for automatic deployment

## Local development

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) (0.157+)
- [Go](https://go.dev/dl/) (for Hugo Modules)
- [Node.js](https://nodejs.org/) (LTS)

### Run locally

```bash
npm install
npm run serve
```

Open http://localhost:1313

### Build

```bash
npm run build
```

## Pagination test

The blog section at `/blog/` lists 12 dummy posts with 5 per page:

- Page 1: `/blog/`
- Page 2: `/blog/page/2/`
- Page 3: `/blog/page/3/`

See [Pagination Guide](content/en/docs/pagination-guide.md) for details.

## Deploy to GitHub Pages

1. Push this repo to GitHub
2. In **Settings → Pages**, set **Build and deployment → Source** to **GitHub Actions**
3. Push to `main` — the workflow builds and deploys automatically

The workflow sets the correct `baseURL` for `https://<username>.github.io/docsy-test/`.

## License

Apache-2.0
