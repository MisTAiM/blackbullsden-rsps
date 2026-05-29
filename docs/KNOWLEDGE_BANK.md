# AUGUST RSPS — COMPLETE KNOWLEDGE BANK
# Built for Black Bulls Den custom server development
# Source: wiki.august.games + LostCityRS research

---

## ARCHITECTURE OVERVIEW

### August RSPS (what we're studying)
- Live production OSRS-style private server
- Custom content on top of OSRS base
- Uses RuneLite client (with custom plugins)
- Java backend, MySQL (we replaced with SQLite)
- Web panel for hiscores/admin
- ~1,265 wiki pages, active community

### LostCity (what we're building on)
- TypeScript/Node.js engine (Engine-TS repo)
- Content defined in RuneScript language (Content repo)
- TypeScript client port (Client-TS) plays in BROWSER
- Java client (Client-Java) for original applet feel
- Revisions: 225 (May 2004), 244, 245.2, 254 (Sept 2004)
- Start script downloads Engine + Content + Client automatically
- Play at: http://localhost/rs2.cgi
- Dependencies: Git, Node.js 22+, Java 17+, Bun

---

## AUGUST FEATURES TO REPLICATE

### 1. GAME MODES
August has 4 modes (all with 20x XP default except Masochist):
- **PvMer** — 20x XP, +20% PvM talent points, max prestige 7
- **Skiller** — 20x XP, +20% Skilling talent points, max prestige 7
- **Masochist** — 5x XP, +10% all talent points, max prestige 10 (harder mode)
- **Slayer Locked** — 10x XP, can only kill NPCs on slayer task, +20% combat talents, max prestige 9
  - Extra: 2x superior spawns, 5% DR per slayer prestige (max 45%), extra vote rewards

### 2. PRESTIGE SYSTEM ⭐
Core progression loop — MOST IMPORTANT FEATURE
- Hit level 99 → prestige → reset to 1, gain talent points
- Each prestige requires 2 more levels (99→101→103→etc)
- Max prestige varies by game mode (7-10)
- Prestige rewards: bonus talent points, stat buffs
- Prestige XP table:
  - P1: 99 (13M XP)
  - P2: 101 (15.9M XP)
  - P3: 103 (19.4M XP)
  - P4: 105 (23.6M XP)
  - P5: 107 (28.8M XP)
  - P6: 109 (35M XP)
  - P7: 111 (42.8M XP)
  - P8*: 113 | P9*: 115 | P10*: 117 (mode-restricted)

### 3. TALENT SYSTEM ⭐
Drawn from OSRS Leagues relics concept — core power progression
- 3 trees: PvM, Skilling, Utility
- Earn talent points by: leveling skills (every 40 levels), prestiging, consuming talent point orbs
- Game mode bonuses: PvMer/Slayer Locked = +20% PvM points; Skiller = +20% Skilling
- Masochist = +10% all trees
- PvM Tree: 7 tiers (Tier 2=5pts, 3=25pts, 4=55pts, 5=95pts, 6=145pts, 7=215pts)
- Skilling Tree: 5 tiers
- Utility Tree: separate

### 4. HOME AREA (Prifddinas)
Everything centered at one hub:
- Grand Exchange (player economy)
- Portal Nexus (teleport hub — Slayer/Bosses/Skilling presets)
- Spellbook altar (switch Ancient/Standard)
- Altar (prayer training + restore)
- Rejuvenation Pool (heal + prayer + cure venom)
- NPC Shops (runes, starter gear, tools)
- Slayer Masters (all 4 available at home)
- Vote Obelisk
- Shooting Star landing zone
- World Boss Arena
- AFK Zone (north of barrier)
- Dragonstone Donator Zone

