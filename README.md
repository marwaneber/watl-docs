# Watl staff documentation

End-user documentation for restaurant staff, built with [Mintlify](https://mintlify.com).

Every screenshot in `images/` was captured from the running partner app with
real seeded data — a real restaurant, real staff accounts and six real orders.
When a screen changes, recapture rather than redraw.

## Preview locally

```bash
cd docs
npx mint@latest dev          # http://localhost:3000
npx mint@latest broken-links # link check
```

## Publish

Mintlify deploys from a Git repository — it cannot be published from this
machine alone. One-time setup:

1. Commit this `docs/` folder and push it to GitHub.
2. Create a project at [dashboard.mintlify.com](https://dashboard.mintlify.com).
3. Connect the repository and set the **content directory** to `docs`.
4. Install the Mintlify GitHub App when prompted.

After that every push to the default branch redeploys the site automatically.

## Structure

| File                 | Purpose                                        |
| -------------------- | ---------------------------------------------- |
| `docs.json`          | Site config — name, theme, colours, navigation |
| `index.mdx`          | Landing page                                   |
| `signing-in.mdx`     | Invitations, sign-in, where each role lands    |
| `order-statuses.mdx` | The seven statuses and who may change them     |
| `roles/drivers.mdx`  | Driver phone screen                            |
| `roles/managers.mdx` | Orders and Validator                           |
| `roles/owners.mdx`   | All six owner screens                          |
| `images/`            | Screenshots referenced as `/images/<name>.png` |

## Before publishing

- `docs.json` points **Open Watl** at `https://partner.bsahaa.com` — change it if
  that is not your production URL.
- `images/favicon.png` is a placeholder. Replace it with the real Watl mark.
- The cashier role is not documented yet.
