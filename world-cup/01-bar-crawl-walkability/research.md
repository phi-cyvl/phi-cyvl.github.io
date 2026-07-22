# World Cup Bar Crawl Walkability Assessment — Research Brief
## Somerville, MA | Cyvl Demo for Boston CIO Santiago Garces

**Prepared:** April 2026  
**Demo context:** Monday news interview on AI + city infrastructure. Cyvl HQ at 76 School St, Somerville. FIFA World Cup 2026 hosts 7 matches at Gillette Stadium June 13–July 9.  
**Demo pitch:** Show how Cyvl's infrastructure intelligence data enables cities to plan safe, walkable event experiences — concretely illustrated through a real neighborhood bar crawl route.

---

## 1. Bar & Venue Locations

### Proposed Crawl Route

The crawl spans three Somerville hubs connected by walkable streets. Recommended sequence: **Union Square → Davis Square → (optional) Teele/Magoun Square**. Total route is ~2.5 miles end-to-end; participants can do subsets. MBTA Red Line (Davis) and Green Line Extension (Union Sq) provide bookend transit access.

| # | Venue | Address | Neighborhood | Why It Works |
|---|-------|---------|--------------|--------------|
| 1 | **Tony C's Sports Bar & Grill** | 699 Assembly Row, Somerville 02145 | Assembly Row | Best pure sports bar; 40+ drafts, 360° jumbotron, full wall HD TVs, MBTA Orange Line Assembly stop adjacent. Ideal anchor/start for transit riders. |
| 2 | **The Independent** | 75 Union Square, Somerville 02143 | Union Square | Iconic neighborhood pub in heart of Union Sq; strong beer list, good food, indoor/outdoor energy |
| 3 | **Olde Magoun's Saloon** | 518 Medford St, Somerville 02145 | Magoun Square | Top-ranked World Cup watch party spot per GameWatch.info; craft beer focus, local institution |
| 4 | **Parlor Sports** | 1 Beacon St, Somerville 02143 | Ward 2 / Ball Sq | Named top World Cup watch bar in Somerville; many TVs, sports-forward atmosphere |
| 5 | **PJ Ryan's** | Teele Square, Somerville | Teele Square | Classic neighborhood sports bar; walkable from Ball Sq/Davis corridor |
| 6 | **The Burren** | 247 Elm St, Somerville 02144 | Davis Square | Authentic Irish pub, live music 7 nights/week — World Cup + Irish pub = natural fit; large venue capacity |
| 7 | **Foundry on Elm / Saloon** | 255 Elm St, Somerville 02144 | Davis Square | Two connected venues (upstairs/downstairs); Saloon is a speakeasy-style cocktail bar — good change of pace mid-crawl |
| 8 | **The Painted Burro** | 219 Elm St, Somerville 02144 | Davis Square | Mexican kitchen + tequila bar; outdoor patio; rooftop access — great for warm June/July match days |
| 9 | **Five Horses Tavern** | 400 Highland Ave, Somerville 02144 | Davis Square | 36 rotating drafts, 150+ bourbons; patio; strong craft beer destination |
| 10 | **Redbones BBQ** | 55 Chester St, Somerville 02144 | Davis Square | Beloved local BBQ spot with full bar; downstairs Underbones bar; outdoor seating |

**Note on Assembly Row:** Tony C's at Assembly Row is ~1.8 miles from Davis Square — best positioned as a standalone anchor (transit in/out via Orange Line) or as a dedicated Assembly Row watch party stop. The Davis Square cluster (stops 6–10) is tightly walkable within ~0.4 miles.

### World Cup Watch Party Suitability

Key criteria: multiple large TVs, outdoor/patio space, capacity for surges, extended hours.

- **Strongest:** Tony C's (full AV system, 360° jumbotron), Parlor Sports (explicitly recommended by GameWatch.info for World Cup), Olde Magoun's Saloon
- **Good:** The Burren (large Irish pub footprint), Five Horses Tavern (patio), The Painted Burro (rooftop)
- **More intimate:** Saloon (speakeasy — limited capacity), Redbones (food-forward)

