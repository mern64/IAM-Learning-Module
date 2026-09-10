# Setup — adding this to your GitHub repo from the command line

These are the exact commands. Replace the placeholders in ANGLE BRACKETS with
your own values.

## A. If you're adding this to an EXISTING repo (your write-ups repo)

From inside your already-cloned repo folder:

```bash
# 1. Copy the handbook files into the repo folder first (drag them in, or use cp):
#    index.html, README.md, SETUP.md, LICENSE
#    (If you already have a README you want to keep, rename this one to
#     HANDBOOK-README.md instead of overwriting yours.)

# 2. Stage the new files
git add index.html README.md SETUP.md LICENSE

# 3. Commit
git commit -m "Add interactive IAM concepts handbook"

# 4. Push to GitHub
git push origin main
```

If your default branch is called `master` instead of `main`, use `master` in the
push command.

## B. If you're creating a NEW repo for it

```bash
# 1. Make a folder and put the four files in it, then:
cd <folder-with-the-files>

# 2. Initialise git
git init
git branch -M main

# 3. Stage and commit everything
git add .
git commit -m "Initial commit: interactive IAM concepts handbook"

# 4. Create the repo on GitHub first (in the browser: New repository,
#    do NOT initialise it with a README), then connect and push:
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## C. Turn on GitHub Pages (so you get a shareable link + saved progress)

1. On GitHub, open your repo.
2. **Settings** (top nav) → **Pages** (left sidebar).
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Branch: **main**, folder: **/ (root)**. Click **Save**.
5. Wait ~1 minute, refresh, and copy the URL shown ("Your site is live at …").
6. Your handbook is at the site URL, e.g.
  `https://<your-username>.github.io/<repo-name>/`

Once it's on Pages and you open it there, your progress (ticked days, XP, exam
score) will save automatically and persist between visits.

## D. Updating it later

Whenever you get a new version of the file, just replace it and:

```bash
git add index.html
git commit -m "Update handbook"
git push
```

Pages redeploys automatically within a minute or so. Your saved progress is in
your browser, not the file, so updating the handbook won't wipe it.

## Troubleshooting

- **`git push` asks for a password and rejects it:** GitHub no longer accepts
  account passwords over HTTPS. Use a Personal Access Token as the password
  (GitHub → Settings → Developer settings → Personal access tokens), or set up
  an SSH key and use the `git@github.com:...` remote URL instead.
- **Pages shows a 404:** give it a couple of minutes after the first push; make
  sure the branch and `/root` folder are selected; confirm the filename in the
  URL matches exactly (it's case-sensitive).
- **Progress didn't save:** make sure you're opening the file over the Pages
  URL (https://...), not from a `file://` path or inside a private/incognito
  window, both of which can restrict browser storage. Progress is local to
  that browser and device; it will not follow you to another machine.
