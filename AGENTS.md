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

Personal portfolio site, deployed to GitHub Pages (`https://Hualin-Ding.github.io`) by `.github/workflows/deploy.yml` on every push to `main`. See `README.md` for the overview.

- Single page: `src/pages/index.astro` (all content) inside `src/layouts/Layout.astro` (head, global styles, Gruvbox palette taken from the author's Ghostty config, and the `@media print` stylesheet).
- `src/components/DotField.astro`: background canvas (cursor trail that turns into fireflies when the mouse rests; click replays the ignition). Dots clear over text; each of `nav`, `header`, `section`, `footer` is one text zone. Tunables (`REST`, `IGN`, `R`, `G`) are at the top of that script.
- `src/components/StreamText.astro`: the hero streams in a few characters at a time with a following cursor (the full text stays in the DOM).
- `src/components/AgentTrace.astro`: looping mock agent runs; content is invented and generic.
- The résumé is not a file: the *resume* link calls `print()` and the print stylesheet formats the page (two pages, Letter). Keep it that way so the PDF never goes stale.
- The email address must never appear in the HTML or git history. It is stored reversed + base64 + split in `index.astro` and assembled only after a real click or while printing.
- Section headings use file-style names on screen (`about.md`, `stack.yaml`, ...) and plain names in print (`.fn` / `.pr` spans).
- `.npmrc` points npm at the public registry because the global registry is a private one that needs auth.
- Keep phone number and internal project or team names off the site. Contact is email (protected), LinkedIn and GitHub.
