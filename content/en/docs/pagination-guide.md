---
title: Pagination Guide
linkTitle: Pagination
weight: 20
description: How to test pagination on this site
---

This page explains how pagination is set up for testing.

## Configuration

In `hugo.yaml`, pagination is configured with 5 items per page:

```yaml
pagination:
  pagerSize: 5
  path: page
```

## Test content

The [Blog](/blog/) section has **12 dummy posts**. With 5 posts per page, you should see:

| Page | URL |
|------|-----|
| 1 | `/blog/` |
| 2 | `/blog/page/2/` |
| 3 | `/blog/page/3/` |

Each page shows Previous/Next navigation at the bottom.

## Verify on GitHub Pages

After deployment, visit:

- `https://maods2.github.io/docsy-test/blog/`
- `https://maods2.github.io/docsy-test/blog/page/2/`
- `https://maods2.github.io/docsy-test/blog/page/3/`

If all three pages load with correct navigation links, pagination is working.
