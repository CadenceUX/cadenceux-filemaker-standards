# CadenceUX FileMaker Standards

The conventions CadenceUX uses in FileMaker solutions, packaged as a standards pack for Claris's
FileMaker Agentic Development Kit (ADK). A project that follows it gets these rules on top of
ADK's built-in baseline, so your coding agent names and builds things the CadenceUX way and
cites the rules when it reviews work.

| File | What it sets |
|---|---|
| `standards/naming.md` | `Domain: Action` script names, dot-notation fields (`Address.City`) and table occurrences (`Invoice.Contact`), `_g` for globals |
| `standards/patterns.md` | The CadenceUX script header, script layout, error handling with `AnErrorOccurred`, JSON script results, Halt Script, the Settings table |
| `standards/advisory.md` | What a review should point out: `$$` variables passing state, hidden setters, dead code, missing comments |

Everything the pack doesn't mention (keys, housekeeping fields, layouts, variables, value
lists, deprecation) follows ADK's baseline.

## Install and follow it

In Claude Code, once per computer:

    claude plugin marketplace add https://github.com/CadenceUX/cadenceux-skills.git
    claude plugin install cadenceux-filemaker-standards@cadenceux

Then, in each ADK project that should follow it, ask your agent "Make this project follow the
cadenceux standards pack", or run:

    adk standards use cadenceux
    adk standards

The second command lists where each file's rules come from: Baseline, then Pack.

**Other agents (Cursor, Codex, Gemini CLI):** standards packs install through Claude Code. Copy
the three files in `standards/` into the project's `.adk/standards/` folder instead; ADK reads
them there with any agent, and they travel with the project's repository.

**Pack name:** `cadenceux`. It's recorded in every project's `adk.json`, so it won't change. The
plugin name, `cadenceux-filemaker-standards`, is what you install.

## Related

[fmp-dev-design-patterns](https://github.com/CadenceUX/fmp-dev-design-patterns) is the skill
that explains these conventions, writes scripts with them, audits a solution to derive a
client's own pack, and applies them when ADK isn't installed.

## Licence

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

Built and maintained by [Darrin Southern](https://www.linkedin.com/in/darrin-southern/) from [CadenceUX](https://cadenceux.com.au).
