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
