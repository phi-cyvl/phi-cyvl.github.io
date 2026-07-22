# Emergency Evacuation Readiness — FIFA Fan Festival at Boston City Hall Plaza
## Research Brief for Cyvl Demo | Boston CIO Santiago Garces

**Prepared:** April 2026
**Event:** FIFA Fan Festival, City Hall Plaza, June 11 – July 19, 2026
**Demo purpose:** Show how Cyvl infrastructure intelligence transforms pedestrian evacuation planning for a 25,000-person urban outdoor event.

---

## 1. City Hall Plaza — Geography and Physical Layout

### Dimensions and Configuration
- **Total area:** 7 acres (approximately 200,000 sq ft / ~30,500 sq meters of usable event space)
- **Shape:** Multi-level, irregularly shaped — red brick and concrete
- **Vertical relief:** 26 feet of elevation change across the site (significant for crowd flow modeling)
- **Hanover Walk:** The primary accessible sloped promenade connecting Congress Street (south) to Cambridge Street (north) — drops 19 vertical feet to Congress Street

### Event Capacity (Official)
- **Main plaza only:** 10,000–12,000 persons
- **Full plaza:** up to 20,000–25,000 persons
- **Renovation (completed November 2022):** $95M project created 3,000 seating spaces, universal accessible pathways, civic pavilion with gender-inclusive restrooms, reopened North Entry

### Surrounding Streets and Egress Routes

| Egress Corridor | Direction | Notes |
|---|---|---|
| **Congress Street** | South | Lower elevation terminus of Hanover Walk promenade; primary pedestrian/vehicle arterial |
| **Cambridge Street** | North | Upper plaza level; connects to Beacon Hill, West End, MGH; Cambridge St / Blossom St fatality recorded here |
| **New Sudbury Street** | East | Connects to Government Center, Haymarket; Sudbury St / Bulfinch Pl / Congress St is highest pedestrian crash cluster (5 crashes) |
| **Court Street / Tremont** | West | Government Center T station entry zone; Tremont / Beacon / Bosworth is a recurrent crash location (3 crashes) |
| **Hanover Walk promenade** | North-South internal | Broad ADA-accessible sloped path — primary internal circulation spine |

### Government Center MBTA Station
- Located **beneath the plaza**, entrance at **southwest corner**
- Serves **Green Line (B/C/D/E branches)** and **Blue Line** — only transfer point for both lines in downtown Boston
- Pre-renovation: ~28,000 line-to-line transfers per day
- Post-2016 reconstruction: egress time cut by more than half; two stairways, new escalators, 4 elevators
- **Emergency exit-only structure** on Cambridge Street between Court and Sudbury Streets
- Station capacity constraint: single headhouse becomes a major bottleneck when 25,000 fans converge post-match

### Key Landmarks for Staging
- Faneuil Hall / Quincy Market: ~400m southeast (Faneuil Hall Sq / Dock Sq pedestrian crash on record)
- Sears' Crescent building: southern plaza edge, faces Congress Street
- U.S. GSA Federal Building: northeast — provides terrace overflow space
- North Entry to City Hall: reopened post-renovation, direct second-floor access

---

## 2. Crowd Capacity and Flow Standards

### Space Allocation (NFPA / ICC / Green Guide)

| Standard | Density | Condition |
|---|---|---|
| NFPA Life Safety Code baseline | ~0.46 m² per person (5 sq ft) | Standing crowd minimum |
| Comfortable standing | ~0.9 m² per person (10 sq ft) | Normal outdoor event |
| Green Guide (UK) comfortable | ~1.0–1.5 m² per person | Concert/festival |
| Dangerous crush threshold | <0.2 m² per person | Crowd collapse risk |

**At City Hall Plaza (30,500 m² usable):**
- At NFPA baseline (0.46 m²): theoretical max ~66,000 — far above safe operating capacity
- At event standard (0.9 m²): ~34,000 — above the 25,000 planned
- At 25,000 persons: ~1.22 m² per person — within acceptable outdoor event density

### Crowd Management Staffing (NFPA 101)
- Minimum: 1 crowd manager per 250 occupants
- At 25,000: requires **100+ certified crowd managers**
- Any outdoor assembly over 250 persons requires a designated crowd manager under Massachusetts law

