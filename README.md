# CarbonQuest: Your Climate Twin

An interactive carbon footprint simulator that shows how everyday choices change your yearly emissions, and how much real actions could save by 2050.

**Live demo:** [PASTE YOUR GITHUB PAGES LINK HERE]
**Track:** Coding Track | **Category:** Environment

## The problem

Most people have no idea how much CO₂ their lifestyle produces or which changes matter most. Existing calculators give a single number at the end. They do not let you explore "what if" choices or see a long-term pathway.

## What it does

- Live footprint (tonnes CO₂e per year) that updates as you move the sliders.
- The page colour shifts from cool to hot as your footprint rises.
- Planet grade (A to E) and a comparison against the India average, the world average and the 1.5°C-aligned level (about 2.3 t per person by 2030).
- Breakdown by travel, flights, home energy, food, and goods and waste.
- Seven real actions (transit, EV, rooftop solar, vegetarian days, fewer flights, buying less, composting) with the exact yearly saving for your profile.
- A projection chart to 2050: doing nothing versus your chosen actions.
- Four sample personas, climate badges, a copy-my-result button, light and dark mode.
- A "Run judge demo" button that plays through all features automatically.

## How it works

Emissions are calculated in the browser from simple activity-based formulas:

| Source | Formula (summary) |
|---|---|
| Travel | km per week × 52 × mode factor (kg per km) |
| Flights | short flights × 0.2 t + long flights × 1.6 t |
| Home energy | kWh per month × 12 × 0.71 kg per kWh ÷ people in home |
| Food | diet-based yearly estimate (vegan to meat-heavy) |
| Goods and waste | monthly spending factor + waste-habit estimate |

Action savings are computed from your own inputs, so they change when you change your profile. The 2050 pathway applies chosen actions by 2031 and then assumes the grid gets 3% cleaner each year.

## Tech stack

Plain HTML, CSS and JavaScript in a single file. No frameworks, no build step, no external requests, so it runs offline. Charts are drawn with inline SVG and CSS.

## Run it locally

1. Download or clone this repo.
2. Open `index.html` in any modern browser.

## Deploy (GitHub Pages)

Repo Settings, then Pages, then deploy from branch `main` and folder `/ (root)`.

## Sources

1. Central Electricity Authority (India), CO₂ Baseline Database for the Indian Power Sector (grid factor about 0.71 kg per kWh).
2. Our World in Data, per-capita CO₂ emissions (based on the Global Carbon Project).
3. Hot or Cool Institute, *1.5-Degree Lifestyles* (2021).
4. UK DEFRA, Greenhouse gas reporting conversion factors.
5. Poore and Nemecek, *Science* (2018); Scarborough et al., *Climatic Change* (2014).
6. IPCC Sixth Assessment Report (2021 to 2023).

## Limitations

This is an educational estimator. It uses rounded national averages, not your exact grid mix or vehicle. It does not include emissions embedded in housing or large purchases. Results should be read as estimates.

## Future work

City-level grid data, electricity bill upload, Hindi and Marathi language support, a mobile app, and a shared campus or school leaderboard.

## License

MIT License
