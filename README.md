# PM Skills for Claude

A set of product management [Agent Skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) for Claude Code and Claude.ai. Each skill teaches Claude a PM workflow, including the structure to follow, the frameworks to use, and the quality checks to run before handing back the output.

| Skill | What it does |
|-------|--------------|
| [`prd-writer`](skills/prd-writer/SKILL.md) | Turns an idea or rough notes into a full PRD or one-pager with measurable goals, requirements, and guardrail metrics |
| [`user-stories`](skills/user-stories/SKILL.md) | Breaks features into INVEST user stories with Given/When/Then acceptance criteria, ready for Jira, Linear, or GitHub |
| [`prioritization`](skills/prioritization/SKILL.md) | Ranks a backlog with RICE, ICE, MoSCoW, Kano, or value vs. effort, including a sensitivity analysis and a "not doing" list |
| [`user-research-synthesis`](skills/user-research-synthesis/SKILL.md) | Synthesizes interviews, surveys, and feedback into evidence-backed insights and JTBD. It can also draft interview guides |
| [`competitive-analysis`](skills/competitive-analysis/SKILL.md) | Builds feature matrices, positioning, SWOT, and sales battlecards, with a cited source for each claim |
| [`metrics-okrs`](skills/metrics-okrs/SKILL.md) | Defines North Star metrics, metric trees, and OKRs. It also critiques existing goals and diagnoses metric changes |
| [`experiment-design`](skills/experiment-design/SKILL.md) | Designs A/B tests (hypothesis, sample size, duration, decision rules) and interprets test results |
| [`launch-plan`](skills/launch-plan/SKILL.md) | Produces a tiered GTM/rollout plan, a cross-functional checklist, messaging, and release notes |

## Install

### Claude Code (as a plugin)

```
/plugin marketplace add estherchols/pm-skills
/plugin install pm-skills@pm-skills
```

### Claude Code (manual)

Copy the skills you want into your personal or project skills folder:

```bash
git clone https://github.com/estherchols/pm-skills.git
cp -r pm-skills/skills/* ~/.claude/skills/
```

### Claude.ai

Zip a skill folder (for example `skills/prd-writer/`) and upload it under **Settings → Capabilities → Skills**.

## Usage

Skills trigger automatically when the request matches the skill. For example:

- "Write a PRD for adding SSO to our admin console"
- "Break this PRD into user stories for Linear"
- "Here are 12 backlog items. Rank them with RICE"
- "Synthesize these 8 interview transcripts"
- "How do we compare to Notion and Coda on collaboration features?"
- "Write Q1 OKRs for the onboarding team"
- "Design an A/B test for the new pricing page. Baseline conversion is 3.2%"
- "Make a launch plan for our new mobile app"

## Structure

```
pm-skills/
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
└── skills/
    └── <skill-name>/SKILL.md
```

## Contributing

Issues and PRs are welcome. Each skill is one `SKILL.md` file with `name` and `description` frontmatter. The description controls when Claude uses the skill, so make it specific about trigger phrases.

## License

MIT
