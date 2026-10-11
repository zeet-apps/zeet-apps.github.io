# Zeet Apps site

Source of <https://zeet-apps.github.io/>, served by GitHub Pages straight from `main`. Each app has a home page and a
privacy policy at a fixed URL; those are the URLs entered in Google Play Console and App Store Connect and linked from
each app, so **do not rename the folders**.

| App | Home (base URL) | Privacy policy URL |
|---|---|---|
| Ragafy | <https://zeet-apps.github.io/ragafy/> | <https://zeet-apps.github.io/ragafy/privacy/> |
| Brain Boost | <https://zeet-apps.github.io/kids-brain-boost/> | <https://zeet-apps.github.io/kids-brain-boost/privacy/> |
| Music Note Trainer | <https://zeet-apps.github.io/music-note-trainer/> | <https://zeet-apps.github.io/music-note-trainer/privacy/> |
| ZeetRecall | <https://zeet-apps.github.io/recall/> | <https://zeet-apps.github.io/recall/privacy/> |

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
