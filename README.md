# LeadGen Framework Skill

A reusable Codex skill for building channel-based lead generation workflows.

It helps turn messy prospecting across search engines, social platforms, communities, review sites, and partner ecosystems into a repeatable process:

1. define target profiles;
2. search and collect leads by channel;
3. preserve evidence for every lead;
4. score and prioritize;
5. run a pilot pool before touching production data;
6. merge validated leads into a production base;
7. use BD/sales feedback to improve the next search cycle.

The included CFD / Forex / Broker example is only an example industry adaptation. The same workflow can be reused for other B2B, affiliate, SaaS, creator, partner, or sales-development use cases.

## What this skill is good for

- Designing lead generation databases and schemas.
- Running small channel pilots before production imports.
- Standardizing lead categories, priority rules, and evidence fields.
- Cleaning and normalizing lead data.
- Building BD feedback loops.
- Avoiding low-quality bulk scraping that creates noisy sales lists.

## What this skill is not

This skill is not a standalone scraper and does not include API keys, private datasets, or platform-specific automation code.

It gives Codex a workflow and decision framework. The actual data collection method depends on what tools, APIs, browser login state, or spreadsheet/Base/CRM connectors are available in your environment.

## Install

Clone or copy this folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R leadgen-framework ~/.codex/skills/
```

Expected structure:

```text
~/.codex/skills/leadgen-framework/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── cfd-example.md
    └── publication-checklist.md
```

Then start a new Codex conversation and invoke:

```text
Use $leadgen-framework to design a lead generation pilot.
```

Or, for the included industry example:

```text
Use $leadgen-framework to design a CFD broker lead generation pilot.
```

## Recommended lead fields

The skill suggests a flexible schema:

- Lead ID
- Profile / Company Name
- Lead URL
- Channel
- Category
- Language / Market
- Audience Size
- Product / Service Fit
- Evidence Summary
- Contact Channels
- Priority
- Priority Reason
- Status
- Assigned To
- Sales Feedback
- Next Step
- Next Follow-up Date
- Data Correction
- Verification Notes

Use channel prefixes for combined databases, for example:

- `X-001`
- `FB-001`
- `TT-001`
- `YT-001`
- `TG-001`
- `WEB-001`

## Core workflow

1. Clarify target profiles and exclusions.
2. Decide whether the task is a pilot or a production update.
3. Build a channel-specific search plan.
4. Collect leads with URLs and evidence notes.
5. Filter out excluded or low-fit records.
6. Score and prioritize.
7. Create or update the sheet/base.
8. Verify links, counts, required fields, and label consistency.
9. Summarize what changed and what sales/BD should do next.
10. Feed BD feedback back into the next search rules.

## Privacy and safety

Before publishing or sharing any derived version, check:

- No API keys, secrets, cookies, or login tokens.
- No private CRM/Base URLs, app tokens, table IDs, or chat IDs.
- No real employee performance data.
- No private customer or prospect records.
- No proprietary internal strategy.
- No local personal paths such as `/Users/your-name/...`.

See [`references/publication-checklist.md`](references/publication-checklist.md) before making a repository public.

## Example: CFD / Forex / Broker lead generation

The file [`references/cfd-example.md`](references/cfd-example.md) shows how to adapt the generic framework to a CFD broker lead generation use case, including:

- signal providers;
- EA / robot sellers;
- copy trading communities;
- hidden trading KOLs;
- broker review sites;
- trading tools;
- education websites;
- regulator / blacklist research.

It is intentionally generic and contains no private company data.

## License

Choose a license that fits your intended use. If unsure, MIT is a common default for public templates.

