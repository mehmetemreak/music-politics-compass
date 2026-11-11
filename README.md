# Music politics compass

A phone-first political compass of musicians, placed by what they have said, funded and campaigned for. People, not bands: a band is not a voter.

Phone-first, not phone-only: from 1024px wide the person's details sit in a side panel next to the chart instead of a sheet over it, and hovering a mark highlights that person's uncertainty and any shift in position.

**Status:** private while the sourcing pass runs. It goes public when the 100 best-known placements are sourced and zoom works well on a phone.

## How placements work

The axes follow [the Political Compass](https://www.politicalcompass.org) ([background and criticism](https://en.wikipedia.org/wiki/The_Political_Compass)). The chart borrows its axes, not its test or its placements.

### The axes

- **Economic (left/right):** state ownership, redistribution and public provision against free markets and private enterprise.
- **Authority (up/down), separate from economics:** one-party rule, censorship, the death penalty, nationalism and enforced moral codes against civil liberties and limits on state power. Backing the Soviet Union counts the same as backing an ethno-nationalist party. A big public sector on its own is not authoritarian.
- **Being offensive is not authoritarian, and being cancelled is not libertarian.** Neither saying shocking things nor being the target of a boycott, ban or blacklist moves a mark. What counts is what the person calls for.
- **Pressure outside the state counts, narrowly.** An act moves a mark towards authority only if all three hold:
  1. **A sanction, not criticism:** the person calls for someone to lose a job, a platform, a venue, a contract or legal status. Saying someone is wrong, or refusing to work with them yourself, is not a sanction.
  2. **Aimed at speech, belief or identity, not conduct:** demanding a festival drop an abuser fails this test; demanding it drop someone for their opinions passes.
  3. **Called for or organised by the person:** signing on to a campaign counts; being caught up in one does not.

  Weights: state power (laws, police, censorship) counts most, institutional pressure (employers, labels, platforms, radio) less, diffuse social pressure only when organised and sustained. States and their organs are not protected speakers: boycotting a country, a state broadcaster or a company over its policies (Sun City, BDS, Eurovision, Bud Light as a consumer) is not a sanction on speech. Organising others to punish a company for featuring someone because of who they are is. Apply the test the same way whichever side is calling for it; if a case would move one side's mark, the mirror case must move the other's.
- **Guns are a mild authority claim.** Backing gun regulation moves a mark 0.5 towards authority; backing gun rights moves it 0.5 away. It restricts access to an object, not speech or the body, so it weighs less than censorship or abortion law. It has no economic content: a gun stance moves `econ` only as a camp signal, and only where nothing economic is on record. Where gun rights already drive a placement (Killer Mike), it is not counted twice.
- **Bans on conduct are not speech.** Support for banning fox hunting or wildlife markets is animal-welfare law, not censorship, and does not move the authority axis on its own.
- **The axes measure fixed content, never "against whoever is in power".** Anti-establishment temperament is not a position: a person who always opposes the dominant side can sit anywhere. Place them by what they actually back.

### Evidence

- **Gate 1, attribution.** Is the person speaking as themselves? Lyrics count as first-person evidence only when the artist owns them: says the song is their view, performs it at rallies or picket lines, gives its proceeds to the cause or controls its use by campaigns, or writes in that line across a body of work. Characters, irony and stage personas (Bowie, Eminem) fail this gate, and so does a song the writer later disowns (Lydon on "Anarchy in the UK"). Lyrics are credited to whoever wrote them, not whoever sang them.
- **Gate 2, cost.** Weight follows what the evidence cost the person, not its category:
  1. Costly action: office held; prison, exile, bans or violence risked; years of organising; donations large relative to means; money refused (boycotts, withheld licences, a catalogue pulled from a platform).
  2. Sustained public work they stand behind: activism, an owned body of political songs, rally performances.
  3. Explicit self-description and specific policy statements.
  4. Single signals: one vote, one endorsement, a small donation, one remark, one signed open letter. Direction only: a placement resting on nothing stronger stays within 4 units of the centre on that axis, at low confidence.
  5. Stray interview remarks and lyrics that fail gate 1: context only, never move a mark alone.

  Ties go to the more specific claim, then the more consistent record. The current position uses the most recent evidence; an earlier one is kept as a shift.
- **Evidence is turned into a proposition first.** Before anything is placed, each item is restated as the claim it commits the person to on fixed content ("against conscription", "for common ownership of land"), and only that claim is scored. The same slogan can carry different claims in different decades: opposing the Vietnam war meant opposing the draft, an authority claim; opposing a war with no draft is a foreign-policy stance, which neither axis measures. Look for the coercion or ownership claim inside a stance (conscription, policing of protest, nationalising an industry, a call for sanctions) before treating it as a camp signal.
- **Camp signals are weak-to-medium evidence.** A stance that marks which side someone is on without committing them to a claim on either axis (Palestine or Israel, a war, Brexit, climate, Ukraine, backing a party or candidate, opposing Trump) can place a mark, with a ceiling: one camp signal gives confidence 1 on that axis and keeps the mark within 4 units of the centre; two or more independent ones give 2 at most. Independent means a different issue and a different event; Palestine and an anti-war march in the same campaign count once. Confidence 3 needs a direct proposition. Where direct evidence and a camp signal disagree, the direct evidence wins and the camp signal stays in `basis` as context. Camps correlate with positions but do not fix them: plenty of people oppose a war and back free markets.
- **Silence is not a position.** Attitudes common in someone's era are not scored unless the person argued for them. If they did call for coercion (criminalising, banning, deporting), it counts whatever the decade. This keeps today's values from being read into the silence of the past without excusing anyone who spoke.
- **Thin evidence widens the halo, not the pull to the centre.** Having little on record lowers confidence; it is not evidence of moderation. Not voting can itself be a position.
- **Influence does not count.** How far a song spread says nothing about how strongly its writer holds the view. The chart measures belief, not impact.
- **Economic evidence** means positions on taxes, wages, unions, public services, ownership or markets, or sustained campaigning for candidates whose platforms are mainly economic.
  - A single endorsement, a vote or a party preference gives `ce` 1 (a partisan proxy). Holding party office gives `ce` 2.
  - A scholar's or journalist's reading of the person's politics, with no first-person statement, gives `ce` 1 at most.
  - Mixed evidence that cancels out gives an evidenced 0, with the confidence the evidence earns, not `ce` 0.
  - Charity is not economic evidence. Neither is defending one's own copyright: copyright is a state-granted monopoly, not a free-market stance.
  - Private financial behaviour (tax exile, offshore accounts, overpaying tax) is not evidence of a position; what the person says about the economy outranks it. Tax avoidance by someone who calls for higher taxes is hypocrisy, not a different view.

### Confidence and halos

- `ce` (economic) and `ca` (authority) are each high (3, about ±1 unit), medium (2, ±1.5) or low (1, ±2.5). The halo is an ellipse with those two radii.
- `ce` 0 means no economic record and is drawn as ±5. Every current placement has `ce` ≥ 1; a new person should only be added with `ce` 0 after a real search has come up empty, and that should be said in `basis`.
- `confidence` is the overall rating used for the mark's fill and the filters. It currently equals `ca`; whether it should become the weaker of the two axes is an open decision.

### Shifts

- A shift is an earlier position, kept when the record shows a real change. It goes through the same two gates and gets its own `ce`, `ca`, `basis` and `sources`.
- **Solid or dashed:** the arrow is solid only if, on every axis it moves along by 1 unit or more, both ends are at least medium confidence. Otherwise it is dashed and the panel says it is weak. The page works this out from the data.
- The arrow shows where someone stood then and stands now, not why they moved. Do not read "sold out" or "stayed rebellious" into it; that is interpretation, not placement.
- Use dated labels (`"Pistols, 1977"`). Where the record has turning points, prefer the clearest earlier point over a vague era.

### Inclusion and the default view

- **Inclusion:** widely known, or a substantial political record. Cap of 200.
- **The starting 50 (default view)**, filled in this order. The page computes it from `data.json`, so the rule applies itself when the data changes.
  1. Everyone with a documented shift.
  2. The person furthest from the centre in each quadrant.
  3. **Ten with a costly political record** (`cost: 1`): held office, or were jailed, charged, attacked, exiled, banned or blacklisted for their politics. The ten most popular of them get in. This lane exists because English-language popularity alone kept out people like Fela Kuti, Víctor Jara and Nadya Tolokonnikova.
  4. The rest by **popularity**, skipping low-confidence placements, until there are 50.
- **Popularity** is the average of two ranks, so neither measure decides alone:
  - **Reach:** the number of Wikipedia language editions with an article on the person (from Wikidata), with English pageviews breaking ties. It counts every language equally and is stable from month to month. Summing pageviews across all editions was tried first; the Wikimedia APIs rate-limit that many calls from a browser, so it was dropped.
  - **Listeners:** Last.fm listeners. A band is not a voter, but listening happens to bands, so a person known through their band takes the larger of their own and their band's count (Morello uses Rage Against the Machine). This is used only for ranking, never for placement. Someone with no usable Last.fm count is ranked on reach alone.
  - Both measure fame, not belief, so neither affects where anyone sits. Spotify's monthly listeners are not used: they are not in its public API.
- **List view** can be sorted by either measure ("Most read", "Most listened").
- **Sourcing:** every placement needs at least one link. Placements without one are marked *not yet sourced* and are either sourced or removed before the site goes public.

## Adding a person: checklist

Work through this in order for every new entry, and for any re-check of an old one.

1. **Find the fastest source route first.** Wikipedia's API from a browser script (the `/w/api.php` parse or extracts endpoints) for the politics section and the whole article; then targeted searches. Pages that cannot be read (Reddit, paywalls) are noted for a human to open, not guessed at.
2. **Wikipedia link:** set `wiki` to the article title and `wsec` to the anchor of its politics heading, or `""` if there is none.
3. **List the evidence**, restate each item as the proposition it commits the person to, and run it through gate 1 (attribution) and gate 2 (cost). Drop personas, disowned songs and stray remarks from anything that moves the mark.
4. **Economic axis:** look for taxes, wages, unions, public services, ownership, markets, party office or sustained campaigning. Set `econ` and `ce` by the rules above; a single partisan signal keeps `econ` within 4 of the centre.
5. **Authority axis:** state power first, then the three-part test for pressure outside the state. Check for calls to ban, fire, deplatform, drop or blacklist someone, and for defences of others' speech. Apply the mirror test before moving a mark. Then sort what is left into direct propositions and camp signals, and cap confidence by the camp-signal rule if nothing direct remains.
6. **Shift:** is there an earlier, sourced position on fixed content that differs by a unit or more? If so, add `shift` with its own `ce`, `ca`, `basis`, `sources` and a dated `label`.
7. **Write `basis`** in one to three plain sentences: what they did, and how strong it is. Say when something is a single signal or context only.
8. **Sources:** at least one link per claim that moves a mark, primary or reputable press over aggregators. Set `checked` to today.
9. **Cost and popularity:** set `cost`/`costWhy` if the record shows office, prison, charges, violence, exile, bans or blacklists, sourced in `basis`. Fill `langs`, `lfm`, `lfmAct` with the same scripts used for everyone else (Wikidata sitelinks; Last.fm artist pages), so the new person is ranked on the same terms.
10. **Review:** open the person on the page, check the halo, the arrow (solid or dashed) and the panel text read correctly.

### Audits done

- **11 Nov 2026, economic record:** all 180 searched until every placement had an economic source; nobody is left at `ce` 0. Weakest: James Hetfield (a journalist's summary only).
- **11 Nov 2026, authority, pressure outside the state:** all 180 Wikipedia articles scanned for bans, boycotts, blacklists, deplatforming, petitions and censorship, then checked against the three-part test. Moved: Neil Young (−4 → −3, the Spotify ultimatum over Rogan). Context only, no move: Kid Rock, Travis Tritt and John Rich (Bud Light, 2023), Olivia Rodrigo (Kimmel letter). Excluded as boycotts of states or policy: BDS and Eurovision calls (Eno, Björk, Waters and others), Sun City. Excluded as conduct bans: fox hunting, wildlife markets.
- **11 Nov 2026, shifts:** all 11 earlier positions given their own confidence and sources. Solid: Novoselic, Peart, Sinatra, Seeger, Theodorakis. Dashed: Weller, Morrissey, Lydon, Mustaine, Minaj, M.I.A. Lydon's 1977 authority moved from −7 to −3 because it rested on a song he disowns; Morrissey's Smiths-era economics capped at −4.

- **11 Nov 2026, camp signals:** every `basis` scanned for war, Palestine, Brexit, climate, Ukraine, apartheid, party and candidate signals, then checked for a direct authority claim. Apartheid, anti-gay laws, policing, drug laws, guns, abortion, immigration enforcement and the death penalty count as direct claims, since they are about what a state does to its own people. 49 placements rested only on camp signals; a second pass (Wikipedia text scanned from a browser script, then targeted searches) found direct evidence for 44 of them, which was added to `basis` and `sources`. Still camp-only: Mike Love, Bryan Ferry and Frank Sinatra (post-1970 record) at authority confidence 1; Patti Smith and Björk at 2. Kanye West held at authority 4 because his direct record points both ways (anti-abortion, but funding police-brutality victims). The starting 50 came out unchanged.
- **11 Nov 2026, guns:** +0.5 authority for Grohl, Flea, Corey Taylor, Eminem, Cardi B, Grande, Isbell, Bon Jovi, Brandon Flowers, Steve Earle; −0.5 for Nugent, Johnny Ramone, Daniels, Greenwood, John Rich, Joe Perry, Hetfield. Killer Mike unchanged.

## Data

Everything lives in [`data.json`](data.json), one object per person:

| field | meaning |
|---|---|
| `name`, `band` | `band` is `"solo"` for solo artists |
| `genre` | `R` rock, `P` punk & new wave, `M` metal & hard rock, `O` pop, `H` hip-hop, `C` country, `F` folk/soul/reggae, `E` electronic |
| `start` | year the career began |
| `econ`, `auth` | position from -10 to +10 |
| `ce`, `ca` | confidence per axis: 3 high, 2 medium, 1 low; `ce` 0 means no economic record |
| `confidence` | overall rating for the fill and filters: 3, 2 or 1 |
| `basis` | one to three sentences on why |
| `shift` | optional earlier position: `econ`, `auth`, `label`, `ce`, `ca`, `basis`, `sources` |
| `sources` | list of `{title, url}`; `url` may be absent for print sources |
| `checked` | date the sources were last checked, or `null` |
| `wiki`, `wsec` | English Wikipedia article and the anchor of its politics heading (`""` if none) |
| `views` | English Wikipedia user pageviews, Nov 2025 – Oct 2026 |
| `langs` | number of Wikipedia language editions with an article on the person (Wikidata sitelinks) |
| `lfm`, `lfmAct` | Last.fm listeners and the act they were counted under (the person or their band, whichever is larger); `lfmChecked` is the date |
| `cost`, `costWhy` | `1` for a costly political record (office, prison, charges, violence, exile, bans, blacklists), with a few words saying what |

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
