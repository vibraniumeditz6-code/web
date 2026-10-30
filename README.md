# PAUSE Website

A responsive, static landing page for the PAUSE desktop workspace. It uses plain HTML, CSS and JavaScript; no build step or package installation is required.

## Before publishing: connect the GitHub download button

Open `site-config.js` and set `repositoryUrl` to the public repository URL, for example:

```js
window.PAUSE_SITE_CONFIG = {
  repositoryUrl: "https://github.com/your-username/PAUSE"
};
```

All **Download PAUSE** buttons read from this one setting and open that repository in a new tab. Visitors can then choose **Code → Download ZIP** on GitHub. The site intentionally does not guess your repository URL.

## Preview locally

Open `index.html` in a browser, or run a local static server from this folder:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy with Vercel

1. Upload/push the contents of this `website` folder to your repository, keeping the `assets` folder and `site-config.js` beside `index.html`.
2. In Vercel, import the GitHub repository.
3. Set **Root Directory** to `website` if the folder is named `website` in the repository. If you put these files at the repository root, set Root Directory to `.` instead.
4. Set **Framework Preset** to `Other`.
5. Leave **Build Command** blank and set **Output Directory** to `.`.
6. Deploy.

## Important

This is a public marketing/download landing page, not a browser-hosted version of the PAUSE desktop app. The desktop app and browser extension still run locally. Never commit `.env` files, Gemini API keys, OAuth credentials, tokens, local databases or other secrets to a public repository. Rotate any secret that has already been exposed.
