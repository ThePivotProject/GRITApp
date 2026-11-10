THE GRIT - DEPLOY FOLDER - READY TO UPLOAD AS IS

WHAT IS IN HERE
- index.html = your GRIT page, background already embedded, works as is
- grit_icon.png = GRIT icon for home screen and link preview
- grit_icon-192.png / grit_icon-512.png = same icon for manifest
- background.jpg = your wall photo, also embedded in index.html
- manifest.json = makes Add to Home Screen use GRIT icon
- .nojekyll = tells GitHub Pages not to hide your files

HOW TO HOST - GITHUB PAGES (FREE)
1. Create a new repo on GitHub, e.g. grit
2. Upload ALL files in this folder to the repo root, not inside a subfolder
3. Go to Settings > Pages > Branch: main, Folder: /root > Save
4. Your link will be https://YOUR-USERNAME.github.io/grit/

HOW TO HOST - NETLIFY DROP (FASTEST)
1. Go to app.netlify.com/drop
2. Drag this whole folder onto the page
3. You get a live link instantly

IMPORTANT FOR LINK PREVIEW ICON
Before you share, open index.html and replace YOUR-DOMAIN.com in 3 places with your real domain, e.g. yourname.github.io/grit
- og:image
- og:url
- twitter:image
Then share. If an old preview is stuck, add ?v=2 to the end of your link when you send it.

SUPABASE
In the app, open Settings and paste your Supabase URL and anon key.
Table: grit_programs (id text primary key, data jsonb, updated_at timestamptz)
Realtime: alter publication supabase_realtime add table public.grit_programs;

COACH ROSTER
Coach button > create a 4-digit PIN first time.
Roster lives only on the coach phone behind that PIN.
Athletes opening their own link see only their own card, no roster.
Share = link only, no extra text.

SAVING
Saving is persistent in the browser for that program ID. With Supabase connected, the same card loads on both phones.
