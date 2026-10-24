# Steel Cutting Calculator (PWA)

## Publish for a permanent HTTPS link using GitHub Pages
1. Sign in to GitHub and create a **new public repository** named `steel-cutting-calculator`.
2. Upload all files/folders from this package to the repository root. Make sure `index.html`, `manifest.json`, `sw.js`, `.nojekyll`, and `icons/` are at the top level.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**; select branch `main` and folder `/(root)`, then Save.
5. Wait for GitHub Pages to publish. The link will look like `https://YOUR-USERNAME.github.io/steel-cutting-calculator/` (replace YOUR-USERNAME with your GitHub username). Do not use this example URL before publishing.
6. Open the published HTTPS link in Chrome on your Android phone. Tap ⋮ → **Install app** or **Add to Home screen**.

## Calculator formula
- Original weight = original length (ft) × kg per ft
- Cut length (ft) = cut length (mm) ÷ 304.8, capped at original length
- Cut weight = cut length (ft) × kg per ft
- Leftover weight = max(0, original length − cut length) × kg per ft
- Required customer amount = original stock value − scrap sale value + cutting + loading + unloading + paint + per-kg other cost + fixed costs
- Required rate = required customer amount ÷ cut material weight
- Suggested rate rounds up to the next whole Tk/kg.

This app is static and does not send calculation data to a server. It includes a service worker for offline use after the app has loaded once. GitHub Pages publishes public websites; do not put private business data in the repository.