---

## 2. Route Safety Data

### What the Boston CKAN Open Data Portal Provides

Boston's open data portal (data.boston.gov) contains two directly relevant safety datasets. **Important caveat:** Boston CKAN covers Boston proper — Somerville is a separate municipality with its own data systems. The crawl route passes through Somerville, not Boston. The Boston data below illustrates the *type* of analysis Cyvl would perform, and provides comparator data for the Somerville/Boston border zone.

#### Vision Zero Crash Records (Boston)
**Dataset:** Vision Zero Crash Records  
**Source:** `data.boston.gov/dataset/7b29c1b2-7ec2-4023-8292-c24f5d8f0905`  
**Coverage:** Through December 31, 2025  
**Schema fields:** dispatch timestamp, mode_type (mv/ped/bike), street, cross-streets, lat/long

**Live query results — crash mode breakdown (all Boston, full dataset):**

| Mode | Crash Incidents |
|------|----------------|
| Motor Vehicle (mv) | 32,134 |
| Pedestrian (ped) | 6,655 |
| Bicycle (bike) | 3,896 |

Pedestrian crashes represent ~15% of all incidents — disproportionately dangerous given pedestrian volume.

**Sample pedestrian crashes near Somerville border (lat 42.36–42.40, long -71.13–-71.07):**
- Cambridge St @ Maffa Way — 2 incidents (2025)
- Carter St @ Cambridge St — 2024
- Roland St — 2025
- Cedar St @ Phillips St — 2025

These are Charlestown/Cambridge border crossings — the closest Boston data to the Somerville bar crawl corridor.

#### 311 Service Requests (Boston) — Sidewalk/Crosswalk Issues
**Dataset:** 311 Service Requests — 2026  
**Source:** `data.boston.gov/dataset/8048697b-ad64-4bfc-b090-ee00169f2323`

**Live query results — pedestrian infrastructure complaints (2026 dataset):**

| Issue Type | Reports |
|------------|---------|
| Unshoveled Sidewalk | 12,025 |
| Request for Pothole Repair | 4,951 |
| Sidewalk Repair (Make Safe) | 1,298 |
| New Sign / Crosswalk / Pavement Marking | 134 |
| Sidewalk Cover / Manhole | 79 |
| Sidewalk Repair | 1 |

The 311 data is Boston-only. During a World Cup demo, this illustrates the **scale of unresolved sidewalk complaints** that Cyvl's automated scanning would surface faster and with location precision.

### Somerville-Specific Safety Data (Not in Boston CKAN)

Somerville maintains its own open data and Vision Zero program:

- **Vision Zero Somerville:** Active since ~2020. 623 total crashes in 2024 (MassDOT IMPACT). Zero fatal crashes for second consecutive year (2023–2024).
- **High-Injury Network:** Broadway is identified as a high-crash corridor requiring infrastructure intervention.
- **Traffic calming:** 100+ traffic calming features built in 2024.
- **Intersection improvements:** 5 intersections reconstructed in 2024–2025 for pedestrian safety.
- **ADA gap:** Estimated $75M backlog to bring Somerville sidewalks to ADA standard.
- **Interactive crash map:** Available at somervillema.gov for 2017–2022 data.

**This is the Cyvl gap:** Somerville's Vision Zero data exists but is not in Boston CKAN. Cyvl's platform would provide **ground-truth sidewalk condition data** (LiDAR + 360° imagery) for the exact bar crawl route — rating each block segment for sidewalk width, surface condition, crosswalk presence, curb cuts, and lighting — independent of whether the city's 311 data is current.

---

## 3. Walkability Factors

### Somerville's Baseline

