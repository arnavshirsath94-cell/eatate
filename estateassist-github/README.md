# EstateAssist AI — GitHub package

This package contains the public website files and the original local Node.js prototype source. It does not include local database records, backups, or credentials.

## Publish the website with GitHub Pages

1. Create a GitHub repository and upload the contents of this folder.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and the `/docs` folder, then save.
4. Wait for GitHub to show the published website link in the Pages settings.

The published Pages site is a static website. Its appearance and guided sample conversation are included. Features that call the local server—AI-backed answers, saving contact requests, saved enquiries, admin queue, and agency workspace—need a separate backend and will not operate on GitHub Pages alone. Do not collect real personal information through this static demo.

## Run the original prototype locally

The source is in `local-source/`. Copy those files into one folder, then from that folder run:

```powershell
node server.js
```

Open `http://127.0.0.1:4174/`. Node.js 18 or newer is required. The server creates fresh local data files on first run. The local admin and agency pages have no authentication; keep them on your own computer and do not expose this server publicly.

## Package contents

- `docs/` — files selected for GitHub Pages.
- `local-source/` — original website, admin/agency UI and local Node server source.

The `data/` records, backups, and test scripts from the working project are intentionally excluded. No Wrangler/D1 configuration is included because this project has no Worker entrypoint or D1 migrations.
