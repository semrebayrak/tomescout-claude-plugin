# Security policy

## Reporting a vulnerability

Please report security issues privately through GitHub's
[private vulnerability reporting](https://github.com/semrebayrak/tomescout-claude-plugin/security/advisories/new)
for this repository. Do not open a public issue for security problems.

Include what you found, how to reproduce it, and the impact you expect. We aim to
acknowledge reports within 3 business days and to ship a fix or mitigation for
confirmed issues as quickly as their severity requires.

## Scope

- This plugin (skills and MCP configuration).
- The hosted TomeScout MCP server at `https://tomescout.vercel.app/mcp`.

The plugin contains no credentials and no executable code; it connects to the
hosted server over HTTPS.
