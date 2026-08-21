# Learning patterns and teaching strategies

This project consumes the canonical learning-pattern library in [`getrdone/agent-skills`](https://github.com/getrdone/agent-skills/tree/main/skills/curiosity-driven-scripture-journey). Do not fork or copy the pattern definitions into this repo; improve them at the canonical source.

## Agent workflow

1. Load [the skills catalog](https://github.com/getrdone/agent-skills/blob/main/CATALOG.md) and the [Curiosity-Driven Scripture Journey skill](https://github.com/getrdone/agent-skills/blob/main/skills/curiosity-driven-scripture-journey/SKILL.md).
2. Define the question, audience, known anchor, new idea, evidence path, payoff, and interpretive boundaries.
3. Use the [learning-pattern router](https://github.com/getrdone/agent-skills/blob/main/skills/curiosity-driven-scripture-journey/references/learning-patterns.md) to select 3–5 patterns from at least two families. Give each one a different learning job.
4. Record the selection in the project's `learning_pattern_plan`.
5. Load only the selected family files:
   - [guided understanding](https://github.com/getrdone/agent-skills/blob/main/skills/curiosity-driven-scripture-journey/references/pattern-guided-understanding.md)
   - [active discovery](https://github.com/getrdone/agent-skills/blob/main/skills/curiosity-driven-scripture-journey/references/pattern-active-discovery.md)
   - [feedback and mastery](https://github.com/getrdone/agent-skills/blob/main/skills/curiosity-driven-scripture-journey/references/pattern-feedback-and-mastery.md)
   - [access, agency, and momentum](https://github.com/getrdone/agent-skills/blob/main/skills/curiosity-driven-scripture-journey/references/pattern-access-agency-momentum.md)
6. Implement the learner action, evidence-based feedback or payoff, and accessible equivalent. Validate against the skill's quality gates.

## Required plan shape

```yaml
learning_pattern_plan:
  - id: LP-XX-00
    job:
    placement:
    learner_action:
    feedback:
    accessible_fallback:
    evidence_material:
```

A pattern is not a decorative widget. It must help the learner orient, understand, inspect, practice, recover, retrieve, access, reflect, or choose. Do not grade doctrine, hide the answer behind an interaction, assign fixed learning-style labels, or use streak pressure.

For observed platform flows and primary references, use the [provenance ledger](https://github.com/getrdone/agent-skills/blob/main/skills/curiosity-driven-scripture-journey/references/learning-pattern-sources.md).

## Source-material boundary

Study documents, transcripts, passage research, and other evidence belong in this repo's existing [`sources/`](sources/) library and registry. The learning-pattern definitions remain in `agent-skills`.
