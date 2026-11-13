# Client preview

A password-protected preview page. The page itself is encrypted (AES-256-GCM, key from PBKDF2-SHA256, 600,000 iterations) in `payload.enc.json`. `index.html` is only the password gate; the browser decrypts the page after the right password is entered. The password is not stored in this repo.

## Rebuild

1. Put the full page in `source.html` (git-ignored; never commit it).
2. `node encrypt.mjs source.html '<password>'`
3. Commit and push `payload.enc.json`.
