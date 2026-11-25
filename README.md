# App privacy policies

Each app gets its own directory. The directory is what the Play listing's
privacy policy URL points at, so it must keep working:

| App | Package | Policy URL |
|---|---|---|
| Wake Loop | `com.bjfhkj.wakeup` | https://sunorr007.github.io/appPrivacy-pages/wake-loop/ |

## Adding an app

1. `mkdir <app-slug>/`
2. Drop `index.html` (language router), `<app-slug>-en`/`-zh` style pages, or a single `index.html` if the app only needs one language.
3. Push to `main`. GitHub Pages serves this repo from the branch root.

Keep the page self-contained: no external CSS, fonts or scripts. Policy pages must
render behind a captive portal and inside in-app WebViews.
