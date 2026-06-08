# 🏷️ Luggage Tag — Deepak Krishna

A modern, animated luggage tag webpage designed to be linked via a QR code. When someone scans the QR code on the luggage tag, they land on this page and can instantly contact the owner via phone, WhatsApp, email, or find the address on Google Maps.

## ✨ Features

- **Glassmorphism card** with a frosted dark-teal glass effect
- **Animated rain background** — diagonal streaks mimicking a loading.io rain pattern, with white streaks falling faster than cyan ones
- **Teal blob layer** — soft glowing blobs drifting beneath the rain for depth
- **Subtle 3D tilt** on mouse movement
- **One-tap actions** for every contact method:
  - 📍 Address → opens Google Maps
  - 📞 Phone → dials directly via `tel:`
  - 📞 Alternate Phone → dials directly via `tel:`
  - 💬 WhatsApp → opens chat via `wa.me`
  - ✉️ Email → opens mail app with pre-filled subject line
- **JetBrains Mono** font throughout
- Fully self-contained — **single HTML file, zero build step, no backend**

## 📁 File Structure

```
luggage-tag/
└── luggage-tag.html     # The entire app — one self-contained file
```

## 🚀 Usage

### Option 1 — Open locally
Just open `luggage-tag.html` in any modern browser. No server needed.

### Option 2 — Host on GitHub Pages
1. Push `luggage-tag.html` to your repo (rename to `index.html` for root hosting)
2. Go to **Settings → Pages**
3. Set source to your branch and `/ (root)`
4. Your page will be live at `https://<your-username>.github.io/<repo-name>/`

### Option 3 — Any static host
Drop the file on Netlify, Vercel, Cloudflare Pages, or any web server — no configuration needed.

### Generating the QR Code
Point the QR code to your hosted URL. Free generators:
- [qr-code-generator.com](https://www.qr-code-generator.com)
- [goqr.me](https://goqr.me)

## 🔧 Personalisation

All personal details are in the HTML file. Search for these placeholders and replace:

| What | Where in the file |
|---|---|
| Profile photo | Replace the `<svg>` placeholder inside `.avatar-inner` with `<img src="your-photo.jpg">` |
| Name | `Deepak Krishna` and subtitle `Owner & Traveller` |
| Address + Maps link | The `href` on the address row and the display text |
| Phone | `href="tel:+919606713180"` and display value |
| Alternate Phone | `href="tel:+919480489375"` and display value |
| WhatsApp | `href="https://wa.me/919844667500"` and display value |
| Email | `href="mailto:..."` and display value |

## 📦 External Dependencies

Everything is loaded via CDN — **no npm, no installs, nothing to build.**

| Dependency | Version | How it's used | CDN |
|---|---|---|---|
| [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) | latest | All text on the page | Google Fonts |

That's it. The rain animation, blob background, glassmorphism card, and tilt effect are all written in **vanilla HTML, CSS, and JavaScript** — no canvas libraries, no animation frameworks.

## 🌐 Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). `backdrop-filter` (the blur/glass effect) requires a Chromium or WebKit-based browser; Firefox users will see a solid background instead.

## 📄 License

MIT — do whatever you want with it.
