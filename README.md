# Ukraine OSINT Archive — public information website

This repository contains **only** the public-facing homepage and privacy policy for a separate, single-user open-source evidence preservation utility.

- `index.html` — homepage and explanation of the workflow
- `privacy.html` — Google user data and OAuth authorization practices
- `styles.css` — standalone page styling
- `.nojekyll` — serve files unchanged with GitHub Pages

This repository intentionally contains **no** Google credentials, Google Drive files, private archive URLs, or research materials. The working archiver code remains in a separate **private** GitHub repository.

## Publish the GitHub Pages site

The current repository name accidentally starts with a leading hyphen (`-jklars92-star.github.io`). For a user homepage, open **Settings → General → Repository name**, change it to exactly `jklars92-star.github.io` (without the leading `-`), and confirm the rename.

After renaming, navigate to **Settings → Pages → Build and deployment → Deploy from a branch**. Select `main` and `/(root)` and click **Save**.

The expected public pages, **only after Pages deployment has succeeded**, are:

- https://jklars92-star.github.io/
- https://jklars92-star.github.io/privacy.html

Never enter these as Google OAuth app URLs until both pages load publicly in an incognito window.

## Google OAuth caveat

Google requires verified ownership of the domain used for a production OAuth app's homepage and privacy policy. Hosting on GitHub Pages does **not automatically** meet that ownership requirement. Google may reject a hosted GitHub subdomain. First test via Google Search Console URL-prefix verification; do not claim a completed Google domain authorization unless Google confirms it.

Daily archiving remains disabled until durable OAuth authorization is proven and an ordinary scheduled run with Drive readback has passed.
