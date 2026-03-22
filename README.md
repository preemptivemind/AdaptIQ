# AdaptIQ — K–12 Adaptive Assessment

A single-file, browser-based adaptive testing platform covering the full K–12 curriculum in Mathematics and Reading & Vocabulary. No server, no login, no installation — open the HTML file in any browser and start.

---

## Features

### Two Test Modes

**Standard Test**
- 60 questions (Math) or 45 questions (Reading)
- Computer-adaptive: question difficulty adjusts after every answer
- Choose your starting grade (K–12)
- Full answer review at the end
- Results saved to browser storage

**Live Test**
- Infinite adaptive questions — no finish line
- Real-time stats dashboard: Grade Equivalent, accuracy bar, streak dots, per-domain breakdown
- State saved after every answer; resume where you left off via the home screen banner
- Exit at any time; discard to clear the session

---

## Question Bank

**567 questions** across 7 domains, K–12

| Domain | Questions | Grades |
|---|---|---|
| Algebra | 89 | K–12 |
| Numbers & Operations | 58 | K–12 |
| Geometry | 83 | K–12 |
| Statistics & Data | 76 | K–12 |
| Comprehension — Fiction | 48 | K–12 |
| Comprehension — Nonfiction | 56 | K–12 |
| Vocabulary | 157 | K–12 |

All questions are aligned to CCSS standards, verified for a single correct answer, and free of duplicate values in the choice set.

---

## Adaptive Engine

### Question Selection
The engine maintains a per-domain level score (0–12.9) that adjusts ±0.3 after each answer. Questions are selected by expanding outward from the target grade until an unused question is found, matching difficulty (easy/medium/hard) as closely as possible.

### Reported Level (Standard Test)
The displayed Grade Equivalent reflects the **highest grade where per-grade accuracy ≥ 75%**. Early failures at high grades do not permanently cap the score — each grade is assessed independently.

### Reported Level (Live Test)
Uses a **sliding window of the last 12 answered questions per domain**. The level rises when you perform well at higher grades and falls when performance drops — allowing natural movement up and down over time.

### Grade Equivalent Display
- Format: `8.5` = Grade 8, 5 months
- Accompanied by Lexile (Reading) or Quantile (Math) measure
- Overall GE = average of domain reported levels

---

## Scoring Rules

- **I don't know** counts the same as a wrong answer for scoring and adaptive level
- **Correct answers are never revealed** during the live test
- **75% proficiency threshold**: a grade is considered mastered when ≥75% accuracy is achieved across all attempted questions at that grade

---

## Grade Mapping (Selected Topics)

| Topic | Grade |
|---|---|
| Fact families (addition/subtraction) | 1–2 |
| Fact families (multiplication/division) | 3 |
| Linear equations, one operation | 6 |
| Linear equations, variables on both sides | 8 |
| Trapezoid area | 8 |
| Complex numbers — addition, i² | 10 |
| Conic sections — circle, parabola | 10 |
| Complex numbers — multiplication, conjugate, modulus | 11 |
| Conic sections — ellipse | 11 |
| Conic sections — hyperbola | 12 |
| Inferential statistics (hypothesis testing, p-values) | 12 |

---

## Storage

All data is stored in **localStorage** (no server, no account required).

| Key | Contents |
|---|---|
| `adaptiq-session` | In-progress standard test state |
| `adaptiq-live` | In-progress live test state |
| `adaptiq-results` | Past completed standard test results |

Past results are never capped — every completed standard test is saved. Use "Clear all" on the home screen to reset.

---

## Usage

1. Open `adaptive-test-site.html` in any modern browser (Chrome, Edge, Firefox, Safari)
2. Select a subject (Mathematics or Reading & Vocabulary)
3. Select your current grade
4. Click **Continue** for a standard test, or click **⚡ Live Math / ⚡ Live Reading** for live mode
5. Answer questions — press **I don't know** to skip with a penalty
6. Standard test: view your full results and answer review at the end
7. Live test: press **✕ Exit** at any time; your session is saved for resuming

---

## Technical Notes

- **Single HTML file** — all questions, styles, and logic are self-contained
- **No external dependencies** at runtime (fonts loaded from Google Fonts CDN)
- **Pure localStorage** for persistence — works in any browser including Edge
- **~242 KB** file size
- Tested in Chrome, Microsoft Edge, Firefox, and Safari

---

## Question Notation

- Arithmetic multiplication: raised dot `·` (e.g. `7 · 8`)
- Dimensions and scientific notation: `×` (e.g. `4 cm × 5 cm`, `4.7 × 10⁻⁵`)
- Linear algebra and matrix operations: `×`
- Combinatorics: standard `nCr` / `nPr` notation (e.g. `8C3`, `6C2`)# AdaptIQ
Repo for the evalearned project
