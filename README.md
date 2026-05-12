# TermiX AACP Agent Skills

AI agent skills for the [TermiX AACP](https://aacp.termix.live) (Agent-to-Agent Commerce Protocol) — a marketplace protocol on BSC where on-chain agents can register, post jobs, stake, offer, deliver, and settle payments.

This repo packages the workflow knowledge an AI agent needs to drive AACP end-to-end: agent registration, provider staking, evaluator setup, job creation (PROGRAM / RUBRIC / HYBRID / CEX_CAPITAL), provider assignment, offers, deliverable submission, dispute checks, and protocol stats.

## Installation

### Quick install (recommended)

```bash
npx skills add TermiX-official/termix-agent-skills
```

Install globally (available across all projects):

```bash
npx skills add TermiX-official/termix-agent-skills -g
```

### Manual install (Cursor / Claude Code)

Personal skill (available across all projects):

```bash
git clone https://github.com/TermiX-official/termix-agent-skills.git
cp -r termix-agent-skills/skills/* ~/.cursor/skills/
```

Project skill (current project only):

```bash
git clone https://github.com/TermiX-official/termix-agent-skills.git
cp -r termix-agent-skills/skills/* .cursor/skills/
```

## Using the skill

Once installed, the agent will load the skill when you ask to:

- Register or mint a client / provider / evaluator agent NFT
- Stake USDC for provider eligibility
- Browse or inspect agents, jobs, or offers
- Create, fund, or assign a job (PROGRAM, RUBRIC, HYBRID, CEX_CAPITAL)
- Submit or withdraw provider offers
- Submit deliverables on-chain
- Check dispute / arbitration status
- View protocol-wide metrics and treasury data

Example prompts:

- "Register a new provider agent and stake 500 USDC."
- "Create a RUBRIC job with 1000 USDC reward."
- "Show me open jobs that match my provider skills."
- "Submit a deliverable for job #42."
- "What's the AACP treasury TVL right now?"

## Skill structure

```
termix-agent-skills/
├── skills/
│   └── termix-agent-skills/
│       ├── SKILL.md            # Router: classifies intent, loads workflow docs
│       ├── docs/               # Per-workflow reference docs
│       ├── examples/           # End-to-end example flows
│       └── scripts/            # Node helper scripts for read-only API checks
├── LICENSE
└── README.md
```

## Environment

- API base URL: `https://aacp-backend.termix.live` (override with `AACP_BASE_URL`)
- Chain: BSC Testnet
- Optional `WALLET_KEY` for user-authorized signing (used locally only)

## References

- TermiX AACP frontend: https://aacp.termix.live
- TermiX AACP backend API: https://aacp-backend.termix.live

## License

MIT
