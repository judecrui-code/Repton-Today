# Repton Today — video site

A blue, single-page video site for the Repton Today podcast. Anyone can watch; only team members can log in to upload or delete videos. Everything is stored in this GitHub repo.

## Set it up (about 5 minutes)

1. **Make a repo** on GitHub, e.g. `repton-today` (public, so visitors can watch).
2. **Upload these files** to it: `index.html`, `videos.json`, and an empty `videos/` folder isn't needed — it's created on the first upload.
3. **Edit `index.html`** — near the bottom, fill in:
   ```js
   const CONFIG = {
     owner:  "your-github-username",
     repo:   "repton-today",
     branch: "main"
   };
   ```
4. **Turn on GitHub Pages**: repo → Settings → Pages → Source: *Deploy from a branch* → `main` / root → Save.
   Your site will be live at `https://your-github-username.github.io/repton-today/`.

## Who can log in

Login = having **write access to the repo**. Add each Repton Today team member under repo → Settings → Collaborators. Nobody else can upload, even if they find the login button.

Each team member makes their own token once:
1. Go to https://github.com/settings/personal-access-tokens/new
2. Repository access → *Only select repositories* → pick the Repton Today repo
3. Permissions → **Contents: Read and write**
4. Generate, copy, paste it into **Team login** on the site.

(If the repo belongs to an organisation, the org may need to allow fine-grained tokens.)

## Uploading

- **Upload file** — drops the MP4 into `videos/` in the repo and adds it to the library. Max **100 MB** per file (GitHub's limit). Export reels/episodes as MP4, H.264.
- **GitHub link** — paste a link to a video already on GitHub (e.g. `https://github.com/user/repo/blob/main/ep1.mp4`); it's converted to a playable link automatically.
- New uploads show for the team instantly and for everyone else after GitHub Pages rebuilds (~1–2 min).

## Limits to know

- GitHub Pages sites should stay under ~1 GB total. For long full episodes, keep files compressed or host big ones in a separate repo and use the GitHub link option.
- Tokens are saved only in the browser of the person who logged in. Untick "Keep me logged in" on shared computers.
