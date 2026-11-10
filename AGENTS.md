# noahkiss.github.io

This is the root GitHub Pages site for noahkiss. It serves a directory listing of project repos.

## How GitHub Pages Routing Works

- **This repo** (`noahkiss.github.io`) serves at the root: `https://noahkiss.github.io/`
- **Project repos** with Pages enabled serve at: `https://noahkiss.github.io/{repo-name}/`
- Project repos take precedence over directories in this repo, so do not create a directory here that matches a project repo name.

## Project Repos

`index.html` lists every project repo that serves Pages under this domain, one `<li>` per repo.
Before you create a new repo that will use GitHub Pages, check that list and confirm the name is free:

```bash
gh repo view noahkiss/{name} 2>/dev/null && echo "Taken" || echo "Available"
```

## Adding a New Project Repo to GitHub Pages

1. **Create the repo** on GitHub (or push an existing local repo).
2. **Enable GitHub Pages** in the repo settings:
   - Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main` (or `gh-pages`)
   - Folder: `/ (root)` or `/docs`, depending on structure
3. **Add the project to `index.html`**:
   ```html
   <li>
       <a href="/new-project/">
           <div class="project-name">new-project</div>
           <div class="project-desc">Brief description here</div>
       </a>
   </li>
   ```

## Constraints

- Each project repo has its own GitHub Pages configuration.
- This repo holds only the `index.html` landing page and its assets, not project content.
