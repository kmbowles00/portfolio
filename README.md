# Katie Bowles: portfolio site (Quarto)

## Run locally in VS Code
1. Install [Quarto](https://quarto.org/docs/get-started/) and the **Quarto** VS Code extension (recommended automatically).
2. Open this folder in VS Code. In the terminal run: `quarto preview`
3. The site opens in your browser and reloads as you save.

## Fill in the placeholders
Search the project for `TODO` (Ctrl/Cmd+Shift+F). Key items:
- `_quarto.yml`: `site-url`
- `index.qmd`: photo (`images/`), LinkedIn and GitHub links, optional personal note
- `contact.qmd`: links; consider a resume PDF without your home address or phone
- `projects/wpi-dataviz-cultures/index.qmd`: role, motivation, findings, links

## Add a project
Copy `projects/_project-template/` to `projects/<new-name>/`, edit `index.qmd`, add a thumbnail. It shows up on the Projects page automatically.

## Publish to GitHub Pages
1. Create a GitHub repo and push this folder to the `main` branch.
2. Run once locally: `quarto publish gh-pages` (creates the `gh-pages` branch).
3. In GitHub: Settings > Pages > Source: **Deploy from a branch**, branch `gh-pages`, folder `/ (root)`.
4. After that, every push to `main` republishes automatically via `.github/workflows/publish.yml`.
5. Update `site-url` in `_quarto.yml` to your live URL.

If you later add Python/R code that runs on render, run `quarto render` locally and commit the `_freeze/` folder so CI doesn't need your environment.
