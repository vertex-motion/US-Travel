# Lodging and Transport

## Tag Map

Tags: planning-notes

Use the tag column to decide what can feed the HTML dashboard. Sync rows tagged `current-plan`, `traveler-notes`, or `to-confirm`. Do not sync rows tagged `planning-notes`, `sources`, `constraints`, or `fallback`.

## Lodging Strategy

| Tags | Rule or note | Detail |
| --- | --- | --- |
| constraints | Hotel budget | Target comfortable, well-located family hotels at USD $200-$250 per night. Do not exceed $250 per night without explicit approval. |
| constraints | Room setup | Prefer one confirmed room or suite that fits all four travelers. Two-room setups are too expensive and should be a fallback only if no acceptable one-room option exists. |
| planning-notes | Location priority | Book locations before optimizing hotel brand. The right base saves more family energy than a more famous hotel in the wrong neighborhood. |
| current-plan | Gateway shape | Use LAX as the start and end airport for the selected closed-circle plan. |
| current-plan | Flight anchors | UA 842 arrives at LAX at 6:10 am on Sunday, June 28, 2026. UA 839 departs LAX at 10:45 pm on Saturday, July 18, 2026, and arrives SYD at 7:00 am on Monday, July 20, 2026. |
| current-plan | Rental car anchor | Rental car is booked from Los Angeles International Airport on Sunday, June 28, 2026 at 8:00 am to Los Angeles International Airport on Saturday, July 18, 2026 at 8:00 pm. |
| traveler-notes | Final Los Angeles night | Keep the final Los Angeles night practical. The final hotel is in Pasadena, so prioritize a large Day 21 LAX traffic buffer over sightseeing. |
| traveler-notes, to-confirm | Las Vegas total cost | Treat the booked Strip hotel as the baseline and confirm the full stay cost, not only the headline room rate. Include resort fees, taxes, parking, pool access, and any extra-person fees. |
| to-confirm | Common hotel checks | Confirm crib/rollaway policy, parking height, resort fees, parking fees, family occupancy, and cancellation terms before arrival. |
| constraints | Public repository privacy | Keep hotel names, exact addresses, prices, confirmation numbers, guest names, membership numbers, phone numbers, private contact details, payment details, and booking references out of this public repository. |

## Current Lodging Bases

| Tags | Base | Nights | Current plan | Traveler notes | To confirm |
| --- | --- | ---: | --- | --- | --- |
| current-plan, traveler-notes, to-confirm | Los Angeles arrival | 6 | Booked Pasadena-area hotel from Sunday, June 28 to Saturday, July 4, 2026, with 3:00 pm check-in and 12:00 pm checkout. | Starts the closed circle, supports recovery, and gives the family a fuller LA sample before driving north. Pasadena improves Griffith, Kidspace, and east/central LA access while making beach / Westside days more drive-dependent. | Early check-in or luggage storage, parking cost, family occupancy, cancellation terms, and private total cost. |
| current-plan, traveler-notes, to-confirm | Central Coast / Route 1 overnight | 1 | Booked Santa Maria hotel from Saturday, July 4 to Sunday, July 5, 2026. | Splits the Los Angeles-to-Monterey coast drive after removing Santa Barbara and gives the family a confirmed July 4 bed. Santa Maria is practical for US-101 and Santa Ynez / Pismo-area routing, but it is south of Cambria / San Simeon. | Check-in time, parking, family occupancy, cancellation terms, taxes/fees, private total cost, and current Caltrans status before any full Highway 1 / Big Sur routing. |
| current-plan, traveler-notes, to-confirm | Monterey / Carmel | 2 | Booked Monterey-area hotel from Sunday, July 5 to Tuesday, July 7, 2026. | Protects the aquarium day and supports Pacific Grove, Carmel, 17-Mile Drive, and a short Big Sur reach if timing is easy. With only two nights, avoid adding a full Big Sur day unless conditions and energy are excellent. | Parking, family occupancy, resort/amenity fees, cancellation terms, taxes/fees, checkout time, and private total cost. |
| current-plan, traveler-notes, to-confirm | San Francisco / Bay Area | 6 | Booked Mountain View hotel from Tuesday, July 7 to Monday, July 13, 2026, with check-in at 4:00 pm and checkout at 11:00 am. | Supports Golden Gate, Presidio, Stanford-area downtime, Silicon Valley tech stops, and two extra Bay Area buffer nights before Yosemite. Mountain View improves Stanford / Silicon Valley logistics, while San Francisco / Golden Gate remains a deliberate day trip. | Final taxes/fees, cancellation terms, free parking, free WiFi, family occupancy, parking details, and any incidentals. |
| current-plan, traveler-notes, to-confirm | Yosemite / Mammoth Lakes | 1 | Booked Mammoth Lakes hotel from Monday, July 13 to Tuesday, July 14, 2026, with check-in from 4:00 pm and checkout until 11:00 am. | Supports the July 13 plan: drive from the Bay Area in the morning, explore Yosemite Valley, cross Tioga Road, and sleep on the east side before Death Valley. This stages July 14 well, but makes July 13 long and dependent on Tioga Road, smoke, traffic, and weather. | Parking, check-in process, property fees, family occupancy, cancellation deadline, private total cost, and whether any additional local fees apply. |
| current-plan, traveler-notes, to-confirm | Las Vegas | 3 | Booked Las Vegas Strip hotel from Tuesday, July 14 to Friday, July 17, 2026, with 3:00 pm check-in and 11:00 am checkout. | First-visit Strip landmarks, pool/rest time, indoor attractions, and heat-aware finale. The booking confirms one suite for two adults and two children and puts the family close to first-visit Strip landmarks. | Final folio, resort fee and tax, parking fees, pool access, quiet-room request, cancellation terms, smoky casino paths, summer heat logistics, extra-person fees, and any incidental holds. |
| current-plan, traveler-notes, to-confirm | Los Angeles departure | 1 | Booked Pasadena-area hotel from Friday, July 17 to Saturday, July 18, 2026, with 3:00 pm check-in and 12:00 pm checkout. | Protects the LAX international departure after the Las Vegas drive while reusing a known family setup. Pasadena is not airport-adjacent, so Day 21 stays logistics-first. | $35/night parking, final folio, family occupancy, housekeeping preference, checkout timing, incidentals, and a large Day 21 LAX drive buffer. |

