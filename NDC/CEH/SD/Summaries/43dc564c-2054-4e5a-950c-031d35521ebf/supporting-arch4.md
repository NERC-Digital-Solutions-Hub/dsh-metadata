# Characterization of the invasion process of Pinus radiata in South-Central Chile

## Overview and objective
- Aim: Characterize how Pinus radiata invades in South-Central Chile and identify which variables influence invasion success.
- Rationale: Invasion depends on both the species and the invaded community; thus, study seed source (plantation), invaded habitat, and P. radiata natural regeneration (wildings).
- Outcome focus: Determine relevant attributes of plantations, habitat factors (including fire), and regeneration metrics that affect invasion dynamics; inform which data are needed to understand and predict invasion.

## Study area and sampling framework
- Five representative ecosystems in central Chile were selected: 
  - Bosque caducifolio andino (Huepil)
  - Matorral esclerófilo (San Javier)
  - Bosque Maulino (Constitución)
  - Bosque esclerófilo (Florida)
  - Bosque caducifolio de Concepción (Hualqui)
- For each ecosystem:
  - Three Pinus radiata commercial plantations near native patches, recently affected by fires.
  - A control (unburned) area within the same plantation.
  - In total: 6 sites per ecosystem (3 burned, 3 not burned) = 30 sites.
- Temporal context: Fires occurred in 2017 (Constitución), 2010–2012 (Florida), 2021 (Hualqui); data collection occurred mainly in 2020–2021.

## Sampling design and variables collected
- Plantation (seed source) characterization:
  - Plots: three 20 × 20 m plots per site inside the plantation.
  - Variables per plantation: density (trees/ha), tree height (m), serotinity (proportion of open vs. closed cones).
  - Additional data: plantation age, year of fire (from owners).
  - Cone assessment: three trees per site; two observers counted open/closed cones in the canopy via binoculars; height measured with a hypsometer.
- Invasion (seed dispersal and early spread) assessment:
  - Transects: three 2 m-wide transects starting at plantation edge; sections of 10 m along transects, up to 100 m total length, to capture the first wave of short-distance dispersal.
  - At each section: record all P. radiata wildings, tallest tree height, and age.
- Native patch assessment (habitat context):
  - Within each section for the native patch: Braun-Blanquet abundance-cover index to estimate ground, understory, and canopy cover (categories 0–4; 0 = no cover; 4 = 75–100% cover in a category-based scheme).
- Summary of data collected per site:
  - Habitat structure around native patches (cover categories)
  - Seed source attributes (density, height, cone status/serotinity)
  - Invasion indicators (presence/age/height of wildings)

## Data structure and assets
- Data registered in three CSV files:
  - Database_Pradiata_invasion-Habitat.csv
    - Habitat description and cover: ground, understory, canopy
    - Fields include study area, fire status (NQ = not burned; Q = burned), Site, Transect, Section, and cover categories (Braun-Blanquet 1–4)
  - Database_Pradiata_invasion_Plantation.csv
    - Plantation seed-source data: study area, fire status, Site, Fire date, Plantation year
    - Plantation density (trees/ha), sampled trees (1–3) with height (m) and cone counts (open, closed, total) from two observers
  - Database_Pradiata_invasion_Regeneration.csv
    - Regeneration data (wildings): study area, fire status, Site, Transect, Section
    - Pine abundance (wildings), tallest height (m), age (years), estimated density (pines/ha)
- Data collection specifics:
  - Units and coding clearly defined (e.g., NQ vs Q; Braun-Blanquet categories 1–4)
  - Observational methods include dual-observer cone counts to support reliability

## Implications for data management and use
- Data governance and discoverability:
  - Data are organized into three integrated datasets aligned to concrete ecological questions (seed source, habitat, regeneration).
  - Standardized fields and coding support cross-site comparisons and meta-analysis across ecosystems and fire treatments.
- Quality considerations:
  - Serotinity estimation and cone counts involve manual observation; multiple observers help assess measurement reliability.
  - Height estimates via hypsometer introduce potential measurement error; explicit documentation of methods aids reproducibility.
- Potential uses for Data Leaders:
  - Assess data gaps and plan harmonized data collection across additional sites or regions.
  - Leverage the linked datasets to model invasion dynamics, assess how habitat context and fire history influence invasion success, and identify key predictors for policy or management actions.
  - Facilitate data sharing and collaboration by maintaining clear metadata and consistent data structures across projects.