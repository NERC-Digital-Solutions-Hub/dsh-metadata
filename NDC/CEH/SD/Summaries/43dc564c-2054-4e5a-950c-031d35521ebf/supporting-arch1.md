# Characterization of the invasion process of Pinus radiata in South-Central Chile

- Aim
  - Characterize the invasion process of Pinus radiata in South-Central Chile.
  - Identify which variables are relevant for invasion success and how they affect the process.
  - Consider both the invasive species and the invaded community (seed source, invaded habitat, and natural regeneration).
  - Use commercial plantation data as seed sources and supplement with field sampling.
  - Collect data on plantation attributes (age, height, density, cone counts) and estimates of serotiny; assess invaded habitat with burn status and habitat type; characterize natural regeneration (density, height, age, cone presence).

- Study area and sampling design
  - Five representative ecosystems in central Chile: Bosque caducifolío andino, Matorral esclerófilo, Bosque Maulino, Bosque esclerófilo, and Bosque caducifolio de Concepción.
  - For each ecosystem: three Pinus radiata commercial plantations near native forest patches, recently affected by fires or unburned control areas.
  - Experimental setup: within each ecosystem, six sites (three burned, three not burned) across three plantations per condition; total of 30 sites.
  - Geographic scope: Maule and Biobío Regions; data collection years span 2020–2021 with fires occurring in 2010–2012, 2017, and 2021 depending on site.
  - Site layout visuals: plots and transects designed to capture short-distance invasion waves from plantations into native patches.

- Sampling methods and variables collected
  - Plantation characterization
    - Three 20x20 m plots per site to estimate plantation density (trees/ha) and tree height (m).
    - Serotiny: estimate percentage of open vs. closed cones on sampled trees.
    - Additional data from plantation owners: plantation year, year(s) of fire.
    - Cone assessment: three trees per site, two observers counting open/closed cones via binoculars; height estimated with a hypsometer.
  - Invasion wave assessment
    - Three 2 m wide transects starting at plantation edge; sections of 10 m, up to 100 m length depending on native patch size.
    - Within each section: record all P. radiata wildings, tallest tree height, and age.
  - Native patch characterization
    - Along transects: Braun-Blanquet cover estimates for ground, understory, and canopy in five categories (0 to 4; 0=none, 1-4 increasing cover).
  - Data capture emphasis
    - First wave of invasion from short-distance dispersal into native vegetation patches; align plantation attributes with invasion observations.

- Database structure and data formats
  - Database_Pradiata_invasion-Habitat.csv
    - Habitat description; ground, understory, and canopy cover per section.
    - Columns include study area, fire status (NQ or Q), Site, Transect, Section, and Braun-Blanquet cover categories.
  - Database_Pradiata_invasion_Plantation.csv
    - Seed-source plantation data per site: study area, fire status, Site, Fire date, Plantation year, density (trees/ha), sampled trees (1-3), height, and cone counts (open, closed, total) by two observers.
  - Database_Pradiata_invasion_Regeneration.csv
    - Regeneration data per site: study area, fire status, Site, Transect, Section, pine abundance (wildings), tallest height, age, and estimated pine density (pines/ha).

- Key considerations for analysis
  - Integrate plantation attributes with invasion observations and regeneration status to model invasion success.
  - Use burn status and habitat type to assess how disturbance influences seed fall, germination, and recruitment.
  - Aggregate data across sites and ecosystems to identify patterns in seed-source proximity, habitat receptivity, and regeneration dynamics.
  - Maintain traceability of data sources, including plantation records and field measurements, to support reproducibility and metadata-rich datasets.