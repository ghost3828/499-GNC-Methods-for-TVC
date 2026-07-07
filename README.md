# GNC Methods for Thrust Vector Control — Course Website

Courseware for a 3-week (3 semester hour) independent study: **Guidance, Navigation, and Control
methods for a thrust-vector-controlled model rocket.** USAFA Astro department. Pure static
HTML/CSS — no build step, no dependencies — designed to deploy directly on GitHub Pages.

## Site map

| File | Contents |
|---|---|
| `index.html` | Study overview, 15-day timeline, phase summaries, milestone table |
| `syllabus.html` | Course info, prerequisites, learning outcomes, full schedule, grading |
| `phase1.html` | Days 01–05: attitude kinematics/dynamics, open-loop 3DOF sim, MR-1 |
| `phase2.html` | Days 06–10: PID, discrete-time FSW, sensor models, estimation, MR-2 |
| `phase3.html` | Days 11–15: Arduino flight software, bench closed loop, MR-3, final report |
| `hardware.html` | Parts list (verified SparkFun part IDs), wiring notes, safety |
| `resources.html` | Full reference library + glossary |
| `assets/style.css` | Single shared stylesheet |
| `.nojekyll` | Tells GitHub Pages to skip Jekyll processing (faster, safer for plain HTML) |

## Deploy on GitHub Pages

1. **Create a repository** on github.com (e.g., `tvc-gnc-study`). Public repos get free Pages
   hosting on all plans.

2. **Push these files** (they must sit at the repo root):

   ```bash
   cd tvc-gnc-site
   git init
   git add .
   git commit -m "Initial courseware"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/tvc-gnc-study.git
   git push -u origin main
   ```

3. **Enable Pages:** on GitHub, open the repo → **Settings → Pages** → under *Build and
   deployment*, set **Source: Deploy from a branch**, **Branch: `main`**, folder **`/ (root)`** →
   **Save**.

4. Within a minute or two the site is live at:

   ```
   https://YOUR-USERNAME.github.io/tvc-gnc-study/
   ```

   (Or upload the files through the GitHub web UI — *Add file → Upload files* — if you'd rather
   skip the command line.)

## Editing

- Everything is plain HTML; edit any page in a text editor (or directly on GitHub with the pencil
  icon) and push — Pages redeploys automatically on every commit to `main`.
- Fill in the bracketed placeholders in `syllabus.html`: honor-code and AI-tool policies.
- Colors, fonts, and spacing all live in `assets/style.css` (design tokens at the top of the file).
- Items tagged **Shared folder** refer to material in
  `\USAFA Astro - GNC TVC Study\` that isn't publicly linkable; adjust those pointers to
  wherever your student will actually access them.

## Local preview

Just open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit
`http://localhost:8000`.
