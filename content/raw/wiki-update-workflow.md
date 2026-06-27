---
draft: true
---

# Wiki Update Workflow — Reference

How to update my notes and the live website after the initial setup.

**Live site:** https://edwchris.github.io/AI_wiki_site/

**Two repos, two jobs:**
- `AI_wiki` — my source notes (the thing I protect / version-control)
- `AI_wiki_site` — the published Quartz website (the Quartz folder at `C:\Users\c8edw\quartz`)

Obsidian, GitHub, and the website do **not** sync automatically. Each step below is manual.

---

## After I change notes

### 1. Back up the notes (version control)

1. Open **GitHub Desktop**.
2. It shows changed files in the `AI_wiki` repo.
3. Type a short summary (e.g. "Added notes on backpropagation").
4. Click **Commit to main**.
5. Click **Push origin**.

Nothing reaches GitHub until I push. Bundling a session's edits into one commit is fine.

### 2. Update the live website

The website uses a *copy* of my vault, so it doesn't see edits until I refresh that copy and re-publish.

1. Re-copy my updated vault into Quartz's `content` folder. Open Command Prompt and run:
   ```
   robocopy "C:\Users\c8edw\OneDrive - Queensland University of Technology\Research\_Obsidian\AI_wiki" "C:\Users\c8edw\quartz\content" /MIR /XD .obsidian .claude .git /XF .gitignore
   ```
   `/MIR` mirrors the source (picks up additions and deletions). `/XD` excludes Obsidian config, Claude config, and the git folder. This replaces the manual drag-and-drop.
2. Go to Quartz:
   ```
   cd C:\Users\c8edw\quartz
   ```
3. Build and publish:
   ```
   npx quartz sync
   ```
   (The `--no-pull` flag was only needed for the very first push — not needed now.)
4. Check the **Actions** tab in the `AI_wiki_site` repo — wait for the
   "Deploy Quartz site to GitHub Pages" run to go green (~2 min).
5. Site is updated.

---

## Preview the site locally (optional, before publishing)

From the Quartz folder:
```
npx quartz build --serve
```
Then open `http://localhost:8080` in a browser.
Stop the server with `Ctrl + C`.

---

## Key config facts (in case something breaks)

- Quartz config file: `quartz.config.yaml` (in the Quartz folder). v5 uses `.yaml`, not `.ts`.
- `baseUrl` must be: `edwchris.github.io/AI_wiki_site`
  (Wrong baseUrl = broken links pointing to the wrong path.)
- The deploy workflow lives at `.github/workflows/deploy.yml` and watches the **v5** branch.
- The workflow must include the **"Install Quartz plugins"** step
  (`npx quartz plugin install`) before the build — without it, the build fails with
  a `Could not resolve "../../.quartz/plugins"` error.
- Pages source must be set to **GitHub Actions** (Settings → Pages).

---

## Niggles I can fix later (not urgent)

- **Re-copy friction:** switching Quartz from "copy" to a **symlink** would make
  `content` always mirror my vault automatically (no manual re-copy). OneDrive can
  make symlinks fiddly, so this was deferred.
- **Dependabot noise:** Dependabot keeps opening pull requests in `AI_wiki_site`.
  Harmless. Can be disabled in repo Settings if it gets annoying.
- **Adding a second field/wiki:** repeat the Quartz setup, or combine multiple
  vaults into one site.
