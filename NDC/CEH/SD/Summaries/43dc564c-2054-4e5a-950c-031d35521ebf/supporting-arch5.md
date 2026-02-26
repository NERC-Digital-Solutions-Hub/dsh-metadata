# Invasion of Pinus radiata in South-Central Chile

## Overview
- Aim: Characterize the invasion process of Pinus radiata in South-Central Chile to identify variables relevant to invasion success, considering seed source (plantation), invaded habitat, and natural regeneration (wildings).
- Key variables to capture:
  - From plantations (seed source): age, height, density, number of cones per tree; estimated serotinity (open vs closed cones).
  - From invaded habitat: effect of fire on seed fall and germination; habitat type (native forests, shrublands, grasslands).
  - From regeneration: density of wildings, height, age, cone presence.
- Context: Invasion depends on both the invasive species and the native community; uses plantation data and field sampling to assess early invasion dynamics.

## Study area and sampling design
- Five representative ecosystems in central Chile: Bosque caducifolio andino (Huepil), Matorral esclerófilo (San Javier), Bosque Maulino (Constitución), Bosque esclerófilo (Florida), Bosque caducifolio de Concepción (Hualqui).
- Within each ecosystem: three Pinus radiata commercial plantations near native patches, with recent fires (no more than ~10 years) and corresponding unburned control areas; three sites per condition (burned or not burned), yielding six sites per ecosystem and a total of 30 sites.
- Fire timing: recorded fires at various years (some areas burned in 2017, 2010–2012, 2021); data collection occurred in 2020–2021 across sites.

## Sampling methods and data collection
- Plantation characterization (seed source):
  - Three 20x20 m plots per site.
  - Measurements: plantation density (trees/ha), tree height (m), serotinity level (open vs closed cones) using two observers counting cones from three trees per site; height estimated with a hypsometer.
  - Auxiliary data from plantation owners: plantation year, year of last fire.
- Invasion wave assessment (native patch and short-distance dispersion):
  - Three 2 m wide transects starting at plantation edge; transects divided into 10 m sections, up to 100 m long.
  - Within each section: record all P. radiata wildings, height and age of tallest wilding.
  - Native patch characterization along transects: Braun-Blanquet cover categories for ground, understory, and canopy (categories 0–4).
- Native patch sampling across sites:
  - Data aligned with transects to describe surrounding vegetation structure and potential barriers or facilitators to invasion.

## Data structure and access (database design)
- Database_Pradiata_invasion-Habitat.csv
  - Habitat description and cover data (ground, understory, canopy) by study area, burn status, site, transect, and section; Braun-Blanquet categories 1–4.
- Database_Pradiata_invasion_Plantation.csv
  - Plantation data by study area, burn status, site, fire year, plantation year, density (trees/ha); cone counts (open, closed, total) for three sampled trees per site; height data per tree; observer data.
- Database_Pradiata_invasion_Regeneration.csv
  - Regeneration data by study area, burn status, site, transect, section; pine abundance (wildings) per section; tallest height and age; estimated density (pines/ha).

## Data governance, quality, and reproducibility
- Provenance and transparency:
  - Data collected from field sampling across multiple sites, with some metadata provided by plantation owners (fire year, plantation year).
  - Two observers used for cone counts to improve reliability; height measured with standardized tools.
- Standardization and interoperability:
  - Clear, consistent units (meters for height, trees per hectare for density, years for age, Braun-Blanquet categories for cover).
  - Structured sampling design (plots, transects, sections) to enable replication and cross-site comparisons.
- Metadata and cataloging readiness:
  - Datasets labeled with study area, site, transect, section, and burn status; explicit column mappings for habitat, plantation, and regeneration data.
- Temporal coverage:
  - Data collected mainly in 2020–2021, with fire history spanning 2010–2021 across sites.
- Limitations and considerations:
  - Some areas only unburned; fire history data may be incomplete for certain sites.
  - Dependence on plantation-owner data for some metadata (fire year, plantation year).
  - Braun-Blanquet categorization requires consistent application across habitats for comparability.

## Practical implications for data stewardship
- Facilitates discovery and reuse by clearly described variables related to invasion drivers, habitat context, and regeneration dynamics.
- Supports meta-analyses comparing invasion dynamics across ecosystems with standardized measures.
- Provides a robust data framework for tracking updates, adding new sites, or extending temporal coverage.