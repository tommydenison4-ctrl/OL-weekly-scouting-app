ULM OL OPPONENT ENGINE

Files:
- index.html

DEPLOYMENT
1. Create a new GitHub repository for the OL engine.
2. Upload index.html to the root of the repository.
3. Import the repository into Vercel.
4. Framework preset: Other.
5. No build command is required.
6. Deploy.

DATA SOURCE
The app is already pointed at the same Supabase master opponent file used by the RB engine:
https://hzrosmevuejjlxigdxmg.supabase.co/storage/v1/object/public/rb-scout/current.csv

When current.csv is replaced, the OL engine will load the new opponent on refresh.

LOGIC
The target opponent is identified automatically as the team code appearing most often across pff_OFFTEAM and pff_DEFTEAM. The OL engine then analyzes rows where that team is pff_DEFTEAM.

CAM'S MODULES
- Fronts: Even / Odd / Special + exact front names
- Stunts: stunt frequency, situation and front
- Pressure: rush count, blitz / 5+, pressure, sack and unblocked pressure
- RB / TE indicators: uses directional information only when present in the source
- Personnel: offensive personnel faced, defensive personnel and packages
- 3rd Down: front, package, stunt, blitz and pressure tendencies
- Play Explorer: raw snap-level review

NOTE
PFF's pff_STUNT field identifies stunt snaps but does not always encode inside/outside direction. Likewise, exact to/away-from-RB or TE pressure direction is only reported where the source data provides enough side/directional information. The app labels unavailable directional data as Not charted rather than guessing.
