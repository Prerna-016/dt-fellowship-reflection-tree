# Daily Reflection Tree — Submission

A deterministic end-of-day reflection tool built for the DT Fellowship assignment.
No LLM at runtime. Questions designed from personal experience. Tree walked by simple JavaScript.

---

## Files

```
/
├── reflection-tree.json   ← The tree data (Part A)
├── index.html             ← Working agent — open in browser (Part B)
├── write-up.md            ← Design rationale
└── README.md
```

---

## How to Run

1. Download both `index.html` and `reflection-tree.json` into the same folder
2. Open `index.html` in any browser
3. Click Begin

No server needed. No install. No dependencies.

---

## The Three Axes

| Axis | Question | Spectrum |
|------|----------|----------|
| 1 — Locus | When plans didn't work out, what was your first thought? | Victim ↔ Victor |
| 2 — Orientation | When you helped someone, what was going through your mind? | Entitlement ↔ Contribution |
| 3 — Radius | In a disagreement, what were you mostly thinking about? | Self-centric ↔ Altrocentric |

---

## How the Tree Works

- Every question has **fixed options** — no free text
- Every option leads to a **known next node** — fully deterministic
- **Decision nodes** route based on selected answers or accumulated signals
- **Signals** tally which pole the person is leaning toward per axis
- **Reflections** are pre-written — no generation at runtime
- **Summary** is assembled from template strings based on dominant signals

Same answers always produce the same path. Every time.

---

## Node Types

| Type | What it does |
|------|-------------|
| start | Opens the session |
| question | Fixed-option question — employee picks one |
| decision | Internal routing — invisible to employee |
| reflection | Pre-written insight based on path taken |
| bridge | Transition between axes — auto-advances |
| summary | End-of-session synthesis |
| end | Closes the session |
