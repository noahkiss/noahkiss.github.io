# noahkiss.github.io

This is the root GitHub Pages site for noahkiss. It serves as a directory listing for project repos.

## How GitHub Pages Routing Works

- **This repo** (`noahkiss.github.io`) serves at the root: `https://noahkiss.github.io/`
- **Project repos** with Pages enabled serve at: `https://noahkiss.github.io/{repo-name}/`
- Project repos take precedence over directories in this repo (so don't create directories here that match project repo names)

## Current Project Repos

Before creating a new project repo that will use GitHub Pages, check this list to avoid conflicts:

| Path | Repo | Description |
|------|------|-------------|
| `/tools/` | [tools](https://github.com/noahkiss/tools) | Single-file HTML tools |
| `/markshift/` | [markshift](https://github.com/noahkiss/markshift) | Text-to-Markdown conversion |
| `/quadcam-voices/` | [quadcam-voices](https://github.com/noahkiss/quadcam-voices) | QuadCam voice packs: index and previews |

## Adding a New Project Repo to GitHub Pages

1. **Create the repo** on GitHub (or push an existing local repo)

2. **Enable GitHub Pages** in the repo settings:
   - Go to Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main` (or `gh-pages` if you prefer)
   - Folder: `/ (root)` or `/docs` depending on structure

3. **Update this repo's index.html** to add the new project to the listing:
   ```html
   <li>
       <a href="/new-project/">
           <div class="project-name">new-project</div>
           <div class="project-desc">Brief description here</div>
       </a>
   </li>
   ```

4. **Update the table above** in this CLAUDE.md file

## Checking if a Path is Available

```bash
# Check if a repo name is already taken
gh repo view noahkiss/{name} 2>/dev/null && echo "Taken" || echo "Available"

# Or just check the table above
```

## Notes

- All project repos should have their own GitHub Pages configuration
- This repo should only contain the index.html landing page, not project content
- Keep project content in their respective repos to maintain clean separation
