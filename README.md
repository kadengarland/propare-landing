# Propare Landing Page

Live: [proparesignup.com](https://proparesignup.com)

Marketing and waitlist page for [Propare](https://propareapp.com), a coaching 
marketplace connecting athletes with verified coaches through live 1:1 sessions 
and video analysis. Built as a multi-file static site and deployed on Netlify.

## Sections

**Hero**
Particle animation background, "ELITE COACHING, ANYWHERE." headline, live 
waitlist counter, and a scrolling ticker bar highlighting platform values.

**How It Works**
Two side-by-side phone mockups. Left phone shows a live 1:1 coaching session 
with real-time video call UI and coach messaging. Right phone shows a video 
analysis session with annotated video, timeline scrubber, playback controls, 
and coach voice note cards.

**Coach Social Proof**
Three featured coaches with credentials and sport specialization:
- Shaquille Emanuelson — Netherlands National Record Holder, Discus
- Garrett Kaaland — #2 All-Time Indoor 200m - 19.95, 9.93 100m
- Texas Tanner — All-American in All Four Throwing Events

**Athlete Signup**
Netlify form with conditional parent/guardian flow that activates for 
athletes under 18. Fields include name, email, phone, sport/event, and 
preferred contact method. Form acknowledgment links to Terms of Service 
and Privacy Policy.

**Coach Signup**
Separate Netlify form for coach applications with its own email notification 
and Zapier routing.

**FAQ**
Accordion-style FAQ section covering platform basics, session types, 
payments, and eligibility.

**Legal**
Dedicated `terms.html` and `privacy.html` pages linked from the footer and 
from form acknowledgment text. All three files cross-link correctly.

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
- Fully mobile-optimized

## Repo

[github.com/kadengarland/propare-landing](https://github.com/kadengarland/propare-landing)
