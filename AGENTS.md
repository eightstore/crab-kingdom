# Crab Kingdom — Instructions for Codex

You are working in the Roblox game **Crab Kingdom**, a cute, premium-styled tropical crab colony simulator inspired by the *progression loop* of Build An Ant Empire, not its intellectual property.

## Scope and workflow
- This repository is a Codex-ready project specification scaffold. The full previous alpha source bundle has **not** been imported yet. Never claim you reviewed files that are not in the repo.
- Build a playable **Rojo + Luau** project iteratively, with real functional Roblox scripts—not pseudocode and not an external web app.
- Read `docs/GDD.md` before designing or changing game mechanics.
- Prefer a runnable, testable vertical slice to a broad shallow scaffold. Write clear installation and play-test instructions for Roblox Studio.
- Do not claim to have tested behavior in Roblox Studio unless an actual Studio run occurred; provide steps for human in-Studio tests.
- Keep code modular, strongly validate all RemoteEvents and client inputs on the server, rate-limit transactions, and keep economy/data ownership server-authoritative.
- Use versioned DataStore profiles with proper error handling and prevention of profile loss; no trusted client economic values.
- Use a configuration-driven crab catalogue with **exactly 200 unique IDs CK001–CK200**, each with manually authored distinct names, biome, rarity, trait, stats and visual design keys. Do not create 200 meaningless color swaps or placeholder names.
- Target a coherent premium cute cartoon aesthetic. Characters must not look like stiff sliding blocks, and UI must not look like generic unstyled programmer boxes. Make responsive accessible mobile/desktop interfaces and clear UX state feedback.
- Share skeleton animation rigs/locomotion where appropriate, but reserve distinct silhouettes, appearances and signature flourishes for high-rarity crabs.
- Keep game design monetization ethical. Auto Sell is free, cosmetic purchases optional. Don't implement paid random loot or unverified MarketplaceService products.
- A full 200 bespoke 3D asset collection is a **separate art-production requirement**; code and procedural prototype meshes do not equal finished premium art.

## Completion criteria for the first playable build
1. Two starter crabs gather shell resources, move smoothly, carry visible cargo, deposit, and repeat without getting stuck.
2. Server calculates resources, warehouse stock, sales, coin balance, recruitment, slots, upgrades, and quest rewards.
3. Starter Beach and Tidal Flats exist; tide rotation changes which resource types are productive without making new players unable to earn.
4. Working Royal Conch with visible candidates, clear rarity information, and coin-only recruitment.
5. Responsive inventory/Crab Index searchable and sortable across 200 configuration entries.
6. Player progress persists safely across sessions; multiplayer plots remain private and visits are non-destructive.
7. Rojo project structure, start instructions, static checks, and a Studio manual QA checklist exist.

## Output discipline
For each meaningful coding task, summarize files changed, how to run it, which tests were actually executed, what remains untested in Studio, and known limitations.
