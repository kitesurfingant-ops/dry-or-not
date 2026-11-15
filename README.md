# Dry or Not

A private dry-day / drinks tracker for Ant and Jules, installed on the iPhone home screen and synced through Supabase (project `ant-data`, table `public.dry_docs`).

- `index.html` – the whole app
- `config.js` – Supabase URL and publishable key (public by design)
- The table is closed to the web; the app can only call `dry_list`, `dry_put` and `dry_del`, which need the household key from each person's private link
- `icon-*.png` – home screen icon

Each person opens a private link of the form `https://kitesurfingant-ops.github.io/dry-or-not/#<ant|jules>.<key>` once, then adds it to the home screen. The key is not stored in this repo.


## Updating
Bump `APP_VERSION` near the top of the script in `index.html` with every change. When the app opens, it fetches the live page fresh, and if the version differs it reloads onto the new one, so neither phone is stuck on a cached copy.
