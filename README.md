# Kuwait Bridge Club — Join Page

Static registration website for GitHub Pages. No server or build step required.

## Publish

1. Create a **public** GitHub repository named `kbc-join` (or another name).
2. Upload `index.html` and `.nojekyll` to the root of `main`.
3. Repository **Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save**.
4. Test the GitHub Pages URL shown by GitHub (usually `https://USERNAME.github.io/kbc-join/`).
5. In **Settings → Pages → Custom domain**, enter `join.q8bridge.com` and click **Save**. GitHub creates the required `CNAME` file when publishing from a branch.
6. In GoDaddy DNS for `q8bridge.com`, add a **CNAME** record: **Host** `join`; **Points to** `USERNAME.github.io` (substitute your actual GitHub account or organization username; do not append `/kbc-join`). Do not change root `@` or `www` records.
7. Once DNS resolves, enable **Enforce HTTPS** in GitHub Pages.
8. Add a normal link on the GoDaddy site to `https://join.q8bridge.com`.

## Form testing

- Registration form sends a normal POST to FormSubmit for `info@q8bridge.com`.
- FormSubmit may email an activation message to that mailbox. Activate it before relying on registrations.
- Submit a test registration and check that it is received. No user registration is stored in GitHub Pages.
- WhatsApp invitation and YouTube video link are external destinations; confirm them on the deployed site.

## Included files

- `index.html` — entire webpage, styling and form.
- `.nojekyll` — prevents Jekyll processing.

No video or image files are required: the official KBC logo is fetched from the GoDaddy CDN and the video preview links to YouTube.
