# dileepPDK123.github.io

Public policy pages for **Content Engine**, required by the Google Cloud OAuth consent screen and
the YouTube API compliance audit.

This repo is public **only** so that GitHub Pages will serve it on a free account. It contains no
source code — the Content Engine repo itself stays private.

## What it serves

| Path | File | Used for |
|---|---|---|
| `https://dileeppdk123.github.io/` | `index.html` | OAuth "Application home page" |
| `https://dileeppdk123.github.io/privacy` | `privacy/index.html` | OAuth "Privacy policy link" |
| `https://dileeppdk123.github.io/terms` | `terms/index.html` | OAuth "Terms of service link" |

Authorized domain to enter in the consent screen: `dileeppdk123.github.io`

## Why plain HTML

`.nojekyll` disables Jekyll entirely. Each page is a directory containing `index.html`, so the
extensionless URLs above resolve through ordinary static-file serving — no build step, no theme
dependency, and no ambiguity about whether `/privacy` or `/privacy.html` is the real address. A
404 on a policy link is a fast way to fail the audit.

## Setup

1. Create a **public** repo named exactly `dileepPDK123.github.io` under the `dileepPDK123` account.
2. Push this directory to its `main` branch.
3. **Settings → Pages** → Source: *Deploy from a branch* → Branch `main`, folder `/ (root)` → Save.
4. Wait a minute, then load all three URLs in a browser and confirm they render.
5. Verify `https://dileeppdk123.github.io/` in [Google Search Console](https://search.google.com/search-console)
   using the **HTML file** method — commit the verification file to this repo's root and push.

Keep the contact email here in sync with the OAuth consent screen and the audit submission.
