Figma Link: https://www.figma.com/proto/oXebpvc3rY8uVBnM3mNYjW/SneakVerse-%E2%80%94-Step-Into-the-Future-%C2%B7-UI-UX-Submission?node-id=7-320&starting-point-node-id=7%3A320&t=9uZgmW620jbRjOT4-1



# SneakVerse-UIUX-LandingPage
SneakVerse is a premium, responsive sneaker landing page built with React, TypeScript, Vite, and Tailwind CSS. It features product search, category filters, a wishlist, and interactive demo shopping features with a bold, modern UI.
# SNEAKVERSE.

### Step Into the Future.

A premium, responsive sneaker discovery landing page for **UI/UX Design Using Figma**. An individual academic project with native Figma work, a working React implementation, and a documented submission package.

![SneakVerse desktop website](docs/screenshots/desktop.png)

## Project and assignment

Designed for college students, young professionals, sneaker enthusiasts, collectors and streetwear fans, primarily aged 16–35. The primary task is discovering and exploring a curated fictional collection.

The assignment requires a desktop landing page, header/logo/navigation/CTA, hero, at least three feature cards, footer, Auto Layout, reusable components, shared styles and an audience/design explanation. Tablet/mobile designs, a prototype and the coded site extend that brief. The code is an additional implementation, **not a substitute for native Figma work**.

**Website status:** implemented and locally tested; see the actual results in [QA report](docs/qa-report.md).  
**Figma status:** native frames/components/styles/prototype reactions created; final image rendering, export/cleanup and reviewer-access checks remain pending after the Starter quota.  
**GitHub status:** local Git repository initialized on `main`; no commit, remote repository or push yet.

## Figma and prototype

