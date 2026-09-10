# MASTER EXECUTION PROMPT — NORTH DAKOTA NORTHERN LIGHTS LIVE

Build and release **North Dakota Northern Lights Live** end to end as an independent Vercel/GitHub product. Michigan is the reference implementation only. Do not edit `izworskic/chrisizworski-com`, `/northern-lights-michigan/`, Michigan `/api/aurora`, parser files, routing, canonical metadata, or create a Michigan runtime dependency. Any Michigan write is a -100 hard veto.

## User decision
First viewport must answer: **Is it worth going out tonight in North Dakota, where should I go, when is the best window, and what could ruin the view?** Show verdict, 0–100 Viewing Score, selected region, local NOAA OVATION, NWS clouds, peak 24h Kp, best dark window, and three-night outlook. The score is a planning index, not a sighting probability and never displayed with `%`.

## Data and truth
Use NOAA SWPC Kp forecast/current Kp, OVATION Aurora 30-Minute Forecast, real-time solar wind magnetic field/speed, NWS sky cover/hourly darkness, and USNO moon context. Use soft-failure handling. Missing values remain null. Never turn missing data into zero. Never call Kp or OVATION a local probability. Suppress score without useful darkness; no numeric score when both Kp and OVATION are unavailable.

## North Dakota regions
Use `config/state.js` as truth: Turtle Mountains/International Peace Garden, Pembina/northeast, Minot/north-central, Devils Lake, Theodore Roosevelt/Badlands, Bismarck/central, Fargo/southeast. Regional planning Kp is approximate travel guidance, not a hard physical boundary.

## Score
OVATION 40, regional Kp fit 25, NWS clouds 20, darkness 8, southward Bz 4, solar-wind speed 3, bright-moon penalty up to 5; clamp 0–100. Labels: Strong viewing setup / Possible — worth checking / Watch conditions / Unlikely right now / Aurora signal, poor sky / No useful darkness / Live space-weather unavailable.

## UX
Michigan-like editorial shell without copying Michigan text: light paper body, restrained green type, dark aurora hero, circular score gauge, region selector, three decision factors, three-night strip, current Kp/solar-wind/moon cards, North Dakota regional outlook, source transparency, mobile-first layout.

## SEO
Canonical `https://chrisizworski.com/national-tools/aurora/north-dakota/`; unique metadata and WebApplication/BreadcrumbList schema; page index/follow; API `X-Robots-Tag: noindex, nofollow`; state-specific content. Target northern lights North Dakota tonight, aurora forecast North Dakota, International Peace Garden aurora, Turtle Mountains northern lights, Theodore Roosevelt northern lights, best place to see northern lights North Dakota.

## Reliability and tests
Static HTML under 150 KB; `s-maxage=300, stale-while-revalidate=900`; ~8 s upstream timeout; no paid API, DB, Replit, or Michigan runtime dependency. Test Kp headers, OVATION longitude normalization, sky intervals, null preservation, score clamps, darkness suppression, no-score missing signals, unique valid regions/default, canonical, score-not-percent, and API noindex.

## Value function >=92/100
Decision clarity 20; data truth/reliability 20; state specificity 15; repeat value 10; mobile/accessibility 10; performance/resilience 10; SEO 10; source transparency 5.

## Loss
Michigan write -100; false probability -50; missing→zero -40; broken region/API -35; stale-as-live -35; generic clone -25; tests/build failure -25; bad canonical -25; weak mobile first view -20.

Execute implementation, tests, build, Git commit, Vercel deployment, smoke tests, canonical/API header checks, then verify Michigan SHA unchanged before hub linking.