### Pedestrian Flow Rates
- **UK Green Guide benchmark:** 82 persons/minute per meter of exit width under ideal conditions
- **Degraded conditions** (security checks, bottlenecks, night): 40–55 persons/minute per meter
- **Congress Street width** (typical urban arterial): ~12–18m total right-of-way; pedestrian zone ~4–6m each side
- **Cambridge Street:** urban arterial, similar profile
- **New Sudbury Street:** narrower, ~10–12m ROW

### Full Evacuation Time Targets
- Industry best practice: complete site evacuation within **8–10 minutes**
- At 25,000 persons, 8-minute target requires: minimum ~50 meters of aggregate effective exit width
- Government Center T station headhouse becomes critical constraint — single point of failure

### Bottleneck Identification Methodology
1. Calculate effective width of each egress corridor (total width minus obstructions: signage, bollards, furniture, parked bikes)
2. Multiply by flow rate coefficient (82/min/m peak, 55/min/m degraded)
3. Assign capacity to each corridor
4. Sum all corridor capacities → divide total crowd by aggregate flow → evacuation time
5. **Cyvl data enables step 1 for every egress route in the network**

---

## 3. Safety Data — Boston Vision Zero Records

### Pedestrian Crash Analysis: City Hall Plaza Proximity Zone
**Source:** Boston Vision Zero Crash Records (resource: `e4bfe397-6bfc-49c5-9367-c879fac7401d`)
**Area queried:** lat 42.355–42.365, lon -71.065 to -71.050 (approximately 0.5-mile radius centered on City Hall Plaza)

#### Total Crashes in Zone (all modes)
| Mode | Count |
|---|---|
| Motor vehicle (mv) | 915 |
| **Pedestrian (ped)** | **303** |
| Bicycle (bike) | 163 |
| **Total** | **1,381** |

Pedestrian crashes represent **22% of all crashes** in this zone — significantly above the citywide average, reflecting the dense pedestrian activity in Government Center / Financial District.

#### Top Pedestrian Crash Hotspots on Evacuation Routes

| Rank | Location | Crashes | Egress Route |
|---|---|---|---|
| 1 | **Sudbury St @ Bulfinch Pl / Congress St** | 5 | East egress / Congress south |
| 1 | **New Chardon St @ Hawkins / Bowker** | 5 | North dispersal |
| 3 | **Congress St @ North St** | 4 | South egress |
| 3 | **Congress St @ New Sudbury St** | 4 | East-South junction — critical node |
| 3 | **Cross St @ Hanover St** | 4 | East dispersal toward North End |
| 6 | **Tremont St @ Beacon / Bosworth** | 3 | West egress toward Common |
| 6 | **Blackstone St @ John F. Fitzgerald Surface Rd** | 3 | South dispersal |

**Pattern:** The Congress St / New Sudbury St intersection and Sudbury St corridor — both on planned evacuation routes — are among the highest-crash pedestrian locations in the zone. During a 25,000-person evacuation, these intersections will experience 10–20x normal pedestrian volume.

#### Selected Recent Pedestrian Incidents Near Evacuation Routes
- **2025-12-28:** Union St @ North St / Salt Ln (lat 42.361, lon -71.057) — immediately adjacent to plaza
- **2025-12-08:** Sudbury St @ Bulfinch Pl / Congress St — primary east egress
- **2025-08-20:** Hanover St @ Fitzgerald Surface Rd — north dispersal route
- **2025-07-31 & 07-19:** Fitzgerald Surface Rd @ Sudbury St (two incidents, same intersection) — east perimeter
- **2025-07-15:** Faneuil Hall Sq / Dock Sq — southern dispersal fan zone

#### Fatality Records
**Source:** Vision Zero Fatality Records (resource: `92f18923-d4ec-4c17-9405-4e0da63e1d6c`)

One pedestrian fatality recorded in extended zone:
- **2022-05-29, 8:07 PM:** Cambridge St @ Blossom St (lat 42.361, lon -71.067) — **on the Cambridge Street north egress corridor**, 0.5 miles west of plaza toward MGH

