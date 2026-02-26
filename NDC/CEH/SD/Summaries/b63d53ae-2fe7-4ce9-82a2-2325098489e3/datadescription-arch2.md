# EIDC dataset: Tritrophic phenology and associated data from 44 sites in Scotland, 2014-2021

## Overview
- Longitudinal, multi-taxa dataset describing tritrophic interactions (trees, caterpillars, and blue tits) across 44 woodland sites in Scotland from 2014 to 2021.
- Data streams include temperature, tree phenology, caterpillar abundance/mass, and blue tit breeding phenology and outcomes.
- Data are organized into seven CSV files with a consistent site coding scheme to enable cross-year site-level analyses.

## Sampling design and fieldwork
- Sites: 30 woodland sites initially (2014), expanded to 44 sites by 2017; sites selected for spacing and proximity to major roads (M90 and A9). Most sites had eight nestboxes by 2017.
- Nestboxes: 26 mm Schwegler 1B woodcrete boxes; eight per site where possible.

- Timeline:
  - Field visits every 2 days from early April to mid-June (2014–2016 started mid/late March; 2020 fieldwork delayed due to Covid-19; southern 22 sites visited regularly in 2020).
  - Temperature data loggers deployed at opposite ends of each site, ~1.5 m above ground.

## Data streams and measurements
- Temperature (Temperature file)
  - Hourly air temperatures recorded per site.
  - Loggers: two DS1922 L thermochrons placed at opposite ends of each site.
  - Time window: from ordinal day 46 to 163; NA where not recording.

- Tree phenology (Tree_Phenology file)
  - Representative deciduous taxa at each site; phenophases recorded at each visit.
  - Phenophases:
    - First budburst (fbb)
    - Complete budburst (cbb)
    - First leaf (flf)
    - Complete leaf (clf)
  - Taxon can be species or genus depending on site.

- Caterpillars (Branch_Beating file)
  - Branch beating conducted on selected trees with accessible live branches.
  - Sampling: branches beaten every four days; 30 hits per beating.
  - Measurements: number of caterpillars dislodged; total mass of caterpillars per sample (mass < 0.02 g recorded as < 0.02 g).
  - Additional notes on weather, recorder, and any issues; mass uncertainty flag included.

- Blue tit breeding phenology and outcomes (Bird_Phenology, Nestlings, Adults files)
  - Nestbox monitoring to record:
    - First egg date, clutch size, first incubation
    - Hatching date and nestling development
    - Ringing and morphometrics (mass, wing length) of nestlings and adults
    - Breeding success measured as number fledged
  - Nestbox and individual identifiers:
    - Box number, site code, year, ringer IDs
  - Data are split into:
    - Bird_Phenology: nestbox-level phenology and breeding events
    - Nestlings: individual nestling data (mass, wing, fledging status)
    - Adults: adult bird data (age, sex, morphometrics)

## Data structure and integration
- Dataset consists of 7 CSV files:
  - site_details: site codes, names, mean latitude/longitude, elevation
  - temperatures: yearly hourly data by site
  - Tree_Phenology: year, site, TreeID, taxon, budburst and leaf dates (fbb, cbb, flf, clf)
  - Branch_Beating: year, site, treeID, taxon, date, weather, caterpillar counts and mass, notes, mass uncertainty
  - Bird_Phenology: year, site, box, species, first egg date, clutch size, incubation, hatching, fledging, clutch_swap_treatment, other timing fields
  - Nestlings: year, site, box, v1/v2 dates, masses, wing lengths, ringers, fledging status
  - Adults: ring, year, site, box, age, sex, wing, mass, date/time, ringer
- Data for the same sites and years can be combined using the site code and year identifiers.

## Data quality, gaps, and provenance
- Standardized data collection and terminology to support cross-year analyses and comparability.
- Some missing data: 2020 field data incomplete (e.g., some phenology and temperature gaps; southern sites experienced regular visits only).
- Clutch swap treatment introduced in 2017–2019 within some nestboxes; requires consideration in analyses.
- Several peer-reviewed studies have utilized these data, demonstrating their scientific value across environmental phenology and trophic interactions.

## Uses for environmental monitoring and policy analysis
- Demonstrates multi-taxa environmental phenology and trophic interactions across landscapes and time.
- Enables:
  - Temporal trends in temperature, tree phenology, caterpillar emergence, and blue tit breeding timing and success.
  - Cross-taxa analyses to explore phenological synchrony and potential mismatch risks.
  - Integration with other environmental datasets to enhance monitoring value beyond single-use outputs.
- Outputs suitable for reports, maps, and charts to illustrate environmental health and policy-relevant dynamics over time.

## Access, reuse, and relevant literature
- Data structured to support reuse across years and sites via consistent coding.
- Cited publications illustrate use in exploring: timing and abundance of caterpillars, habitat effects on blue tit productivity, spatial phenological patterns, and environmental predictors of breeding phenology.