# Changelog

## [1.0.0] — 2026-11-19

First release: the conventions from `fmp-dev-design-patterns` 2.1 as an ADK standards pack
(pack name `cadenceux`), written to Claris's "rules an agent can carry out" checklist, so each
rule gives one result and every choice has a default.

- `naming.md`: `Domain: Action` script names with the pipe variant and the `[Mode]` and
  `[OLD]` suffixes; dot-notation field namespaces; `_g` for globals; dot-notation table
  occurrence context paths; import and staging prefixes.
- `patterns.md`: replaces the Baseline's "Script commenting headers" and "Script results";
  adds "Script layout", "Error handling", "Halt Script" and "Configuration globals".
- `advisory.md`: `$$` state passing, hidden setters, comments, dead code, divider scripts.
- Checked: every formula the pack prescribes evaluated on the FileMaker 26.1.1 engine, and
  `adk standards` resolves the pack over the Baseline in a scratch ADK project.
