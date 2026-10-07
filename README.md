# Pokémon GO Toolkit

[Download plugin ZIP](https://github.com/CthulhuDancing/pogo-tools/releases/latest/download/pokemon-go-toolkit.zip)

A plugin that helps your AI assistant answer Pokémon GO questions with sourced data, deterministic calculations, Showcase analysis, and current event planning.

- Look up Pokémon, forms, evolutions, moves, and PvP or raid information.
- Calculate CP, stats, PvP IV ranks, and the highest level under a league's CP cap.
- Compare Stardust, Candy, and Candy XL costs.
- Compare Pokémon sizes, estimate PokéStop Showcase scores, and decide which specimens to keep.
- Build concise weekly event plans with actionable preparation and high-priority month-ahead warnings.

Includes four skills: `pokemon-go-data`, `pokemon-go-calculations`, `pokemon-go-showcases`, and `pokemon-go-events`.

Try asking:

- “How does my 0/15/15 Azumarill rank for Great League?”
- “How much Stardust and Candy do I need to go from level 20 to 45?”
- “Which moves should I use for raids, and why?”
- “Give me the Pokémon GO events I should prepare for this week.”

The plugin lives in [`plugins/pokemon-go-toolkit`](plugins/pokemon-go-toolkit) and includes manifests for Codex, Claude Code, and clients supporting the Agent Plugins format. Marketplace entries are in [`.agents/plugins/marketplace.json`](.agents/plugins/marketplace.json) for Codex and [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json) for Claude Code.

Your assistant needs Python to run the calculators and web access to look up current data and events. Calculations depend on the supplied stats, IVs, and levels; Showcase results are estimates.
