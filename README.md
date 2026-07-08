# Knowledge Node Prototype 001

A single-file static prototype (HTML/CSS/vanilla JS, no build step, no
framework, no backend) for testing the Knowledge Node UX — including the
full-screen YouTube video viewer.

## Deploying to Cloudflare Pages via GitHub

1. **Create a new GitHub repository**
   - On github.com, click "New repository"
   - Give it any name (e.g. `knowledge-node-prototype`)
   - Keep it Public or Private, doesn't matter for this test
   - Click "Create repository"

2. **Upload this file**
   - On the new repo's page, click "Add file" → "Upload files"
   - Drag in `index.html` from this folder
   - Click "Commit changes"

3. **Connect Cloudflare Pages to the repo**
   - In your Cloudflare dashboard, go to **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
   - Choose the GitHub repository you just created
   - Build settings: leave **Framework preset** as "None", **Build command** blank, **Build output directory** as `/` (or just leave default — there's nothing to build, it's a single static HTML file)
   - Click **Save and Deploy**

4. **Test the real, deployed link**
   - Cloudflare will give you a real `https://your-project.pages.dev` URL
   - Open that on your phone directly (not through any other site's preview/editor)
   - This will tell us definitively whether the full-screen video viewer bug was caused by oneclicklive.app's own preview wrapper, or by the code itself

## What this tests

- Sticky header with social icons
- Collapsible summary ("Read more")
- Video thumbnail → full-screen video viewer (X button, YouTube controls, Watch Again / Return to Node)
- Related Knowledge placeholder cards

No backend, no database, no build tools — just this one HTML file.
