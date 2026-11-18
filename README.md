# baaqmd.gov measured — RFI 2026-037 demonstration artifact

Independent measurement of the Bay Area Air Quality Management District public web
estate, prepared by MANSA LLC as a demonstration for RFI 2026-037 (Website
Modernization and Content Management System). Not affiliated with or endorsed by the
Air District.

Live: https://mansaj.github.io/baaqmd-website-modernization-demo/

## What it shows

1. **Measured inventory** — 26,871 sitemap entries, of which 25,362 (94.4%) are
   Sitecore authoring paths that soft-404 for visitors. Live public pages: 1,509.
2. **Disposition map** — all 1,509 pages classified keep / merge / archive / retire
   before any migration work: 594 keep, 183 merge, 726 archive, 6 retire.
3. **Structured records** — three real pages re-expressed as typed content records,
   with the JSON an API would return.

## Method

- `sitemap.xml` fetched from each domain on 2026-11-17; every `<loc>` counted.
- Authoring-path finding proven by 30 live requests (all soft-404 to `/utils/404`).
- Document count: 120-page random sample, all document links extracted and resolved;
  mean 2.38 document references per page; 45/45 sampled PDFs returned
  `application/pdf`.
- Figures that are extrapolations are labeled as such on the page.

Single static HTML document. No framework, no external requests.
