# Get this running on your iPhone (no Mac needed)

Regular Safari on iPhone doesn't allow webpages to use Bluetooth. **Bluefy**
is a free browser app that adds that capability, so this web app can behave
like a real app.

## Step 1 — Install Bluefy
Search "**Bluefy – Web BLE Browser**" in the App Store, or:
https://apps.apple.com/app/bluefy-web-ble-browser/id1492822055
Free, no account needed.

## Step 2 — Put `index.html` online (needs HTTPS)
Web Bluetooth only works over a secure (https://) connection, so the file
needs to be hosted somewhere — it can't just be opened from your Files app.
Easiest free option, no coding:

1. Go to https://github.com and create a free account (if you don't have one).
2. Create a new repository, e.g. named `scooter-app`. Make it **Public**.
3. Upload `index.html` into it (there's an "Add file → Upload files" button
   on the repo page — works fine from an iPhone browser).
4. Go to the repo's **Settings → Pages**, set Source to the `main` branch,
   root folder, and Save.
5. After a minute, GitHub gives you a URL like:
   `https://yourusername.github.io/scooter-app/`
   That's your app's live address.

(Netlify Drop or Cloudflare Pages work the same way if you'd rather use
those — any static HTTPS host is fine.)

## Step 3 — Open it in Bluefy
1. Open the Bluefy app.
2. Type or paste your GitHub Pages URL into its address bar.
3. Tap **Scan & Connect**, pick your scooter ("G100") from the list.

## Step 4 — Add it to your Home Screen (make it feel like a real app)
In Bluefy, use the Share button → **Add to Home Screen**. You'll get an icon
that opens straight into the app.

## Step 5 — Calibrate speed/battery
Same as before: watch the raw log while riding, compare against the
scooter's own display, and send me a few labeled samples (e.g. "battery
82%: `24 22 88 17 ...`") so I can fill in the real decode formula in the
`decode()` function near the bottom of `index.html`.

---

If GitHub feels like too much, tell me and I'll walk you through Netlify
Drop instead — it's literally drag-and-drop, no account required for a
one-off deploy.
