# e-invoicing.org — open dataset

A structured, machine-readable **summary** of the global e-invoicing
mandate tracker at **[e-invoicing.org](https://e-invoicing.org)** — status,
model, format, and issuing authority for 241 countries and territories,
plus 488 tracked mandate obligations (B2B/B2G, per flow and segment) with
effective dates and legal basis.

This is a teaser layer, not a mirror. The full curated write-up for each
country — executive overview, detailed legal basis, timeline, scope,
penalties, and primary sources — lives only at
**[e-invoicing.org](https://e-invoicing.org)**, along with live countdowns
to deadlines, interactive timelines, model explainers with diagrams, and
FAQs. Every record below links back to its live page.

## What this is (and isn't)

The underlying facts here are drawn from public government and tax-authority
sources — legislation, official announcements, gazette notices. They aren't
proprietary. What e-invoicing.org actually does, and what this repo
deliberately doesn't give you, is the ongoing work: continuously monitoring
~25 primary sources, filtering real regulatory change from noise, and
re-verifying and rewriting the full dossier for every affected country.
That full dossier content stays on the live site, not here — this repo
ships summary fields only, by design, not as an oversight.
**This snapshot goes stale the moment it's exported.** Treat it as a
pointer to the live site, not a replacement for it.

**Not tax, legal, or accounting advice.** Verify anything material against
primary sources or a qualified advisor before acting on it.

## Contents

```
data/
  meta.json            summary counts + export timestamp
  countries.json        all 241 countries, summary fields only
                         (status/model/format/authority/one-line summary)
  mandates.json         flat table: every tracked obligation row (flow, direction,
                         requirement, segment, status, effective_date, legal_basis...)
  models.json           the five e-invoicing model archetypes (4-corner/Peppol,
                         5-corner/DCTCE, clearance, CTC reporting, interoperability)
```

Full per-country dossiers (executive overview, detailed legal basis,
timeline, scope, penalties, sources) are intentionally **not** included —
those stay on the live site.

Every country record carries a `slug` — the live page is always
`https://e-invoicing.org/<slug>/`.

## Staying current

This snapshot is refreshed periodically, not continuously. For live change
tracking instead of a point-in-time export:

- **RSS**: https://e-invoicing.org/feed/
- **JSON Feed**: https://e-invoicing.org/feed.json
- **Change log (human-readable)**: https://e-invoicing.org/updates/
- **Live JSON API** (same data this repo mirrors, always current):
  `https://e-invoicing.org/api/v1/countries`, `/api/v1/mandates`,
  `/api/v1/countries/:slug`, `/api/v1/meta`

## License

[CC BY 4.0](LICENSE) — free to use, including commercially, with
attribution back to `https://e-invoicing.org`. See [LICENSE](LICENSE) for
the exact terms and suggested attribution text.

## Using this in your own project?

We'd like to know — open an issue or a PR. If you're building something in
the invoicing/compliance/ERP space, we're generally happy to talk.
