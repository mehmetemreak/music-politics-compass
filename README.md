# Music politics compass

A phone-first political compass of musicians, placed by what they have said, funded and campaigned for. People, not bands: a band is not a voter.

**Status:** private while the sourcing pass runs. It goes public when the 100 best-known placements are sourced and zoom works well on a phone.

## How placements work

- **Economic axis (left/right):** redistribution, unions and public provision against markets, low tax and business.
- **Authority axis (up/down):** nationalism, immigration restriction, moral regulation and state power against civil liberties, anti-censorship and anti-state positions. Being offensive is not the same as being authoritarian.
- **Evidence order:** self-description, then endorsements and donations, then sustained activism, then interviews. Lyrics count least.
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

## Disputing a placement

Open an issue with the *Placement dispute* template and include a source. Newer, better-sourced statements usually win, but the final call is the maintainer's.

## Running locally

The page loads `data.json` with `fetch`, so serve the folder instead of opening the file directly:

```sh
python3 -m http.server
```

Then open http://localhost:8000.
