# Long-term multisite Scots pine trial, Scotland: mother tree, cone and seed phenotypes, 2007

## Overview
- Dataset of phenotypes for Scots pine (Pinus sylvestris) mother trees and their cones/seed from 21 native populations across Scotland.
- Seed used to establish a long-term multisite common garden trial at three nurseries/field sites.
- Two linked files contain measurements for mother trees and cone/seed traits.

## Sampling design
- Ten seed trees sampled from each population in March 2007.
- Population selection aimed to cover native range with three populations per seeding zone.
- Spatial sampling around a central tree within a circle ~1 km in diameter.
- Protocol: nine sampling points in predetermined random directions, stratified by distance from center in 1:3:5 ratio to avoid central bias.
- For small woodland fragments or few cone-bearing trees, directions adjusted to cover area while ensuring minimum distances between sampled trees of 50 m.

## Measurements and traits

### Mother trees (MotherTraits)
- For each mother tree: height and diameter at breast height (DBH).
- Ten cones collected per mother tree; cone width and length measured before drying; cone weight measured after drying.
- Seed data: total seed weight, count of seeds, and percentage of viable seeds (viable = has a wing and obvious seed).
- Averages: mean values for each mother tree computed across the 10 cones.

### Cone and seed traits (ConeSeedTraits)
- Cone traits: Cone (1–10 per population), Width (Wi, mm), Length (Le, mm), Weight (We, g).
- Seed traits per cone: Total seeds (SN, count), Viable seed percentage (SV, %), Weight of viable seeds (SW, g).

## Dataset structure

### Files
- ConeSeedTraits.txt
- MotherTraits.txt

### Key variables and structure
- PopulationCode: population identifier.
- Family: mother tree ID (links to individuals within a population; same family = same mother tree).
- Population: full population name.
- SeedZone: Scots pine seed zone (EC: east central; N: north; NC: north central; NE: north east; NW: north west; SC: south central; SW: south west).
- Latitude/Longitude: geographic coordinates of populations (decimal degrees).
- Aspect: cardinal direction of slope.
- Slope: approximate slope severity (flat to steep).
- Altitude: elevation in meters.
- Regeneration: extent of regeneration around the mother tree (1–4 scale).
- SoilDepth: depth of soil around the mother tree (cm; up to 1.5 m).
- SoilMoisture: soil moisture around the mother tree (1–5 scale from very wet to very well drained).
- Competition: mean distance from the mother tree to the nearest three trees (m).
- HA: Height of the mother tree (m).
- DA: Diameter at breast height of the mother tree (m).
- ConeSeedTraits file-specific: Cone (1–10), Wi (mm), Le (mm), We (g), SN (count), SV (% viable), SW (g viable seeds).

## Practical notes and potential uses
- Enables analysis of maternal effects and cross-population phenotypic variation in cone and seed traits.
- Supports long-term common garden studies and exploration of relationships between mother-tree traits, cone/seed characteristics, and environmental/contextual variables (seed zone, altitude, soil moisture, competition).
- Useful for data quality checks, dataset integration, and development of data products (dashboards, summaries, or reports) for broader reuse.

## Data quality and considerations
- Measurements were collected in March 2007 following a defined sampling protocol to ensure broad geographic and environmental coverage.
- Some fields use qualitative or ordinal scales (e.g., SeedZone, Regeneration, SoilMoisture, Slope); others are precise measurements (e.g., height, DBH, cone dimensions, seed counts).
- Units are specified for measurable traits (e.g., mm for dimensions, g for weights, percentages for viability).
- Data are organized to support linking mother-tree data with corresponding cone/seed trait data via the Family and Population fields.