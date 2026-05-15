# Closed-Circle Start City Comparison

Accessed: 2026-05-15

## Recommendation

Use **Los Angeles (LAX) as the default start and end city** for a closed-circle version of the trip.

Why:

- LAX has the strongest Sydney flight market among the three candidates.
- LAX has the best chance of cheaper fares because it has more nonstop airline competition.
- A LAX loop can include Los Angeles, the coast, San Francisco, Yosemite, and Las Vegas without forcing the family to backtrack all the way from Las Vegas to San Francisco.
- Returning the rental car to the same airport should reduce one-way rental risk compared with the previous SFO-to-LAS open-jaw plan.

Use **San Francisco (SFO)** only if flights are close in price and the family wants the easiest jet-lag arrival. Use **Las Vegas (LAS)** only if an unusually good fare appears or the family wants the trip to feel like a Southwest loop first and a California coast trip second.

## Scorecard

Scores are for this family and this itinerary, not for the airports in general.

| Candidate | Overall fit | Flight strength from Sydney | Airport quality for this trip | Ease into city | Closed-loop route fit | Cost risk | Best use |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | --- |
| Los Angeles / LAX | 1 | 1 | 3 | 3 | 1 | 1 | Default closed-circle gateway. |
| San Francisco / SFO | 2 | 2 | 1 | 2 | 3 | 2 | Softer arrival, but awkward loop closure. |
| Las Vegas / LAS | 3 | 3 | 2 | 1 | 2 | 3 | Easy local airport, weak July 2026 Australia access. |

## Flight Comparison

| Start/end city | Sydney flight position | Current fare signal | Interpretation |
| --- | --- | --- | --- |
| LAX | Strongest. FlightsFrom lists four airlines with nonstop LAX-SYD service: American, Delta, Qantas, and United. Qantas also lists direct Los Angeles-Sydney service. | United showed Sydney-Los Angeles round-trip economy from **AU$1,228** on a fare page viewed today. | Best chance of lower fares and schedule flexibility. Quote first. |
| SFO | Good. Qantas and United operate nonstop Sydney-San Francisco service. | United showed Sydney-San Francisco round-trip economy from **AU$1,428** for July 2026 on a fare page viewed today. | Still viable, but less competition than LAX and a weaker closed-loop shape. |
| LAS | Weak for July 2026. Qantas announced direct Sydney-Las Vegas service only from late 2026 into March 2027, after this trip window. July 2026 needs a connection. | United showed Sydney-Las Vegas round-trip economy from **AU$1,359** on selected 2026 dates, but this is not a nonstop Australia route. | Possible, but connection risk and timing make it a poor default. |

Do not treat these fare anchors as bookable quotes. United states that fare availability can change and that displayed economy fares may be Basic Economy. Run live quotes for all four travelers before booking.

## Airport and City Transfer Comparison

| City | What works | What hurts | Family judgment |
| --- | --- | --- | --- |
| LAX | Best long-haul competition. Good rental-car ecosystem. Works well as the loop anchor because Las Vegas is only a reasonable final drive away. LAX FlyAway runs to Union Station and Van Nuys, and Metro connects via LAX/Metro Transit Center plus terminal shuttle. | LAX is the most stressful airport of the three. Transfers depend on traffic, terminal shuttles, and hotel location. A first-night hotel should be chosen carefully. | Best for money and route shape; not best for comfort. |
| SFO | Easiest pleasant arrival. BART connects SFO with downtown San Francisco, and the current plan already assumes no car at the start. SFO is a strong international airport with nonstop Sydney service. | A closed loop from SFO makes the end messy. After Las Vegas, the family must either drive a long desert/interstate return to SFO or remove Las Vegas from the finale. | Best arrival experience; weaker closed-circle plan. |
| LAS | Airport is very close to the Strip, and arrival/departure logistics are simple. A Las Vegas start can avoid ending the trip in July desert heat if the route goes west immediately. | No July 2026 nonstop Sydney service. Starting in Las Vegas creates a hot, possibly tiring arrival for a family with a 2-year-old. The route becomes a Southwest-first loop rather than a classic West Coast first trip. | Best local airport transfer; worst international gateway. |

## Route Shapes

### Best Closed Loop: LAX Start and End

Use this as the planning default:

| Leg | Base | Nights | Notes |
| --- | --- | ---: | --- |
| Arrival recovery | Los Angeles / Santa Monica or Westside | 3 | Recover from Sydney flight; avoid heavy cross-city sightseeing on Day 1. |
| Northbound coast | Santa Barbara / Central Coast / Monterey | 4 | Split the coast so the family is not forced into one huge coastal transfer. |
| Bay Area | San Francisco | 3 | Keep car parking minimal; consider returning or parking the car depending on hotel costs. |
| Sierra | Yosemite area | 3 | Book first because lodging is still the hardest constraint. |
| Desert finale | Las Vegas | 3 | Keep July heat controls from the current plan. |
| Loop closure | Return to LAX | 1 transfer day or late final drive | Drive Las Vegas-Los Angeles, sleep near LAX or return car before the outbound flight. |

This keeps the recognizable West Coast arc and makes the last long drive manageable.

### Softer Arrival: SFO Start and End

Use only if SFO fares beat LAX or the family strongly prefers the San Francisco arrival:

