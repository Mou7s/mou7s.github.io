# Repository Guidelines

## Project Structure & Module Organization
This repository is a small static site built with Vite, Vue 3, and Tailwind CSS. Application code lives in `src/`: `main.js` boots Vue, `App.vue` is the root component, and `style.css` loads Tailwind layers. The HTML entry point is `index.html`; it currently redirects visitors to `https://linktr.ee/mou7s`, so any UI work should account for that behavior first. Static public assets belong in `public/`. Build tooling is defined in `vite.config.js`, `tailwind.config.js`, and `postcss.config.js`.

## Build, Test, and Development Commands
Use `pnpm`; the lockfile is committed.

- `pnpm install` installs dependencies.
- `pnpm dev` starts the local Vite dev server at `http://localhost:5173`.
- `pnpm build` creates a production bundle in `dist/`.
- `pnpm preview` serves the built output locally for a final check.

Before opening a PR, run `pnpm build` to catch broken imports, invalid Vue syntax, or Tailwind config issues.

## Coding Style & Naming Conventions
Follow the existing style in this repo: ES modules, semicolons in `src/*.js`, and 2-space indentation in HTML, Vue, and config files. Prefer Vue 3 `script setup` for components. Name Vue components in PascalCase, keep utility styles in `src/style.css`, and avoid checking generated `assets/` output into feature branches unless the change is specifically about deployment artifacts.

## Testing Guidelines
There is no automated test framework configured yet. For now, treat `pnpm build` as the required verification step and manually test in `pnpm dev` or `pnpm preview`. If you add tests later, place them alongside the feature or under a dedicated `tests/` directory, and use clear names such as `App.test.js`.

## Commit & Pull Request Guidelines
Recent history favors short imperative commits, often with prefixes like `chore:` or direct verbs such as `update`. Prefer messages like `chore: update redirect target` or `feat: add landing page hero`. Keep pull requests focused, describe the user-visible change, link related issues when applicable, and include screenshots for any page or styling change. Call out explicitly if a PR changes redirect behavior in `index.html`.

## Deployment Notes
This is a GitHub Pages-style repository, so changes to the entry HTML and built output can affect production immediately. Verify links, titles, and asset paths before merging.
