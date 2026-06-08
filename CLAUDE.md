# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Propare is a static landing page for a remote coaching marketplace connecting athletes with elite coaches. The site is deployed on Netlify.

## Development

This is a static HTML/CSS/JS site with no build process. To develop:
- Open `index.html` directly in a browser, or use any local server (e.g., `python -m http.server 8000`)
- No package manager, bundler, or transpilation required

## Architecture

**Files:**
- `index.html` (~5000 lines) - Main landing page with all CSS and JS embedded. Single source of truth; everything ships from this one file.
- `privacy.html`, `terms.html` - Legal pages with their own embedded styling (duplicated, not shared)
- `images/` - Coach photos and favicon

**Page sections** (anchor IDs used by nav links): `#how-it-works`, `#athlete`, `#coach`, `#faq`.

**Forms:** Both athlete and coach signup forms use Netlify Forms (`data-netlify="true"`) with honeypot spam protection (`netlify-honeypot="bot-field"`). Netlify form names are `athlete-signup` and `coach-signup` — these must match in the Netlify dashboard. Submissions go through client-side validation first, then POST to Netlify. Athlete form conditionally reveals guardian fields when the age dropdown reports the user is under 18.

**Styling:** CSS uses custom properties defined in `:root` (colors, fonts, spacing, transitions). Two font families: Bebas Neue (display) and Inter (body), loaded from Google Fonts. Green accent (`#059669`) for athletes, purple (`#A855F7`) for coaches — keep these tokens consistent when adding accents. `--section-padding` shrinks at the 900px breakpoint.

**JavaScript (embedded in index.html):**
- Navigation scroll hide/reveal and smooth anchor scrolling (accounts for `--nav-height`)
- Canvas particle animation in the hero (`#particleCanvas`). Disabled on mobile and when `prefers-reduced-motion` is set; dimensions are locked at load to avoid re-init on scroll-driven viewport resizes.
- "How It Works" panels contain scripted demos (coach typewriter, SVG video-analysis animation in `#va-canvas` with `#va-stage1/2/3`, voice-note reveals). These trigger on IntersectionObserver and respect reduced motion.
- Form validation with conditional guardian fields for minors and at-least-one-contact-method check
- FAQ accordion with tabbed categories

**Deployment:** Netlify auto-deploys from `master`. There is no `netlify.toml` (intentionally removed in commit `4887d3b`) — Netlify uses default detection for a static site. No build step runs.
