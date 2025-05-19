# Authere: Your No-Nonsense Browser-Based TOTP Authenticator

Welcome to **Authere**, a lean, mean, TOTP-generating machine that lives in your browser. Think of it as an open-source love letter to [Aegis Authenticator](https://getaegis.app/), but without the app install or server nonsense. Built to run entirely on your device via GitHub Pages, Authere keeps your two-factor authentication (2FA) codes safe, simple, and accessible—because who has time for overcomplicated security apps?

## Why Authere?

- **No Server, No Problem**: Everything happens in your browser. No cloud, no backend, no "we've been hacked" emails.
- **Aegis-Compatible**: Import and export tokens in Aegis JSON format, so you can switch without losing your mind.
- **Lightweight & Open-Source**: Hosted on GitHub Pages, Authere is free, transparent, and ready for you to poke around in the code.
- **Dark Mode Vibes**: Clean, responsive design that’s easy on the eyes, even at 3 AM when you’re debugging your life.
- **Time Sync Smarts**: Checks your device’s time against the internet to keep TOTP codes accurate (because a 5-second drift is a 2FA death sentence).

## Features That Don’t Suck

- **Add Tokens**: Pop in your Base32 secret, issuer, and account name. Done. No PhD required.
- **Copy Codes**: Click or tap a code to copy it. A sassy "Copied!" tooltip confirms you’re not dreaming.
- **Import/Export**: Move tokens in and out with Aegis JSON or a simple text format. No lock-in here.
- **Edit & Delete**: Fix typos or yeet tokens you don’t need anymore. Your call.
- **Progress Bars**: Visual countdowns so you know exactly when your code’s about to expire.
- **Responsive Design**: Works on your phone, tablet, or that ancient laptop you refuse to retire.

## Getting Started

1. **Visit the App**: Head to [authere](https://authere.github.io)
2. **Add a Token**: Click "Add Token," enter your issuer (e.g., "Google"), secret (Base32, like `JBSWY3DPEHPK3PXP`), and optional account name. Hit save.
3. **Copy & Go**: Click the 6-digit code to copy it and paste it into your login. Feel like a hacker, but the legal kind.
4. **Import Tokens**: Got a backup from Aegis or a text file? Use the "Import" option in the settings menu (cog icon, top-right).
5. **Export Tokens**: Save your tokens as a JSON file or text for safekeeping. Don’t lose it—there’s no server to bail you out.

## Pro Tips

- **HTTPS Only**: Authere demands HTTPS for security. If you’re on HTTP (why?), it’ll yell at you. Localhost is cool for testing, though.
- **Time Sync Warning**: If your device’s clock is off by more than 5 seconds, you’ll see a red alert. Fix your clock or your codes might betray you.
- **Backup Your Tokens**: Authere uses `localStorage`, so if you clear your browser data or switch devices, your tokens vanish. Export them regularly.
- **No QR Codes (Yet)**: You’ll need to manually enter secrets for now. QR scanning might come later if we feel fancy.

## Security Notes (Because We Care)

- **Local Storage**: Tokens live in your browser’s `localStorage`. It’s convenient but not Fort Knox. Don’t store your life’s secrets here without a backup.
- **No Encryption (Yet)**: Exported JSON files are unencrypted, so keep them safe. We might add password protection if you beg nicely.

## Privacy & Open Source

- **Privacy Policy**: We don’t collect data because there’s no server. Your tokens stay in your browser.
- **Open Source**: Dive into the code at [authere](https://github.com/authere/authere.github.io).

## Known Quirks

- If `localStorage` is disabled (e.g., incognito mode), you’ll get an alert. Enable it or export your tokens elsewhere.

---

Built with ☕ and 🤓 by [0x0ut0].
