## Development

When starting the dev server, use background mode:

```
astro dev --background
```

Manage the background server with `astro dev stop`, `astro dev status`, and `astro dev logs`.

## Documentation

Full documentation: https://docs.astro.build

Consult these guides before working on related tasks:

- [Adding pages, dynamic routes, or middleware](https://docs.astro.build/en/guides/routing/)
- [Working with Astro components](https://docs.astro.build/en/basics/astro-components/)
- [Using React, Vue, Svelte, or other framework components](https://docs.astro.build/en/guides/framework-components/)
- [Adding or managing content](https://docs.astro.build/en/guides/content-collections/)
- [Adding styles or using Tailwind](https://docs.astro.build/en/guides/styling/)
- [Supporting multiple languages](https://docs.astro.build/en/guides/internationalization/)

## Project

Personal portfolio site, deployed to GitHub Pages (`https://Hualin-Ding.github.io`) by `.github/workflows/deploy.yml` on every push to `main`.

- Single page: `src/pages/index.astro` (content) inside `src/layouts/Layout.astro` (head, global styles, Gruvbox palette taken from the author's Ghostty config).
- `src/components/DotField.astro` holds the background canvas effect: a dot grid with a cursor trail that turns into fireflies when the mouse rests. Dots clear away over text; each of `nav`, `header`, `section`, `footer` is treated as one text zone. Tunables (`REST`, `IGN`, `R`, `G`) are at the top of that script.
- `.npmrc` points npm at the public registry because the global registry is a private Artifactory that needs auth.
- Keep contact details (phone, email) off the site; links are GitHub and LinkedIn only.
