# Zeet Apps site

Source of <https://zeet-apps.github.io/>, served by GitHub Pages straight from `main`. Each app has a home page and a
privacy policy at a fixed URL; those are the URLs entered in Google Play Console and App Store Connect and linked from
each app, so **do not rename the folders**.

| App | Home (base URL) | Privacy policy URL |
|---|---|---|
| Ragafy | <https://zeet-apps.github.io/ragafy/> | <https://zeet-apps.github.io/ragafy/privacy/> |
| ZeetQuest: Quiz for All | <https://zeet-apps.github.io/zeetquest/> | <https://zeet-apps.github.io/zeetquest/privacy/> |
| Music Note Trainer | <https://zeet-apps.github.io/music-note-trainer/> | <https://zeet-apps.github.io/music-note-trainer/privacy/> |
| ZeetRecall | <https://zeet-apps.github.io/recall/> | <https://zeet-apps.github.io/recall/privacy/> |

`kids-brain-boost/` (the app's former name, Brain Boost) is kept only as a browser redirect to `zeetquest/` so old store and policy links keep working. It is not a separate app.

Landing page: <https://zeet-apps.github.io/> · Contact: zeetforfun@gmail.com

## Layout

```
index.html                  landing page listing the apps
<app>/index.html            app home page (also used as the store support URL)
<app>/privacy/index.html    privacy policy
```

## Updating

Pages are published from the apps' repos with the shared release tools (`release site publish`, see
`release-tools/docs`). Edit a page here only for a one-off fix, and keep the app's `store/` copy in sync.
When an app's data practices change (new SDK, ads, purchases, sync), update its privacy policy **before** the
release that ships the change.

Older standalone policy repos (for example `zeet-apps/journal_app_privacy_policy`) are superseded by the
`/<app>/privacy/` URLs above.

## Developer identity and ZeetRecall refresh

Local draft prepared 2026-10-19 on `codex/developer-and-recall-pages`: home identifies Balaji Sivakumar as the independent developer in Canada; Recall support page describes current local profiles, sharing, notes/tags/search, cleanup and advertising/network behavior. Stable URLs retained. See `docs/DEVELOPER_PAGES_TRACKER.md` for checks and pending visual acceptance. No deployment in this slice.

Recall sharing tutorials are in `recall/videos/`, embedded in the app page with captions, posters and optional GIF links. They show actual simulator UI with synthetic content, not physical-device release testing. Source/export provenance and separate store-preview drafts live in the journal_app repository under `release_notes/videos/` and `tool/video/`.