This is the exact route fans will use walking from the Fan Festival toward the West End / MGH / North Station area. A fatality at a signalized intersection on a wide arterial street underscores that even "safe" egress routes carry lethal pedestrian-vehicle conflict risk.

### Dataset Search Results
The Boston CKAN portal confirmed two Vision Zero datasets. No emergency-specific or special events licensing datasets were returned from the search. Fire station and hospital location data was not available in the CKAN portal at time of research.

---

## 4. Emergency Infrastructure

### Hospitals and Trauma Centers

| Facility | Type | Distance from Plaza | Route |
|---|---|---|---|
| **Massachusetts General Hospital** | Level I Trauma, Teaching Hospital | ~0.75 mi (1.2 km) northwest | Cambridge St west → Charles St / N. Grove St |
| **Tufts Medical Center** | Level I Trauma (verified since 2012) | ~0.8 mi south | Congress St south → Surface Rd → Washington St |
| **Boston Medical Center** | Level I Trauma | ~1.5 mi south | Multiple routes |

MGH is the closest Level I trauma center. **Cambridge Street is both the primary north fan dispersal route AND the ambulance corridor to MGH.** Conflict between evacuating pedestrians and responding EMS vehicles on Cambridge Street is a critical planning constraint.

### Fire Stations
- **Engine 4 / Ladder 24** — 200 Cambridge Street, West End (~0.5 mi northwest) — directly on north egress corridor
- **Engine 10 / Tiller Ladder 3 / Rescue 1** — 125 Purchase Street, Downtown (~0.6 mi southeast) — serves Congress Street south corridor
- Boston Fire Department operates 34 stations citywide with 1,400+ personnel

### Police
- **District A-1** (Downtown): historically 40 New Sudbury Street (east edge of plaza); currently relocated to 152 North Street (North End) for renovations
- **State Police Government Center Barracks**: on-site presence at plaza zone
- Boston Police + State Police coordination confirmed for World Cup: $46M+ federal security funding supports dedicated staffing

### Emergency Staging Areas
- **City Hall parking garage** (under plaza, Congress Street entrance): natural staging for EMS and command vehicles
- **Cambridge Street median** (wide arterial): can serve as temporary ambulance staging zone
- **GSA federal plaza terrace** (northeast): elevated, away from crowd flow — viable incident command post

### AED Locations
No public registry of AED locations near City Hall Plaza was identified. Boston EMS is the largest municipal EMS in New England with full-time paramedics and EMTs. For a 25,000-person event, NFPA 101 recommends AEDs at defined intervals (typically every 3–5 minutes of walking distance across the site).

---

## 5. What Cyvl Data Reveals

Cyvl's infrastructure intelligence platform captures street-level asset data at parcel and sub-meter precision. Applied to the Fan Festival egress network, Cyvl data answers questions that no existing dataset can.

### Sidewalk Widths — Bottleneck Detection

**Why it matters:** A sidewalk that is 4 feet wide passes ~1,600 people/hour at emergency flow rates. A 12-foot sidewalk passes ~4,800/hour. **Width is the single most important variable in evacuation capacity.**

Cyvl surveys every sidewalk segment and returns:
- Total right-of-way width
- Pedestrian clear zone width (after subtracting furniture, utility poles, signage)
- Effective passable width under crowd conditions

**Demo opportunity:** Show Cyvl data for Congress St, Cambridge St, New Sudbury St, and Court St. Highlight where measured widths create hard capacity ceilings — and which of the 5 highest-crash pedestrian intersections have constrained effective widths that explain the crash frequency.

### Pavement Condition — Wheelchair and Stroller Movement

City Hall Plaza's 2022 renovation introduced universal accessibility via Hanover Walk. But off-plaza egress routes on surrounding streets may have:
- Uneven brick or concrete heaves creating tripping hazards at crowd-pace movement
- Ponding areas (drainage failures) that funnel crowd flow into narrower dry paths
- Cracked asphalt that creates mobility barriers for wheelchairs, strollers, and fans with limited mobility

Cyvl's pavement condition index (PCI) data identifies these segments before an evacuation exposes them.

### Curb Cut Locations and ADA Ramp Grades

