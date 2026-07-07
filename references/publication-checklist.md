# Public publication checklist

Before publishing this skill or a derivative repository to GitHub, remove or generalize:

- Real client names unless intentionally public.
- Company names, internal brand strategy, CRM/base names, app tokens, table IDs, chat IDs.
- API keys, secrets, cookies, login instructions tied to a private account.
- BD or employee names, performance numbers, assignment logic tied to real people.
- Private file paths such as `/Users/<name>/...`.
- Internal language like “take over competitor clients” if it reveals sensitive strategy.
- Any downloaded leads containing personal data or non-public contact details.

Safe to publish:

- General workflow.
- Generic schema.
- Generic category definitions.
- Generic scoring/prioritization rules.
- Sanitized examples.
- Industry-neutral advice.
- A CFD example that uses no private companies, no private records, and no proprietary source lists.

Recommended public repo structure:

```text
leadgen-framework/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── cfd-example.md
    └── publication-checklist.md
```

Recommended README, if creating a GitHub repo outside Codex skill packaging:

- What this skill does.
- How to install under `~/.codex/skills/leadgen-framework`.
- Example prompt: `Use $leadgen-framework to design a CFD broker lead generation pilot.`
- Privacy warning: do not commit secrets or real CRM data.

