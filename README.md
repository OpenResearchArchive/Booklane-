# Booklane RYK

The website for **Booklane RYK**, a volunteer reading initiative running free book lanes, reading circles, and a student writing desk in Rahim Yar Khan, Pakistan.

A static, no-build site — plain HTML, CSS, and JavaScript. No framework, no dependencies to install.

## Pages

| File | Page |
|---|---|
| `index.html` | Home |
| `about.html` | About Us |
| `mission.html` | Our Mission |
| `donate.html` | Donate |
| `submit.html` | Write With Us — essay/article submissions from student writers |
| `gallery.html` | Project photo gallery |
| `style.css` | Shared styles for all pages |
| `script.js` | Shared behavior (mobile nav, gallery lightbox, form handling) |

## Running it locally

No build step needed. Either:

- Open `index.html` directly in a browser, or
- Serve the folder so relative paths and fonts behave exactly like production:
  ```bash
  python3 -m http.server 8000
  ```
  then visit `http://localhost:8000`

## Deploying with GitHub Pages

1. Push this folder to a GitHub repository.
2. In the repo, go to **Settings → Pages**.
3. Under **Source**, choose the branch (usually `main`) and the root folder.
4. Save — GitHub will publish the site at `https://<username>.github.io/<repo-name>/`.

## Things to customize before going live

- **Gallery photos** (`gallery.html`) — currently placeholder stock images. Replace the `src` URLs with real photos of your book lanes, ideally hosted in an `/images` folder in this repo.
- **Bank / mobile wallet details** (`donate.html`) — search for `[add your bank name]` and `[add account number]` and fill in real details.
- **Contact email** — currently `hello@booklaneryk.org`; update everywhere if you're using a different address (search for it across all files).
- **Donate and submission forms** — these currently save entries in the visitor's browser only (`localStorage`) and show a confirmation message; they are **not** connected to a real backend yet. To actually receive donations or essays from visitors, connect the forms in `donate.html` and `submit.html` to a service like [Formspree](https://formspree.io) or Google Forms, or to a backend of your own.

## Structure notes

- Colors, fonts, and spacing are all defined as CSS variables at the top of `style.css` — change the palette or type there and it updates the whole site.
- The navigation is styled as book spines on a shelf; each page repeats the same header/footer markup since there's no templating layer.

## License

Add a license here if you want the code to be reusable by others (MIT is a common simple choice for a project like this).
