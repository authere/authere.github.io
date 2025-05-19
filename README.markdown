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

1. **Visit the App**: Head to [autherest.github.io](https://autherest.github.io) (or wherever you’ve deployed this bad boy).
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
- **Sanitized Inputs**: We scrub all inputs to prevent XSS attacks, so hackers can’t sneak in naughty scripts.
- **CDN Dependencies**: We use `jsSHA` for TOTP math and Font Awesome for icons, pulled from Cloudflare’s CDN. They’re legit, but we’re considering SRI hashes for extra paranoia.

## Contributing

Love Authere? Hate it? Want to make it better? Fork the repo, tinker, and send a pull request. Ideas we’d love:
- QR code scanning for lazy token imports.
- Optional encryption for `localStorage` or exports.
- Support for 8-digit codes or funky TOTP algorithms (SHA-256, anyone?).
- Smoother animations using `requestAnimationFrame`.

Check the [issues](https://github.com/Autherest/autherest.github.io/issues) for what’s cooking or to report bugs. Be nice—we’re all just trying to make 2FA less painful.

## Privacy & Open Source

- **Privacy Policy**: We don’t collect data because there’s no server. Your tokens stay in your browser. [Read more](/privacy-policy).
- **Open Source**: Dive into the code at [github.com/Autherest/autherest.github.io](https://github.com/Autherest/autherest.github.io). It’s MIT-licensed, so go wild.
- **Contact**: Got questions or want to roast our UI? Hit us up at [/contact](/contact).

## Known Quirks

- If `localStorage` is disabled (e.g., incognito mode), you’ll get an alert. Enable it or export your tokens elsewhere.
- Time sync relies on `worldtimeapi.org`. If it’s down, codes might be off. We’re working on fallbacks.
- No token grouping or favorites yet. If you’ve got 50 tokens, good luck scrolling.

## Why “Authere”?

Because “Authenticator” was too long, and we thought it sounded cool. Also, it’s “there” for your authentication needs. Get it? *Wink.*

---

Built with ☕ and 🤓 by [Your Name or Handle]. Licensed under MIT. Now go secure your accounts like a pro.