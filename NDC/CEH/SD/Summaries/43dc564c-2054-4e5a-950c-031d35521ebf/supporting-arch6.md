# Characterization of the invasion process of Pinus radiata in South-Central Chile

## Aim
- Characterize the invasion process of Pinus radiata in South-Central Chile.
- Identify which variables influence invasion success, considering both the seed source (plantation) and the invaded habitat (burned vs unburned, native habitat types) and the natural regeneration (wildings).
- Use plantation data and field sampling to determine key attributes (age, height, density, cones per tree, serotinity) and how fire and habitat type affect seed dispersal, germination, and regeneration.
- Develop a data-driven understanding to inform invasion status and potential management actions.

## Study Area
- Five representative ecosystems in central Chile: Bosque caducifolio andino (Huepil), Matorral esclerófilo (San Javier), Bosque Maulino (Constitución), Bosque esclerófilo (Florida), Bosque caducifolio de Concepción (Hualqui).
- In each ecosystem: three Pinus radiata commercial plantations near native forest patches (recently affected by fires, within 10 years) plus a non-burned control area from the same plantation.
- For each condition (burned Q and not burned NQ), three sites were studied, totaling six sites per ecosystem and 30 sites overall.
- Fire history varies by site (fires recorded in 2017, 2010–2012, 2021; data collected 2020–2021).
- Data collection locations span Maule and Biobío Regions.

## Sampling Methods
- Plantation characterization:
  - Three 20 x 20 m plots per site within the plantation stand.
  - Recorded: density (trees/ha) if possible, tree height (m), serotinity (open vs closed cones as a percentage of total cones on sampled trees).
  - Additional data from plantation owners: plantation year, year of fire.
  - Cone counts: three trees per site, two observers; count open/closed cones in canopy using binoculars; height estimated with a hypsometer.
- Invasion wave assessment (native vegetation adjacent to plantations):
  - Three 2 m wide transects starting at plantation edge; transects subdivided into 10 m sections, up to 100 m sections depending on patch size.
  - Recorded all P. radiata wilding trees, plus the height of the tallest wilding and its age.
- Native patch characterization:
  - For each section, assessed ground, understory, and canopy cover using Braun-Blanquet categories (0–4) with 5 class divisions.

## Data Collection and Variables (Data Files)
- Data are stored in three CSV files, each covering different aspects of the study:
  - Database_Pradiata_invasion-Habitat.csv: habitat description and Braun-Blanquet cover for ground, understory, and canopy; fields include study area, fire status (NQ or Q), Site, Transect, Section, and cover categories (1–4).
  - Database_Pradiata_invasion_Plantation.csv: plantation source data; fields include study area, fire status (NQ or Q), Site, Fire date (summer), Plantation year, plantation density (trees/ha), sampled trees (1–3) with height (m) and cone counts (open, closed, total) from two observers.
  - Database_Pradiata_invasion_Regeneration.csv: regeneration data; fields include study area, fire status (NQ or Q), Site, Transect, Section, pine abundance (number of wildings in section), tallest pine height (m), age (years), and estimated pine density per section (pines/ha).

## Data Structure and Provisional Outputs
- Data are organized by area and condition, enabling analyses of:
  - Seed-source influence: plantation age, density, height, and serotinity.
  - Habitat influence: burn status, habitat type, and canopy/ground understory cover.
  - Regeneration dynamics: density and characteristics of wildings, height, age, and spatial distribution along transects.
- The standardized field collection (e.g., multiple observers for cone counts, hypsometer-based heights, Braun-Blanquet cover) supports data quality and comparability across sites and ecosystems.