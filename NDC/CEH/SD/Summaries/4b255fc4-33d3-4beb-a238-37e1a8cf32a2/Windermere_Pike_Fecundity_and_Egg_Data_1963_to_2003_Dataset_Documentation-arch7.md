# Windermere Pike Fecundity and Egg Data (1963 to 2003)

## Overview
- Dataset of fecundity, egg data, and related measurements for female pike (Esox lucius) from Windermere Lake, Cumbria, Great Britain.
- Time span: 1963–2003; data originally collected by the Freshwater Biological Association (FBA) and since 1989 by CEH and its predecessor IFE.
- File: Windermere_Pike_Fecundity_and_Egg_Data_1963_to_2003.csv (CSV, ~160 KB).
- Copyright: Database Right/Copyright © NERC - CEH/FBA.

## Data Content and Structure
- Primary variables (for each fish): 
  - YEAR, MONTH (capture date)
  - LENGTH (fork length in cm, to 1 mm precision)
  - SOMATIC INDEX (relative body condition factor, unitless)
  - EGG NUMBER (estimated number of eggs)
  - EGG WEIGHT (average egg weight in grams)
- Location information:
  - Sampling site: Windermere Lake (Windermere, Cumbria)
  - Approximate center coordinates and multiple coordinate representations:
    - OS Grid Reference: SD393960
    - OSGB36 Easting/Northing: 339385, 496080
    - WGS84: 54.360193, -2.935836
- Species: Esox lucius (Pike)

## Spatial and Temporal Coverage
- Spatial: Windermere Lake, with sampling across its north and south basins.
- Temporal: 1963–2003, with long-running monitoring since 1944.
- Sampling regime notes:
  - Since 1982: standardized gill-netting (64 mm bar mesh, 40 m × 3 m nets) deployed at ~10 sites per basin, depths ~4–5 m.
  - Seasonal sampling window: typically October–December; nets set mid-October to late December, rotated among sites.
  - Post-1982 protocol ensured systematic coverage; production of annual sampling effort details (c. 348 net days in 1982–1989; ~240 net days since 1990, balanced between basins).

## Data Collection, Methods, and Processing
- Field collection:
  - Gill-netting used to capture pike; nets set on the lake bottom, lifted every few days, sites rotated to cover entire lake.
  - All captured pike euthanized and processed in the lab.
- Laboratory analysis:
  - Each pike measured (fork length to 1 mm) and weighed (to 100 g).
  - Sex determined by dissection; aging via left opercular bone (birth date 1 April).
  - Female fecundity estimated (number of eggs) and ovarian weight measured.
  - Somatic index calculated as somatic weight divided by predicted somatic weight from population relationships.
- Quality control:
  - Measurements validated through permutations involving three individuals to ensure accuracy.

## Data Processing and Standards
- Data standards and key references underpinning techniques:
  - Aging: Frost & Kipling (1959)
  - Fecundity methodology: Kipling & Frost (1969)
  - Somatic index definition (Edeline et al., 2007)
  - Contextual methods for pike population analysis (Winfield et al., 2008; related foundational works)
- Data were standardized beginning in 1982, enabling consistent comparisons over time.

## Provenance and Rights
- Original data collected by FBA; ongoing collection and curation by CEH and its predecessor institutes since 1989.
- Rights and licensing noted as Database Right/Copyright © NERC - CEH/FBA.

## GIS and Analytical Considerations for Map-Based Use
- Suitable for spatial-temporal mapping of fecundity and egg metrics across Windermere Lake:
  - Link year-month data to individual fish measurements and lake basins.
  - Use precise coordinates (OSGB36 and WGS84) to map sampling sites and potential spatial trends.
- Data integration:
  - Can be joined with other Windermere-based biological or environmental datasets, noting differing resolutions and the long temporal span.
  - Ensure consistent coordinate reference system when visualizing (convert OSGB36 to WGS84 for global GIS compatibility if needed).
- Caveats:
  - Sampling effort varied historically (1982–1989 vs. post-1990), which may influence spatial/temporal comparisons.
  - Age estimation and fecundity estimates are derived measurements with established, but complex, methodology; consider uncertainty in analyses.
- Potential uses:
  - Visualizing spatial distribution of fecundity and egg metrics over time.
  - Analyzing relationships between fish size, body condition, and fecundity across basins and years.
  - Integrating with environmental data to assess trends in Windermere pike biology.