- **Walk Score:** 89/100 — "Walker's Paradise" (most errands on foot)
- **Named top 10 city** nationally for walking and transit
- **Union Square, Porter Square, Inman Square:** Among highest walk scores in city
- **20 mph safety zones:** Cover most residential streets plus schools, senior centers, medical facilities
- **Complete Streets program:** Active city policy (SomervillebyDesign)
- **Somervision 2040:** Long-range plan includes mobility as a core pillar

### Walkability Assessment Dimensions (for the Demo Scoring System)

Each segment between bar crawl stops should be scored on:

| Factor | What Cyvl Measures | Why It Matters |
|--------|-------------------|---------------|
| **Sidewalk continuity** | Gap detection via LiDAR | No gaps = no trip hazards for night-time crowds |
| **Sidewalk width** | Sub-inch measurement | Min 5 ft (ADA), ideally 8+ ft for event crowds |
| **Surface condition** | Crack/heave classification | Key for ADA compliance; uneven surfaces = fall risk |
| **Crosswalk presence** | Sign + pavement marking detection | Safe pedestrian crossing at each intersection |
| **Curb cuts / ramps** | ADA ramp detection | Required at every crossing; $75M Somerville backlog |
| **Street lighting** | Luminaire inventory from imagery | Critical for 9 PM–midnight post-match crowds |
| **Buffer from traffic** | Distance from curb to sidewalk edge | Parked car buffer = perceived safety |
| **Intersection control** | Signal vs. stop vs. uncontrolled | Traffic signal timing matters for drunk-friendly crossings |
| **Traffic speed** | Road geometry + posted speed | 20 mph zones vs. arterials (Broadway, Highland Ave) |
| **Crime / disorder** | (Not Cyvl, but contextual) | 311 data for neighborhood context |

### Key Route Segments to Analyze

- **Union Square to Davis Square:** Holland St / Elm St corridor (~1.0 mile). Mixed residential/commercial, mostly sidewalked.
- **Davis Square cluster (internal):** Elm St between The Burren, Foundry, Painted Burro, Redbones — very short blocks, high pedestrian activity.
- **Assembly Row to broader route:** Requires Orange Line transit; walking not recommended (industrial zone between Assembly Row and residential Somerville).
- **Highland Ave:** Wider arterial — Five Horses Tavern location. Sidewalks present but narrower buffer from traffic.

---

## 4. World Cup Event Context

### Match Schedule at Gillette Stadium (Foxborough, MA)

| Date | Match | Group | Kickoff (ET) | Watch Party Demand |
|------|-------|-------|--------------|-------------------|
| June 13 | Haiti vs. Scotland | C | 9:00 PM | Moderate |
| June 16 | Playoff Winner vs. Norway | I | 6:00 PM | Moderate |
| June 19 | Scotland vs. Morocco | C | 6:00 PM | Moderate |
| **June 23** | **England vs. Ghana** | **L** | **4:00 PM** | **VERY HIGH** — England fan base enormous; prime time for bar crawl |
| **June 26** | **Norway vs. France** | **I** | **3:00 PM** | **HIGH** — France is a powerhouse; large French expat community in Boston |
| June 29 | Round of 32 (TBD) | — | 4:30 PM | High |
| July 9 | Quarterfinal (TBD) | — | 4:00 PM | Very High |

**Gillette Stadium capacity:** 65,878 for soccer. Expected 450,000 visitors to Boston across the tournament; 3M+ international visitors to the region.

### Economic & Crowd Context

- Projected $500M–$1B economic impact for Greater Boston region
- FIFA Fan Festival at Boston City Hall Plaza (up to 16 days in June) — draws additional foot traffic
- Bar crawl demo should be pitched as a June 23 scenario (England vs. Ghana) — 4 PM kickoff means crowds in bars from 3 PM, crawling from 6 PM through midnight
- June/July weather: typically 70–80°F, favorable for outdoor patios and walking
- Somerville is approximately 25–30 min by MBTA from Gillette Stadium (MBTA + commuter rail), making it a realistic post-game destination

