# bstpub

Publicly hosted calendar feed for Paula Solé's (PS) blood-donation campaign schedule.

This repo holds nothing but the generated `.ics` file below. It's regenerated **in full,
every week**, by [`genera_ics.py`](https://github.com/paulasolsal/bst/blob/main/genera_ics.py)
in the private `bst` repo — never edit `calendari_bst.ics` here by hand, it will be
overwritten on the next run.

## Subscribe

Once GitHub Pages is enabled for this repo (Settings → Pages → Source: "Deploy from a
branch" → Branch: `main`, folder `/(root)` → Save), the feed is reachable at:

```
https://paulasolsal.github.io/bstpub/calendari_bst.ics
```

Add that URL (or its `webcal://` form, which most calendar apps recognize as a one-click
subscribe link) as a new calendar subscription in Google Calendar / Apple Calendar /
Outlook:

```
webcal://paulasolsal.github.io/bstpub/calendari_bst.ics
```

The calendar app will periodically re-fetch the URL and pick up whatever changed — no
import step needed after the first subscribe.

## What's in it

One event per campaign (date + location + `mati`/`tarda` session), timed as:

- `mati` → 08:00–14:00
- `tarda` → 15:00–20:00

(Europe/Madrid timezone.) Cancelled campaigns are kept but prefixed `[ANUL·LADA]` in the
title rather than silently dropped.
