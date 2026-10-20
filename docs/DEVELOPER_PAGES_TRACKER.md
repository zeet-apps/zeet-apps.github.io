# Developer and ZeetRecall pages — 2026-10-19

| ID | Requirement / acceptance criteria | Status |
|---|---|---|
| WEB-001 | Home identifies Balaji Sivakumar as independent developer in Canada, retains all app links/contact, avoids blanket tracking claims and private identifiers. | Done |
| WEB-002 | Recall page explains current profiles, notes/tags/search, native sharing, local cleanup and ad/network limitations; keeps stable support/privacy URLs and avoids unverified store availability. | Done |
| WEB-003 | Validate HTML/links, responsive light/dark presentation; document evidence and checkpoint locally. No publication/push/store changes. | Done |

## Evidence and limits

- Python HTMLParser checks passed for both pages: one h1 each, developer identity present, every relative link resolves locally. `git diff --check` passed.
- Responsive max-width, viewport metadata, light/dark CSS retained; added email wrapping and keyboard focus outlines. No JavaScript, build tooling or analyzer/test suite exists in this static site.
- Browser visual verification remains pending: local-file URL rejected by browser policy; local server could not bind under sandbox. No workaround attempted. WEB-003 is complete for available static checks only; rendered mobile/desktop light/dark acceptance is still deferred.
- All four home app links and Recall privacy path preserved. No unverified store availability badges, government identifiers, private address or phone included. No site publication, push or store changes.
- Next: owner reviews copy; browser visual acceptance when available; publish only after explicit authorization.

## WEB-004 — Recall screenshot gallery (2026-10-19)

Requirement: show four verified current-widget scenes (Sources, Tags, Search, Notes) on the Recall home page with responsive sizing, descriptive alt text, captions and full-size links. Preserve privacy/support links. Use existing synthetic store artwork, no generation or fabricated screens. Acceptance: four images resolve and decode with correct intrinsic dimensions, optimized copies remain readable and existing URLs remain intact. Status: In progress.

WEB-004 complete: Python HTMLParser/Pillow validation passed (4 decodable 660×1434 WebP assets with alt text; every relative image/link target resolves); `git diff --check` passed. Source hashes recorded in recall/images/manifest.json. Existing verified artwork downsampled without cropping; CSS uses intrinsic aspect ratio, two desktop columns and one mobile column. Browser layout verification remains pending under the previously documented browser restriction. No store changes, push or publication in this slice.
