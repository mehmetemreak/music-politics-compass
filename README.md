# Off Key

**A political compass of musicians**, placed by what they have said and done, with the uncertainty drawn in.

**[Open the chart →](https://mehmetemreak.github.io/offkey-politics-compass/)**

191 musicians, from Woody Guthrie to Kneecap. Every placement has a written basis and at least one source; tap anyone on the chart to read them. Last full audit: 11 November 2026 ([log](METHODOLOGY.md#audits-done)).

## People, not bands

A band does not hold a view. Roger Waters and David Gilmour wrote the same records and disagree about most things, and John Lydon is not Joe Strummer. So each mark is one person, and members of the same band can sit far apart.

## What the axes measure

The chart borrows the two axes of [the Political Compass](https://www.politicalcompass.org), not its test or its placements, and the framework has [well-known critics](https://en.wikipedia.org/wiki/The_Political_Compass). The authority axis here is defined by coercion: what a person wants the state, or an organised group, to force on others.

| | Counts | Does not count |
|---|---|---|
| **Economic** (left–right) | Taxes, wages, unions, public services, ownership, markets | Charity, which is not economic evidence; private tax arrangements; defending one's own copyright |
| **Authority** (libertarian–authoritarian) | Censorship, policing, drug laws, immigration enforcement, the death penalty, backing for one-party states; calls for someone to lose a job, platform or venue over their views. Guns count lightly either way. | Being offensive; being cancelled; boycotting a state or company over its policies; bans on conduct such as fox hunting |
| **Neither, on its own** | | Which side someone takes on a war, a party, Brexit or Palestine. These "camp signals" can place a mark only at low confidence. |

The axes measure fixed content. Opposing whoever is in power is a temperament, not a position, and the same scale applies to 1940 and 2026.

## How strong the evidence is

Weight follows what a stance cost the person, not what kind of evidence it is:

1. **Costly action:** office held, prison, exile, bans, years of organising, money turned down.
2. **Sustained public work** they stand behind, including songs they own and perform at rallies.
3. **Explicit self-description** and specific policy statements.
4. **Single signals:** one vote, one endorsement, one remark. Direction only, never far from the centre.

Lyrics sung in character, and songs the writer later disowns, do not count. Silence is not a position. Each axis gets its own confidence (high, medium, low), drawn as a halo of ±1, ±1.5 or ±2.5 units. The full rules, with every edge case met so far, are in **[METHODOLOGY.md](METHODOLOGY.md)**.

## What a record looks like

All data is in [`data.json`](data.json), one object per person. John Lydon, shortened:

```json
{
  "name": "John Lydon",
  "band": "Sex Pistols",
  "econ": 2, "auth": 0.5,
  "ce": 1, "ca": 3,
  "basis": "Defended Brexit and Farage (2017) and voted for Trump (2020), while still talking up a borderless world.",
  "shift": {
    "label": "Pistols, 1977",
    "econ": -3, "auth": -3, "ce": 1, "ca": 1,
    "basis": "Rests mostly on 'Anarchy in the UK', which fails the attribution gate: Lydon says he is \"not an anarchist\"..."
  },
  "sources": [{ "title": "Dazed: Johnny Rotten defends Donald Trump, Brexit and Nigel Farage (2017)", "url": "https://..." }]
}
```

An earlier position is kept as a `shift` and drawn as an arrow, dashed when either end is low confidence. Every field is described in [METHODOLOGY.md](METHODOLOGY.md#data).

## Your taste

Enter a Last.fm username under the chart to see which of your top 1,000 artists are on it and where your listening sits on average, weighted by plays. A band's plays are split evenly among its members on the chart. That point shows where the musicians you play sit, not where you do.

## Disagree? Missing someone?

Open an issue with a source:

- **[Dispute a placement](https://github.com/mehmetemreak/offkey-politics-compass/issues/new?template=placement.yml):** which axis, where you think the person belongs, and a link to an interview, statement, filing or record. Disputes without a source are closed.
- **[Suggest a musician](https://github.com/mehmetemreak/offkey-politics-compass/issues/new?template=suggest.yml):** their economic and authority record, one source per claim.

Every case is checked the same way whichever side it favours: if it would move one side's mark, the mirror case must move the other's.

## Privacy

Visits are counted with [GoatCounter](https://www.goatcounter.com), which sets no cookies and collects no personal data. A Last.fm username is sent only to Last.fm and remembered only in your own browser.

## Run it locally

No build step and no dependencies. The page loads `data.json` with `fetch`, so serve the folder:

```sh
git clone https://github.com/mehmetemreak/offkey-politics-compass.git
cd offkey-politics-compass
python3 -m http.server
```

Then open http://localhost:8000.

## Credits

Inspired by [a reel](https://www.instagram.com/p/DfkCZ8VRQhA) by @mcantuzer. Listening data from [Last.fm](https://www.last.fm). Made by [@mehmetemreak](https://github.com/mehmetemreak); if it is useful to you, [help cover costs](https://github.com/sponsors/mehmetemreak).

## Licence

Code: [MIT](LICENSE). Data (`data.json`, including every `basis`): [CC BY 4.0](LICENSE-DATA.md). Reuse it freely, with credit to Off Key and a link back.
