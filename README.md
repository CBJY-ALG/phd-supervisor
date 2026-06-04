# PhD Supervisor Skill

`phd-supervisor` is a Codex Skill for advisor-style supervision of doctoral research projects. It helps a PhD student move from a vague research direction toward a defensible thesis, dissertation, or publishable paper through staged research gates, critical feedback, and reusable research artifacts.

## What It Does

- Refines vague doctoral research directions into answerable research questions.
- Checks novelty, contribution, feasibility, literature positioning, and methodology fit.
- Provides stage gates for thesis, dissertation, proposal, experiment, paper, revision, defense, and publication workflows.
- Supports supervisor meetings, literature matrices, methodology blueprints, claim-evidence ledgers, revision matrices, and defense preparation.
- Flags common PhD research failure modes such as topic drift, weak novelty, method-claim mismatch, unverified citations, result shopping, and over-delegation to AI.

## Repository Structure

```text
.
+-- README.md
+-- LICENSE
+-- .gitignore
+-- phd-supervisor/
    +-- SKILL.md
    +-- agents/
    |   +-- openai.yaml
    +-- references/
        +-- failure-modes.md
        +-- stage-gates.md
        +-- templates.md
```

The `phd-supervisor/` directory is the actual Skill package. The root files are for GitHub distribution.

## Installation

Copy the `phd-supervisor` folder into your Codex skills directory:

```text
~/.codex/skills/phd-supervisor
```

On Windows, this is commonly:

```text
C:\Users\<YourUserName>\.codex\skills\phd-supervisor
```

Then restart Codex or open a new conversation so the Skill can be discovered.

## Usage

Invoke the Skill explicitly:

```text
Use $phd-supervisor to help me refine my PhD research topic.
```

Useful prompts:

```text
Use $phd-supervisor to turn my broad research direction into 3 feasible research questions.
```

```text
Use $phd-supervisor to run a supervisor meeting. My current stage is literature review, and I am stuck on novelty.
```

```text
Use $phd-supervisor to audit whether my methodology can support my main claim.
```

```text
Use $phd-supervisor to simulate committee questions for my dissertation defense.
```

## Included Skill Files

- `SKILL.md`: main Skill instructions, trigger description, operating stance, stage router, modes, and output defaults.
- `agents/openai.yaml`: Codex UI metadata.
- `references/stage-gates.md`: doctoral research stage gates and pass/fail criteria.
- `references/templates.md`: reusable templates for supervision briefs, RQ briefs, novelty maps, literature matrices, methodology blueprints, claim-evidence ledgers, review reports, and defense briefs.
- `references/failure-modes.md`: diagnostic checklist for common doctoral research failure modes.

## Validation

If you have the Codex `skill-creator` validation script available, validate the Skill folder:

```powershell
python C:\Users\<YourUserName>\.codex\skills\.system\skill-creator\scripts\quick_validate.py .\phd-supervisor
```

Expected result:

```text
Skill is valid!
```

## Design Principles

This Skill is designed to act like a rigorous supervisor, not a ghostwriter. It preserves student decision-making, separates evidence from inference, demands traceable claims, and avoids fabricating citations, results, or novelty.

## License

MIT License. See `LICENSE`.
