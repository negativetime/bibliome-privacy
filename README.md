# bibliome-privacy

Public Privacy Policy + Support page for the Bibliome app, hosted on GitHub Pages
(same pattern as `figmint-privacy`). One page, two anchors: `#privacy` and `#support`.

## Before publishing
- **Set a real support inbox.** The page uses `info@psychosonicconsulting.com`
  (your domain) — make sure mail to it reaches you (Cloudflare Email Routing on
  psychosonicconsulting.com can forward it), or swap in another address in `index.html`.

## Publish (GitHub Pages, ~2 min)
```
cd ~/Developer/bibliome-privacy
git init && git add -A && git commit -m "Bibliome privacy + support page"
gh repo create negativetime/bibliome-privacy --public --source=. --push
# then enable Pages from the default branch root:
gh api -X POST repos/negativetime/bibliome-privacy/pages -f source.branch=main -f source.path=/ 2>/dev/null || \
  echo "If that errors, enable Pages in the repo: Settings -> Pages -> Branch: main / root"
```

## URLs for App Store Connect
After Pages builds (a minute or two):
- **Privacy Policy URL:** `https://negativetime.github.io/bibliome-privacy/#privacy`
- **Support URL:** `https://negativetime.github.io/bibliome-privacy/#support`

(Both can also just be the base `https://negativetime.github.io/bibliome-privacy/`.)
A custom domain like `privacy.psychosonicconsulting.com` can be added later via
Pages → Custom domain.