## Fallback Lodging

| Tags | Fallback | When to use | Action |
| --- | --- | --- | --- |
| fallback | Bakersfield / Tehachapi midpoint | Use only if Tioga Road, US-395, CA-190, Death Valley conditions, heat, smoke, weather, fatigue, or family energy makes the direct Mammoth-Lakes-to-Las-Vegas route unsafe or too long. | Keep Bakersfield, Tehachapi, or another practical CA-99 / CA-58 corridor hotel as a cancellable fallback. Do not book unless route checks show the direct transfer is unsafe or too tiring. |

## Transport Plan

| Tags | Step | Plan |
| --- | ---: | --- |
| current-plan | 1 | Fly Sydney to Los Angeles on UA 842, arriving LAX at 6:10 am on Sunday, June 28, 2026. |
| current-plan, to-confirm | 2 | Pick up the booked rental car at Los Angeles International Airport at 8:00 am on Sunday, June 28, 2026, after clearing immigration and collecting luggage. |
| current-plan, traveler-notes | 3 | Drive from LAX to the booked Pasadena-area arrival hotel and keep the first day low-driving because it follows the long-haul flight. Use luggage storage or a low-effort local plan until 3:00 pm check-in if needed. |
| current-plan | 4 | Use the car for the Central Coast / Route 1 overnight, the booked Monterey-area stay, the booked six-night Mountain View / Bay Area stay, Yosemite, the direct Death Valley transfer, the booked Las Vegas Strip stay, and the return to Los Angeles. |
| current-plan, traveler-notes, to-confirm | 5 | During the Mountain View / Bay Area stay, use the car for Stanford / Mountain View / Cupertino / San Jose tech stops, while deciding whether the Golden Gate / Presidio day suits self-driving, Caltrain plus rideshare, or another planned transfer. |
| current-plan, to-confirm | 6 | On Day 16, drive from the Bay Area to Yosemite Valley, explore Yosemite, cross Tioga Road if conditions are safe, and sleep at the booked Mammoth Lakes hotel. |
| current-plan, traveler-notes, to-confirm | 7 | On Day 17, drive Mammoth Lakes to the booked Las Vegas Strip hotel through Death Valley only if US-395 / CA-190, Death Valley road status, weather, smoke, heat, and family energy are acceptable. Keep Death Valley stops short and paved. |
| fallback | 8 | Restore Bakersfield / Tehachapi as a midpoint fallback if the direct Mammoth-Lakes-to-Las-Vegas route is unsafe or too tiring. |
| current-plan | 9 | Drive Las Vegas to the booked Pasadena-area final Los Angeles hotel on Day 20. |
| current-plan, traveler-notes, to-confirm | 10 | Return the car at Los Angeles International Airport at 8:00 pm on Saturday, July 18, 2026, allowing enough buffer for fuel, luggage, rental return, terminal transfer, and international check-in. |
| current-plan | 11 | Fly Los Angeles to Sydney on UA 839 on Day 21, departing LAX at 10:45 pm on Saturday, July 18 and arriving SYD at 7:00 am on Monday, July 20. |

