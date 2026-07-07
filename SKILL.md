---
name: leadgen-framework
description: A reusable framework for channel-based lead generation, first-pass qualification, pilot databases, production lead bases, BD assignment, and feedback loops. Use when designing or operating lead generation workflows across channels such as Google/Search, X, LinkedIn, Facebook, Instagram, TikTok, YouTube, Telegram, Discord, forums, review sites, regulator lists, or affiliate/partner ecosystems; includes CFD/Forex/Broker lead generation as an example without private business data.
---

# LeadGen Framework

## Purpose

Use this skill to turn messy multi-channel prospecting into a repeatable lead generation workflow:

1. define target profiles;
2. search channels;
3. collect evidence;
4. score and prioritize;
5. run a pilot pool;
6. merge validated data into a production base;
7. collect BD/sales feedback to improve the next run.

This is a workflow skill, not a scraper by itself. Pick tools based on the user's available connectors, APIs, browser login state, spreadsheets, or CRM/Base system.

## Core operating rules

- Treat production databases as production systems. Do not modify a production lead base unless the user explicitly asks for that specific update.
- For new channels, untested keywords, or uncertain quality, start with a pilot sheet or temporary base. Merge into production only after user review.
- Do not store or reveal API keys, secrets, cookies, login tokens, private CRM data, or sensitive internal strategy in skill files or public artifacts.
- Every lead should preserve evidence, not just a name: URL, channel, category, fit reason, product/service evidence, audience/size, language/market, activity, contact path, and verification notes.
- Prefer small, verifiable batches over huge low-quality lists.
- Keep final labels consistent. Avoid leaving ambiguous placeholders like `TBD` or `To verify` in production fields unless the user explicitly wants a staging state.

## Default lead table schema

Use or adapt these columns:

- `Lead ID`
- `Profile / Company Name`
- `Lead URL`
- `Channel`
- `Category`
- `Language / Market`
- `Audience Size`
- `Product / Service Fit`
- `Evidence Summary`
- `Contact Channels`
- `Priority`
- `Priority Reason`
- `Status`
- `Assigned To`
- `Sales Feedback`
- `Next Step`
- `Next Follow-up Date`
- `Data Correction`
- `Verification Notes`

Use channel prefixes for IDs when combining sources, for example `X-001`, `FB-001`, `TT-001`, `YT-001`, `TG-001`, `WEB-001`.

## Workflow

1. Clarify target profiles and exclusions.
2. Decide whether this is a pilot or production update.
3. Build a channel-specific search plan.
4. Collect leads with evidence URLs and notes.
5. Filter out low-fit or excluded records.
6. Score and prioritize.
7. Create or update the sheet/base.
8. Verify links, counts, required fields, and label consistency.
9. Summarize what changed and what BD should do next.
10. Capture user/BD feedback and update search rules.

## Channel guidance

- Search/web: useful for websites, review pages, tools, directories, education platforms, affiliate pages, regulator lists.
- X/Twitter: useful for frequent posters, signal providers, analysts, communities, hidden KOLs, and affiliate traces.
- Facebook: useful for groups, local communities, education pages, and public social proof.
- Instagram/TikTok: useful for creator-led funnels, lifestyle/KOL signals, short-form proof, bio links, and private communities.
- YouTube: useful for education channels, review content, tutorials, livestream analysts, and affiliate links.
- Telegram/Discord: useful for signal groups, paid communities, bot/automation sellers, and copy-trading funnels.
- LinkedIn: useful for BD people, affiliates, broker staff, ex-employees, B2B partners; verify profiles carefully.
- Regulator/blacklist sources: useful for reverse engineering ecosystems, but aggressively filter off-topic or unreachable domains.

## Priority model

Adapt to the user's business, but default to:

- `P1`: strong product fit + strong evidence + reachable contact path + active audience/community.
- `P2`: good product fit but smaller audience, weaker evidence, or needs manual qualification.
- `P3`: exploratory leads, education/tool/review sources, or useful but less direct prospects.

Keep priority reasons concise and auditable.

## Feedback loop

Ask the user or BD team to mark:

- useful / not useful;
- replied / no reply;
- wrong category;
- wrong language or market;
- stale / inactive;
- bad URL;
- strong similar pattern to search more;
- exclusion pattern to avoid next time.

Turn this feedback into updated search keywords, exclusion rules, category definitions, and scoring rules.

## References

- For a concrete CFD/Forex/Broker example, read `references/cfd-example.md`.
- Before publishing this skill or a derived template publicly, read `references/publication-checklist.md`.