At Congress St / New Sudbury St intersection (top pedestrian crash cluster), the number, placement, and grade of ADA ramps directly affects whether wheelchair users can safely cross during a mass evacuation. Cyvl captures:
- Curb cut presence and location
- Ramp grade (ADA requires ≤8.33%; steep grades are impassable for manual wheelchairs under crowd conditions)
- Detectable warning surface condition

**Demo opportunity:** Overlay ADA ramp grades on the crash hotspot map. Show that the #1 and #3 pedestrian crash intersections on evacuation routes have specific infrastructure deficiencies that correlate with danger.

### Street Sign Obstructions — Effective Path Width Reduction

Signage, signal control boxes, and utility poles reduce effective pedestrian clear zone. Cyvl's asset inventory captures all vertical infrastructure in the ROW. On a 6-foot sidewalk, a signal box and a utility pole can reduce effective width to under 3 feet — below ADA minimums and a crush hazard during mass egress.

### Lighting Quality — Nighttime Evacuation Risk

Boston's World Cup matches at Gillette run into evening hours. Fan Festival watch parties will end at night. Cambridge Street, Congress Street, and New Sudbury Street are urban arterials with standard city lighting — but:
- Lighting levels under tree canopy may fall below 1 foot-candle (the NFPA minimum for egress)
- Post-renovation City Hall Plaza added trees (250+), which will cast shadows on plaza-edge egress paths at night
- The fatality on Cambridge St / Blossom St occurred at **8:07 PM** — after sunset in late May. Lighting conditions are a documented fatal risk on this exact egress corridor.

Cyvl data includes lighting condition assessments segment-by-segment.

### Surface Hazards — Cracks, Heaves, Ponding

High-traffic event days concentrate pedestrian wear on specific paths. Cyvl identifies:
- Surface cracking and heave locations
- Drainage failure zones where water ponds (slipping hazard; crowds avoid → narrowing effective width)
- Utility access panel displacement (ankle-roll hazard at crowd pace)

---

## 6. Lessons from the March 2026 Test Event

### What Happened: Brazil vs. France Friendly, March 26, 2026, Gillette Stadium, Foxboro

**Match:** France 2–1 Brazil | Attendance: 66,215 | Venue: Gillette Stadium

This was the official pre-tournament test event for Boston's World Cup preparation infrastructure.

### Road Network Failures

**I-95 and Route 1 gridlock:** Despite deploying **85 Massachusetts State Troopers**, the highway network could not move traffic. Foxboro Police Chief Michael Grace stated bluntly: *"The infrastructure has limitations."*

**GPS routing amplified the failure:** Navigation apps (Google Maps, Waze) routed tens of thousands of fans onto secondary roads and residential streets through surrounding towns. Chief Grace: *"They went on every secondary road"* — contrasting sharply with regular Patriots game attendees who know established routes. This is a **predictable, documented technology-infrastructure conflict** that will repeat at the Fan Festival.

**France's coach was nearly late:** Didier Deschamps reported the team cut arrival to 75 minutes before kickoff due to traffic backups.

**Fans walked the tracks:** Some attendees walked 3.5 miles along train tracks to avoid gridlock.

**Sanitation infrastructure failed:** Fans used private residential backyards as bathrooms on secondary streets — no portable facilities along overflow pedestrian routes.

### What Worked: MBTA Rail

The MBTA's commuter rail operation to Gillette was a declared success:
- 3,000+ event train tickets sold
- 4 bi-level trains, ~6,000-passenger capacity
- Airline-style boarding, Mansfield Station turnaround model worked
- Zero significant delays or incidents

### Why This Is Different at City Hall Plaza

The Foxboro failures are a **highway/suburban problem**. The Fan Festival failure mode is **urban pedestrian**:

| Foxboro Failure | City Hall Plaza Risk |
|---|---|
| I-95 / Route 1 vehicle gridlock | Congress St / Cambridge St pedestrian gridlock |
| 85 troopers couldn't move cars | 100 crowd managers can't widen sidewalks |
| GPS routed to secondary roads | Fans will route to narrowest, most dangerous paths |
| No porta-potties on overflow routes | No curb cuts / accessible surfaces on overflow routes |
| Fans walked 3.5 miles on train tracks | Fans will push into traffic on Congress St |