## Rental Car and Operating Checks

| Tags | Area | Requirement or check |
| --- | --- | --- |
| current-plan | Booking | Rental car is booked LAX-to-LAX from June 28, 2026 at 8:00 am to July 18, 2026 at 8:00 pm. |
| to-confirm | Vehicle fit | Confirm vehicle class and luggage space for four passengers, pram, and long-haul luggage before pickup. |
| to-confirm | Child seat | Confirm child seat requirements for the younger child before pickup. Bring or rent an approved seat. |
| to-confirm | Driving documents | Confirm whether the rental company requires an International Driving Permit for an Australian license. |
| to-confirm | Drivers | Add a second authorized driver if both adults may drive. |
| constraints | Rental privacy | Keep provider, price, and booking reference out of this public repository. |
| to-confirm | First hotel parking | Because the first hotel is in the Pasadena area, confirm parking cost and height/entry details before arrival. |
| traveler-notes, to-confirm | Central Coast move | For the July 4 coast move, confirm the booked Santa Maria hotel check-in time, parking, room occupancy, and cancellation terms. Keep Day 8 flexible because Santa Maria makes a full Highway 1 / Big Sur routing more timing-sensitive than Cambria or San Simeon. |
| to-confirm | Monterey transfer | Confirm the booked Monterey-area hotel parking, room occupancy, resort/amenity fees, cancellation terms, and checkout time before the July 7 Bay Area transfer. |
| traveler-notes, to-confirm | Bay Area transport | Use the booked Mountain View hotel as the Bay Area base. Confirm free parking and compare self-driving against Caltrain/rideshare for the Golden Gate day if San Francisco parking or traffic is expensive. |
| to-confirm | Yosemite / Mammoth Lakes route | Before the July 13 Yosemite / Mammoth Lakes day, confirm Tioga Road, Yosemite Valley roads, smoke, weather, and Mammoth Lakes check-in timing. |
| traveler-notes, to-confirm | Death Valley transfer | Before the July 14 transfer, confirm US-395, CA-190, Death Valley road status, weather, smoke, and heat. Carry extra water, snacks, fuel margin, and keep stops paved and short. |
| fallback | Midpoint option | Keep a cancellable Bakersfield / Tehachapi midpoint option only as a fallback if the direct Mammoth-Lakes-to-Las-Vegas route looks unsafe or too tiring. |
| to-confirm | Full vehicle logistics | Confirm parking fees at each hotel, toll handling, fuel policy, additional driver fees, and whether the booked Las Vegas Strip hotel has self-parking that fits the vehicle. |

## Airport and Transfer Notes

| Tags | Moment | Traveler note | To confirm |
| --- | --- | --- | --- |
| current-plan, traveler-notes, to-confirm | LAX arrival | UA 842 arrives at 6:10 am on June 28. The booked rental car pickup is 8:00 am at Los Angeles International Airport. If immigration, luggage, or rental counter timing slips, keep the arrival day flexible. | Arrival-day timing, rental counter timing, and luggage buffer. |
| current-plan, to-confirm | First hotel arrival | Pasadena-area hotel check-in is 3:00 pm on June 28 and checkout is 12:00 pm on July 4. | Early luggage storage, parking, room occupancy, and cancellation terms. |
| current-plan, to-confirm | Central Coast arrival | Santa Maria hotel is booked for July 4-5. | Check-in time, parking, room occupancy, cancellation terms, taxes/fees, and private total cost. |
| current-plan, to-confirm | Monterey arrival | Monterey-area hotel is booked for July 5-7. | Check-in time, checkout time, parking, room occupancy, resort/amenity fees, cancellation terms, taxes/fees, and private total cost. |
| current-plan, to-confirm | Bay Area arrival | Mountain View hotel is booked for July 7-13, with check-in at 4:00 pm and checkout at 11:00 am. | Final taxes/fees, cancellation terms, free parking, free WiFi, family occupancy, and any incidentals. |
| current-plan, to-confirm | Mammoth Lakes arrival | Mammoth Lakes hotel is booked for July 13-14, with check-in from 4:00 pm and checkout until 11:00 am. | Parking, check-in process, property fees, family occupancy, and any incidentals. |
| current-plan, to-confirm | Las Vegas arrival | Las Vegas Strip hotel is booked for July 14-17, with 3:00 pm check-in and 11:00 am checkout. | Resort fee and tax, parking, pool access, quiet-room request, cancellation terms, and final folio. |
| current-plan, to-confirm | Final Los Angeles arrival | Pasadena-area hotel is booked for July 17-18, with 3:00 pm check-in and 12:00 pm checkout. | $35/night parking, family occupancy, housekeeping preference, final folio, and any incidentals. |
| current-plan, traveler-notes, to-confirm | LAX departure | UA 839 departs at 10:45 pm on July 18. The booked rental car return is 8:00 pm at Los Angeles International Airport. Leave a large traffic buffer for fuel, rental car return, luggage, terminal transfer, and international check-in. | Terminal, luggage timing, fuel policy, rental return buffer, and check-in buffer. |
| traveler-notes | Final-day option | Book late checkout or a day room rather than filling the departure day with sightseeing. | None unless the hotel gap before airport check-in is too long. |
| planning-notes | Unselected gateways | SFO and LAS are no longer selected gateways. | None. |

