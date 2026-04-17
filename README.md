# Propare Landing Page

Live: [proparesignup.com](https://proparesignup.com)

Marketing and waitlist page for [Propare](https://propareapp.com), a coaching
marketplace connecting athletes with verified coaches through live 1:1 sessions
and video analysis. Built as a multi-file static site deployed on Netlify.

## Sections

**Navigation**
Fixed nav with frosted glass effect on scroll. Links to athlete and coach
signup sections. Social icons (Instagram, TikTok, X, Facebook) with live
links to all Propare accounts.

**Hero**
Interactive particle constellation background — particles float, connect with
lines when in proximity, and repel from the cursor on hover. Staggered
fade-in animations on load. "ELITE COACHING, ANYWHERE." headline with dual
CTAs routing to each signup form.

**Ticker Bar**
Scrolling marquee of platform phrases running between the hero and How It Works
section.

**How It Works**
Two floating phone mockups running a fully coordinated, looping animation
sequence that restarts every time the section scrolls into view.

Left phone shows a live 1:1 coaching session. A session timer ticks in real
time and a coach message types out character by character. The timer and
typewriter reset together on each loop.

Right phone shows a video analysis session. A shot put annotation system
cycles through three stages — hip mechanics, release point, and footwork
sequence — each rendered as SVG overlays on the video preview. A timeline
scrubber advances to match each stage, voice note cards fade in with
typewriter text as the scrubber hits each timestamp, and a deliver session
button appears only after the final card finishes. The sequence holds, then
resets and loops.

The two phones are coordinated: the live session typewriter fires first, then
the video analysis starts four seconds later. On mobile, the animation detects
screen width and starts immediately on scroll-in with a shorter delay.

**Coach Social Proof**
Three featured coaches with credentials and sport specialization:
- Shaquille Emanuelson — Netherlands National Record Holder, Discus
- Garrett Kaaland — #2 All-Time Indoor 200m, 9.93 100m, 19.85 200m
- Texas Tanner — All-American in All Four Throwing Events

**Athlete Signup**
Netlify form with a conditional parent/guardian flow that activates for
athletes under 18. Fields include name, email, phone, sport/event, and
preferred contact method. Form acknowledgment links to Terms of Service
and Privacy Policy.

**Coach Signup**
Separate Netlify form for coach applications with its own email notification
and Zapier routing.

**FAQ**
Tabbed accordion FAQ covering five categories: General, Coaches, Pricing,
Safety, and For Coaches. Includes a "Still have a question?" footer row
linking directly to support email.

**Legal**
Dedicated `terms.html` and `privacy.html` pages linked from the footer and
from form acknowledgment text. The footer also links to Quick Links and all
social accounts.

## Stack

- Multi-file static site — HTML, Bebas Neue + Inter via Google Fonts
- Netlify Forms with email notifications for athlete and coach submissions
- Zapier for routing form data to Google Sheets (separate sheets per form)
- Propare logo embedded as base64
- Deployed via Netlify Drop

## Security

- Honeypot field on athlete signup form for bot filtering
- All form data routed through Netlify's infrastructure
- No sensitive data stored client-side

## Design

- Dark theme, Emerald 600 `#059669` primary, Purple `#A855F7` secondary accent
- Scroll reveal and staggered fade-in animations throughout
- `prefers-reduced-motion` support — all animations disabled for users who
  have it enabled
- Fully mobile-optimized with mobile-specific animation behavior

## Repo

[github.com/kadengarland/propare-landing](https://github.com/kadengarland/propare-landing)