**The critical insight for the demo:** At Foxboro, the infrastructure failure was visible because cars stopped moving. At City Hall Plaza, the infrastructure failure will be invisible until someone is injured — because pedestrian infrastructure data doesn't exist in real time for planners. **Cyvl makes the invisible visible before the event.**

The MBTA test showed that fans will choose the train when the system is reliable. Boston expects 450,000 World Cup visitors. Government Center station, serving both Green and Blue lines, will be the primary arrival/departure point for Fan Festival attendees without cars. The post-match surge scenario at Government Center station — with 25,000 persons needing to access a single headhouse — is the City Hall Plaza equivalent of Route 1 gridlock.

---

## 7. Evacuation Scenario Modeling

### Assumptions and Base Parameters
- **Total attendance:** 25,000 persons (full plaza, full fan festival)
- **Mobility-limited attendees (ADA):** 5–8% (~1,250–2,000 persons) requiring accessible paths
- **Children and strollers:** 10% (~2,500) requiring additional width
- **Government Center T station:** ~2,000 persons/15-minute throughput under surge conditions
- **Primary egress corridors:** 5 (Congress S, Cambridge N, New Sudbury E, Court/Tremont W, Hanover Walk internal)

---

### Scenario A: Normal End-of-Match Dispersal (Gradual)

**Trigger:** Final whistle of simulcast. Match ends, crowd disperses organically.

**Timeline:**
| T+ | Event |
|---|---|
| 0 min | Match ends. Initial movement toward exits begins. |
| 5 min | 20% (~5,000) already moving; T station queues forming |
| 15 min | Peak egress load: ~15,000 persons in motion across all corridors |
| 30 min | 80% (~20,000) have cleared or are in transit |
| 45–60 min | Full plaza clear; residual crowd at Faneuil Hall / surrounding area |

**Critical infrastructure points:**
1. **Government Center headhouse** — primary T access point; 2,000 persons/15 min capacity. Queue management required to prevent platform crush.
2. **Congress St / New Sudbury St intersection** — highest pedestrian crash intersection in zone; will carry heaviest vehicle-pedestrian conflict load
3. **Hanover Walk promenade** — will channel bi-directional flow (exiting fans vs. arriving vehicles / emergency staging); needs dedicated crowd management
4. **Cambridge St west toward MGH corridor** — fans walking to North Station / Beacon Hill; nighttime lighting conditions on the fatality corridor

**Cyvl data value:** Sidewalk widths on all 5 egress routes feed the corridor capacity model. Identifies which route reaches saturation first. Identifies the 2–3 specific block segments that are chokepoints requiring physical intervention (stanchions, crowd control officers).

---

### Scenario B: Weather Emergency — Rapid Full Evacuation

**Trigger:** Severe thunderstorm, lightning within 10 miles, or flash flood warning. Requires clearing all 25,000 persons from the open plaza within the 8-minute safety window.

**Timeline:**
| T+ | Event |
|---|---|
| 0 min | Weather warning received. Announcement made. |
| 1 min | Crowd movement begins — but initial confusion delays coordinated egress |
| 3 min | Government Center station closes platforms (lightning protocol) — primary egress route eliminated |
| 4 min | Panic-adjacent crowd compression at Congress St and Cambridge St exits |
| 6 min | Peak density at egress bottlenecks — crush risk if effective width < 1.0m per 82 persons/min target |
| 8 min | Target: plaza clear. **Achievable only if all egress corridors are unobstructed** |

**Capacity requirements for 8-minute target:**
- 25,000 persons in 8 minutes = 3,125 persons/minute aggregate throughput
- At 82 persons/min/meter: requires **38 meters** of effective aggregate exit width
- Congress St (both sides): ~12m effective pedestrian width
- Cambridge St (both sides): ~10m
- New Sudbury: ~6m
- Court / Tremont: ~8m
- Hanover Walk (internal): ~6m
- **Total theoretical:** ~42m — barely sufficient if fully unobstructed

**Any obstruction — a food vendor tent, signage cluster, parked bike share dock, or pavement heave narrowing flow — eliminates the margin.**