### Crawl Timing Recommendation (June 23 England vs. Ghana)

```
2:00 PM  — Pre-game gathering at Tony C's (Assembly Row) — watch party anchor
4:00 PM  — Match kickoff
6:30 PM  — Match ends; crowd flows out
7:00 PM  — Bar crawl begins: Union Square → Davis Square
7:00–8:00 PM  — Stop 2: The Independent (Union Square)
8:00–9:00 PM  — Stop 3: Olde Magoun's / Parlor Sports area
9:00–10:00 PM — Stops 4–6: Davis Square cluster (The Burren → Foundry → Painted Burro)
10:00–11:30 PM — Stops 7–9: Five Horses Tavern → Redbones
```

---

## 5. Permitting Requirements

### Somerville Special Event / Bar Crawl Permits

**Primary pathway:** Somerville City Clerk / Licensing Commission via CitizenServe platform at somervillema.gov/citizenserve.

**Application type:** "Public Event / Special Alcohol License" — required even for events on public property without alcohol; required for any event with alcohol sales or consumption.

**Key requirements:**

| Requirement | Details |
|-------------|---------|
| **Lead time** | Allow up to **6 weeks** for approval |
| **Alcohol sourcing** | All alcohol sold/consumed must be purchased from a Mass. ABCC-licensed supplier. Exception: registered nonprofits may use donated alcohol |
| **Licensing authority** | Somerville Licensing Commission + Massachusetts ABCC (Alcoholic Beverages Control Commission) |
| **Compliance** | Somerville Code of Ordinances + state + federal law |
| **Contact** | cityclerk@somervillema.gov or call 311 |
| **Road closures** | Separate permit required if any street segment is closed; coordinate with DPW and Traffic/Parking |
| **Individual venue compliance** | Each participating bar must have a valid all-alcohol or beer/wine license; special event endorsements may be needed for extended hours |
| **Small Event Parking** | Small Event Parking Permit Application available separately for associated parking needs |

**For a bar crawl specifically (no road closures):**
1. Organizer files Public Event / Special Alcohol License application (CitizenServe)
2. Each venue participates under its existing license
3. If selling a "crawl wristband" or ticket: additional ABCC coordination required
4. No road closures anticipated — route uses existing sidewalks

**Massachusetts ABCC:** Special event licenses (Section 14) allow non-licensees to sell alcohol at specific events; however, for a bar crawl, each bar operates under its own license. The crawl organizer's permit covers the event structure, crowd management plan, and public space use.

---

## 6. App Concept: "Crawl Guide" Card Interface

### UX Overview

A mobile-first card-swiping app showing each crawl stop with Cyvl-powered walkability data between stops. Designed for one-handed use by people who've been drinking — large text, minimal taps, high contrast.

### Card Structure

Each stop is a **full-screen card** (think Tinder / Duolingo):

```
┌─────────────────────────────────────┐
│  STOP 3 OF 10                [map]  │
│                                     │
│  🍺 The Burren                      │
│  247 Elm St · Davis Square          │
│                                     │
│  "Authentic Irish pub · Live music  │
│   7 nights/week · Large capacity"  │
│                                     │
│  ──────── WALK HERE ──────────     │
│                                     │
│  From Foundry on Elm: 0.1 mi       │
│  ~2 min walk · Elm St              │
│                                     │
│  Walkability Score: 94/100  [A]    │
│  ✓ Wide sidewalk (8+ ft)           │
│  ✓ Street lighting: good           │
│  ✓ Curb cuts at both crossings     │
│  ⚠ 1 sidewalk crack flagged        │
│                                     │
│  [  Street View  ] [ Navigate ]    │
│                                     │
│  ← swipe to go back  →  next stop  │
└─────────────────────────────────────┘
```

### Card Components