| Leg | Shape | Problem |
| --- | --- | --- |
| SFO -> Yosemite -> Monterey -> Santa Barbara -> LA -> Las Vegas -> SFO | Keeps the current route order almost intact. | The final Las Vegas-to-SFO closure is too long and not rewarding enough for this family. It risks turning the last part of the trip into a road chore. |
| SFO -> coast -> LA -> Las Vegas -> Yosemite -> SFO | More circular on a map. | Yosemite after Las Vegas means a long hot transfer and loses the clean California-to-Vegas finale. |

### Southwest Loop: LAS Start and End

Use only as a fallback:

| Leg | Shape | Problem |
| --- | --- | --- |
| LAS -> LA -> coast -> SF -> Yosemite -> LAS | The map closes neatly and LAS is easy locally. | It depends on connecting flights from Sydney in July 2026 and creates a long Yosemite-to-Las Vegas return. It also starts the trip in July desert heat. |

## Suggested Decision Rule

1. Quote **SYD-LAX-SYD** for July 1-20, 2026 first.
2. Quote **SYD-SFO-SYD** second, only to see whether the arrival comfort is worth the route penalty.
3. Quote **SYD-LAS-SYD** third, but treat it as a fallback unless it is materially cheaper and has family-safe connection times.
4. If LAX is within about **AU$300-AU$500 per person** of the cheapest option, choose LAX because the route and rental-car simplicity are worth it.
5. If SFO is cheaper by more than that, compare whether the extra final driving or route reshuffle cancels the airfare saving.
6. If LAS is cheapest, check connection time, arrival hour, stroller/luggage handling, and whether the family is comfortable starting in Las Vegas heat.

## Implementation Status

The LAX closed-circle recommendation has been promoted into the canonical trip files.

| Affected area | Impact | Proposed change | User decision needed |
| --- | --- | --- | --- |
| `02-current-plan-options.md` | Current plan now uses LAX as the selected closed-circle gateway. | Done. | Confirm after live quotes. |
| `04-daily-itinerary.md` | Day order now follows LAX -> Santa Barbara -> Monterey -> San Francisco -> Yosemite -> Las Vegas -> LAX. | Done. | Review the Yosemite-to-Las-Vegas transfer. |
| `05-lodging-transport.md` | Rental car pickup/return and first/last hotel strategy now center on LAX. | Done. | Decide Day 1 vs. Day 4 car pickup after hotel quotes. |
| `06-budget.md` | Airfare and rental-car assumptions now use SYD-LAX-SYD and LAX-to-LAX as baselines. | Done. | Run live quote round. |
| `07-booking-checklist.md` | Flight quote tasks now prioritize the LAX closed loop. | Done. | Confirm dates before bookings. |

## Sources

| Fact supported | Source | URL | Accessed | Status |
| --- | --- | --- | --- | --- |
| Qantas lists direct Sydney service with Los Angeles and San Francisco, and Sydney-Las Vegas seasonal service beginning after this trip window. | Qantas | https://www.qantas.com/en-us/where-we-fly/international-flight-routes | 2026-05-15 | Current; verify before booking |
| Qantas Sydney-Los Angeles flight page lists direct flight time around 13h45m. | Qantas | https://www.qantas.com/au/en/flight-deals/flights-from-sydney-to-los-angeles.html/syd/lax/business | 2026-05-15 | Current; verify exact dates |
| LAX-SYD has four nonstop airlines listed by schedule aggregator. | FlightsFrom | https://www.flightsfrom.com/LAX-SYD | 2026-05-15 | Use for route comparison only; quote airlines directly |
| SYD-SFO has Qantas and United nonstop service listed by schedule aggregator. | FlightsFrom | https://www.flightsfrom.com/SYD-SFO | 2026-05-15 | Use for route comparison only; quote airlines directly |
| United displayed Sydney-Los Angeles round-trip economy fares from AU$1,228. | United Airlines | https://www.united.com/en-au/flights-from-sydney-to-los-angeles | 2026-05-15 | Volatile fare anchor; not a booking quote |
| United displayed Sydney-San Francisco round-trip economy fares from AU$1,428 for July 2026. | United Airlines | https://www.united.com/en-au/flights-from-sydney-to-san-francisco | 2026-05-15 | Volatile fare anchor; not a booking quote |
| United displayed Sydney-Las Vegas round-trip economy fare examples from AU$1,359. | United Airlines | https://www.united.com/en-au/flights-from-sydney-to-las-vegas | 2026-05-15 | Volatile fare anchor; not a booking quote |
| Qantas announced Sydney-Las Vegas direct seasonal service from the end of 2026, after the July 2026 trip. | Qantas Agency Connect | https://www.qantas.com/agencyconnect/us/en/agency-news/february-2026/qantas-new-route-las-vegas.html | 2026-05-15 | Current; not useful for July 2026 |
| SFO has BART connection to downtown San Francisco. | BART | https://www.bart.gov/guide/airport/sfo | 2026-05-15 | Current |
| LAX has FlyAway and Metro/LAX connector transit options. | Los Angeles World Airports | https://www.lawa.org/commutelax/transit | 2026-05-15 | Current |
| LAS is two miles from the Las Vegas Strip and 15 miles from downtown. | Harry Reid International Airport | https://www.lasairport.com/Directions | 2026-05-15 | Current |
| Existing route constraints, family pace, and previous open-jaw plan. | Repository planning files | `01-trip-purpose.md`, `02-current-plan-options.md`, `05-lodging-transport.md` | 2026-05-15 | Local planning source |