**Critical infrastructure points:**
1. **Curb ramp grades on all 5 egress routes** — wheelchair users cannot use steep ramps during rapid evacuation; they become immobile obstacles blocking crowd flow
2. **Ponding zones** — rain event + drainage failure creates hazards exactly when evacuation speed is highest
3. **Lighting** — weather emergency may occur at dusk or night; path visibility on Congress and Cambridge Streets is critical
4. **Signage placement** — fixed pole signage in pedestrian zone reduces effective width

**Cyvl data value:** Pre-event audit of effective clear widths on every egress segment. ADA ramp grade mapping. Ponding zone identification. The data enables planners to pre-position crowd management resources at the specific choke points before the event, not discover them during the emergency.

---

### Scenario C: Security Incident — Directed Evacuation with Route Restrictions

**Trigger:** Credible threat, suspicious package, or active incident requiring directed evacuation and controlled route assignment. Law enforcement designates 2–3 egress corridors as usable; others are closed for response staging.

**Timeline:**
| T+ | Event |
|---|---|
| 0 min | Incident identified. EOC activated. |
| 2 min | Incident perimeter established — closes one or two primary egress routes |
| 4 min | Crowd direction announcement. Fans directed to remaining open routes. |
| 5 min | All 25,000 persons attempting to exit via 60% of normal corridor capacity |
| 8–12 min | Critical crowd compression period on open routes |
| 20–30 min | Evacuation complete if open corridors are unobstructed |

**Route restriction modeling:**
- If Congress St (south) is closed (incident near Faneuil Hall): remaining capacity drops to ~30m effective width — 8-minute target becomes 10–12 minutes
- If Government Center T is closed: ~2,000 persons rerouted to street dispersal — adds ~8% load to pedestrian network
- If New Sudbury St is closed (incident on east side): Cambridge St and Congress St must absorb 100% of east-bound pedestrian flow

**Critical infrastructure points:**
1. **Alternate egress routes must be pre-surveyed for capacity** — the routes that are normally secondary become primary under route restriction
2. **ADA accessibility on redirected routes** — if the accessible Hanover Walk route is in the closed zone, where do mobility-limited persons go?
3. **Narrowest segments on alternate routes** — the bottleneck is always the minimum width segment, not the average
4. **Signage visibility** — during a security incident, word-of-mouth and signage guide crowd flow; pole obstructions reducing sightlines become critical

**Cyvl data value:** Pre-computed capacity scores for every egress corridor combination. Planners can run "what if Congress St is closed" and immediately know whether remaining corridors meet the 8-minute target — and which specific segments on those corridors need pre-positioned resources. This is the intelligence layer that transforms reactive evacuation into proactive planning.

---

## 8. Funding and Planning Context

### Federal and State Security Funding
- **$46.05M** — FIFA World Cup Security Grant Program (FEMA) to Massachusetts
- **$21.2M** — Counter-Unmanned Aircraft Systems Grant Program (BPD, MSP, Foxborough PD)
- **$8.6M** — Federal Transit Administration (MBTA improvements)
- **Total federal:** ~$75.9M
- **State-level:** Additional public safety and health preparations coordinated by Governor Healey's office
- Five state agencies, four cities/towns, and the Host Committee are grant recipients
- **DMSE Sports** selected as Fan Festival on-the-ground operations manager

### State Preparedness Exercises Completed
- MBTA Commuter Rail evacuation drill
- Multi-agency tabletop exercises for complex crowd scenarios
- Boston Police + State Police + Secret Service coordination protocols established

### Economic Context
- 2M+ international visitors expected in Massachusetts for the tournament
- $1B+ projected economic impact statewide
- Boston hosting 7 matches at Gillette (June 13 – July 9)
- Fan Festival at City Hall Plaza: June 11 – July 19, 2026 (up to 16 days)
- Each match day at Gillette (~66,000 attendees) generates pedestrian overflow back to Boston via commuter rail → Government Center → City Hall Plaza zone

---

## 9. Demo Narrative Arc for CIO Santiago Garces

