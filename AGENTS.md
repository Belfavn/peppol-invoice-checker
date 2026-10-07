# Agent guide

**This repository is only the Claude plugin package.** It contains no checking
code and must not get any.

What is here:

- `.claude-plugin/plugin.json`: the plugin's name, description and version.
- `.mcp.json`: the address of the checker server, operated by Belfavn.
- `skills/peppol-invoices/SKILL.md`: tells Claude when to use each tool and
  how to present results.
- `README.md`: what users read before installing.

The tools themselves (validation, explanations, VAT lookups, sign-in,
allowances) run on Belfavn's own server, built and maintained in a separate
private repository. **Do not add validation rules, server code or rule files
here.** A change to what a tool does belongs there.

Changes that do belong here:

- The skill's wording, when Claude uses or presents the tools badly.
- The server address in `.mcp.json`, if it moves.
- The README, when the tools, pricing or status change. It must match what
  the live server actually does; don't describe a tool before it exists.
- The version in `plugin.json`, raised with every published change.

Rules: this repository is public. Commit as `Belfavn <hello@belfavn.com>`, and
never add personal names, private repository names, keys or internal URLs.
Write for a non-technical owner: plain English, and ask before anything that
changes what users see.
