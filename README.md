# ⚔️ Black Bulls Den RSPS

> A custom OSRS-era private server for The Black Bulls Den community.
> Built on [LostCityRS](https://github.com/LostCityRS/Server) (revision 254 — September 2004).
> Inspired by August RSPS feature set.

---

## 🏰 Features (Roadmap)

### Phase 1 — Foundation ✅ In Progress
- [x] Knowledge bank built from August RSPS wiki
- [x] LostCity engine identified and documented
- [ ] LostCity rev 254 running locally
- [ ] Forked Engine-TS + Content to this org

### Phase 2 — Core Custom Systems
- [ ] Prestige system (level 99 → prestige → talent points)
- [ ] Talent tree (PvM / Skilling / Utility — 3 trees)
- [ ] Game modes (PvMer, Skiller, Challenge mode)
- [ ] Custom home area — Black Bulls Den themed

### Phase 3 — Economy
- [ ] Custom shops (Token stores, Prestige store)
- [ ] Voting system (vote streak rewards)
- [ ] Drop rate modifier system
- [ ] Grand Exchange

### Phase 4 — Content
- [ ] Custom bosses (Black Clover inspired)
- [ ] Achievements system (6 tiers)
- [ ] AFK training zone
- [ ] Item sacrifice/sink
- [ ] Collection log

### Phase 5 — Polish
- [ ] Web panel (hiscores, voting, admin)
- [ ] Discord bot
- [ ] Black Bulls Den branding + wiki

---

## 🚀 Quick Start

### Dependencies
- Git
- Node.js 22+
- Java 17+ ✅
- Bun (auto-installed by setup)

### Run It
```bash
git clone https://github.com/LostCityRS/Server.git lostcity
cd lostcity
start.bat        # Windows
# Pick revision 254 when prompted
# Choose "Start Server"
# Open http://localhost/rs2.cgi
```

---

## 📚 Research & Knowledge Bank

All August RSPS research is documented in [`docs/KNOWLEDGE_BANK.md`](docs/KNOWLEDGE_BANK.md).

This covers:
- All August game systems (prestige, talents, game modes, shops, voting, etc.)
- Full boss list (55 bosses)
- Gear progression tiers
- LostCity engine architecture
- RuneScript content scripting guide
- Black Bulls Den development roadmap

---

## 🏗️ Architecture

```
blackbullsden-rsps/
├── docs/
│   └── KNOWLEDGE_BANK.md     ← Complete August + LostCity research
├── engine/                   ← Fork of LostCityRS/Engine-TS (rev 254)
├── content/                  ← Fork of LostCityRS/Content (rev 254)
├── webclient/                ← Fork of LostCityRS/Client-TS (rev 254)
└── custom/                   ← Our custom RuneScript content
    ├── prestige/
    ├── talents/
    ├── bosses/
    ├── shops/
    └── home/
```

---

## 👥 Community
**Discord**: The Black Bulls Den  
**Owner**: Morpheus  
