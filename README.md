# App privacy policies

Each app gets its own directory. The directory is what the Play listing's
privacy policy URL points at, so it must keep working:

| App | Package | Policy URL |
|---|---|---|
| FamilyGM | `com.bjfhkj.familygm` | https://privacy.fenghongtech.cn/familygm/ |
| Wake Loop | `com.bjfhkj.wakeup` | https://privacy.fenghongtech.cn/wake-loop/ |

`privacy.fenghongtech.cn` is a Cloudflare Worker reverse proxy in front of this
repo's GitHub Pages site. GitHub Pages remains the origin, and the old
`https://sunorr007.github.io/appPrivacy-pages/...` URLs keep working. The Worker
source lives in `sunorr007/app-config/privacy-proxy`.

Existing app links and Play listings can stay on the GitHub Pages URLs; both
serve the same content.

## Adding an app

1. `mkdir <app-slug>/`
2. Drop `index.html` (language router), `<app-slug>-en`/`-zh` style pages, or a single `index.html` if the app only needs one language.
3. Push to `main`. GitHub Pages serves this repo from the branch root; the app is then automatically available at `https://privacy.fenghongtech.cn/<app-slug>/` without changing the Worker.

Keep the page self-contained: no external CSS, fonts or scripts. Policy pages must
render behind a captive portal and inside in-app WebViews.
