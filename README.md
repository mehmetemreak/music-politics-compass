# Music politics compass

A phone-first political compass of musicians, placed by what they have said, funded and campaigned for. People, not bands: a band is not a voter.

Phone-first, not phone-only: from 1024px wide the person's details sit in a side panel next to the chart instead of a sheet over it, and hovering a mark highlights that person's uncertainty and any shift in position.

**Status:** private while the sourcing pass runs. It goes public when the 100 best-known placements are sourced and zoom works well on a phone.

## How placements work

The axes follow [the Political Compass](https://www.politicalcompass.org) ([background and criticism](https://en.wikipedia.org/wiki/The_Political_Compass)). The chart borrows its axes, not its test or its placements.

- **Economic axis (left/right):** state ownership, redistribution and public provision against free markets and private enterprise.
- **Authority axis (up/down), separate from economics:** one-party rule, censorship, the death penalty, nationalism and enforced moral codes against civil liberties and limits on state power. Backing the Soviet Union counts the same as backing an ethno-nationalist party. A big public sector on its own is not authoritarian. Being offensive is not the same as being authoritarian.
- **Evidence, gate 1: attribution.** Is the person speaking as themselves? Lyrics count as first-person evidence only when the artist owns them: says the song is their view, performs it at rallies or picket lines, gives its proceeds to the cause or controls its use by campaigns, or writes in that line across a body of work. Characters, irony and stage personas (Bowie, Eminem) fail this gate. Lyrics are credited to whoever wrote them, not whoever sang them.
- **Evidence, gate 2: cost.** Weight follows what the evidence cost the person, not its category:
  1. Costly action: office held; prison, exile, bans or violence risked; years of organising; donations large relative to means; money refused (boycotts, withheld licences).
  2. Sustained public work they stand behind: activism, an owned body of political songs, rally performances.
  3. Explicit self-description and specific policy statements.
  4. Single signals: one vote, one endorsement, a small donation, one remark. Direction only: a placement resting on nothing stronger stays within 4 units of the centre on that axis, at low confidence.
  5. Stray interview remarks and lyrics that fail gate 1: context only, never move a mark alone.

  Ties go to the more specific claim, then the more consistent record. The current position uses the most recent evidence; an earlier one is kept as a shift.
- **Thin evidence widens the halo, not the pull to the centre.** Having little on record lowers confidence; it is not evidence of moderation. Not voting can itself be a position.
- **Influence does not count.** How far a song spread says nothing about how strongly its writer holds the view. The chart measures belief, not impact.
- **Inclusion:** widely known, or a substantial political record. Cap of 200.
- **The starting 50 (default view):** everyone with a documented shift, the person furthest from the centre in each quadrant, then the most-viewed English Wikipedia articles (Nov 2025 – Oct 2026) until there are 50. The page computes this from `data.json`, so the rule applies itself when the data changes.
- **Confidence:** high (about ±1 unit), medium (±1.5), low (±2.5). The page draws that uncertainty.
- **Sourcing:** every placement needs at least one link. Placements without one are marked *not yet sourced* and are either sourced or removed before the site goes public.

## Data

Everything lives in [`data.json`](data.json), one object per person:

| field | meaning |
|---|---|
| `name`, `band` | `band` is `"solo"` for solo artists |
| `genre` | `R` rock, `P` punk & new wave, `M` metal & hard rock, `O` pop, `H` hip-hop, `C` country, `F` folk/soul/reggae, `E` electronic |
| `econ`, `auth` | position from -10 to +10 |
| `confidence` | 3 high, 2 medium, 1 low |
| `basis` | one or two sentences on why |
| `shift` | optional earlier position: `econ`, `auth`, `label` |
| `sources` | list of `{title, url}`; `url` may be absent for print sources |
| `checked` | date the sources were last checked, or `null` |
| `wiki`, `views` | English Wikipedia article and its user pageviews, Nov 2025 – Oct 2026 |

## Disputing a placement

Open an issue with the *Placement dispute* template and include a source. Newer, better-sourced statements usually win, but the final call is the maintainer's.

## Running locally

The page loads `data.json` with `fetch`, so serve the folder instead of opening the file directly:

```sh
python3 -m http.server
```

Then open http://localhost:8000.

## Later

Parked on 11 Nov 2026, with the reason each one is waiting.

- **Evidence-type tag on each source** (action, work, self-description, single signal, context), shown in the panel so a reader sees what a mark rests on. About 540 sources to tag by hand; worth doing before going public.
- **Render cost on low-end Android.** `draw()` rebuilds the whole points layer with `innerHTML` on every pan and zoom frame. Measure before changing anything: Chrome DevTools, 6x CPU throttle, All 180, halos and shifts on. If frames drop, move only a wrapper `<g>` with `transform` during a gesture and redraw labels and groups once when it ends. Do not switch to canvas: it would break keyboard and screen-reader access to the points.
- **Share cards and meta tags** (description, OpenGraph, Twitter card, a PNG card image). These only matter once the page has its own public address. The claude.ai shared page runs inside a frame, so link previews never read its tags. Waiting on two decisions: hosting (GitHub Pages needs the repo public, or a paid plan) and the final title ("Off Key: A Political Compass of Musicians" is a candidate, not confirmed).
