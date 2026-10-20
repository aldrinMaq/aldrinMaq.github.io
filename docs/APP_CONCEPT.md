# APP_CONCEPT

Personal portfolio for Aldrin Maquiling. Resume PDF is the content source of truth for experience, skills, education, and featured work blurbs, except for the user-corrected school pairing below until the PDF is updated.

---

## Name

Aldrin Maquiling — Portfolio (`aldrinMaq.github.io`)

## One-liner

Static dark-theme portfolio showcasing fullstack work, commercial experience at mykuan.app, and personal/academic apps.

## Vision / problem

A single place for recruiters and clients to see experience, projects, skills, and contact — aligned with the downloadable resume.

## Who it's for

Hiring managers, clients, and collaborators evaluating Aldrin for fullstack / web development roles.

## Main flows

1. Land on hero → skim positioning
2. Read experience (mykuan.app)
3. Browse working demos and the Growgreen thesis screenshots → open project links
4. Check skills / education → contact or download resume

## Screens

Single page sections: Hero, Experience, Selected Work, Skills, Education, Contact. Mobile navigation links to the key sections; Experience, Projects, Skills, and Education are highlighted while their sections are in view. Contact keeps its normal button styling.

Target reader: hiring managers and recruiters for remote Java/Spring Boot + Vue.js/TypeScript roles. The hero names the stack, shows "open to remote · UTC+8", and repeats the resume numbers as stat tiles.

Selected Work features GoFindPro as a wide card (screenshot, problem, what I built, stack chips), followed by DinkSpot, WeatherCheck, Growgreen, and A&Z RentHub. Every live project has a screenshot in `assets/img/` (WebP, with 480px variants). DinkSpot links to its root URL because `/map` 404s on direct load. Growgreen shows two screenshots from the working 2025 thesis build (virtual tree and event eligibility); its frontend preview is available, but its backend is not deployed. The activity map screenshot is excluded because its displayed totals have not been verified as real-world results.

## Features

- Resume-aligned copy for KUAN / mykuan.app
- Selected projects with working links, concise descriptions, and two linked Growgreen thesis screenshots
- Technical expertise tags matching the resume
- Resume PDF download
- Contact via email + GitHub

## Out of scope

- Blog, CMS, auth, backend
- Vue/Vite migration (unless requested)

## Constraints

- Keep existing visual language unless a redesign is requested
- Content must stay consistent with `MAQUILING_ALDRIN_RESUME.pdf`

## Visual

- **Font:** Plus Jakarta Sans + JetBrains Mono
- **Accent:** emerald / teal on near-black zinc surfaces
- **Corner radius:** rounded-xl / rounded-2xl
- **Icon set:** inline SVG symbols in `index.html` (GitHub mark + stroke icons)

## Notes

- Commercial product: KUAN Store / mykuan.app
- Education: Computer Science (graduated, 2022–2025) is from North Eastern Mindanao State University; Information Technology (coursework through 3rd year, 2018–2021) is from Jose Rizal University. The resume PDF now matches.
- Project stacks and details not on the resume (DinkSpot uses React; RentHub uses JSON-LD) come from the project repos in `../`.
- Audit, gap matrix, and 5-second test: `docs/PORTFOLIO_AUDIT.md`.
