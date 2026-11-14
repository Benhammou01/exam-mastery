# Exam Mastery — a strict AI tutor skill for Claude

A [Claude skill](https://claude.com) that turns Claude into a strict, patient private tutor. Give it your own course files and an exam date; it teaches in short modules, quizzes you after each one, makes you explain concepts back, tracks your mistakes, and ends with a revision sheet and a spaced-revision plan.

Works for **any subject** (physics, cosmology, chemistry, maths, economics, biology, law…) and any exam type (QCM/MCQ, exercises, oral, essay).

## What it does

- Stays **strictly inside your course**: your notation, definitions and examples. Outside additions are labelled "Hors cours :".
- Never invents a formula or result; flags unreadable or missing passages.
- Teaches in **10–15 minute modules**, simplest to hardest, adapting pace to your answers.
- Asks **3 questions after every module** (direct, application, trap/transfer) *before* giving answers, and refuses to advance on "ok, continue".
- Makes **you teach it back**, then attacks the weak spots like a confused classmate.
- Keeps an **error journal** (concept / calculation / method / carelessness / memorization).
- Produces a **one-page revision sheet** and a **spaced-revision plan** up to exam day.
- Prioritizes past-exam themes and TD exercises when time is short.

## Install

### Claude.ai (web / desktop / mobile)
1. Download [`exam-mastery.skill`](https://github.com/Benhammou01/exam-mastery/raw/main/exam-mastery.skill) (click the link, the file downloads directly).
2. Open it in Claude and click **Save skill** (or go to Settings → Capabilities → Skills → Upload skill).
3. Make sure skills / code execution are enabled in your settings.

### Claude Code
```bash
git clone https://github.com/Benhammou01/exam-mastery.git
cp -r exam-mastery/skills/exam-mastery ~/.claude/skills/
```

## How to use

Attach your course (PDF, slides, notes, TDs, past exams) and say what you need. Examples:

> I have a QCM exam in 2 days on thermodynamics. Here is my course. I have 2 hours today and no background.

> Fais-moi réviser le chapitre 3 de génétique, examen vendredi, j'ai 1h30. Cours et TD en pièces jointes.

> Teach me this chapter and quiz me, my exam is tomorrow.

The skill triggers automatically. Then:

1. **Confirm** the files Claude received.
2. Answer the 2 starter questions (no background) or the short diagnostic.
3. Work module by module. **Answer every question before asking for the solution.**
4. End the session by **copying the error journal** Claude gives you.
5. Next session, paste the journal back in so Claude starts with your weak points.

### Tips
- The more complete the files (course + TD + past exams), the better the prioritization.
- State the exam date and your time budget; the skill compresses or expands the plan accordingly.
- It teaches in the language you write in. Write in French, it teaches in French.
- The official TD correction always wins over the tutor if they disagree.

## Repository layout

```
skills/exam-mastery/
├── SKILL.md                  # the skill instructions
└── references/templates.md   # error journal, sheet, revision-plan formats
```

## Contributing

Issues and pull requests welcome: new exam-type handling, better trap-question patterns, translations of the templates.

## License

MIT
