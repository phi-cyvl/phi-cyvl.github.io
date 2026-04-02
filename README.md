# AI-Powered Event Planning for Cities

**Live site:** [phi-cyvl.github.io](https://phi-cyvl.github.io)

What happens when a city's infrastructure data meets AI? You get instant, comprehensive event planning — without a single site visit, without weeks of permit research, without guessing which sidewalks are safe for 10,000 fans.

These six demos show how **any city** can use AI agents + infrastructure intelligence to plan safer, more accessible community events. Every number is real. Every image is from an actual street scan. Every pavement score, business license, and permit requirement comes from live data — queried in real time through [Cyvl's MCP server](https://cyvl.ai) and [Boston's Open Data portal](https://data.boston.gov).

Built for the **City of Boston** ahead of the **2026 FIFA World Cup** — 7 matches at Gillette Stadium, 450,000 visitors expected, $10M in state grants for community watch parties, and a city that needs to know exactly where it's safe to host them.

---

## Who This Is For

**City leaders and CIOs** — See what's possible when your infrastructure data is AI-accessible. These demos answer real planning questions: *Where should we host a fan zone? Which streets are safe for a block party? What does it actually take to permit an event?* Santiago Garces, CIO of Boston, is already exploring this with Cyvl.

**Municipal planners and DPW** — Every demo surfaces actionable infrastructure findings. Failed pavement segments that need repair before an event. ADA ramps that aren't compliant. Sidewalk gaps on evacuation routes. The kind of intelligence that normally takes weeks of field surveys, delivered instantly.

**Technology partners** — This is what MCP (Model Context Protocol) looks like in production. Cyvl's infrastructure data and Boston's open data are both queryable by AI agents through the same standard. Any platform — ClearGov, Zencity, CivicPlus — can plug into this ecosystem.

**The public** — Boston is hosting the World Cup. These demos show the city is using cutting-edge AI to make sure every neighborhood event, watch party, and block party is safe, accessible, and well-planned.

---

## The Demos

### 1. [World Cup Bar Crawl Walkability](01-bar-crawl-walkability/)
*"Is it safe to walk between bars on match day?"*

An 11-stop route from Davis Square to Union Square — every sidewalk, crosswalk, and curb ramp assessed.
- 1,798 pavement segments scored, worst segment flagged for pre-World Cup repair
- Road-snapped routing on interactive maps, real street-level photos at each stop
- B+ walkability grade (82/100) with specific hazards identified

### 2. [Newbury Street Pop-Up Playbook](02-newbury-popup-playbook/)
*"How does a small business host a summer pop-up on Newbury Street?"*

The complete guide — permits, costs, timeline, infrastructure, and World Cup timing strategy.
- 8-step permit process ($230–$950), 68 past event licenses analyzed
- 49 real pavement segments scored (avg PCI 66.4), 799 Cyvl imagery matches
- 69 licensed businesses mapped, 50K+ Open Newbury Sunday foot traffic

### 3. [Davis Square Community Block Party](03-davis-square-block-party/)
*"Can we host a 100% accessible block party in Davis Square?"*

Full event plan with infrastructure audit, business participation, and ADA compliance.
- 7,277 infrastructure data points: 1,798 pavement + 2,190 signs + 3,289 assets
- 2 Failed pavement segments (PCI 1.2, 9.6) caught before anyone arrives
- 12 local businesses with $25K–$50K projected revenue lift

### 4. [From Parking Lot to Party](04-school-st-parking-lot/)
*"What would it take to throw a party in that empty lot?"*

200-person event plan built entirely from infrastructure data — zero site visits required.
- $23,705 budget from 9 Cyvl data points (fire hydrants, utility poles, pavement, lighting)
- 8-step regulatory checklist, week-by-week timeline, noise/safety/parking plans
- Proof that AI + infrastructure data can replace traditional site surveys

### 5. [Fan Zone Site Selector](05-fan-zone-selector/)
*"Where should Somerville host World Cup watch parties?"*

7 candidate sites ranked across 6 weighted criteria — the kind of analysis that justifies a $10M grant application.
- Assembly Row ranked #1 (87/100), Teele Square disqualified (9 Failed pavement segments)
- ADA accessibility weighted highest (25%) because accessibility isn't optional
- Transparent scoring methodology cities can adapt for any event type

### 6. [Emergency Evacuation Readiness](06-evacuation-readiness/)
*"Are our streets safe for 50,000 fans to evacuate?"*

Pedestrian evacuation corridor assessment — the finding that makes city leaders pay attention.
- **PCI 23.55 structural failure on McGrath Highway** — co-located with a construction zone, on a route tens of thousands would use. Cyvl found it. Planners missed it.
- 4 corridors analyzed against $76M in federal security funding
- 2 ADA-non-compliant ramps, sidewalk gaps up to 128 feet

---

## The Data Behind It

Every claim in every demo traces back to one of three live data sources:

| Source | Coverage | Data Points |
|--------|----------|-------------|
| **[Cyvl](https://cyvl.ai)** | 1,003 miles (Boston + Somerville) | 271K street-level images, pavement scores, signs, assets, distresses, markings |
| **[Boston Open Data](https://data.boston.gov)** | City of Boston | Event licenses, business licenses, Vision Zero crashes, accessible parks |
| **[OSRM](https://project-osrm.org)** | Global | Pedestrian routing (maps follow real streets, not straight lines) |

### What Cyvl Sees

Cyvl's sensor-equipped vehicles scan every street, automatically detecting and scoring:
- **Pavement condition** — PCI scores from 0 (Failed) to 100 (Excellent)
- **Traffic signs** — MUTCD classification, condition, location
- **Above-ground assets** — Trees, hydrants, ramps, poles, signals, bike racks, CCTV
- **Distresses** — Cracking, potholes, rutting, weathering with severity and area
- **Markings** — Striping, crosswalks, lane markings

The 59 street-level photos embedded in these demos are real images from Cyvl scans — not stock photos, not renderings.

---

## How It Was Built

This site was built in a single [Claude Code](https://claude.ai/claude-code) session using parallel AI agent orchestration. No frameworks. No build tools. No server.

```
Claude Code (orchestrator)
├── 6 research agents (parallel) → Cyvl MCP + Boston CKAN + web
├── 6 build agents (parallel) → branded HTML pages
├── Audit agents → mobile responsiveness, data accuracy, imagery
└── Output: 12,724 lines of static HTML → GitHub Pages
```

**The key insight:** Cyvl and Boston both expose their data through **MCP (Model Context Protocol)** servers. Claude Code queries them the same way — structured requests in, structured data out. The AI agent handles the orchestration: geocoding locations, assessing infrastructure, searching imagery, cross-referencing crash data, and assembling it all into a coherent narrative.

This is what the future of civic technology looks like. Not dashboards that require training. Not APIs that require developers. Just AI agents that understand your data and answer your questions.

---

## For City Leaders

If you're a CIO, city manager, or municipal planner wondering what this means for your city:

1. **You already have the data.** Open data portals, infrastructure assessments, permit databases — they're sitting there. MCP makes them AI-accessible.
2. **The analysis is instant.** What used to take weeks of field surveys, permit research, and cross-referencing databases happens in minutes.
3. **It scales.** These demos cover Somerville and Boston. The same approach works for any city with infrastructure data.
4. **It's transparent.** Every number has a source. Every score has a methodology. Every image is verifiable.

**Interested?** [Contact Cyvl](https://cyvl.ai) to see what your city's data looks like through AI.

---

## Running Locally

```bash
python3 -m http.server 8000
# Open http://localhost:8000
```

No dependencies. No build step. Static HTML.

---

## World Cup 2026 Context

| Fact | Detail |
|------|--------|
| Venue | Gillette Stadium, Foxborough MA (7 matches) |
| Dates | June 13 – July 9, 2026 |
| Key matches | England vs Ghana (June 23), Norway vs France (June 26), Quarterfinal (July 9) |
| Visitors | 450,000 to Massachusetts |
| Fan Festival | City Hall Plaza, Boston (free, full tournament) |
| State grants | $10M — Governor Healey's Sports & Entertainment Events Fund |
| Federal security | $76M ($46.6M FIFA + $21.2M counter-UAS + $8.6M FTA) |

---

*Built by [Cyvl](https://cyvl.ai) with [Claude Code](https://claude.ai/claude-code). Infrastructure intelligence for safer communities.*
