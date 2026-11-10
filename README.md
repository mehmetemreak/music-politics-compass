# Music politics compass

A phone-first political compass of musicians, placed by what they have said, funded and campaigned for. People, not bands: a band is not a voter.

**Status:** private while the sourcing pass runs. It goes public when the 100 best-known placements are sourced and zoom works well on a phone.

## How placements work

The axes follow [the Political Compass](https://www.politicalcompass.org) ([background and criticism](https://en.wikipedia.org/wiki/The_Political_Compass)). The chart borrows its axes, not its test or its placements.

- **Economic axis (left/right):** state ownership, redistribution and public provision against free markets and private enterprise.
- **Authority axis (up/down), separate from economics:** one-party rule, censorship, the death penalty, nationalism and enforced moral codes against civil liberties and limits on state power. Backing the Soviet Union counts the same as backing an ethno-nationalist party. A big public sector on its own is not authoritarian. Being offensive is not the same as being authoritarian.
- **Evidence order:** endorsements, donations, votes and offices held, then sustained activism, then self-description, then interviews. Lyrics count least.
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