## Sources

Tags: sources

| Fact or decision supported | Source | Original page | Accessed | Status |
| --- | --- | --- | --- | --- |
| LAX is the selected closed-circle gateway because it has the strongest Sydney flight market among the candidate start/end cities. | Local comparison file | [work/closed-circle-start-city-comparison.md](work/closed-circle-start-city-comparison.md) | 2026-05-15 | Current planning decision |
| Confirmed flights are United UA 842 SYD-LAX on June 28, 2026 and United UA 839 LAX-SYD departing July 18, 2026 and arriving July 20, 2026. | Traveler booking | User-provided ticket details | 2026-05-15 | Booked; seat assignments intentionally omitted |
| Rental car is booked from Los Angeles International Airport on June 28, 2026 at 8:00 am to Los Angeles International Airport on July 18, 2026 at 8:00 pm. | Traveler booking | User-provided rental booking details | 2026-05-31 | Booked; provider, price, and booking reference intentionally omitted |
| First Los Angeles hotel is booked in the Pasadena area from June 28 to July 4, 2026, with 3:00 pm check-in and 12:00 pm checkout. | Traveler booking | User-provided first hotel booking details | 2026-05-31 | Booked; exact hotel name, address, price, and booking reference intentionally omitted |
| Central Coast hotel is booked in Santa Maria from July 4 to July 5, 2026. | Traveler booking | User-provided Central Coast hotel booking details | 2026-06-02 | Booked; exact hotel name, address, price, and booking reference intentionally omitted |
| Monterey-area hotel is booked from July 5 to July 7, 2026. | Traveler booking | User-provided Monterey hotel booking details | 2026-06-02 | Booked; exact hotel name, address, price, and booking reference intentionally omitted |
| Bay Area hotel is booked in Mountain View from July 7 to July 13, 2026, with check-in at 4:00 pm and checkout at 11:00 am. Rate notes list free parking and free WiFi. | Traveler booking | User-provided Bay Area hotel booking details | 2026-06-06 | Booked; exact address, confirmation number, guest name, membership number, phone, and contact details intentionally omitted |
| Mammoth Lakes hotel is booked from July 13 to July 14, 2026, with check-in from 4:00 pm and checkout until 11:00 am. | Traveler booking | User-provided Mammoth Lakes hotel booking details | 2026-06-06 | Booked; booking PIN, exact address, payment details, contact details, and booking reference intentionally omitted |
| Las Vegas Strip hotel is booked from July 14 to July 17, 2026, with 3:00 pm check-in and 11:00 am checkout, in one Luxury 2 Queen suite for two adults and two children. | Traveler booking | User-provided Las Vegas hotel booking details | 2026-06-07 | Booked; confirmation number, guest name, membership number, exact address, phone, and private contact details intentionally omitted |
| Final Los Angeles hotel is booked in the Pasadena area from July 17 to July 18, 2026, with 3:00 pm check-in and 12:00 pm checkout, in one room for two adults and two children. | Traveler booking | User-provided final Los Angeles hotel booking details | 2026-06-07 | Booked; confirmation number, guest name, membership number, exact address, phone, and private contact details intentionally omitted |
| Qantas lists direct Sydney service with Los Angeles and San Francisco, and Sydney-Las Vegas seasonal service beginning after this trip window. | Qantas | [International flight routes](https://www.qantas.com/en-us/where-we-fly/international-flight-routes) | 2026-05-15 | Current; verify before booking |
| United displayed Sydney-Los Angeles round-trip economy fare examples from AU$1,228 before booking; keep only as a historical planning anchor. | United Airlines | [Sydney to Los Angeles flights](https://www.united.com/en-au/flights-from-sydney-to-los-angeles) | 2026-05-15 | Historical pre-booking fare anchor |
| LAX has FlyAway and Metro/LAX connector transit options. | Los Angeles World Airports | [LAX transit](https://www.lawa.org/commutelax/transit) | 2026-05-15 | Current; choose transfer after hotel base |
| Las Vegas has family-friendly hotel, pool, free-sight, indoor attraction, and dining options, but selected lodging and attraction terms need current checks. | Visit Las Vegas | [Things to Do in Vegas With Kids](https://www.visitlasvegas.com/experience/post/things-to-do-in-las-vegas-with-kids/) | 2026-05-13 | Current; verify selected hotel terms |
| Yosemite Valley Lodge should be checked first only if it can fit the hotel cap, because location materially reduces daily driving. | Yosemite Hospitality | [Yosemite Valley Lodge](https://www.travelyosemite.com/lodging/yosemite-valley-lodge/) | 2026-05-08 | Needs live rate quote against $250/night cap |
| Forestiere Underground Gardens offers a one-hour guided Fresno tour and strongly recommends reservations, with extra arrival time needed because of nearby high-speed-rail construction. | Forestiere Underground Gardens | [Guided tour and visitor information](https://undergroundgardens.com/) | 2026-05-31 | Current; route-dependent midpoint stop |
| CALM Zoo is a Bakersfield family wildlife option, open Tuesday-Sunday 9am-4pm and mostly outdoors. | CALM Zoo | [Visit](https://calmzoo.org/visit/) | 2026-05-31 | Current; use only if heat and timing work |
| Kern County Museum is a Wednesday-Sunday 9am-4pm Bakersfield history option with historic buildings and regional exhibits. | Kern County Museum | [Home / hours](https://kerncountymuseum.org/) | 2026-05-31 | Current; re-check hours before visit |
| Tehachapi is a route-adjacent town / rail-engineering stop on the CA-58 corridor. | Visit Tehachapi | [Official visitor site](https://www.visittehachapi.com/) | 2026-05-31 | Current; keep as a brief stop |
| Yosemite current conditions show Yosemite Valley roads and Tioga Road open, but roadwork and condition changes still require re-checks before the July 13 Yosemite Valley / Mammoth Lakes crossing and July 14 Death Valley transfer. | National Park Service | [Yosemite current conditions](https://www.nps.gov/yose/planyourvisit/conditions.htm) | 2026-06-05 | Current; re-check before travel |
| Tioga Road opened for the 2026 season on May 15, 2026, with limited services along Tioga Road. | National Park Service | [Tioga and Glacier Point roads update](https://www.nps.gov/yose/planyourvisit/tioga.htm) | 2026-06-05 | Current; re-check before July 14 |
| Caltrans provides current California highway conditions and should be checked for CA-120, US-395, CA-190, and I-15 before the Mammoth-Lakes-to-Las-Vegas via Death Valley transfer. | Caltrans | [California highway conditions](https://roads.dot.ca.gov/) | 2026-06-05 | Current; re-check before and during travel |
| Death Valley NPS warns that summer temperatures can reach 130 F / 54 C, advises against hiking in lower elevations when hot, and says to check alerts, road status, and weather before visiting. | National Park Service | [Death Valley safety](https://www.nps.gov/deva/planyourvisit/safety.htm) | 2026-06-05 | Current; keep July 14 as paved transit only |
| Death Valley road status can change quickly; the current conditions page lists paved-road cautions and links to Caltrans / Sierra Nevada pass checks. | National Park Service | [Death Valley alerts and conditions](https://www.nps.gov/deva/planyourvisit/conditions.htm) | 2026-06-05 | Current; re-check before July 14 |
| Highway 1 is usable but not frictionless: Caltrans reports one-way controlled traffic north of Big Sur through July 31, 2026 and near Jamala Road in Santa Barbara County due to a washout. | Caltrans | [Highway 1 road status](https://roads.dot.ca.gov/?roadnumber=1) | 2026-06-01 | Current; re-check before travel |