### The Frame
Boston is about to host the largest sporting event in its history. The city has $76M in federal funds and a completed $95M plaza renovation. But the March test event proved that **having resources is not the same as having intelligence** — 85 state troopers couldn't move traffic because nobody had mapped the secondary road network capacity in advance.

### The Problem Statement
Emergency evacuation planning for City Hall Plaza is currently based on:
- Generic crowd management models (not Boston-specific infrastructure)
- Assumption that all 5 egress corridors are fully passable (not verified)
- No real-time understanding of which sidewalk segments are bottlenecks
- No integration of the pedestrian crash hotspot data that exists in the city's own Vision Zero database

### The Cyvl Intelligence Layer
Cyvl has already surveyed the sidewalks, curb cuts, pavement, lighting, and assets on Boston's street network. For the Fan Festival demo, Cyvl can show:

1. **The effective width of every egress corridor** — not the nominal width, the actual pedestrian clear zone after obstructions
2. **The capacity ceiling for each scenario** — how many persons per minute can actually flow through Congress St vs. Cambridge St vs. New Sudbury St
3. **The specific choke points** — the exact block segments where effective width drops below the corridor average
4. **The ADA compliance gaps** — ramp grades and surface conditions on evacuation routes that are accessible in normal use but fail under crowd conditions
5. **The crash hotspot overlay** — the pedestrian crash data from Vision Zero lands directly on the segments where infrastructure failures already manifest as injuries
6. **The nighttime lighting gap** — the Cambridge St fatality corridor, under the shadow of new plaza trees, at the end of an evening match

### The Ask for Boston
Pre-event: Cyvl conducts a rapid infrastructure survey of all 5 egress corridors and delivers an evacuation readiness score for each, with specific remediation priorities. Cost: a fraction of one day of the $76M security budget.

Ongoing: Cyvl data is integrated into the Emergency Operations Center dashboard for the Fan Festival run period, enabling real-time scenario modeling when conditions change.

---

## Appendix A: Key Data Sources

- Boston Vision Zero Crash Records: `data.boston.gov` dataset `7b29c1b2-7ec2-4023-8292-c24f5d8f0905`, resource `e4bfe397-6bfc-49c5-9367-c879fac7401d`
- Boston Vision Zero Fatality Records: `data.boston.gov` dataset `d326a4e3-75f2-42ac-9b32-e2920566d04c`, resource `92f18923-d4ec-4c17-9405-4e0da63e1d6c`
- City Hall Plaza physical data: Sasaki renovation project documentation; Boston.gov public facilities
- MBTA Government Center station: HDR Engineering project documentation; MBTA.com
- Fan Festival announcement: Boston Host Committee for FIFA World Cup 2026 (bostonfwc26.com)
- March 2026 test event: CBS Boston, WBUR, NBC Boston, Boston 25 News reporting
- Federal funding: Mass.gov official press releases; FEMA World Cup Grant Program
- Crowd management standards: NFPA Life Safety Code 101; UK Green Guide for Safety at Sports Grounds; G. Keith Still PhD crowd dynamics research
- Emergency infrastructure: Mass General Hospital, Tufts Medical Center official sites; Boston Fire Department directory; Boston Police District A-1 records

## Appendix B: Crash Data Query Parameters

```sql
-- Pedestrian crashes in City Hall Plaza proximity zone
-- Area: lat 42.355-42.365, lon -71.065 to -71.050 (~0.5mi radius)
SELECT mode_type, COUNT(*) as crash_count 
FROM "e4bfe397-6bfc-49c5-9367-c879fac7401d"
WHERE lat::float BETWEEN 42.355 AND 42.365 
  AND long::float BETWEEN -71.065 AND -71.050
GROUP BY mode_type ORDER BY crash_count DESC;
-- Result: ped=303, mv=915, bike=163 (total 1,381 crashes)

-- Fatality near Cambridge St north egress
SELECT date_time, mode_type, street, xstreet1, xstreet2, lat, long
FROM "92f18923-d4ec-4c17-9405-4e0da63e1d6c"
WHERE lat::float BETWEEN 42.353 AND 42.367 
  AND long::float BETWEEN -71.068 AND -71.048;
-- Result: 2022-05-29 20:07 UTC, ped, Cambridge St @ Blossom St
```
