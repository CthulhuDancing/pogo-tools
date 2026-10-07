---
name: pokemon-go-events
description: Produce concise, planning-focused Pokemon GO event reports from current official and reliable sources. Use for weekly event briefings, upcoming-event planning, monthly early warnings, bonus calendars, raid/Max/event schedules, legacy-move windows, or questions about what Pokemon/resources to save, trade, transfer, evolve, Mega Evolve, raid, hatch, or stockpile before announced events. Filter routine recurring features unless a specific occurrence has an exceptional bonus.
---

# Pokemon GO events

Act as the planning and reporting layer for current Pokemon GO events. Research the live schedule, identify what materially changes player behavior, and present a compact action-oriented brief.

Use `pokemon-go-data` when detailed species, PvP, PvE, move, or mechanics facts are needed. Do not use calculators unless a numeric calculation materially affects the event-planning decision.

## Workflow

1. Resolve the reporting window and timezone from the request. For a weekly brief, use the next 7 days plus a high-level remainder-of-month outlook.
2. Retrieve current event information from official Pokemon GO / Niantic sources first. Use reliable secondary sources for aggregation, cross-checking, or details that are awkward to extract from official posts.
3. Separate confirmed information from leaked, inferred, region-limited, or otherwise uncertain information.
4. Identify actions the user should take before or during the reporting window.
5. Exclude routine recurring features unless that specific occurrence has an unusual or materially valuable bonus.
6. Produce the report in the compact format below.

## What to include

Include events or bonuses that materially affect planning, such as:

- raid rotations and Raid Days;
- Community Days, Research Days, Hatch Days, and similar limited events;
- Max Battle events;
- meaningful shiny-boosted events;
- PvP-relevant spawn events;
- legacy or special-move evolution windows;
- increased transfer Candy or Candy XL;
- increased trade Candy or Candy XL;
- guaranteed Candy XL from trades;
- reduced trade Stardust or extra Special Trades;
- increased catch Candy or Candy XL;
- meaningful hatch bonuses;
- other limited bonuses that should change what the player saves, spends, transfers, trades, evolves, walks, raids, hatches, or Mega Evolves.

Do not include minor events merely because they appear on the calendar.

## Recurring-event filter

Omit known routine weekly occurrences by default, including ordinary recurring showcase or friendship features and similar predictable weekly mechanics.

Include a recurring occurrence only when that specific date has something materially different or valuable, such as guaranteed extra Candy XL, an unusual multiplier, a special encounter pool, or another bonus that changes player behavior.

## Planning rules

Translate event mechanics into concrete preparation.

For transfer bonuses:
- state whether the bonus applies to all transfers or only a subset;
- identify what is worth holding beforehand;
- prioritize rare families, legendaries, traded Pokemon, and important Candy XL targets when appropriate.

For trade bonuses:
- state what is worth saving for trades;
- mention distance-trade or guaranteed-XL mechanics when they matter.

For PvP-relevant Pokemon:
- identify useful league(s);
- give the IV target compactly, e.g. `GL - low Atk / high Def+HP`;
- use `pokemon-go-data` when current PvP relevance needs verification.

For raid/PvE targets:
- distinguish genuine investments from dex/shiny hunts;
- use compact labels such as `Worth passes`, `Selective`, or `Mostly dex/shiny`;
- use `pokemon-go-data` when current PvE relevance or movesets need verification.

For legacy moves:
- explicitly say when evolution should be delayed until the move window.

For Candy bonuses:
- mention a relevant Mega type when pre-Mega-Evolving would materially improve returns.

## Weekly report format

Default to this structure for weekly planning requests.

### Prepare now

Maximum 5 rows. Include only actions worth taking before or during the coming week.

| Priority | Action | Reason / deadline |
|---|---|---|

If nothing requires preparation, write `No immediate preparation needed.`

### Coming week

Cover materially useful events occurring in the next 7 days.

| Date / time | Event | Pokemon / bonus | What to do |
|---|---|---|---|

Keep cells terse. Prefer actionable fragments over explanatory prose.

Examples:
- `GL - low Atk / high Def+HP`
- `PvE - high IV / 15 Atk; worth passes`
- `Mostly dex/shiny`
- `Hold legendaries + rare XL targets for transfer`
- `Save distance trades for guaranteed XL`
- `Mega Evolve Water for catch Candy`
- `Delay evolution for legacy move`

### Rest of month - early warnings only

Include only events important enough to change what the user should save or spend now.

| Date | Important later event | Prepare |
|---|---|---|

Maximum 5 rows. Keep this section extremely terse.

Good candidates include:
- 2x or better transfer Candy;
- increased transfer Candy XL;
- 2x or better catch Candy;
- increased catch Candy XL;
- unusually valuable trade or guaranteed-XL bonuses;
- major reduced trade costs;
- valuable legacy-move windows;
- major raid or Max events that justify saving passes/resources;
- Hatch Days or hatch bonuses worth saving incubators or eggs for;
- events where stockpiling Pokemon beforehand materially increases value.

Do not list ordinary future events just because they are announced.

If nothing qualifies, write `No major preparation events currently announced for later this month.`

## Source and uncertainty handling

Prefer official Pokemon GO / Niantic announcements for event dates, bonuses, featured Pokemon, and move windows.

Use reliable secondary sources for schedule aggregation or cross-checking. When source reliability matters, follow the source-selection and conflict-handling principles in `pokemon-go-data/references/source-routing.md`.

Label unconfirmed, leaked, inferred, or region-limited information clearly. Do not mix uncertain information into confirmed tables without marking it.

## Style

- Be concise and predominantly tabular.
- Lead with actionable preparation.
- Do not explain basic Pokemon GO mechanics unless needed to avoid a mistake.
- Do not pad the report with commentary.
- Do not repeat routine weekly mechanics that do not change the player's plan.
- The weekly section should be complete enough to plan the next 7 days.
- The rest-of-month section should answer only: `Is there anything later this month that should change what I save or spend today?`
