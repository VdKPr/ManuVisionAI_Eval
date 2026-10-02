# ManuVisionAI-Eval

A standard procedure for evaluating AI models and systems, and the record of applying it to real systems.

**Status: early.** The standard is being written. The first engagement has not started yet.

---

## What this is

Two things will live here.

**The standard** — a general procedure for evaluating an AI model or system: what to establish before measuring, how to evaluate a system made of several components, how to write an evaluation guideline, how to choose methods and data, and how to check that the evaluation pipeline itself is trustworthy.

It is meant to be general. It should apply to a foundation model application, a classifier, or a pipeline that mixes both — not to one project.

**The engagements** — the record of running that procedure against a specific system: what was measured, what the numbers were, what went wrong, and what the evaluation failed to catch.

The standard is the product. A system being evaluated is just the first client.

---

## Why separate the two

A procedure written around one project's problems is a post-mortem, not a standard. Keeping the engagement record separate from the procedure forces the procedure to stay general enough to reuse, and keeps the evidence where it belongs.

---

## First engagement (planned)

**ManuVision AI** — [`VdKPr/ManuVisionAI`](https://github.com/VdKPr/ManuVisionAI) — an automated visual defect inspection system built on the MVTec AD benchmark: a ResNet18 defect classifier, a U-Net segmenter, a measurement stage with accept/reject tolerances, a GPT-4o-mini root-cause stage, and a LangGraph agent routing between them.

It makes a reasonable first subject because it is a hybrid — several close-ended components and one open-ended one — so it exercises the whole procedure rather than half of it.

---

## Structure

```
standard/      The evaluation procedure.
engagements/   One folder per system evaluated.
tools/         Shared harness and reporting code.
reference/     Study notes behind the standard.
```

---

## Sources

The structure follows Chip Huyen, *AI Engineering: Building Applications with Foundation Models* (O'Reilly, 2025), Chapter 4, "Evaluate AI Systems." The book itself is not included here — it is copyrighted and excluded by `.gitignore`.

---

## Licence

Code in this repository is MIT licensed (see `LICENSE`).

---

*Varad Pawar — [github.com/VdKPr](https://github.com/VdKPr) · [linkedin.com/in/varadkpawar](https://linkedin.com/in/varadkpawar)*
