# RNA — Repositories Needing Attention

A landing page that tracks GitHub repositories needing attention across the [RobertsLab](https://github.com/RobertsLab) organization.

**Live site:** Enable [GitHub Pages](https://docs.github.com/en/pages) in repo settings (Settings → Pages → Source: Deploy from branch, Branch: `main`, Folder: `/ (root)`).

## How to update the repo list

All data lives in the `REPOS` array near the top of `index.html`. Each entry looks like:

```js
{
  owner: "RobertsLab",
  name: "repo-name",
  desc: "Short description of what needs attention.",
  tags: ["needs-review", "stale"]
}
```

### Available tags

| Tag | Meaning |
|---|---|
| `stale` | No recent activity, may need archival or cleanup |
| `needs-review` | Open PRs or branches waiting for review |
| `needs-docs` | Documentation is missing or outdated |
| `needs-update` | Code or analysis needs updating |
| `needs-tests` | Tests or CI pipeline need work |
| `archived` | Marked for archive, shown as dimmed |

Edit the array, commit, and the page updates automatically.
