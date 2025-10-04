# React + TypeScript + Tailwind + Vite — Starter Pack

A minimal, production-ready starter for building React applications with TypeScript, Tailwind CSS and Vite.

This repository provides a light scaffold including TypeScript configuration, ESLint, Vite (with the React SWC plugin), and Tailwind integration so you can start a new project quickly.

## Highlights

- Vite for fast dev server and build
- TypeScript configured for modern bundler workflows
- Tailwind CSS integrated via `@tailwindcss/vite`
- ESLint configuration for TypeScript + React
- React 19 with the new JSX runtime

## Project structure

Key files and folders:

- `index.html` — Vite entry HTML.
- `src/` — source files
  - `main.tsx` — app bootstrap (React StrictMode + root render)
  - `App.tsx` — main App component (simple starter)
  - `index.css`, `App.css` — base and component styles
  - `assets/` — static images/icons used in the starter
- `public/` — static assets served as-is by Vite
- `vite.config.ts` — Vite configuration with React SWC and Tailwind plugins
- `tsconfig.json`, `tsconfig.app.json`, `tsconfig.node.json` — TypeScript configs
- `eslint.config.js` — ESLint configuration
- `package.json` — npm scripts and dependencies

## Tech stack

- Vite (dev server and build)
- React 19
- TypeScript (~5.9)
- Tailwind CSS (with `@tailwindcss/vite` integration)
- ESLint with recommended configs for TypeScript and React

## Installation

On Windows (PowerShell), run:

```powershell
npm install
```

or with pnpm/yarn if you prefer:

```powershell
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
```

## Available scripts

These scripts are defined in `package.json`:

- `npm run dev` — Start Vite dev server (hot reload)
- `npm run build` — Build the app for production (runs `tsc -b` then `vite build`)
- `npm run preview` — Preview the production build locally (runs `vite preview`)
- `npm run lint` — Run ESLint across the project

Examples (PowerShell):

```powershell
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
```

## TypeScript notes

- `tsconfig.json` is configured for bundler mode with strict type checking enabled.
- `tsconfig.app.json` contains app-specific options and includes `src`.

If you edit tsconfig options, ensure the `references` in the root `tsconfig.json` remain correct.

## ESLint

This project uses an `eslint.config.js` which extends recommended rules for JavaScript, TypeScript and React hooks, plus Vite/React refresh settings. Run `npm run lint` to inspect issues.

## Vite configuration

- `vite.config.ts` registers the `@vitejs/plugin-react-swc` plugin for fast React transforms and `@tailwindcss/vite` to automatically re-run Tailwind processing during development.

## Tailwind setup

- Tailwind is included and wired into the build through the Vite Tailwind plugin. Add your utilities and components to `index.css` or component-level CSS files.

## Development tips

- Use the React DevTools and Vite's overlay for runtime errors during development.
- Keep type checking and linting active in your editor for the best DX.

## Suggested next steps

- Replace `App.tsx` with a starting layout or a design system.
- Add Storybook or component tests (Vitest/Jest) if you plan to build components.
- Configure CI (GitHub Actions) to run `npm run build` and `npm run lint` on PRs.

## License

This starter is provided as-is. Add a LICENSE file if you plan to publish it.

---