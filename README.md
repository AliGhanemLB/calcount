# CalCount — Calorie Tracker PWA

A mobile-first calorie calculator and daily food log that works as a Progressive Web App.

## Features
- **Daily food log** with running calorie total and visual progress ring
- **BMR/TDEE calculator** using the Mifflin-St Jeor equation
- **Set a daily goal** manually or from the calculator result
- **Works offline** via service worker caching
- **Installable** on your phone home screen (iOS & Android)
- **Data persists** between sessions via localStorage (auto-resets each new day)

---

## Running locally on your phone

### Option A — Python (simplest, no install needed)
```bash
cd calorie-pwa
python3 -m http.server 8080
```
Then on your phone, open: `http://YOUR_COMPUTER_IP:8080`

Find your IP with:
- Mac/Linux: `ifconfig | grep "inet "` or `ipconfig getifaddr en0`
- Windows: `ipconfig` → look for IPv4 Address

> Both your phone and computer must be on the same Wi-Fi network.

### Option B — Node.js (npx, no install)
```bash
cd calorie-pwa
npx serve .
```

### Option C — VS Code Live Server extension
Install the "Live Server" extension, right-click `index.html` → "Open with Live Server", then visit the address on your phone.

---

## Installing to your home screen

**iOS (Safari):**
1. Open the app URL in Safari
2. Tap the Share button (box with arrow)
3. Scroll down and tap "Add to Home Screen"
4. Tap "Add"

**Android (Chrome):**
1. Open the app URL in Chrome
2. Tap the three-dot menu
3. Tap "Add to Home Screen" or "Install app"
4. Tap "Add"

Once installed, the app opens full-screen with no browser chrome, just like a native app.

---

## Files
```
calorie-pwa/
├── index.html      ← The entire app (HTML + CSS + JS)
├── manifest.json   ← PWA metadata (name, icons, colors)
├── sw.js           ← Service worker (enables offline use)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```
