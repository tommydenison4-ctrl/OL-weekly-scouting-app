Cameron Blankenship OL Weekly Scouting Engine v4

Dark-mode ULM build with a three-opponent toggle:
- UAB loads first
- Mississippi State remains available on the same screen
- Southeastern Louisiana is available as the third opponent tab
- Both complete play feeds are embedded in a local JavaScript dataset, so switching works when index.html is opened directly from Windows
- The actual maroon star ULM roundel is packaged in the assets folder
- index.html is now fully self-contained: the opponent data and roundel are also embedded directly in that one file for GitHub/Vercel deployment

This build is organized around Cam's exact questions:
1. Front: Even / Odd / Special
2. Stunt: Inside / Outside
3. Stunt: To / Away from RB
4. Blitz: Field / Boundary
5. Blitz: To / Away from RB and TE
6. Who is it? (most common blitz participants)
7. Formational triggers
8. Personnel matching and sub-packages
9. 3rd-down / special packages

The engine uses packaged weekly play feeds for UAB and Mississippi State.
Directional answers are shown only when the source data supports them; uncharted directional snaps are not guessed.

Deploy: replace the existing GitHub index.html with this index.html. Vercel should redeploy automatically.
