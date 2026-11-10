# claude-harness

Claude Code skills, hooks, and session tools from [Robert Nyborg](https://github.com/robertmnyborg). This repo is the catalog: one marketplace that installs any of them.

```
/plugin marketplace add robertmnyborg/claude-harness
/plugin install skill-eval@claude-harness
```

Codex, Cursor, and other agents that read `SKILL.md` can use the [skills CLI](https://skills.sh) on any skill repo below: `npx skills add robertmnyborg/<repo>`.

<table>
  <tr>
    <td width="33%" align="center"><a href="https://github.com/robertmnyborg/skill-eval"><img src="https://raw.githubusercontent.com/robertmnyborg/skill-eval/main/docs/images/skill-eval/cover.png" alt="skill-eval: A/B test whether a skill helps"></a></td>
    <td width="33%" align="center"><a href="https://github.com/robertmnyborg/analyst-rigor-skills"><img src="https://raw.githubusercontent.com/robertmnyborg/analyst-rigor-skills/main/docs/images/causal-claim/cover.png" alt="causal-claim: red-team a group comparison before running it"></a></td>
    <td width="33%" align="center"><a href="https://github.com/robertmnyborg/plan-notes"><img src="https://raw.githubusercontent.com/robertmnyborg/plan-notes/main/docs/images/plan-notes/cover.png" alt="plan-notes: inline review notes on a plan"></a></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/robertmnyborg/cmux-agent-kit"><img src="https://raw.githubusercontent.com/robertmnyborg/cmux-agent-kit/main/docs/images/spinoff/cover.png" alt="spinoff: move a side thread into a fresh session"></a></td>
    <td align="center"><a href="https://github.com/robertmnyborg/ux-evidence"><img src="https://raw.githubusercontent.com/robertmnyborg/ux-evidence/main/docs/images/ux-evidence/cover.png" alt="ux-evidence: evidence before UI code"></a></td>
    <td align="center"><a href="https://github.com/robertmnyborg/product-thinking"><img src="https://raw.githubusercontent.com/robertmnyborg/product-thinking/main/docs/images/product-thinking/cover.png" alt="product-thinking: from idea to build-ready plan"></a></td>
  </tr>
</table>

## The bar

- Each repo starts from a failure I counted: a wrong answer an agent shipped, or a cost I measured. The tables below name the number where one exists.
- Deterministic work runs as a script. The model handles judgment only.
- Hooks and gates ship with tests you can run on your machine before you trust them.
- I run [skill-eval](https://github.com/robertmnyborg/skill-eval) to decide what stays. A skill that scores worse loaded than unloaded gets cut.

## Install with the marketplace

| Plugin | What it does | Skills |
|---|---|---|
| [skill-eval](https://github.com/robertmnyborg/skill-eval) | Runs a skill with and without, judges both arms, reports the pass-rate delta. A public skill scored 77% loaded vs 97% without it. | skill-eval, retro |
| [analyst-rigor-skills](https://github.com/robertmnyborg/analyst-rigor-skills) | Stops an agent from fabricating causal claims, root causes, quotes, and personas | causal-claim, metric-diagnosis, trustworthy-insights, job-card |
| [everyday-agent-skills](https://github.com/robertmnyborg/everyday-agent-skills) | Writes steps someone else can follow, judges a tool before you adopt it, decodes a confusing message, reads Reddit and X read-only | procedure-writing-rules, tool-fit, explain-message, social-research |
| [ux-evidence](https://github.com/robertmnyborg/ux-evidence) | Makes the agent name the user, the pain, and the kill metric before it writes UI code | ux-evidence |
| [product-thinking](https://github.com/robertmnyborg/product-thinking) | Walks a non-engineer from an idea to a build-ready plan, one question at a time | product-thinking |
| [self-review-evaluator](https://github.com/robertmnyborg/self-review-evaluator) | Rates a self-review against your leveling framework and plans the gap to the next level | self-review-evaluator |
| [principal-reps](https://github.com/robertmnyborg/principal-reps) | Timed interview reps that train the Principal-level PM answer pattern | principal-reps |

Install one with `/plugin install <plugin>@claude-harness`.

## Install from the repo

These need scripts on your PATH or entries in `settings.json`, so each README walks you through it.

| Repo | What it does | The number behind it |
|---|---|---|
| [claude-guardrails](https://github.com/robertmnyborg/claude-guardrails) | Hooks that enforce rules a CLAUDE.md file can't | Chained `sleep` calls fell from 138 a week to 1 after a 10-line hook |
| [cmux-agent-kit](https://github.com/robertmnyborg/cmux-agent-kit) | Pair, spin off, and split Claude Code sessions in cmux | One 8-day session cost 48% of two weeks of spend |
| [plan-notes](https://github.com/robertmnyborg/plan-notes) | Inline `@@` review notes on a plan, answered in one pass, with a decision ledger | |
| [agent-overworld](https://github.com/robertmnyborg/agent-overworld) | Live map of every agent session, with status and last-reply recap | |
| [harness-doctrine](https://github.com/robertmnyborg/harness-doctrine) | Four questions that decide where a model belongs in a harness | A 70-line normalizer hit 99.89% recall in 2 s; a local 30B model hit 94.95% in 2.6 h |

## License

This catalog is MIT. Each linked repo carries its own license file.
