# Propare Landing Page

Live: [proparesignup.com](https://proparesignup.com)

Marketing and waitlist page for [Propare](https://propareapp.com), a coaching 
marketplace connecting athletes with verified coaches through live 1:1 sessions 
and video analysis. Built as a multi-file static site and deployed on Netlify.

## Sections

**Hero**
Particle animation background, "ELITE COACHING, ANYWHERE." headline, and a 
scrolling ticker bar highlighting platform values.

**How It Works**
Two side-by-side phone mockups running a fully coordinated, looping animation 
sequence that restarts every time the section scrolls into view.

Left phone shows a live 1:1 coaching session. A session timer ticks in real 
time and a coach message types out character by character via a typewriter 
animation. The timer and typewriter reset together on each loop.

Right phone shows a video analysis session. A shot put annotation system 
cycles through three stages — hip mechanics, release point, and footwork 
sequence — each rendered as SVG overlays on the video preview. A timeline 
scrubber advances to match each stage, voice note cards fade in with 
typewriter text as the scrubber hits each timestamp, and the deliver session 
button appears only after the final card finishes. The sequence holds, then 
resets and loops.

The two phones are coordinated: the live session typewriter fires first, 
then the video analysis starts four seconds later so visitors can read 
one at a time. On mobile, the animation detects screen width and starts 
immediately on scroll-in rather than waiting.

**Coach Social Proof**
Three featured coaches with credentials and sport specialization:
- Shaquille Emanuelson — Netherlands National Record Holder, Discus
- Garrett Kaaland — #2 All-Time Indoor 200m - 19.95, 9.93 100m
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
Accordion-style section covering platform basics, session types, payments, 
and eligibility.

**Legal**
Dedicated `terms.html` and `privacy.html` pages linked from the footer and 
from form acknowledgment text.

## Stack

- Multi-file static site — HTML, Tailwind CSS via CDN
- Netlify Forms with email notifications for athlete and coach submissions
- Zapier for routing form data to Google Sheets (separate sheets per form)
- Propare logo embedded as base64
- Deployed via Netlify Drop

## Design

- Dark theme with Emerald 600 `#059669` as the primary brand color
- Inter typography
- Scroll reveal animations throughout
- Fully mobile-optimized with mobile-specific animation behavior

## Repo

[github.com/kadengarland/propare-landing](https://github.com/kadengarland/propare-landing)
