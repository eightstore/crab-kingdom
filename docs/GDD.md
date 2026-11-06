# Crab Kingdom — Core GDD v2.0

## Vision
Premium cute cartoon Roblox colony simulator, borrowing the gather/sell/upgrade **genre loop**, but with unique crab characters, living seaside colony, and a meaningful tide mechanic. Player controls their avatar, not the crabs. Crabs are workers assigned to resources and animated in a polished stylized manner. Avoid stiff movement and generic/slop UI.

## Gameplay loop
Recruit/preview crab at Royal Conch → add to inventory → place in a colony slot → assign shell/resource zone → crab walks/gathers/carries/deposits automatically → warehouse sells manually (+15% design bonus) or via free Auto Sell → earn Sand Coins → buy crabs/slots/upgrades → discover new zones → complete Crab Index.

## Player onboarding
Start with two working crabs, three active slots, 100 warehouse capacity, zero Sand Coins. Tutorial: assign → gather → sell → recruit → upgrade → discover tide pools. Target first recruit within minutes. Everything must be saveable/restart-safe.

## World and Zones
Ten planned biomes, with 20 character concepts from each: Starter Beach, Tidal Flats, Coral Garden, Mangrove Maze, Shipwreck Bay, Frostshell Fjord, Ember Coast, Moonlight Reef, Royal Trench, Starfall Atoll. **MVP only Starter Beach and Tidal Flats**. Six private plots per server as initial scale test; don't assume this is performance guaranteed. Shared map, non-destructive social visiting.

## 200 crabs
Exactly **CK001–CK200**, 20 per biome. Distinct name, rarity, readable silhouette, three or more intentional visual differences, motion personality, trait and game balance. Rarity catalogue distribution: Common 40, Uncommon 50, Rare 50, Epic 30, Legendary 20, Mythic 10. **This catalogue split is NOT a roll probability table.** Families/traits: Hauler, Runner, Gatherer, Near, Far, LowTide, HighTide, Team, Explorer, Stable, Specialist. Share modular rigs as needed, but 200 bespoke production-quality 3D models are an additional asset-production task. Keep the initial code capable of using prototype crab assets with premium hand-authored replacements.

## Recruit / Royal Conch
Coin-only candidate roll with disclosed odds, visible price/statistics, cooldown, optional saved candidate, inventory capacity checks. **No Robux-purchased random loot** in MVP. All roll decisions and sales handled server-side. Candidates can also come from quests to reduce RNG frustration.

## Tide
Four minutes low tide, four minutes high tide, repeat server-wide. Low tide makes certain beach deposits productive, high tide improves coral/tidepool deposits. Starter shells must remain accessible at all times. Do not interrupt a crab carrying cargo mid-tide; update assignment after deposit. Tide visual effects must be light on mobile.

## Economy
Sand Coins, warehouse and resources are server authoritative. Starter Beach Crab: capacity 8, example 20-second round-trip, Small Shell worth 1 coin. Starter 2 crabs → theoretical 48 coins/minute before pauses; manual selling +15%; free Auto Sell. Upgrade examples: slot 4 = 180, slot 5 = 420, slot 6 = 1000, slot 7 = 2600, slot 8 = 6500; warehouse 100→250 = 200. Balance is provisional; measure in Studio testing. Source capacity and reservations cannot overdraw. An economic action must be idempotent/atomic as relevant.

## Interface
Oceanic Playful Premium design system: warm sands, coral pink, sea teal, deep readable text; cohesive icons; clear feedback on idle/gathering/cargo/full warehouse/transaction error; responsive mobile & PC UI. Inventory and index need search, biome/rarity filters, sorting, favorites, locks, loadouts. Don't overload with glitter/glow or unpolished gradients.

## Animation and sound
Crabs accelerate/decelerate, turn smoothly, step sideways with coordinated legs; animate pickup, carrying weight, deposit and idle expressions. Visual simulation client, gameplay timers and validation server. Distinct silhouettes and assets; don't just recolor generic model. Provide reduced-effects option.

## Multiplayer/data/security
Server owns assignments, slots, sources, purchases, tide, inventory and coin changes. Rate-limit and validate RemoteEvents. Save versioned profiles and fail safely without overwriting unavailable data. Guard against duplicate receipts if monetization later added. Multiplayer test with 6 players × up to 8 active crabs as a **benchmark target**, not guarantee.

## Monetization
Cosmetics, optional decoration/themes, showcase expansions, clear value and price. Auto Sell free. Do not lock core zones or meaningful species behind Robux. Any future paid random items must comply with Roblox policy before design or implementation.

## Delivery roadmap
Phase 1: working crab/shell/nest loop (Rojo/Luau).
Phase 2: warehouse/economy/recruitment/slots.
Phase 3: biome, tide, resource assignment.
Phase 4: persistence, quests, multiplayer.
Phase 5: coherent visual assets, responsive UI, audio, animation polish.
Phase 6: anti-exploit, performance, Studio QA, launch readiness.

## QA exit criteria
No resource duplication or negative coins; workers recover from source depletion/full warehouse/tide changes; saved crabs and upgrades survive rejoin; UI usable on mobile; movement smooth with no obvious snapping; 200 catalog entries searchable; game remains playable without Robux.

**Important:** This GDD is a specification, not evidence of working code or validated Roblox gameplay.
