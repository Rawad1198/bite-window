# Bite Window

A fishing weather app: best times to fish, moon feeding times, wind, waves, tides and a 7-day outlook.
Live data from [Open-Meteo](https://open-meteo.com/) (free, no API key).

It is an installable web app (PWA): once it is hosted on HTTPS, phones and computers can install it
to the home screen, it opens full-screen with its own icon, and it keeps working with the last saved
forecast when there is no signal.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app (layout, styles, forecast logic) |
| `manifest.webmanifest` | App name, colours and icons used when installing |
| `sw.js` | Service worker that keeps the app available offline |
| `icons/` | App icons |

## Run it on this computer

```bash
python -m http.server 8765
```

Then open http://localhost:8765 in Chrome or Edge.

## Put it online (needed to install on a phone)

Any static host with HTTPS works. Upload this folder as-is, for example:

- **Netlify Drop**: drag the folder onto https://app.netlify.com/drop
- **GitHub Pages**: push the folder to a repository and turn on Pages for the main branch
- **Cloudflare Pages**: create a project and upload the folder

## Install it

- **Android (Chrome)**: open the site and tap **Install app**, or menu ⋮ → *Install app*.
- **iPhone (Safari)**: tap Share → **Add to Home Screen**.
- **Windows / Mac (Chrome or Edge)**: click the install icon in the address bar.

## Updating

After changing files, bump `VERSION` in `sw.js` (for example `bw-v2`) so installed copies pick up the new app files.
