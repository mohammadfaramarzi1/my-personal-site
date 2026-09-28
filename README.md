# Mohammad Faramarzi — Personal Branding Website

A fast, single-file portfolio website with a 3D globe, glassmorphism design, smooth scroll animation and three languages (English, Persian, Arabic).

Built by **Mohammad Faramarzi**, front-end developer and instructor.
Contact: [faramarzi.dev@gmail.com](mailto:faramarzi.dev@gmail.com) · [LinkedIn](https://linkedin.com/in/mohammadfaramarzii) · [GitHub](https://github.com/mohammadfaramarzi1)

<!-- Add a screenshot: ![Preview](./preview.png) -->
<!-- Add your live URL: **Live site:** https://your-domain.com -->

## Features

- **3D hero:** a rotating globe made of points, with glowing "city lights" and an orbiting satellite, drawn with three.js. It reacts to the mouse and moves as you scroll.
- **Glassmorphism UI:** frosted glass panels over soft animated color, with a light spot that follows the cursor.
- **Scroll animation:** GSAP and ScrollTrigger drive the headline reveal, section reveals, animated counters, and a timeline line that fills as you scroll.
- **Project pages:** each project card opens its own detail page (hash routing, no page reload) with client, date, role, description, what was built, tech stack and a link to the live site.
- **Mo-Bot guide:** a small robot that describes each section and project as you reach it, with quick buttons for skills, projects and contact.
- **Three languages:** English, Persian (فارسی) and Arabic (العربية) with a language switcher, full right-to-left layout, the Vazirmatn font, and the choice saved in the browser.
- **Light and dark themes:** follows the visitor's system setting.
- **Responsive:** works from phones to large desktops, with safe-area support for notched devices.

## Tech stack

| Purpose | Tool |
| --- | --- |
| Styling | [Tailwind CSS](https://tailwindcss.com) (Play CDN) plus custom CSS variables |
| 3D | [three.js](https://threejs.org) r128 |
| Animation | [GSAP](https://gsap.com) 3.12 and ScrollTrigger |
| Fonts | Bricolage Grotesque, Vazirmatn (Google Fonts) |

There is no build step and no dependencies to install. Everything is in one `index.html` file.

## Getting started

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

Open `index.html` in your browser, or serve it locally:

```bash
npx serve .
# or
python3 -m http.server 8000
```

An internet connection is needed because the libraries and fonts load from CDNs.

## Deploy

Upload the repository to any static host. Keep the file name `index.html`.

- **GitHub Pages:** Settings → Pages → deploy from the `main` branch, root folder.
- **Netlify, Vercel or Cloudflare Pages:** import the repository, with no build command and the root as the output directory.

## Customize

| What | Where in `index.html` |
| --- | --- |
| Colors | CSS variables at the top of the `<style>` block (`--bg`, `--amber`, `--sky`, and the glass values) |
| Page text | The HTML inside `<main>` |
| Persian and Arabic text | The `T` array in the last `<script>` block. Each entry is `[English, Persian, Arabic]`, and the English text must match the HTML exactly |
| Project pages | `P` (English) and `PT.fa` / `PT.ar` (translations) |
| Robot lines | The `L` object and `SK` string, plus matching entries in `T` |
| Globe look | The three.js section: point counts, sizes, colors and scroll movement |

### Add a project

1. Copy one `<a class="proj glass rv" href="#/p/...">` card in the projects section and change its text and link id.
2. Add a matching entry with the same id to `P`.
3. Add the translated fields to `PT.fa` and `PT.ar`.
4. Add the card description to the `T` array.

## Performance and accessibility

- Pixel ratio is capped at 1.5 and rendering pauses when the tab is hidden.
- Animations are turned off for visitors who prefer reduced motion.
- Visible keyboard focus, semantic headings and an accessible robot control.
- Language changes update the page `lang` and `dir` attributes.

## Browser support

Current versions of Chrome, Edge, Firefox and Safari. Glass blur (`backdrop-filter`) needs a modern browser; older ones fall back to plain translucent panels.

## Roadmap

- Add photo and project screenshots
- Add more projects
- Optional Claude-powered version of the robot that answers visitors' questions

## License

Add a license before publishing, for example MIT. Copy and personal details in this repository belong to Mohammad Faramarzi.
