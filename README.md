# Marian Sutherland Kirby Library — Website

A modern, clean, static website for the Marian Sutherland Kirby Library in Mountain Top, PA.

## What's Here

```
index.html      — Homepage (hours, catalog search, quick links, programs preview)
programs.html   — Programs & Events (children, teens, adults)
resources.html  — Online Resources (eBooks, databases, career tools)
about.html      — About (hours, location, library card, volunteer, donate, services)
css/styles.css  — All styles
```

## Key Features

- **Catalog search** wired directly to the Luzerne County Aspen Discovery system
- **Online resources** linked (cloudLibrary, Hoopla, Libby, Mango Languages, Creativebug, BlueCareer, POWER Library, NewsBank)
- **Chat with a Librarian** linked to the county system
- **Mobile responsive** — works on phones, tablets, desktops
- **Accessible** — skip links, semantic HTML, readable contrast
- **Zero dependencies** — no build tools, no JavaScript frameworks, no database
- **Today's hours highlighted** automatically via a small JS snippet

## How to Update Content

Every page is plain HTML. To update:

1. Open the `.html` file in any text editor
2. Find the section you want to change
3. Edit the text between the HTML tags
4. Save and re-upload

Common updates:
- **Hours changed?** → Update the `<table class="hours-table">` in `index.html` and `about.html`, plus the footer hours list in all four pages
- **New program?** → Copy an existing `<div class="program-card">` block in `programs.html` and change the text
- **New online resource?** → Copy an existing `<a class="resource-card">` block in `resources.html`
- **Announcement banner?** → Edit the `<div class="announcement">` section near the top of `index.html`

## Free Hosting on Cloudflare Pages

### Option 1: Drag and drop (easiest)

1. Go to [dash.cloudflare.com](https://dash.cloudflare.com)
2. Sign up for a free account
3. Go to **Workers & Pages** → **Create** → **Pages** → **Upload assets**
4. Drag this entire folder into the upload area
5. Deploy — you'll get a `.pages.dev` URL immediately
6. Optionally connect a custom domain (like `kirbylib.org`)

### Option 2: GitHub + auto-deploy (better for ongoing updates)

1. Push this folder to a GitHub repository
2. In Cloudflare dashboard, go to **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
3. Select the repo, set build output to `/` (root)
4. Every push to `main` auto-deploys

### Custom Domain

Once deployed on Cloudflare Pages:
1. Go to the project → **Custom domains** → **Set up a custom domain**
2. Enter `kirbylib.org` (or whatever domain)
3. Cloudflare will provide DNS records to add
4. SSL is automatic and free

## Integrations

| Service | How it's connected |
|---------|-------------------|
| Library Catalog | Form submits search to `luzerne.aspendiscovery.org` |
| Chat with a Librarian | Links to `luzernelibraries.org/chat-with-a-librarian/` |
| cloudLibrary | External link |
| Hoopla | External link |
| Libby | External link |
| Mango Languages | External link |
| Creativebug | External link (Luzerne-specific URL) |
| BlueCareer | External link (Wilkes-Barre library URL) |
| POWER Library | External link (PA state resource, library ID included) |
| NewsBank | External link |
| Library Card Application | Links to Aspen Discovery self-registration |

All integrations are simple links — no API keys, no backend, no accounts needed.

## What This Replaces

The previous site (`kirbylib.org`) was built with HTML framesets, table-based layouts, and image-based navigation from the late 1990s. Many images were broken, making the site effectively unusable. This replacement contains all the same information in a modern, accessible, mobile-friendly format.
