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

## WEB-005 — Supported shared links and precise privacy copy

2026-10-19: Explain supported social URL sharing, recognized sources versus Other and unavailable private-post previews; remove public ad-availability sentence. Validate local HTML/links and copy against app detector and AdRequest. No push authorized in this slice. Status: In progress.

WEB-005 complete: HTML parser/local link checks and whitespace validation pass; copy verified against app source detector and empty ad requests. Removed public availability sentence; clarified automatic SDK collection versus saved-content targeting and preview network requests. Browser visual checks not rerun for text-only changes. No push or deployment.

## WEB-006 — Consistent advertising disclosure (2026-10-19)

Requirement: align Recall home/privacy statements with SDK automatic collection, distinguish saved content from preview requests, avoid claiming denial stops all collection, and remove contradictory no-third-party/no-personal-data claims. Acceptance: both pages name the same categories/purposes, preserve links, and policy covers local profiles/cleanup. Local preparation only. Status: In progress.

WEB-006 complete: compared app AdRequest fields, startup/consent code, preview fetch and current Google Android/iOS disclosure documentation (2026-10-19). Both pages disclose matching categories and purposes; policy corrects blanket non-sharing claims, adds consent limitations, developer identity, local profiles/cleanup and support email processing. HTMLParser/local link/category checks and `git diff --check` pass. No executable changes or packet capture; no assertion that SDK traffic has been measured on a physical device. Provider references: https://developers.google.com/admob/android/privacy/play-data-disclosure and https://developers.google.com/admob/ios/privacy/data-disclosure . Browser visual review remains pending. No push or publication.

## WEB-007 — iPhone/Android sharing tutorial videos

2026-10-19: Owner requested genuine sharing tutorials for website and separate store assets; Android emulator selected. Waiting for capture before adding video players (no fake/missing media). Use captions, MP4 controls, preload=none and portrait max-width; no autoplay. Separate Apple in-app-only preview from source-browser/OS sharing tutorial. Status: Pending real footage.

WEB-007 complete locally: real iPhone Safari and Android Chrome MP4 tutorials embedded with controls, playsinline, preload=none, no autoplay, captions, posters and transcripts; optional GIF download links. Visible simulator/test-ad labels; example source is Other. Two responsive columns collapse below600px. All media/link checks passed, both H.264 clips fully decode, intrinsic dimensions and15–30s tutorial durations validated. Key-frame montages visually reviewed. Website publication is authorized by the owner's request to post these tutorials; mobile store configuration remains deferred.
