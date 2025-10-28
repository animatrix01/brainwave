
# Brainwave

Brainwave is a modern marketing/landing site built with React and Vite. It uses Tailwind CSS for styling and aims to be a fast, responsive single-page experience for showcasing product features, pricing, roadmap, and more.

## Tech stack

- Framework: React (v19)
- Build tool / dev server: Vite
- Styling: Tailwind CSS + PostCSS
- Linting: ESLint
- Routing: react-router-dom
- UX/animations: react-just-parallax
- Utilities: scroll-lock
- Languages & runtime: JavaScript (ES Modules), Node.js, npm

Core dependencies (from `package.json`):

- react
- react-dom
- react-router-dom
- react-just-parallax
- scroll-lock

Dev dependencies:
# Brainwave

Brainwave is a modern marketing/landing site built with React and Vite. It uses Tailwind CSS for styling and aims to be a fast, responsive single-page experience for showcasing product features, pricing, roadmap, and more.

## Project overview

- Single-page React app (component-driven)
- Built with Vite for fast local development and HMR
- Styled with Tailwind CSS and PostCSS

## Tech stack (exact versions)

Runtime / core

- React: 19.1.1
- react-dom: 19.1.1
- react-router-dom: 7.9.3
- react-just-parallax: 3.1.16
- scroll-lock: 2.1.5

Build & dev tools

- Vite: 7.1.7
- @vitejs/plugin-react: 5.0.4

Styling

- Tailwind CSS: 3.4.18
- PostCSS: 8.5.6
- Autoprefixer: 10.4.21

Linting & types

- ESLint: 9.36.0
- @eslint/js: 9.36.0
- eslint-plugin-react-hooks: 5.2.0
- eslint-plugin-react-refresh: 0.4.22
- Type hints: @types/react 19.1.16, @types/react-dom 19.1.9

Languages & environment

- JavaScript (ES Modules), Node.js (recommended: 18+ LTS)
- npm (bundled with Node)

## Installation (Windows PowerShell)

1. Ensure you're in the project directory that contains `package.json`.
	- If you opened a parent folder, `cd` into the folder that contains `package.json` before running install or scripts.

```powershell
# install dependencies
npm install
```

## Available npm scripts (from `package.json`)

- `npm run dev` — start Vite dev server
- `npm run build` — build production assets
- `npm run preview` — preview production build locally
- `npm run lint` — run ESLint across the codebase

Run the dev server:

```powershell
npm run dev
```

If you run `npm run dev` and get an error complaining that `package.json` cannot be found, make sure your current shell path is the folder that contains `package.json`.

Example: if your repository is nested (`.../brainwave/brainwave`), and you're in `.../brainwave` (the parent), then run:

```powershell
cd brainwave
npm install
npm run dev
```


## Folder structure

Here is the repository layout (top-level and important source files/directories). This reflects the current project state.

```
brainwave/
├─ .gitignore
├─ .vscode/
├─ eslint.config.js
├─ index.html
├─ node_modules/
├─ package-lock.json
├─ package.json
├─ postcss.config.js
├─ public/
├─ README.md
├─ src/
│  ├─ App.jsx
│  ├─ main.jsx
│  ├─ index.css
│  ├─ assets/
│  │  ├─ index.js
│  │  ├─ 4-small.png
│  │  ├─ background.jpg
│  │  ├─ brainwave-symbol.svg
│  │  ├─ brainwave-symbol-white.svg
+│  │  ├─ brainwave.svg
│  │  ├─ check-02.svg
│  │  ├─ check.svg
│  │  ├─ chrome-cast.svg
│  │  ├─ collaboration/
│  │  ├─ hero/
│  │  ├─ notification/
│  │  ├─ pricing/
│  │  ├─ roadmap/
│  │  ├─ services/
│  │  ├─ socials/
│  │  └─ svg/
│  │     └─ yourlogo.svg
│  ├─ components/
│  │  ├─ Benefits.jsx
│  │  ├─ Button.jsx
│  │  ├─ Collaboration.jsx
│  │  ├─ Companylogos.jsx
│  │  ├─ Footer.jsx
│  │  ├─ Generating.jsx
│  │  ├─ Header.jsx
│  │  ├─ Heading.jsx
│  │  ├─ Hero.jsx
│  │  ├─ Notification.jsx
│  │  ├─ Pricing.jsx
│  │  ├─ PricingList.jsx
│  │  ├─ Roadmap.jsx
│  │  ├─ Section.jsx
+│  │  ├─ Services.jsx
│  │  ├─ Tagline.jsx
│  │  └─ design/
│  │     ├─ Benefits.jsx
│  │     ├─ Collaboration.jsx
│  │     ├─ Header.jsx
│  │     ├─ Hero.jsx
│  │     ├─ Pricing.jsx
│  │     ├─ Roadmap.jsx
│  │     └─ Services.jsx
│  └─ constants/
│     └─ index.js
├─ tailwind.config.js
└─ vite.config.js
```

Notes:
- `src/components/design/` contains design-specific component variants.
- `src/assets/svg/` contains reusable SVG components (e.g. `Arrow.jsx`, `Brackets.jsx`) and icons.
- Keep `node_modules/` out of source control (it's already ignored via `.gitignore`).

The project follows a component-driven structure where UI is broken into small, reusable components.

## Troubleshooting — OneDrive / EPERM notes

If you encounter permission/EPERM errors (for example when Vite tries to remove `node_modules/.vite`), these are frequently caused by OneDrive file locks or other processes holding file handles.

Quick steps:

1. Ensure you're running commands from the directory that contains `package.json`.
2. Stop running dev servers and close code editors that may hold locks.
3. Remove Vite cache and restart the dev server:

```powershell
Remove-Item -Recurse -Force .\node_modules\.vite
npm run dev
```

4. If permission errors persist, consider moving the project out of OneDrive (e.g., `C:\projects\brainwave`) or exclude the project folder from OneDrive syncing.

## Contributing

Contributions are welcome.

Suggested workflow:

1. Fork the repo
2. Create a feature branch: `git checkout -b feat/my-change`
3. Make changes and add tests where relevant
4. Run `npm run lint` and `npm run build` locally
5. Open a pull request with a clear description of your changes

## Next steps (optional additions)

- Add `.nvmrc` or GitHub workflow to pin Node version
- Add `CONTRIBUTING.md` and `CODE_OF_CONDUCT.md`
- Add badges (build, lint) to the README

---

If you'd like, I can add a `.nvmrc` file, create a `CONTRIBUTING.md`, or generate a small CI workflow for GitHub Actions. Which would you prefer next?