| Component | Data Source | Cyvl Provides? |
|-----------|-------------|---------------|
| Venue name + address | Curated venue list | No |
| Walk distance + time | Google Maps / OSM routing | No |
| Street name of route | Routing engine | No |
| **Walkability Score** | **Cyvl i3 Index** | **YES** |
| **Sidewalk width** | **Cyvl LiDAR measurement** | **YES** |
| **Street lighting status** | **Cyvl luminaire inventory** | **YES** |
| **Curb cut presence** | **Cyvl ADA detection** | **YES** |
| **Sidewalk condition flags** | **Cyvl crack/heave ML model** | **YES** |
| **360° street-level imagery** | **Cyvl imagery capture** | **YES** |
| Crash history near route | Boston/Somerville Vision Zero | Partial (public data) |
| Current 311 complaints | Boston/Somerville 311 | No (public data) |

### Scoring Methodology

**Walkability Score (0–100)** per segment, computed from Cyvl data:

```
Score = (
  sidewalk_continuity     × 25 pts   # gaps = hard deductions
  + sidewalk_width        × 20 pts   # <5ft = fail; 8ft+ = full points
  + surface_condition     × 20 pts   # crack/heave severity rating
  + lighting_adequacy     × 15 pts   # luminaire spacing + lux estimate
  + curb_cut_presence     × 10 pts   # ADA compliance at each crossing
  + crosswalk_marking     × 10 pts   # visible pavement markings
)
```

Letter grades: A (90–100), B (75–89), C (60–74), D (below 60).

### Navigation Experience

- **Segment card** appears *between* venue cards as user swipes
- Shows static map + Cyvl 360° street-level imagery of the actual sidewalk
- Walk time countdown (optional live mode)
- Safety tip if score < 75: "This block has a narrow sidewalk — walk single file and watch for the construction scaffolding at Elm + Grove"
- Accessibility mode: can filter to ADA-compliant route alternatives

### Demo Flow for CIO Presentation

1. Open app to a preloaded "June 23 — England vs. Ghana" crawl
2. Swipe through 3–4 stop cards to show venue info
3. Tap into a segment walkability card — show Cyvl street imagery of the actual sidewalk
4. Show a "flagged" segment (score < 75) — e.g., a block on Highland Ave with a narrow sidewalk and a missing curb cut
5. Zoom out to city map view — show all flagged segments citywide, color-coded by score
6. Land on: "Boston and Somerville can use this data to prioritize sidewalk repairs before World Cup match days"

---

## 7. Data Gaps — What Cyvl MCP Would Fill

| Data Need | Available from Open Data? | Cyvl Fills It? |
|-----------|--------------------------|---------------|
| Sidewalk width along crawl route | No — not in any public dataset | YES — LiDAR measurement |
| Sidewalk surface condition (cracks, heaves) | No | YES — 50+ ML models |
| Curb cut / ADA ramp inventory | No public dataset (Somerville ADA backlog is ~$75M unfunded) | YES — detection from imagery |
| Street lighting inventory (pole locations, condition) | No — Boston CKAN had no streetlight dataset | YES — luminaire detection |
| 360° street-level imagery | Google Street View (stale) | YES — recent Cyvl captures |
| Crash hotspots near route | Somerville Vision Zero (but not in Boston CKAN) | Partial — Cyvl can overlay |
| 311 sidewalk complaints near route | Boston 311 available (Boston proper only); Somerville separate | No — public data, not Cyvl |
| Real-time crowd density | No | No (out of scope) |
| Bar capacity / wait times | No | No (out of scope) |

---

## 8. Demo Narrative for Boston CIO

**Headline:** "When 65,000 fans leave Gillette on June 23rd, thousands will end up in Somerville. Do we know if the sidewalks are safe?"

