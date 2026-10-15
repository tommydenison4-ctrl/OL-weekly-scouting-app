# Louisiana Tech · Week 7

October 17, 2026, from the existing Command Center schedule.

Depth chart: Ourlads posting updated 10/10/2026 9:08 AM ET. `depth-chart.json` is a local snapshot, not a PFF dataset or full official roster.

`upload-manifest.json` specifies proposed public Supabase Storage paths and filenames for the next upload. No folders, tables, files or permissions were created in Supabase. Edit storageBase and files to match the actual uploads; file values can be strings or arrays of candidate names. Reload checks this manifest and then each dataset independently. Missing files stay pending; prior opponents are never used as fallbacks. Play feeds must identify LATU in the appropriate offense/defense field and the 2026 season. The existing project uses LATU in its PFF feeds.

Verified Supabase source (bucket `Offensive Intelligence`, folder `Current/Louisiana Tech`):

- `play_feed-6.csv` — 362 plays across five 2026 games (338 playable snaps tagged `LATC`)
- `roster.json` — the Louisiana Tech roster
- `depth-chart.json` — Week 7 depth chart snapshot

The apps load the play feed dynamically; existing opponents remain intact.