- [Native design file](https://www.figma.com/design/oXebpvc3rY8uVBnM3mNYjW?node-id=7-320)
- [Desktop prototype entry](https://www.figma.com/proto/oXebpvc3rY8uVBnM3mNYjW?node-id=7-320&starting-point-node-id=7%3A320) — playback/access still requires verification.
- [Figma construction and acceptance guide](docs/figma-guide/README.md)
- [Design system](docs/design-system.md)
- [Audience and design choices](docs/project-overview.md)
- [College report](docs/project-report.md)

The Figma file contains desktop 1440px, tablet 768px and mobile 390px native frames; 21 shared variables; 12 text styles; and eight component families (25 main components in seven variant sets plus FeatureCard). The Starter plan's three-page limit groups the seven requested areas across three pages. Further MCP calls were blocked before final exports/cleanup. Blank image areas observed in Safari are explicitly unresolved; follow the guide to restore fills from `public/images` if needed. Do not mark the Figma submission complete until its acceptance checklist passes.

## Working features

- Eight required areas with a sticky header and responsive mobile menu.
- Dark editorial hero, original geometric wordmark, electric-lime accents and original unbranded sneaker concept images.
- Four typed fictional products with consistent INR prices.
- Name/style/color search, clearable results and recoverable empty state.
- Lifestyle, Performance and Limited Drops filters; category cards filter the collection.
- Wishlist toggles and saved-product panel.
- Product dialogs, UK size selection, removable **demo bag**, and concept totals.
- Local email validation with accessible errors and an explicit no-subscription confirmation.
- Meaningful footer navigation and concept explanations for support/social destinations.
- Keyboard navigation, skip link, focus styles, native modal focus handling, Escape dismissal and reduced motion.
- Locally bundled WebP images and Latin variable fonts; no API keys required.

No live stock, real payments, checkout, authentication, customer reviews or newsletter storage is claimed. State resets on reload. All names, designs and prices are fictional academic content.

## Technology

React 19 · TypeScript · Vite · Tailwind CSS 4 · CSS · Lucide React. Vitest, Testing Library, Playwright, axe, ESLint and Prettier support verification. Motion is implemented with CSS because a separate animation dependency was unnecessary.

## Run locally

Use Node.js 22.12+ (this project was built on Node 24.21.0) and npm. In Terminal:

```bash
cd /Users/shailen11/Desktop/SneakVerse-UIUX
npm install
npm run dev
```

The verified development URL is **http://127.0.0.1:5173/**. Vite prints a different port if that port is occupied. No `.env` file or secret key is needed.

```bash
npm run typecheck
npm run lint
npm run test
npm run build
npm run preview
```

The verified production preview URL is **http://127.0.0.1:4173/**. `npm run check` combines type checking, lint, unit tests and production build. `npm run format` formats the source and configs.

## Browser tests

```bash
npx playwright install chromium firefox webkit
npm run test:e2e
```

Playwright starts Vite automatically when needed. The current Mac's Firefox executable could not locate its profile folder, so its tests were **not verified**. The measured passing subset can be rerun with:

```bash
npm run test:e2e:verified
```

This runs Chromium and WebKit at 320, 375, 390, 430, 768, 1024 and 1440px plus the main functional flow and page/dialog accessibility scans. WebKit is useful Safari-engine coverage; actual Safari inspection is separately documented. CI configuration is prepared in `.github/workflows/verify.yml` but has not run remotely.

## Design system

Black `#111111`, Electric Lime `#C7FF28`, Off White `#F7F7F5`; Space Grotesk headings, Inter body; an 8-point spacing family; 8/12/20/pill radii; a 1312px maximum content container. See the full [token and component specification](docs/design-system.md).

## Screenshots and evidence

- [Desktop website](docs/screenshots/desktop.png)
- [Tablet website](docs/screenshots/tablet.png)
- [Mobile website](docs/screenshots/mobile.png)
- [QA evidence](docs/qa-report.md)
- [Lighthouse report](docs/lighthouse.report.html)

These three responsive images are website screenshots. Final native Figma exports remain pending and must not be confused with the code screenshots.

## Structure

```text
public/
  images/                 Original optimized WebP product imagery
  fonts/                  Local fonts and OFL license notices
src/
  components/UI.tsx       Shared brand, buttons, product cards and dialog
  sections/               Eight landing-page areas
  data/products.ts        Typed product/category data and INR formatter
  styles/global.css       Tokens, components, breakpoints and motion
  tests/                  Vitest and Testing Library coverage
  App.tsx                 Exploration state and dialog composition
  main.tsx                Application entry
tests/                    Playwright functional/responsive/axe checks
 docs/
  figma-guide/            Native construction steps and remaining checks
  screenshots/            Website screenshots at reference widths
  design-system.md
  project-overview.md
  project-report.md
  qa-report.md
  github-submission.md
  task-checklist.md
```

## Assets and attribution

Product imagery was generated for this original fictional concept using the built-in image-generation tool, then cropped/optimized locally. [Asset provenance and prompts](docs/assets.md) identify the files and generation method. Font license notices are bundled under `public/fonts`. Lucide icons are provided by the `lucide-react` package. No third-party sneaker image URLs are hotlinked.

## College submission checklist

- [x] Eight-section responsive website and working local demo interactions.
- [x] Native desktop/tablet/mobile frames created with editable layers and Auto Layout.
- [x] At least three real reusable Figma components; variables and typography styles created.
- [x] Audience/design explanation, report, README and website screenshots prepared.
- [x] Local type/lint/unit/build and Chromium/WebKit checks executed; see QA results.
- [ ] Restore/verify native image rendering and finish Figma cover/temporary-capture cleanup.
- [ ] Verify live prototype interactions and export final native screenshots.
- [ ] Verify professor access to Figma design/prototype links.
- [ ] Confirm GitHub destination and visibility, commit/push, add the real URL.
- [ ] Perform final college submission after pending items are resolved.

[GitHub publishing instructions](docs/github-submission.md) cover the local Xcode license blocker and exact commands. Do not claim the project has been uploaded until the remote push and access are verified.
