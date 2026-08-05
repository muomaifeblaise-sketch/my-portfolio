# Muomaife Justin — Portfolio

Full-stack developer portfolio built with plain HTML, CSS, and JavaScript.

## Structure
- `index.html` — homepage (hero, about, services, projects, contact)
- `project.html` — live product demos (EMOL, TEMPLIX, PeaceSpot)
- `emol-demo.mp4`, `templix-demo.mp4`, `peacespot-demo.mp4` — screen
  recordings for the "See the products run" section. **Add these
  yourself** (see below) — they are not included here.

## Adding your screen recordings
The video cards in `project.html` are already wired up and just need
the files dropped into this same folder, named exactly:
- `emol-demo.mp4`
- `templix-demo.mp4`
- `peacespot-demo.mp4`

Once the files are present, the placeholder auto-hides and the video
plays. `.mp4` is recommended; `.webm` and `.mov` also work if you
update the `src` attribute in `project.html` to match.

**Keep videos small.** GitHub blocks files over 100MB outright and
warns above 50MB. Compress your recordings (e.g. HandBrake, or export
at 720p/30fps) — a 1–2 minute demo should comfortably fit under 20MB.

## Deploying

### 1. Push to GitHub
```bash
cd portfolio          # this folder
git init
git add .
git commit -m "Initial portfolio"
```
Then create a new empty repository on GitHub (github.com → New
repository — do NOT initialize it with a README), and run the two
commands GitHub shows you, which look like:
```bash
git remote add origin https://github.com/<your-username>/<repo-name>.git
git branch -M main
git push -u origin main
```

### 2. Deploy on Vercel
Easiest path — no CLI needed:
1. Go to vercel.com and sign in with your GitHub account.
2. Click **Add New → Project**.
3. Select the repo you just pushed.
4. Framework preset: choose **Other** (it's a static site, no build
   step needed).
5. Click **Deploy**.

Vercel will give you a live URL (e.g. `your-portfolio.vercel.app`)
within about a minute. Every time you `git push` after this, Vercel
redeploys automatically.

Alternatively, from the CLI:
```bash
npm i -g vercel
cd portfolio
vercel
```
Follow the prompts (link to your Vercel account, accept defaults).

### 3. Custom domain (optional)
In the Vercel dashboard → your project → **Settings → Domains**,
add your own domain and follow the DNS instructions shown.
