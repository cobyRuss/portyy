# Prompt Log — Russel Tristan L. Marzo (Coby) Personal Portfolio

**Project:** Single-Page Personal Portfolio Web Application (Matte PC Hardware Theme)  
**Author:** Russel Tristan L. Marzo (Coby)  
**Institution:** Data Center College of the Philippines — Bangued (BSIT, 4th Year)  
**Repository:** [https://github.com/cobyRuss/eportfolio.git](https://github.com/cobyRuss/eportfolio.git)  
**Stack:** HTML5, Tailwind CSS (via CDN), Vanilla JavaScript, Vercel Static Configuration

---

## Prompt 1 — Initial Portfolio Architecture & Matte PC Hardware Theme

### User Prompt
> Act as an expert frontend developer. Build a fully responsive, single-page personal portfolio web application optimized for instant deployment on Vercel. Use HTML, Tailwind CSS (via CDN), and vanilla JavaScript.
>
> **Design System & UI Preferences (MATTE PC HARDWARE THEME):**
> - **Theme/Colors:**
>   - **Background:** Strictly avoid pure black. Use a matte dark charcoal/zinc (e.g., Tailwind's `zinc-900` or `#18181b`) to resemble a premium custom PC chassis or a matte guitar amplifier.
>   - **Accents:** Avoid harsh, eye-straining neon red. Use a soft, premium crimson/cherry red (e.g., `rose-600` or `red-600`).
> - **Style:** Clean, hardware-inspired, and highly readable. Use subtle glassmorphism for cards (`bg-zinc-800/50`) with very thin, 1px crimson borders on hover to mimic subtle PC LED lighting or audio interface indicators. Typography should be crisp and legible (e.g., Inter or Roboto) to prevent eye fatigue.
>
> **Data & Content Structure (PRE-FILL THIS EXACT DATA):**
> Create a central JavaScript data object (`const portfolioData = {...}`) at the top of your script and pre-fill it with Personal Info, Education, Technical Stack (10 items), Projects (4 items), and Certifications & Eligibility (5 items), along with uploaded media archives (`russel_certificates.zip`, `flowershop_ss.zip`, `88minimart_SS.zip`, `rgkrs.zip`, and profile picture).

### Implementation Summary
- Created [`index.html`](index.html) and [`vercel.json`](vercel.json) with the Matte PC Hardware theme (`#18181b` / `zinc-900` chassis surface, `bg-zinc-800/50` frosted glassmorphism cards, `rose-600` 1px LED hover borders, and `Inter` + `JetBrains Mono` typography).
- Extracted all uploaded archives into `assets/profile/`, `assets/certificates/`, and `assets/projects/`.
- Built the central `portfolioData` JavaScript object and dynamic DOM renderers for the Sticky Header, Hero/About Me section, 10-card Technical Stack grid, 5 Earned Certifications, 4 Featured Projects, and interactive Lightbox Gallery Slider Modal.

---

## Prompt 2 — 4th Project Integration (`student_attendance.zip`)

### User Prompt
> 4th project  
> *(Attached: `student_attendance.zip`)*

### Implementation Summary
- Extracted `student_attendance.zip` (`1.jpg`–`5.jpg`) into `assets/projects/attendance/`.
- Replaced the 4th project placeholder in `portfolioData.projects[3]` with **Mobile App - Offline Student Attendance System** (`Mobile Application / Offline`), including a 3-screen portrait mobile showcase on the project card header and all 5 screenshots in the interactive gallery slider.

---

## Prompt 3 — UI Refinements, 3D Depth Carousels & Resume PDF Button

### User Prompt
> remove this from the header img1 and footer img2--- the certificates and projects should be horizontally scrollable where the one being viewed shows closer and the others are animated to the back and replace the explore project to a My Resume Pdf Button and remove the View CErtifications butt beside it  
> *(Attached: reference images + Resume PDF)*

### Implementation Summary
- Removed the `SYS.ONLINE` status pill from the header and the `MATTE HARDWARE UI · OPTIMIZED FOR VERCEL` line from the footer.
- Saved the uploaded resume PDF to `assets/resume/Russel_Tristan_Marzo_Resume.pdf`, replaced the `"Explore Projects"` button with a **`My Resume PDF`** button linking to the PDF, and removed the `"View Certifications"` button beside it.
- Converted both the **Certifications & Eligibility** and **Featured Projects** sections into horizontally scrollable 3D center-focus depth carousels (`setupDepthCarousel`), where the centered card scales forward (`.is-active-card`) and neighboring cards animate to the back (`.is-back-card` / `.is-far-card`).

---

## Prompt 4 — Sequential Screenshot Ordering

### User Prompt
> the projects screenshots are numbered per project, follow the sequence;

### Implementation Summary
- Updated `portfolioData.projects` so that every project's `coverImage`, `mobileShowcase`, and `gallery` array strictly follow the numbered file sequence (`1, 2, 3, ...`) for Flowershop (`1.png`–`9.png`), Registrar Grade Report Keeping System (`1.png`–`5.png`), 88 Mini System (`1.png`–`6.png`), and Offline Student Attendance System (`1.jpg`–`5.jpg`).

---

## Prompt 5 — Footer Looping GIF / Hardware Display Module

### User Prompt
> put this on the footer as a gif; find a spot for it that that doesnt interfere are worsen the footers aesthetics  
> *(Attached: `YouCut_20261108_203754988.mp4`)*

### Implementation Summary
- Saved the video clip to `assets/media/footer-loop.mp4` and embedded it as a silent, seamlessly looping (`autoplay loop muted playsinline`) recessed hardware mini-display module inside the footer's 12-column grid.

---

## Prompt 6 — Footer Display Replacement, Resizing & Column Swap

### User Prompt
> replace it with this and make it bigger and swap places with the socials  
> *(Attached: `VID_20261108211110.mp4`)*

### Implementation Summary
- Replaced `assets/media/footer-loop.mp4` with the newly uploaded clip (`1184 × 720`).
- Enlarged the recessed hardware display frame (`w-64 sm:w-72 md:w-80`) and swapped its column position with the social links so the display sits in the center column (`lg:col-span-4`) and **Connect via Social Channels** sits in the right column (`lg:col-span-3`).

---

## Prompt 7 — GitHub Repository Push & Prompt Log Documentation

### User Prompt
> push to https://github.com/cobyRuss/eportfolio.git  
> create promptlog md

### Implementation Summary
- Initialized the local Git repository on branch `main`, created this [`promptlog.md`](promptlog.md) documentation file, committed all project files, and synced with GitHub.

---

## Prompt 8 — Uniform Hero CTA Button Sizing

### User Prompt
> make this the same size  
> *(Attached: screenshot of `My Resume PDF` and `github.com/cobyRuss` buttons)*

### Implementation Summary
- Standardized both `#heroResumeBtn` (`My Resume PDF`) and `#heroGithubBtn` (`github.com/cobyRuss`) in [`index.html`](index.html) to identical dimensions (`h-11 w-52 px-5 rounded-lg text-sm font-medium inline-flex items-center justify-center gap-2`).

---

## Prompt 9 — Automatic Git Push Configuration

### User Prompt
> auto push changes

### Implementation Summary
- Configured Git credential binding for `cobyRuss`, linked both remote push URLs (`portyy.git` and `eportfolio.git`), and installed a `.git/hooks/post-commit` hook so every commit automatically pushes to `origin/main`.

---

## Prompt 10 — Center-Lock Carousel Fix for Projects & Certificates

### User Prompt
> projects and certificates dont get centered when choosen,, lock center when choosen  
> *(Attached: 4 mobile iOS screenshots showing selected carousel cards shifted slightly right of center)*

### Implementation Summary
- Wrapped each `.depth-carousel-item` inside an untransformed `.carousel-snap-slot` container (`scroll-snap-align: center; scroll-snap-stop: always; flex: 0 0 var(--slot-w)`) so CSS 3D depth transforms (`scale` / `translate3d`) never distort scroll-snap bounding boxes on iOS Safari or desktop browsers.
- Replaced fragile scroll padding with `::before` and `::after` flex spacer pseudo-elements (`flex: 0 0 calc((100% - var(--slot-w)) / 2)`) on `.depth-carousel-track`, guaranteeing the first (`01`) and last (`05` / `04`) cards can lock dead-center in the viewport.
- Updated `setupDepthCarousel()` in [`index.html`](index.html) to compute exact center coordinates from the untransformed `.carousel-snap-slot` elements, added an `isProgrammaticScroll` lock during smooth scrolling so intermediate scroll frames cannot hijack the active selection, and locked the final `scrollLeft` position once the transition completes.

---

## Prompt 11 — Swipe Loop / Wrap-Around Back to Slide 01

### User Prompt
> when i reach the last certificate or project; the next swipe will go back to 1

### Implementation Summary
- Upgraded `.depth-carousel-track` inside `.depth-carousel-viewport` to a transform-driven 3D stage (`translate3d(tx, 0, 0)`) with live 1:1 touch-drag (`touchstart`/`touchmove`/`touchend`), desktop mouse drag, and horizontal trackpad wheel support.
- Mathematically locks every chosen card (`01` through `05` / `04`) to the exact pixel center of `.depth-carousel-viewport` (`viewport.clientWidth / 2 - (slot.offsetLeft + slot.offsetWidth / 2)`), eliminating iOS Safari scroll-snap and rubber-band edge bugs.
- When reaching the last certificate (`05 / 05`) or last project (`04 / 04`), swiping left (or dragging/scrolling forward) wraps smoothly back to `01` (`01 / 05` and `01 / 04`), and swiping right on `01` wraps to the last item.

---

## Prompt 12 — Mobile Full-Screen Section Fitting & Vertical Swipe Deck

### User Prompt
> on phone devices, every pill/badges should fit the screen and instead of scrolling down; itll be a swipe down to next pill/badge. here is how it looks on my phone; most dont fit especially the tech stack (named images)  
> *(Attached: `a.zip` containing `about.jpg`, `education.jpg`, `tech stack.jpg`, `certificates.jpg`, `projects.jpg`, `contact.jpg`)*

### Implementation Summary
- Structured the 6 portfolio views (`#about`, `#education`, `#skills`, `#certifications`, `#projects`, `#contact`) as `.mobile-slide` screens inside `#mobileViewport` and `#mobileDeck`.
- Optimized mobile (`< 640px`) sizing and spacing across all 6 screens so every card, pill, badge, all **10 Technical Stack modules** (`grid-cols-2 gap-2`), Certificate carousel cards, Project carousel cards (including tags and `"Open Gallery Slider →"`), and Contact/Footer elements fit 100% inside a single phone viewport (`calc(100dvh - 3.5rem)`) with zero clipping.
- Implemented `setupMobileVerticalDeck()` in [`index.html`](index.html) so on phone devices (`< 640px`), vertical swipes smoothly transition one full-screen section at a time (`01 About -> 02 Education -> 03 Tech Stack -> 04 Certifications -> 05 Projects -> 06 Contact`, wrapping back to `01 About` after the last section) with right-edge LED progress dots.

---

## Prompt 13 — Tech Stack Card Layout Refinement (Name Beside Logo)

### User Prompt
> everything was good execept the tech stack didnt actually fit. on both phone and pc on tech stack, remove the FW-01,LG-02,UI-03 etc and put the names (Laravel,PHP,HTML5etc) beside the logos, so it fits in the phone

### Implementation Summary
- Removed the module codes (`FW-01`, `LG-02`, `UI-03`, etc.) from `portfolioData.technicalStack` and [`renderTechStack()`](index.html).
- Placed each technology name (`Laravel`, `PHP`, `HTML5`, etc.) directly beside its logo icon on the top row (`flex items-center gap-2.5 sm:gap-3`) with the category badge underneath on both phone and PC, reducing the vertical height of all 5 mobile rows so all 10 Tech Stack cards fit comfortably on phone screens.

---

## Prompt 14 — Mobile Pill & Badge Alignment Fix

### User Prompt
> align pills/badges on phone, its crooked asf

### Implementation Summary
- **Hero Tech Stack Pills (`#heroStackPills`) & CTA Buttons:** Converted `#heroStackPills` on phone (`< 640px`) from a jagged `flex-wrap` row to a symmetric 2-column grid (`grid grid-cols-2 sm:flex sm:flex-wrap gap-1.5`) where every pill shares an exact `h-7 w-full` footprint, centered text, and `leading-none whitespace-nowrap`. Aligned the two CTA buttons (`My Resume PDF` and `github.com/cobyRuss`) in a matching 2-column grid below.
- **Tech Stack Category Badges (`renderTechStack`):** Converted each card's category badge (`Backend Framework`, `Client Logic`, etc.) from a variable-width `inline-block` span into a full-width centered pill (`flex items-center justify-center w-full h-6 px-2.5 rounded-full leading-none whitespace-nowrap truncate`) so all 10 category pills align edge-to-edge across the 2-column grid.
- **Education, Certifications, Projects & Contact Badges:** Standardized heights (`h-6` / `h-8`), vertical centering (`inline-flex items-center justify-center leading-none whitespace-nowrap`), and 2-column symmetric tag grids (`grid grid-cols-2 sm:flex`) across `#education`, `#certifications`, `#projects`, and `#contact`.

---

## Prompt 15 — Mobile Slide Vertical Drift & Disappearing Navbar Fix (iOS Safari)

### User Prompt
> its nice what you did on about but i was talkin bout something entirely different, look at how the images are aligned on the folder. i cant even see the navbar anymore  
> *(Attached: `aaa.zip` containing `1 about.jpg`, `2 education.jpg`, `3 tech stack.jpg`, `4 certificates.jpg`, `5 projects.jpg`, `6 footer.jpg`)*

### Root Cause & Implementation Summary
- **Root Cause Identified from `aaa.zip`:** On iOS Safari, Tailwind CDN's `.min-h-screen` (`min-height: 100vh`) and `.flex-grow` stretched `<body>` (`~750px`) and `#mobileViewport` (`~692px`) by ~90px past the visible viewport above Safari's bottom address bar (`100dvh` / `window.visualViewport.height`, where `.mobile-slide` was clamped to `~602px`). That 90px mismatch:
  1. Allowed iOS Safari to scroll the document down by 90px, pushing the `56px` `<header>` navbar off the top of the screen.
  2. Caused `wrapped * viewport.clientHeight` (`wrapped * 692px`) to overshoot each `.mobile-slide` (`wrapped * 602px`) by `90px × slideIndex` (`90px`, `180px`, `270px`, `360px`, `450px`), cutting every section in half between two slides.
- **Fix Applied in [`index.html`](index.html):**
  - Locked `html, body` on `< 640px` with `position: fixed !important; inset: 0 !important;` and dynamically synced `--app-h` (`visualViewport.height`) and `--slide-h` (`appH - headerH - 2`) with `!important` on both `#mobileViewport` and `.mobile-slide`, keeping `<header>` permanently visible at the top of the screen.
  - Updated [`setupMobileVerticalDeck()`](index.html) to translate `#mobileDeck` to `-slides[wrapped].offsetTop` instead of `wrapped * viewport.clientHeight`, guaranteeing zero cumulative vertical drift across all 6 slides.

