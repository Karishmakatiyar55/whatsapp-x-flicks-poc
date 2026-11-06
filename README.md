# Flam × Meta POCs

**Every brand surface should be interactive.** Interactive proofs of concept by Flam, showing Flicks (swappable, interactive videos) across Meta's apps. Each POC is a self-contained static page in its own folder, so each one can be hosted on its own.

| Folder | POC |
|---|---|
| `/` (root `index.html`) | **WhatsApp × Flicks**: chat messages, business profile, catalog, Status and the Business app's catalog manager |
| `facebook/` | **Flicks on Facebook**: Feed playable ad (Gap), Audience Network rewarded, Messenger reply-with-pick |
| `instagram/` | **Flicks on Instagram**: Stories playable, creator reel link in bio, story link sticker, partnership ad, Content Flicks in Reels (GRWM, MicroDrama) |
| `whatsapp-deck/` | **Flam × WhatsApp pitch deck** |

## Live site (GitHub Pages)

Served from the `main` branch. Every push to `main` updates the same address:

- WhatsApp POC: the site root, unchanged
- Facebook: `/facebook/`
- Instagram: `/instagram/`
- WhatsApp deck: `/whatsapp-deck/`

## Host each POC separately on Vercel

Create one Vercel project per POC, all from this repository:

1. Vercel → Add New → Project → import this repository.
2. Framework preset: **Other**. Leave the build command empty.
3. **Root Directory**: choose the folder: `facebook`, `instagram` or `whatsapp-deck`. Leave it at the root for the WhatsApp POC.
4. Deploy, then repeat for the next folder. Each project gets its own URL.

Every folder has its own `vercel.json`, so each project behaves the same on its own.

## Updating

Replace the `index.html` in the folder you are changing, then commit and push to `main`. The sites refresh within a minute or two.

Every page is self-contained (scripts, fonts and photos inlined). The Flicks, the Gap ad tag and the reel pages load live from their own sites, so present online.
