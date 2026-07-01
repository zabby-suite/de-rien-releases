# de-rien-releases

Public **version manifest** for [De Rien](https://github.com/zabby-suite/de-rien-v2)
(the app repo is private).

Self-hosted instances poll [`version.json`](./version.json) to detect when a
newer release is available and surface a *"new version available"* notice in the
admin area — the same way Dokploy flags updates.

`version.json` is updated automatically by the De Rien release pipeline on every
`v*` tag. **Do not edit it by hand.**

## `version.json` format

| field         | meaning                                                    |
| ------------- | ---------------------------------------------------------- |
| `version`     | latest published app version (semver, no leading `v`)      |
| `url`         | where to read the release notes / changelog                |
| `publishedAt` | ISO-8601 timestamp of the release                          |

The app fetches the raw manifest at:

```
https://raw.githubusercontent.com/zabby-suite/de-rien-releases/main/version.json
```
