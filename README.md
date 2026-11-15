# Dry or Not

A private dry-day / drinks tracker for Ant and Jules, installed on the iPhone home screen and synced through Supabase (project `ant-data`, table `public.dry_docs`).

- `index.html` – the whole app
- `config.js` – Supabase URL and publishable key (public by design)
- The table is closed to the web; the app can only call `dry_list`, `dry_put` and `dry_del`, which need the household key from each person's private link
- `icon-*.png` – home screen icon

Each person opens a private link of the form `https://kitesurfingant-ops.github.io/dry-or-not/#<ant|jules>.<key>` once, then adds it to the home screen. The key is not stored in this repo.

## Thai Spend (`/finance/`)

Shared expense and income log for Ant and Jules in Thailand, in the same Supabase project (tables `fin_entries`, `fin_categories`, `fin_fixed`, `fin_households`; summary view `fin_monthly_summary`).

- The tables are closed to the web; the app can only call `fin_config`, `fin_list`, `fin_put`, `fin_del`, `fin_apply_fixed` and `fin_save_config`, which need the household key
- Private link: `https://kitesurfingant-ops.github.io/dry-or-not/finance/#<ant|jules>.<key>` (the key is not stored in this repo)
