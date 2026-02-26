# Study site

- Location and environment: Study conducted in the unlogged primary forest of Danum Valley Conservation Area (DVCA) and adjacent selectively logged forest of Ulu Segama Forest Reserve (USFR) in Sabah, Malaysia (4°58'N, 117°52'E). DVCA covers 438 km² with mean annual rainfall ~2305 mm and mean daily temperature ~25.8°C.
- DVCA vs USFR context: USFR region sampled was logged between 1981–1993, subdivided into annual coupes (~27 km² each) with harvest of trees >60 cm DBH. Logging intensity averaged ~118 m³ ha⁻¹ (1970–1990) and varied by coupe. Harvesting used tractors on moderate terrain and high-lead cables on steep slopes.
- Silvicultural interventions: In 1993, Reduced Impact Logging (RIL) trials were established to minimize damage; silvicultural interventions targeted restoration of forest carbon stocks as part of the Innoprise-FACE Foundation Rainforest Rehabilitation Project. Other coupes were allowed to recover naturally.

## Seedling plots and inventory

- Plot setup: Seedling plots of 1 m² established in Sep–Oct 2019 during a mast fruiting event. In DVCA, 87 plots were established within the ForestGEO Danum Valley 50 ha forest dynamics plot; in USFR, 96 plots (52 actively restored; 44 naturally regenerating) within the INDFORSUS project.
- Data collection: Fruits dispersed during the mast fruiting event and subsequent new seedling recruits were counted on all plots across four censuses between Sep 2019 and Mar 2021.
  - Census 1: Sep–Oct 2019
  - Census 2: Nov–Dec 2019
  - Census 3: Jan–May 2020
  - Census 4: Feb–Mar 2021
- Identification: Each fruit or seedling identified to species (field-level identification; unidentified species placed into morphospecies).
- Dataset scope: Counts of fruits and seedlings by species and plot at each of the four censuses.

## Danum_Valley_Seedling_Census.csv (data structure)

- File contains columns (summary):
  - Forest (Primary forests or Logged forests)
  - Management (Natural Regeneration or Active Restoration)
  - Seedling.Plot (plot identifier)
  - Family (Plant Family)
  - Species (scientific species name; morphospecies possible for unidentified)
  - Date.1, Count.1 (date and count for Census 1)
  - Date.2, Count.2 (date and count for Census 2)
  - Date.3, Count.3 (date and count for Census 3)
  - Date.4, Count.4 (date and count for Census 4)
- Notes on fields:
  - Date.x fields indicate the census date for each census.
  - Count.x fields indicate the number of individuals (or fruits for recruitment) counted at each census.
  - Some species may be grouped as morphospecies if not identified to species level.