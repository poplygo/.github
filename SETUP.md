# Poplygo org profile — setup

This folder is the `.github` repo for the **poplygo** GitHub organization. Its `profile/README.md`
renders as the org overview (the big README block on github.com/poplygo).

Style: playful neo-brutalist to match poplygo.tech (white panels, black borders, pixel/monospace
wordmark, light pink / green / blue speech-bubble tags). NOT the neon-yellow personal brand.

## Org created. Remaining browser steps

1. Org Settings → upload a square logo, set:
   - Name: `Poplygo`
   - Description: `Live Q&A and real-time polling for any audience. By Dynarq.`
   - URL: `https://poplygo.tech`  (use the exact domain you will verify, no www)
   - Location: your city
2. Verify the domain (green Verified badge). IMPORTANT: the URL shown on the profile must match a
   verified domain exactly. If the profile URL is `poplygo.tech`, verify `poplygo.tech`; a `www.`
   mismatch blocks the badge (this is what happened with Dynarq: profile was www.dynarq.com but only
   dynarq.com was verified).
   - Org Settings → Verified and approved domains → Add `poplygo.tech`
   - Add the TXT record GitHub gives you at your DNS provider, then click Verify.
   - Check propagation first: `nslookup -type=TXT _github-challenge-poplygo-org.poplygo.tech`

## Push this repo (after the org exists)

```
cd poplygo-org-profile
git init
git add -A
git commit -m "Poplygo org profile"
git branch -M main
git remote add origin https://github.com/poplygo/.github.git
git push -u origin main
```

The repo MUST be named `.github` and the file MUST live at `profile/README.md`, or the overview
will not pick it up.

## Popular repositories row

Transfer or create the real Poplygo repos under the org, then use "Customize pins" on the org
page to choose which show in the Popular repositories row.
