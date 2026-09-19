# Upstream source and attribution

- Upstream repository: https://github.com/tenfoldmarc/spy-skill
- Upstream author: [@tenfoldmarc](https://www.instagram.com/tenfoldmarc)
- Initial upstream commit: `6c1dd4dae7e6ff6238c35727e8ef8c6967f8373e`
- Commit date: 2026-04-05
- Distribution relationship: GitHub fork under `JSNGe/spy-skill`

## License status

The upstream repository contained no `LICENSE` file at the pinned revision. This fork therefore does
not add or claim an open-source license. It preserves GitHub's fork relationship, the original
README, commit history, and author attribution.

## Codex compatibility changes

1. Added Codex installation and `$spy` invocation instructions.
2. Resolved `config.json` relative to the installed skill instead of hard-coding Claude's path.
3. Replaced the Claude-specific Apify MCP tool assumption with host capability discovery.
4. Added instructions not to store Apify tokens in the repository, config, reports, or chat.
5. Replaced fixed `/tmp/spy_reel.*` paths with a unique per-run temporary directory.
6. Replaced `which` with the more portable `command -v` for dependency discovery.

The original analysis method remains intact: scrape up to 50 recent posts per specified account,
calculate 5× median-view outliers from the last 30 days, extract spoken/on-screen/caption hooks, and
rank reusable templates.
