# JN Visuals — website

A plain HTML/CSS site (no build tools, no dependencies) ready for GitHub Pages.

## 1. Your photos are already in

All 23 photos from your contact sheet are cropped, named, and placed in
`images/`, and every page already points at them:

| File | Used on | What it shows |
|---|---|---|
| `hero.jpg` | Home hero | Player shouting/celebrating, fist raised |
| `hero-portfolio.jpg` | Portfolio page hero | Wide shot of legs battling for the ball |
| `about-feature.jpg` | About page | Moody black & white portrait shot |
| `gallery-01.jpg` – `gallery-20.jpg` | Portfolio grid | The remaining 20 photos, in the order shown below |

Portfolio grid order and captions (edit these any time in `portfolio.html`):

1. Lined up before kickoff
2. Closing in on goal
3. Squaring up in a local derby
4. Breaking forward as a team
5. Huddled up before the whistle
6. Skill on the ball
7. Focused before kickoff
8. A moment from open play
9. Pure joy at the final whistle
10. A quieter kind of celebration
11. Champions — the whole squad
12. Walking out for the big occasion
13. Talking tactics mid-game
14. Ready to spring off the line
15. Shoulder to shoulder for the ball
16. Diving in for the loose ball
17. Working the ball down the line
18. Down but not out
19. Fists up after the winner
20. Eyes on the game

These captions are guesses based on what's happening in each photo — swap in
real names, teams, and club names wherever you know them. Search each
caption's text in `portfolio.html` (or `index.html` for the 3 featured on the
homepage) to find and edit it.

The `about-feature.jpg` portrait is one of your own action shots, not
necessarily a photo of you — if you want an actual headshot on the About
page, just replace that file with one (same filename) or update the
reference in `about.html`.

Want to add more photos later? Drop a new file into `images/`, then copy one
of the existing `<div class="photo ...">` blocks in `portfolio.html` and
point it at the new filename.

## 2. Put this on GitHub Pages (free hosting)

1. Create a free GitHub account at github.com if you don't have one.
2. Create a new repository — name it anything, e.g. `jn-visuals-site`. Keep it Public.
3. Upload all the files in this folder (keeping the `css/` and `images/` folders intact) using "Add file > Upload files" in the repo, or via git if you're comfortable with it.
4. In the repo, go to **Settings > Pages**.
5. Under "Build and deployment", set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
6. GitHub will give you a URL like `https://yourusername.github.io/jn-visuals-site/` within a minute or two — that confirms it's live.

## 3. Connect your GoDaddy domain

1. Buy your domain on GoDaddy (e.g. `jnvisuals.com`) if you haven't already.
2. Back in your GitHub repo, go to **Settings > Pages > Custom domain**, type in your domain (e.g. `jnvisuals.com`) and save. This creates a `CNAME` file in your repo automatically.
3. In GoDaddy, go to your domain's **DNS** settings and add these records:
   - Four **A records** (Name: `@`) pointing to GitHub's IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - One **CNAME record** (Name: `www`) pointing to `yourusername.github.io`
4. Back in GitHub Pages settings, tick **Enforce HTTPS** once it becomes available (can take up to a few hours after DNS connects).
5. DNS changes can take anywhere from a few minutes to 48 hours to fully propagate.

## 4. Making the contact form actually send emails

The contact form on `contact.html` is just HTML — GitHub Pages can only serve
static files, so it won't send anything on its own. The simplest free fix:

1. Sign up at formspree.io (free tier is fine).
2. Create a form there, which gives you an endpoint URL.
3. In `contact.html`, change `<form>` to `<form action="https://formspree.io/f/yourFormID" method="POST">`.

## 5. Editing content

Everything is plain HTML — open any `.html` file in a text editor (or even
GitHub's own web editor) and change the text directly. Styling lives in
`css/style.css` if you want to tweak colors or fonts later.
