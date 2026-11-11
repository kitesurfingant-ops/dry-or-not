# Dry or Not

A private dry-day / drinks tracker for Ant and Jules, installed on the iPhone home screen and synced through Firebase Firestore.

- `index.html` – the whole app
- `config.js` – Firebase web config (public by design)
- `firestore.rules` – database rules: data lives under `households/<key>/`, reachable only with the key in each person's private link
- `icon-*.png` – home screen icon

Each person opens a private link of the form `https://kitesurfingant-ops.github.io/dry-or-not/#<ant|jules>.<key>` once, then adds it to the home screen. The key is not stored in this repo.
