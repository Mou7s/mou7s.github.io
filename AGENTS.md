# Repository Guidelines

## Project Structure & Module Organization
This repository is intentionally minimal. The only runtime file is `index.html`, which redirects the root URL to `https://mou7s.com`. `README.md` explains the purpose of the repo, and `LICENSE` contains the project license. Avoid reintroducing build tooling or generated assets unless the repository scope changes.

## Build, Test, and Development Commands
There is no build step, package manager workflow, or test runner. Open `index.html` in a browser for a basic check, or push the change and verify the live redirect on GitHub Pages.

## Coding Style & Naming Conventions
Keep HTML simple and readable with 2-space indentation. Prefer standard platform features over JavaScript frameworks. If the redirect target changes, update every occurrence consistently in `index.html`.

## Testing Guidelines
Manual verification is sufficient: load the page and confirm it redirects to the intended URL. If JavaScript behavior changes, also verify the fallback link in the page body.

## Commit & Pull Request Guidelines
Recent history favors short, direct commits. Use messages such as `chore: update redirect target` or `docs: simplify repository docs`. Keep PRs narrow, mention the exact destination URL change, and include a screenshot only if the visible fallback page text changes.

## Deployment Notes
This is a GitHub Pages-style repository. Changes to `index.html` affect production immediately after deployment, so verify the final redirect target before merging.