### 5. BOSSES (55 total)
Standard OSRS bosses + custom:
- **Raids**: Tombs of Amascut, Theatre of Blood, Olympian Raid (custom)
- **Custom bosses**: Apollo, Azrael, Poseidon, Hephaestus, Ignis, Danger Snek, Derwen, Yama
- **Echo Bosses** (harder variants): Cerberus Echo, DKs Echo, Thermy Echo
- **World Bosses**: Sol Heredit World Boss, Vote Goblin (spawns from voting)
- Standard OSRS: Zulrah, Vorkath, Cerberus, Corp, KBD, GWD (4), Kraken, Hydra, etc.

### 6. ITEM SACRIFICE SYSTEM
Mid-end game sink for items:
- Sacrifice items at AFK zone bench for sacrifice points
- Buy perks across 10 categories: Bossing, Raiding, Production, Gathering, Melee, Magic, Ranged, Survival, Slayer, Pets
- Promotional bonus items rotate
- Targets: Pandora essences, Ethereal weapons, Void, God Wars gear, Spirit shields, etc.

### 7. SHOPS (26 total)
- Boss Token Store
- PVM Token Store
- Slayer Point Store
- Skilling Token Store
- Vote Store / Vote Streak Store
- Prestige Store
- Donator Store + Cosmetic Store
- Dragonstone Donator Zone shop
- AFK Store (Seashell Seamus)
- Stardust Store
- Trivia Store
- Tzhaar Store
- League Point Store
- Ironman Store
- General Store
- Greed Store
- Plus: Farming, Herblore, Magic, Melee, Ranged tool/supply shops

### 8. VOTING SYSTEM
- 3 vote sites: RuneLocus, Rune-Server, RuneList
- Vote every 12 hours per site (max 6 votes/day)
- Per vote rewards: +5% talent progress, +100% AFK XP, +20% group XP, +1% drop rate/site, shooting star access
- Daily Vote Rewards: monthly shop reset at Vote Obelisk
- Vote Streak: 7 consecutive days = 1 streak point; 14 days = 2; 21+ = 3
- Vote Streak Store: exclusive rewards
- World Boss spawns from votes (::votes shows count remaining)

### 9. DONATING / RANKS
Ranks (donation required):
- Sapphire $20 | Emerald $50 | Ruby $100 | Diamond $250
- Dragonstone $500 | Onyx $1k | Zenyte $2k | Tanzanite $5k | Olympian $10k
- Double dip: buy Bond ($25) → 25 Donator Credits → spend on Rank Book = 50 total rank
- Perks scale with rank (noted bones on altar, noted logs on bonfire, zone access, etc.)
- Delivered to mailbox near home

