# Russel Tristan L. Marzo (Coby) — Developer E-Portfolio

A responsive, single-page developer e-portfolio engineered with a **Matte PC Hardware UI** aesthetic, built with semantic HTML5, Tailwind CSS, and vanilla JavaScript, and optimized for zero-config static deployment on Vercel.

- **Live Portfolio:** [https://russeltlm.vercel.app](https://russeltlm.vercel.app)
- **GitHub Repositories:** [cobyRuss/eportfolio](https://github.com/cobyRuss/eportfolio) · [cobyRuss/portyy](https://github.com/cobyRuss/portyy)
- **Development Prompt Log:** [`promptlog.md`](promptlog.md)

---

## Design System — Matte PC Hardware Theme

| Token / Element | Specification |
| :--- | :--- |
| **Chassis Background** | Matte dark charcoal/zinc (`#18181b` / `zinc-900`) with a 40×40px technical grid overlay (`rgba(255,255,255,0.018)`) and a diffused radial crimson ambient vignette (`rgba(225, 29, 72, 0.08)`). Pure `#000000` is strictly avoided. |
| **LED Accent Palette** | Soft crimson/cherry red (`#e11d48` / `rose-600`) for status indicators, active borders, and interactive highlights; emerald (`#10b981`) for verified credentials and location badges. |
| **Hardware Cards** | Glassmorphic zinc panels (`rgba(39, 39, 42, 0.55)`) with `backdrop-filter: blur(10px)` and `1px` borders that illuminate with a soft crimson glow on hover. |
| **Typography** | **Inter** for UI headings and body copy; **JetBrains Mono** for system counters, tags, and diagnostic labels. |

---

## Key Features

### 1. Hero & Developer Profile (`#about` & `#education`)
- **Circular Avatar with Diffused Crimson LED Ring:** Displays `assets/profile/profile.jpg` (with an automatic `RM // COBY` monogram fallback) and a `BANGUED, ABRA` location indicator pill.
- **Aligned Tech Stack Summary Pills & Quick Actions:** Renders all 10 core technologies in a symmetric 2-column pill grid on mobile (`< 640px`) and an inline pill strip on desktop (`>= 640px`), paired with uniform-size **My Resume PDF** (`assets/resume/Russel_Tristan_Marzo_Resume.pdf`) and **GitHub** (`github.com/cobyRuss`) buttons.
- **Biography & Academic Specification Cards:**
  - `01 // Developer Profile (BIO.SYS)`: Highlights primary focus (`Web & Offline Systems`) and `CSC Professional` eligibility.
  - `02 // Academic Specification (EDU.LOG)`: Bachelor of Science in Information Technology at **Data Center College of the Philippines — Bangued** (`4th Year - Currently Enrolled`).

### 2. Technical Stack Grid (`#skills`)
- Displays all **10 core technologies** (`Laravel`, `PHP`, `HTML5`, `CSS3`, `JavaScript`, `MySQL`, `SQLite`, `Git & GitHub`, `VS Code`, `XAMPP`) in a responsive 2-column mobile / 5-column desktop grid.
- Each module places the technology name directly beside its custom SVG icon on the top row with a full-width centered category pill underneath so all 10 cards fit cleanly inside a single mobile viewport.

### 3. Center-Locked 3D Depth Carousels (`#certifications` & `#projects`)
- **Mathematical Center Lock:** Built on a transform-driven 3D stage (`translate3d(tx, 0, 0)`) that locks the active card dead-center in the foreground (`.is-active-card` at `scale(1)`) while receding neighboring cards into the background (`.is-back-card` at `scale(0.84)` and `.is-far-card` at `scale(0.76)`).
- **Infinite Wrap-Around (`Last -> 01`):** Swiping left past the final certificate (`05 / 05`) or final project (`04 / 04`) smoothly wraps back to `01` (and swiping right on `01` wraps to the last item).
- **Multi-Input Navigation:** Supports 1:1 touch-drag on mobile, click-and-drag on desktop, horizontal trackpad gestures, `<` `>` buttons, and clickable pagination dots.

### 4. Interactive Lightbox Modal Slider
- Clicking **Inspect Certificate →** or **Open Gallery Slider →** opens a hardware-styled lightbox modal with:
  - Previous/Next slide controls and slide counter (`01 / 09`)
  - Numbered screenshot captions ordered strictly by filename (`1, 2, 3, ...`)
  - Interactive thumbnail strip with active crimson ring indicator
  - Keyboard shortcuts (`←`, `→`, `Escape`) and mobile touch-swipe support

### 5. Mobile Full-Screen Vertical Swipe Deck (`< 640px`)
- **Viewport-Locked iOS Safari Support:** Dynamically syncs `--app-h` (`window.visualViewport.height`) and `--slide-h` (`appH - headerH - 2`) with `position: fixed` on `html, body` so the sticky top navbar (`Coby.`) stays permanently visible and never scrolls off-screen.
- **Section-by-Section Vertical Swiping:** Instead of continuous vertical scrolling on phones, swiping up/down transitions cleanly between the 6 full-screen sections (`01 About -> 02 Education -> 03 Tech Stack -> 04 Certifications -> 05 Projects -> 06 Contact`, wrapping back to `01 About`) using exact DOM `offsetTop` coordinates with zero cumulative vertical drift and right-edge crimson LED progress dots.

### 6. Contact & Recessed Hardware Display Footer (`#contact`)
- Features direct one-tap email (`coby.2339@gmail.com`) and phone (`09357591816`) chips, a recessed looping hardware video display (`assets/media/footer-loop.mp4`) in the center column, and monochrome-to-crimson social channel links (GitHub, Facebook, Messenger, Instagram).

---

## Featured Projects (`portfolioData.projects`)

| # | Project Title | Category | Tech Stack Tags | Gallery |
| :-: | :--- | :--- | :--- | :-: |
| **01** | **Web App - Flowershop Online Website** *(HappyStem by Carmencita)* | Web Application | `PHP`, `MySQL`, `JavaScript`, `HTML5 / CSS3` | 9 Screenshots (`1.png`–`9.png`) |
| **02** | **Registrar Grade Report Keeping System** *(RGKRS)* | Offline Application | `Desktop App`, `SQLite`, `Offline System`, `Transcripts` | 5 Screenshots (`1.png`–`5.png`) |
| **03** | **Desktop App - 88 Mini System** *(88 Mini Mart POS)* | Desktop Application / POS | `POS Terminal`, `Inventory`, `Cash Drawer`, `Analytics` | 6 Screenshots (`1.png`–`6.png`) |
| **04** | **Mobile App - Offline Student Attendance System** | Mobile Application / Offline | `Mobile App`, `SQLite`, `Offline-First`, `Attendance Tracking` | 5 Screenshots (`1.jpg`–`5.jpg`) |

---

## Certifications & Eligibility (`portfolioData.certifications`)

| Code | Credential | Issuer | Date | Status |
| :-: | :--- | :--- | :--- | :-: |
| `CERT-01` | **Civil Service Professional** | Civil Service Commission (CSC CSEVS) | Eligibility, 2023 | Earned |
| `CERT-02` | **DOST Startup Cordillera** | DOST-CAR Innovation Hub (iHub) | September 2, 2026 | Earned |
| `CERT-03` | **Online Safety Through Netiquette** | DICT Region II — Cybersecurity | July 23, 2026 | Earned |
| `CERT-04` | **Introduction to Modern AI** | Cisco Networking Academy · DICT-ITU DTC | October 30, 2026 | Earned |
| `CERT-05` | **Understanding Startups & Philippine Startup Challenge XI** | DICT Cordillera Administrative Region | September 7, 2026 | Earned |

---

## Project Structure

```text
CobyPortfolio/
├── index.html                                      # Single-page application (HTML, CSS, portfolioData & JS controllers)
├── vercel.json                                     # Static Vercel routing configuration
├── README.md                                       # Project documentation
├── promptlog.md                                    # Chronological log of all prompts & architectural updates
└── assets/
    ├── favicon.svg                                 # Red capital "C" browser tab favicon
    ├── profile/
    │   └── profile.jpg                             # Hero avatar photo
    ├── resume/
    │   └── Russel_Tristan_Marzo_Resume.pdf         # Downloadable PDF resume
    ├── media/
    │   └── footer-loop.mp4                         # Recessed footer hardware display loop clip
    ├── certificates/
    │   ├── 1.png                                   # CSC Professional Eligibility
    │   ├── 2.png                                   # DOST Startup Cordillera
    │   ├── 3.png                                   # DICT Online Safety Through Netiquette
    │   ├── 4.jpg                                   # Cisco & DICT-ITU Introduction to Modern AI
    │   └── 5.jpg                                   # DICT Philippine Startup Challenge XI
    └── projects/
        ├── flowershop/                             # 1.png – 9.png (HappyStem Flowershop Web App)
        ├── rgkrs/                                  # 1.png – 5.png (Registrar Grade Report Keeping System)
        ├── minimart88/                             # 1.png – 6.png (88 Mini Mart POS System)
        └── attendance/                             # 1.jpg – 5.jpg (Offline Student Attendance Mobile App)
```

---

## Running Locally & Deployment

### Local Development
No build step or bundler is required:
1. Clone the repository:
   ```bash
   git clone https://github.com/cobyRuss/eportfolio.git
   ```
2. Open `index.html` directly in any modern browser, or serve the folder via XAMPP (`http://localhost/CobyPortfolio`) or VS Code Live Server.

### Deploying to Vercel
This repository includes [`vercel.json`](vercel.json) pre-configured for static hosting. Pushing to the `main` branch automatically triggers a production deployment on Vercel.
