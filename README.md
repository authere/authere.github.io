# Authere: Browser-Based TOTP Authenticator

**Visit the App**: Head to [authere](https://authere.github.io)

- **No Server, No Problem**: Everything happens in your browser. No cloud, no backend, no "we've been hacked" emails.
- **Aegis-Compatible**: Import and export tokens in Aegis JSON format, so you can switch without losing your mind.
- **Lightweight & Open-Source**: Hosted on GitHub Pages, Authere is free, transparent, and ready for you to poke around in the code.
- **Dark Mode Vibes**: Clean, responsive design that’s easy on the eyes, even at 3 AM when you’re debugging your life.

## Security Notes (Because We Care)

- **Local Storage**: Tokens live in your browser’s `localStorage`. It’s convenient but not Fort Knox. Don’t store your life’s secrets here without a backup.
- **No Encryption (Yet)**: Exported JSON files are unencrypted, so keep them safe. We might add password protection if you beg nicely.

## Known Quirks

- If `localStorage` is disabled (e.g., incognito mode), you’ll get an alert. Enable it or export your tokens elsewhere.

---

Built with ☕ and 🤓 by [0x0ut0].
