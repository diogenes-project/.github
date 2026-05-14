# Diogenes

**Deterministic AI research coordination through structured
scientific methodology.**

Diogenes makes AI agents produce defensible, auditable, evidence-based
research instead of sycophantic confirmation of what you already
believe. It combines nine frameworks from intelligence analysis,
clinical medicine, climate science, systematic review methodology,
institutional standards, and the philosophy of science into a
structured process that constrains AI behavior through enforcement
language.

---

## What this is

A structured research methodology that makes AI agents produce
defensible, auditable, evidence-based research. It combines frameworks
from intelligence analysis (ICD 203), clinical medicine (GRADE,
Cochrane, CONSORT), climate science (IPCC), systematic review
methodology (PRISMA, ROBIS), institutional standards (NAS), and the
philosophy of science (Chamberlin/Platt).

The methodology was developed to solve a specific problem: AI agents,
when asked to "research this," default to building a case rather than
conducting an investigation. They confirm what you expect, minimize
contradictions, and present uncertain conclusions as settled. This
methodology constrains that behavior through enforcement language —
telling the AI not just what to do, but what it is prohibited from
doing and why.

The detailed background behind this methodology — the framework
evaluation, the design decisions, and the evidence for every feature —
is discussed in a pair of articles:

- [The Truth is Out There. But How Do You Find It?][part1]
  — the what and the why (Part 1)
- [The Truth is Out There. Now Go Find It.][part2]
  — the how and how to get it (Part 2)

[part1]: https://the-infrastructure-mindset.ghost.io/the-truth-is-out-there/
[part2]: https://the-infrastructure-mindset.ghost.io/the-truth-is-out-there-now-go-find-it/

## Three input types

- **Claims** — factual assertions to verify. Each claim is tested
  against competing hypotheses with evidence scored for reliability,
  relevance, and bias.
- **Queries** — research questions to answer. Each question generates
  hypotheses ranked by evidence strength.
- **Axioms** — facts declared by the researcher that must be assumed
  true during the investigation. Not tested — they function as
  constraints that frame the research.

All three can be combined in a single research run.

Research produces complete evidence archives: source scorecards, search
logs, hypothesis evaluations, collection-level synthesis, gap
identification, and a five-domain self-audit.

## The frameworks

| Domain | Framework |
|--------|-----------|
| Intelligence analysis | ICD 203 |
| Clinical medicine | GRADE, Cochrane, CONSORT |
| Climate science | IPCC |
| Systematic review | PRISMA, ROBIS |
| Institutional standards | NAS |
| Philosophy of science | Chamberlin/Platt |

## The 11-step process

1. **Claim/query received and clarified** — ambiguities surfaced,
   assumptions identified, axioms acknowledged
2. **Vocabulary exploration** — map terminology across domains before
   searching
3. **Competing hypotheses generated** (Chamberlin/Platt) — minimum
   three
4. **Discriminating searches designed** — what would disprove each
   hypothesis?
5. **Searches executed and logged** (PRISMA) — every search documented
6. **Per-source scoring** (GRADE + Cochrane) — reliability, relevance,
   six bias domains
7. **Collection-level synthesis** (IPCC) — evidence quality, source
   agreement, independence
8. **Probability assessment** (ICD 203) — nine-point calibrated scale
   (including deterministic endpoints)
9. **Gap identification** (NAS) — what's missing and what it means
10. **Process self-audit + source-back verification** (ROBIS +
    net-new) — five-domain bias check including interpretation
    verification
11. **Report with revisit triggers** (ICD 203) — every claim sourced,
    every judgment explicit, specific conditions for re-research
    identified
12. **Temporal revisitation archive** — enable periodic re-execution

## Anti-sycophancy by design

The methodology includes explicit behavioral constraints that target
AI's most dangerous default behaviors:

- Evidence from research outranks training data
- The researcher's claims are inputs to test, not truths to confirm
- Contradictory evidence must be highlighted, not minimized
- Embedded assumptions must be surfaced and tested
- Uncertainty must be stated explicitly
- The AI cannot declare victory early — the full process runs every
  time

## Three ways to use it

- **Claude Code plugin** — installs as a skill, integrates directly
  into Claude Code sessions
- **Standalone prompt** — works with any capable LLM (Claude, ChatGPT,
  Gemini, or others)
- **dio CLI** — command-line interface for scripted research workflows

## Get started

The main repository has everything you need:
**[diogenes-project/diogenes](https://github.com/diogenes-project/diogenes)**

---

## Contributing

Contributions are welcome. See the
[contributing guidelines](https://github.com/diogenes-project/.github/blob/develop/CONTRIBUTING.md)
for development setup, workflow, and the AI contributor identity model.

---

## Author

Built by [Phillip Moore](https://github.com/wphillipmoore). The
detailed background behind this methodology — the framework evaluation,
the design decisions, and the evidence for every feature — is discussed
at [The Infrastructure Mindset](https://the-infrastructure-mindset.ghost.io).
