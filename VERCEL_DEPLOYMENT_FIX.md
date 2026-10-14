# Vercel deployment (correct folder structure)

## Important
Keep this folder structure intact when uploading to GitHub. Do not move the files inside `api/` into the repository root.

- `index.html` and `wedding-hall-backdrop.webp` are at the project root.
- `api/` contains `_db.js`, `admin.js`, `rsvp.js`, and `wishes.js`.
- `vercel.json`, `package.json`, and `admin.html` are at the project root.

## Deploy
1. Extract this ZIP.
2. Upload the contents of this extracted folder to the root of your GitHub repository, preserving the `api` folder.
3. In Vercel, open the project connected to this repository. Under Settings → Build and Deployment, choose Framework Preset `Other`, leave Build Command blank, and make sure Root Directory is the repository root (not `api` or another subfolder).
4. Redeploy from Deployments → Redeploy (or push a new commit).
5. If using RSVP/wishes/admin features, set `DATABASE_URL` and `ADMIN_KEY` under Settings → Environment Variables, then redeploy.

The homepage should load at `/`; `/admin` rewrites to `admin.html`.