**Story arc:**
1. World Cup brings 450,000 visitors to Boston. On June 23, England plays Ghana — the biggest bar day of the summer.
2. Somerville — a 10-minute Red Line ride from any MBTA hub — will be packed. The bars are ready. But what about the streets?
3. Boston and Somerville have $75M in unfunded ADA sidewalk work. The city doesn't know which blocks are worst.
4. Cyvl scanned the bar crawl route. Here's what we found: [swipe through app] — 3 blocks with narrow sidewalks, 2 missing curb cuts, 1 lighting gap on the Holland St corridor.
5. With Cyvl, the city can prioritize those 6 blocks for repair by June 13 — the cost of fixing one curb cut ($800–1,200) vs. the cost of one ADA lawsuit ($50,000+).
6. This is infrastructure intelligence. Not inspectors with clipboards — AI that scans the whole city in days.

---

## Sources

- [GameWatch.info — World Cup Watch Parties Somerville](https://gamewatch.info/teams/world-cup-soccer/cities/somerville-ma)
- [Tony C's Sports Bar — Assembly Row](https://assemblyrow.com/explore/tony-cs-sports-bar-grill/)
- [Vision Zero Somerville](https://www.somervillema.gov/departments/programs/vision-zero-somerville)
- [Somerville Named Top 10 City for Walking and Transit](https://www.somervillema.gov/news/somerville-named-top-10-city-walking-and-transit)
- [Somerville Safe Streets Ordinance 2025 Annual Report](https://s3.amazonaws.com/somervillema-live/s3fs-public/somerville-safe-streets-ordinance-2025-annual-report.pdf)
- [Somerville Intersection Improvements](https://www.somervillema.gov/intersectionimprovements)
- [Walk Score Methodology](https://www.walkscore.com/methodology.shtml)
- [FIFA World Cup 2026 — Boston Match Schedule (FIFA.com)](https://www.fifa.com/en/tournaments/mens/worldcup/canadamexicousa2026/articles/boston-host-seven-matches-stadium)
- [Gillette Stadium World Cup Schedule — NESN](https://nesn.com/soccer/news/world-cup-2026-boston-schedule/f3dc28517cc6cd894f062787)
- [World Cup 2026 Gillette Stadium Guide — Sofascore](https://www.sofascore.com/news/gillette-stadium-a-guide-to-the-2026-fifa-world-cup/)
- [Boston Tourism Boom — World Cup Boston](https://bostonfwc26.com/newsroom/fifa-world-cup-26-will-supercharge-bostons-tourism-industry/)
- [Boston FIFA Fan Festival at City Hall Plaza](https://bostonfwc26.com/newsroom/the-boston-host-committee-for-fifa-world-cup-2026-announces-fifa-fan-festival-at-city-hall-plaza/)
- [Somerville Special Event / Alcohol Permit — CitizenServe](https://www3.citizenserve.com/Documents/149/Public%20Event-Special%20Alcohol%20CS%20instructions.pdf)
- [Somerville Public Event License Application](https://s3.amazonaws.com/somervillema-live/s3fs-public/public-event-license-application.pdf)
- [Somerville Licensing Commission](https://www.somervillema.gov/departments/licensing-commission)
- [Cyvl — How It Works](https://www.cyvl.com/how-it-works)
- [Cyvl applies AI to potholes — Cambridge Day](https://www.cambridgeday.com/2025/11/21/somerville-startup-cyvl-applies-ai-to-potholes/)
- [Boston Vision Zero Crash Records — data.boston.gov](https://data.boston.gov/dataset/7b29c1b2-7ec2-4023-8292-c24f5d8f0905)
- [Boston 311 Service Requests — data.boston.gov](https://data.boston.gov/dataset/8048697b-ad64-4bfc-b090-ee00169f2323)
- [Walk Score Somerville](https://www.walkscore.com/score/somerville-teele-square-two-br-somerville)
- [ADA Pedestrian Walkability Research — PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC10800413/)
- [WBUR — State traffic prep for World Cup](https://www.wbur.org/news/2025/08/29/boston-tourism-traffic-world-cup-america250-sail)
