# Pill Diary — Ivory & Burgundy (free personal web app)

An ivory-cream and rich-burgundy iPhone-style medication log. **There are no reminders or notifications.** Instead, tap the outlined round pill with the vertical line on the Today card or next to a calendar date. A faint outline means **not logged** and a fully visible burgundy outline means **logged as taken**. Tap again to undo.

## To preview on your laptop

Open `index.html` in Chrome or Edge. It works without any account or paid tools.

For a local development server, open a terminal inside this folder and run:

```shell
python -m http.server 8000
```

Then open `http://localhost:8000`.

## To add it to your iPhone for free

Publish this folder on an HTTPS static hosting service such as GitHub Pages or Cloudflare Pages, open your new URL in Safari, use Share and **Add to Home Screen**. The exact Safari menu text can vary by iOS version. You do not need to pay Apple for a Developer Program membership to install an HTTPS web app this way.

## Your data

- This app uses `localStorage` and keeps your data in that particular browser/device.
- There is **no automatic synchronization** across devices.
- If you clear browser/site data, uninstall the web app, or lose the device, your records may be lost. Use **Settings → Download backup** regularly.
- Restoring a backup replaces the current data.
- Logged entries do not confirm medication was taken at the scheduled time; this is a self-reporting diary, not a medical or contraceptive guidance tool.
- No notifications, reminders, push subscriptions, analytics, third-party scripts, or external services are included.

## Files

- `index.html` – full interactive responsive UI, storage, calendar, history, settings.
- `manifest.webmanifest` – installable web app details.
- `sw.js` – service worker for caching when served over HTTPS or localhost.
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` – app icons.

You can rename "Desogestrel", change 8:00 AM, and choose your tracking start date in Settings.

## Open the project in VS Code

1. Unzip the downloaded project.
2. Open **Visual Studio Code** and choose **File → Open Folder**.
3. Select the `pill-diary-ivory-burgundy` folder.
4. Open `index.html`. To try the app immediately, right-click the file in File Explorer and choose **Open with → Chrome** or **Microsoft Edge**.
5. To develop locally with full PWA support, run `python -m http.server 8000` in the VS Code terminal, then visit `http://localhost:8000` in your browser.

No paid software, Node packages, or VS Code extensions are required.

## Colour palette

- Ivory cream: `#FFFCEF` (main background)
- Rich burgundy: `#80011F` (sampled from the supplied reference image; the printed `#2B5288` label in that image is not burgundy)
- Soft burgundy wash: `#F5E6E8` (selected states and cards)
- Light ivory: `#FFFEF7` (surfaces)

The outlined tablet icon has a **vertical** divider. It is faded if unlogged and fully opaque if logged.
