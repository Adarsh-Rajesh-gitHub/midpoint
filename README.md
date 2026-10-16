# Midpoint

A learn-by-doing web app that teaches expected value through 14 visual, interactive problems across 5 lessons, with AI-generated adaptive practice layered on learning-science principles.

**Live app:** **https://expected-value-lab.web.app/**

**Decision record / BrainLift:** see [`BrainLift.md`](./BrainLift.md) for the reasoning behind the AI-first build process and the app-design decisions.

## What's in the app

The chapter "Expected Value" is built in three deliberate phases:

- **Phase 1 — Curriculum (no AI).** Five lessons and 14 hand-built, visual, interactive problems that move from simulation intuition to a complete expected value model. The app owns all grading, hints, feedback, mastery, streaks, and milestones.
- **Phase 2 — AI as a controlled generator.** A "Practice" mode generates fresh expected-value problems via OpenAI, **server-side only** through Firebase Cloud Functions. AI fills surface-level content (scenario copy, numbers within constraints, distractors); the app keeps full ownership of grading, answer keys, difficulty, and mastery. A deterministic difficulty matrix and a deterministic fallback guarantee valid problems even if the model fails.
- **Phase 3 — Learning science.** Adaptive practice adds spaced repetition, interleaving across problem types, and difficulty scaffolding (guided → supported → independent) driven by a per-skill mastery model.
