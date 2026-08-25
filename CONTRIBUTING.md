# Updating this README

This README is the single source of truth for the audit history. The portfolio
website (farismln/portfolio-web) parses its tables automatically
(`scripts/sync-portfolio.mjs`) — keep to these conventions so the parser keeps
working:

- **Tables only.** Every entry lives in a markdown table with the columns
  `| Protocol | Description | Findings | Rank | Report |` (private engagements
  use `| Date | Team | Protocol | Category | Report |`).
- **Protocol cell** may be `[name](url)` or plain text.
- **Findings** are space-separated severity counts: `4C 6H 5M`.
- **Rank** is a medal emoji (🥇 🥈 🥉), `Top 10`, a plain number, `N/M`, or `Nth`.
- **Report** is `[📄](url)`, `Private (Platform)`, `*pending*`, or `-`.
- Yearly contest tables live inside `<details>` blocks with
  `<summary><strong>YYYY Public Contests</strong></summary>`, newest year first.
- New private engagements go at the top of their table, newest first.

If the format must change, update the parser in portfolio-web in the same
change — it fails loudly (and the site stops auto-updating) when the structure
does not match.
