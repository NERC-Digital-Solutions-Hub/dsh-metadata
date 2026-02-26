# Invasion process of Pinus radiata in South-Central Chile

## Aim
- Characterize the invasion process of Pinus radiata in South-Central Chile.
- Identify which variables are relevant for invasion success and determine how those variables affect the process.
- Recognize that invasion success depends on both the invasive species and the invaded community; thus, characterize seed source (plantation), invaded habitat, and P. radiata natural regeneration (wildings).

## Study area
- Five representative ecosystems in central Chile: Bosque caducifolio andino (Huepil), Matorral esclerófilo (San Javier), Bosque Maulino (Constitución), Bosque esclerófilo (Florida), and Bosque caducifolio de Concepción (Hualqui).
- For each ecosystem:
  - Three Pinus radiata commercial plantations near native patches recently affected by fires.
  - A corresponding control area within the same plantation that was not burned (three burned, three not burned per ecosystem).
  - Total of six sites per ecosystem, yielding 30 sites overall.
- Fire history and data collection timing:
  - Fires occurred in 2017 (Constitución), 2010–2012 (Florida), 2021 (Hualqui); Huepil and San Javier had no recorded recent fires.
  - Data collected in 2020 (San Javier, Tucapel) and 2021 (Constitución, Hualqui, Florida).
- Location span: Maule and Biobío Regions, South-Central Chile.

## Sampling methods
- Plantation characterization
  - Establish three 20 m x 20 m plots within each plantation site.
  - Record plantation density (trees/ha), tree height (m), and serotinity (percentage of open vs. closed cones) per sampled tree (three trees per site; two observers for cone counts).
  - Collect plantation year and year of last fire from plantation owners.
- Invasion wave assessment (natural regeneration)
  - From plantation edge, establish three 2 m wide transects; transects divided into 10 m sections, up to 100 m long, depending on native patch size.
  - Record all P. radiata wilding trees in each section, plus height of the tallest tree and its age.
- Native patch characterization
  - Along the same transects, assess surrounding native patch using Braun-Blanquet abundance-cover index for ground, understory, and canopy.
  - Use a 5-category scale (0 to 4) corresponding to increasing cover percentages.
- Data collection design visuals
  - Refer to accompanying figures illustrating the sampling design and representative sites (burned vs. unburned).

## Database structure
- Data stored in three CSV files:
  - Database_Pradiata_invasion-Habitat.csv
    - Contains habitat descriptions and Braun-Blanquet cover data for ground, understory, and canopy.
    - Includes study area identifiers (San Javier, Tucapel, Constitución, Santa Juana, Hualqui), fire status (NQ = not burned; Q = burned), Site, Transect, Section, and cover categories (0–4).
  - Database_Pradiata_invasion_Plantation.csv
    - Contains plantation/source data: study area, fire status, Site, Fire date, Plantation year, plantation density (trees/ha), data for three sampled trees (height, cone counts for two observers).
  - Database_Pradiata_invasion_Regeneration.csv
    - Contains regeneration data: study area, fire status, Site, Transect, Section, pine abundance (wildings per section), tallest pine height, age, and estimated pine density per section (pines/ha).
- Data scope includes five study areas (San Javier, Tucapel, Constitución, Santa Juana, Hualqui) and multiple sites, with fire status and transect/section-level detail to capture early invasion dynamics.