### 10. ACHIEVEMENTS
6 tiers: Starter → Apprentice → Adept → Expert → Master → Grandmaster + Heroic
- Example starters: Assign talent point, Vote 3 times, Restore HP at pool, Open clue caskets
- Rewards: PvM talent point orbs, Crystal keys, Coins, Booster tokens, clue scrolls
- Mid-tier: Collection log slots, equip gear sets (Granite, Dragon, Red D'hide)
- Achievement interface redesigned Oct 2025

### 11. COMMANDS (all ::commands)
Teleport: ::home ::afk ::wb (world boss) ::event ::star ::ddz (donor zone) ::slayer
Security: ::2fa ::setpin ::checkpin
General: ::w (wiki) ::staff ::loot ::empty ::discord ::vote ::votes ::claimvotes ::streak ::donate ::refer ::answer ::yell
League-specific league commands

### 12. SKILLS (30 skill pages)
All OSRS skills present. Guides for each.
Skills with AFK training: Firemaking, Woodcutting, Fishing, Mining (AFK zone)
Special: Agility/Construction/Hunter have alternate training methods (FAQ mentions)

### 13. AFK ZONE
Located NE of home barrier (::afk command)
- The Elven City = Prifddinas is the home city
- Contains all major training areas
- Map shows: Farming, Fishing & WC, Mining, Thieving, Multi-Skill Area
- Dragonstone Donator Zone
- World Boss Arena
- Loot Chest Building
- Item Sacrifice bench

### 14. COLLECTION LOG
- Complete slots → unlock rewards
- Starter achievement: unlock 25 slots
- Collection log optimizer suggested in NEXUS feature

### 15. STARDUST
- Earned from Shooting Stars (accessible via voting)
- Spent at Stardust Store (west of Home by Makeover Mage)

### 16. PETS
- Combat pets + Non-combat/Skilling pets
- Skilling pets: +20% XP bonus to their skill when following
- Two distinct pet types

### 17. IRONMAN MODE
Separate from game modes (they stack)
- Ironman Store available
- No GE access implied

### 18. LEAGUES (launched January 2026)
- League Point Store
- League-specific commands
- World-specific broadcast toggles
- TOB Pandora perks for league
- League Account game mode: 0% bonus talent points anywhere

### 19. DROP RATE SYSTEM
- Base drop rate + modifiers
- +1% per vote site (max 3% from voting)
- +3% from 2FA + bank PIN
- Slayer Locked: +5% DR per slayer prestige vs bosses (max 45%)
- Vote buff: active 12 hours after claiming votes

### 20. WORLD EVENTS
- World Boss spawns from vote milestones (::votes shows countdown)
- Shooting Stars (from voting)
- Seasonal events (Christmas 2025 with Big Nagua, Easter event, Halloween)
- Trivia system (::answer command)
- World Boss Arena (::wb)

---

## GEAR PROGRESSION (August's path)
Helmet best-to-worst: Sanguine torva → Radiant oathplate → Torva → Titanforged → Oathplate → Judicator → Echoing → Neitiznot → Dragonstone → Corrupted → Diamond → Bloodfury → Ruby → Emerald → Sapphire → Justiciar
Amulet: Amulet of the monarchs → Monarchs torture → Torture (or) → Torture → Bloodfury → Fury → Glory
Cape: Completionist cape → Titanforged pavis → Infernal → Fire cape

**Custom items hierarchy** (August unique): 
Sanguine > Radiant > Titanforged > Echoing > Dragonstone > Corrupted > Diamond/Bloodfury > Ruby > Emerald > Sapphire (gem tier system)

---

## LOSTCITY ARCHITECTURE (what we build on)

### Repos involved:
1. **LostCityRS/Server** — the launcher/setup scripts (what you clone)
2. **LostCityRS/Engine-TS** — TypeScript game server (branches per revision)
3. **LostCityRS/Content** — RuneScript content files (branches per revision)
4. **LostCityRS/Client-TS** — TypeScript browser client (per revision)
5. **LostCityRS/Client-Java** — Java applet client (per revision)

### Available revisions:
- **225** — May 18, 2004 ✅ Web client + Java client
- **244** — June 28, 2004 ✅ Web client + Java client
- **245.2** — July 13, 2004 ✅ Web client + Java client
- **254** — September 7, 2004 ✅ Web client + Java client (RECOMMENDED — most complete)
- **274** — November 2004 ⚠️ WIP devs only
- **377-wip** — May 2006 ⚠️ WIP devs only

### Content scripting (RuneScript)
- Custom scripting language recreated from Jagex's original
- Scripts define: NPCs, shops, quests, dialogue, skills
- Limitations: no for loops, no true arrays originally
- LostCity extensions: local variables, procs, booleans, structs, enums, dbtables
- VS Code extension available: 2004scape.runescriptlanguage
- Files live in Content repo, organized by category

### How to add custom content:
1. Fork Content repo
2. Write .rs2 script files using RuneScript
3. Engine-TS reads and executes them
4. Client renders the result

### Start flow:
```
start.bat → npm install → node start.js
→ prompts: pick revision (225/244/245.2/254)
→ clones Engine-TS, Content, Client-TS, Client-Java
→ bun install in engine
→ bun run setup (config)
→ menu: Start Server / Update / Run Web / Run Java / Advanced
→ bun start in engine
→ play at http://localhost/rs2.cgi
```

---

## WHAT WE'RE BUILDING: BLACK BULLS DEN RSPS

### Base: LostCityRS revision 254
### Customizations inspired by August:

**Phase 1 — Get it running:**
- Clone LostCityRS, pick rev 254
- Verify it boots and is playable
- Fork Engine-TS and Content to MisTAiM GitHub

**Phase 2 — Core custom features:**
- Custom home area (Black Bulls Den themed)
- Prestige system (OSRS leagues inspiration)  
- Talent tree system (3 trees: PvM, Skilling, Utility)
- Game modes (PvMer, Skiller, Custom Challenge mode)

**Phase 3 — Economy:**
- Custom shops (Token stores, Prestige store, Skilling store)
- Voting system integration
- Drop rate modifiers
- GE (or simplified player market)

**Phase 4 — Content:**
- Custom bosses (Black Clover themed — tie to anime)
- Achievements system
- AFK training zone
- Item sacrifice/sink system

**Phase 5 — Polish:**
- Web panel (hiscores, voting, admin)
- Custom wiki
- Discord bot integration
- Black Bulls Den branding throughout

---

## DEPENDENCIES FOR OUR SERVER
- Node.js 22+
- Git
- Java 17+ (you have this now ✅)
- Bun (fast JS runtime — LostCity uses it)
- VS Code + RuneScript extension (for content development)


---

## UPDATE: FULL WIKI SCRAPE COMPLETE (1,313 pages)

### PRESTIGE SYSTEM (exact numbers)
Prestige 1: Level 99 required | +99 virtual levels
Prestige 2: Level 101 | +200 total
Prestige 3: Level 103 | +303 total
Prestige 4: Level 105 | +408 total
Prestige 5: Level 107 | +515 total
Prestige 6: Level 109 | +624 total
Prestige 7: Level 111 | +735 total (max for PvMer/Skiller)
Prestige 8: Level 113 | +848 total (Slayer Locked max: P9, Masochist max: P10)
Prestige 9: Level 115 | +963 total
Prestige 10: Level 117 | +1080 total

Combat prestige: adds virtual skill levels (P1 = +99 virtual Magic if you prestige Magic)
Skilling prestige: unlocks new training methods or Slayer tasks (no virtual level bonus)

### TALENT POINTS (exact formula)
- Default: 1 talent point per 40 levels gained
- PvMer: +20% in combat skills (1 per 36 levels in combat)
- Skiller: +20% in non-combat skills
- Masochist: +10% all skills (1 per 36 levels)
- Slayer Locked: +20% combat skills; full Skilling tree access without tier prereqs
- Prestige bonus: extra points on prestige (amount varies by game mode)
- Talent point orbs: consumable items that grant points directly

### VOTING (exact rewards per site)
Per vote (RuneLocus gives most):
- RuneLocus: 3x Vote tokens, 1x Corrupted AFK scroll, 2x Major combat XP token
- Rune-Server: 1x Vote token, 1x Corrupted AFK scroll, 2x Major combat XP token
- RuneList: 1x Vote token, 1x Corrupted AFK scroll, 2x Major combat XP token
Total per full vote: 5 Vote tokens, 3 Corrupted AFK scrolls, 6 Major combat XP tokens

Vote Buffs (12 hours): +5% talent point progress, +100% AFK XP, +20% group XP, +1% DR per site

Vote Streak: 7 days = 1 streak point, 14 days = 2, 21+ days = 3

### DONATOR RANKS (exact thresholds)
Sapphire: $20 | Emerald: $50 | Ruby: $100 | Diamond: $250
Dragonstone: $500 | Onyx: $1,000 | Zenyte: $2,000 | Tanzanite: $5,000 | Olympian: $10,000

Double dip: Buy $25 Bond → 25 Donator Credits → buy Rank Book = 50 total rank

Key perks by tier:
- Sapphire+: Noted bones on altar, transmog mode
- Emerald+: Noted logs on bonfire, Mining/Thieving/WC/Fishing donor zone
- Ruby+: Previous teleport on Portal Nexus
- Diamond+: Permanent corrupt AFK zone, Farming corrupt donor zone
- Dragonstone+: Dragonstone donor zone, bypass group proximity for vote buff
- Dragonstone+ gives daily points (1000-1400) + daily slayer spawns (100-180)

### TEMPERING SYSTEM (exact stats)
Items can be tempered up to 15 times:
- Rank 1-3: Free (need 1-3 duplicate items)
- Rank 4: +34.95% stats, 2 more items, 5,000 upgrade gems
- Rank 7: +45.43% stats, 4 items, 25,000 gems
- Rank 10: +54.63% stats, 8 items, 105,000 gems
- Rank 15: +69.66% stats, 16 items, 1,165,000 gems (93 total items needed!)

### ITEM TIER SYSTEM
Items have [T##] tiers visible on examine:
- T70: Giant mole range
- T72: KBD range
- T90: Primordial boots (example)
- T95: Corrupted body
- T105: Echoing body
- T110: Amulet of the monarchs (passive: heals 2.5% of damage dealt)

### YAMA BOSS DROPS (full list)
Always: Infernal ashes
Common (1/10): Coins 120k-600k, Prayer pots, Super restores, Combat pots, XP tokens, Boss tokens 84-240
Rare: Dragon bones 250-1000, Coins 3.6M-6M, Bonds ($5/$10), Talent respec token
Regular always: Sharks, Fire runes 20-40k, Blood/Soul runes, Dragon items, Demonite
Uniques: Oathplate helm/chest/legs, Soulflame horn, Forgotten lockbox
Pet: Yami (1/1000)

### BOSS TOKEN STORE (key items)
15,000 Boss tokens: Pious/Dexterous/Arcane prayer scrolls, World Boss Jars
50 Boss tokens: Overload(+)(4)
30 Boss tokens: Prayer enhance(+)(4)
100,000 Boss tokens: Shard of insurance
20,000 Boss tokens: Looting bag

### ITEM SACRIFICE PERKS (10 categories)
Bossing, Raiding, Production, Gathering, Melee, Magic, Ranged, Survival, Slayer, Pets
Sacrificeable items include: Pandora's essence (lesser/normal/greater/perfect), Ethereal weapons,
Spirit shields (Arcane/Spectral/Elysian/Blood), GWD gear, Dragon items, PvP armors, Void gear

### STARTER TIPS FROM WIKI
1. ::starter and ::refer codes for starter packs + Sapphire rank book
2. ::vote + ::claimvotes every 12 hours
3. ::2fa + ::setpin = +3% drop rate
4. Talents are #1 power source — prioritize earning talent points
5. Achievements give early rewards — claim them
6. Prestige always when you hit the level requirement
7. Same email for multiple accounts allowed

### ACHIEVEMENTS STARTER TIER (exact rewards)
- PvM/Skilling/Utility Talent Tree Novice: 1x respective Talent point orb each
- Vote 3 times: 3x Crystal key, 250k coins
- Restore 10 HP at pool: 75x Upgrade gems
- Restore 5 prayer at pool: 2x Crystal key
- Open 1 Beginner Clue: 1x Beginner clue, 1x Easy clue
- Equip full Granite: 1x PvM Talent point orb
- Kill 200 NPCs: 1x PvM Talent point orb
- Kill 50 each Barrows brother: 3x Barrows chest key
- Kill World Boss: 3x Enhanced crystal key, 300x Boss token
- Unlock 25 Collection Log slots: 3x Crystal key

### DROP RATE SOURCES
Primary methods to increase drop rate:
1. Voting: +1% per site voted (max +3%, lasts 12 hours after claiming)
2. Divine luck flasks: consumable item
3. Bank pin + 2FA: +3% permanent

### AGILITY/CONSTRUCTION/HUNTER
Not currently in game (per FAQ, as of wiki scrape)

### FOOD/POTIONS
No food/potion store — buy from GE (non-ironman), fish/farm/herb for ironman
