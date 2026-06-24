# SemGPA

**Live demo → [semgpa.vercel.app](https://semgpa.vercel.app/)**

A clean, mobile-friendly web tool to plan your semester grades, track CGPA, and calculate the average SGPA you need across remaining semesters to hit your target CGPA.

## Features

- **Live SGPA calculation** — enter CIE marks and SEE targets, grades update instantly
- **Projected CGPA** — see your CGPA after this semester in real time
- **Average SGPA needed** — calculates what you need per remaining semester to reach your goal CGPA
- **Balanced SEE optimizer** — auto-distributes marks as evenly as possible across subjects
- **CGPA history** — save and reload previous semester results
- **Light / Dark mode** — toggle with the button in the header, preference saved
- **Mobile friendly** — fully responsive at all screen sizes

## Usage

Just open `index.html` in any browser — no build step, no dependencies.

## Grade Scale (VTU / similar)

| Grade | Points | Total Marks |
|-------|--------|-------------|
| O     | 10     | ≥ 90        |
| A+    | 9      | 80 – 89     |
| A     | 8      | 70 – 79     |
| B+    | 7      | 60 – 69     |
| B     | 6      | 50 – 59     |
| C     | 5      | 45 – 49     |
| D     | 4      | 40 – 44     |
| F     | 0      | < 40        |

> Total = CIE (out of 50) + SEE / 2 · Minimum passing SEE = 40 / 100

## Formula

**Projected CGPA after this semester:**

$$\text{CGPA}_{n+1} = \frac{\text{CGPA}_n \times n + \text{SGPA}}{n + 1}$$

**Average SGPA needed for remaining semesters:**

$$\text{Avg SGPA needed} = \frac{\text{Target CGPA} \times \text{Total Sems} - \text{Projected CGPA} \times \text{Current Sem}}{\text{Remaining Sems}}$$

## Design

Built with the [Vercel Geist](https://vercel.com/geist) design system — Geist Sans + Geist Mono, near-white canvas, 1px hairline cards, hero mesh gradient.
