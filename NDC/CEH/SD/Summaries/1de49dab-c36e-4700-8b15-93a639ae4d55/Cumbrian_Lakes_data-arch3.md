# Cumbrian Lakes plankton and fish data, used for turning points and early warnings analysis (1940 to 2013)

## Overview
- Dataset description supporting Burthe et al. (2015) on turning points and early warnings in large English lakes.
- Contains phyto- and zooplankton counts, chlorophyll concentration, and fish catch data from Windermere (north and south basins), Esthwaite Water, and Blelham Tarn.
- Original data collected by the Freshwater Biological Association (FBA), later managed by CEH and predecessors; authors recommend contacting data creators before reuse.

## Datasets and Sites
- Windermere North Basin (NBAS) and Windermere South Basin (SBAS)
- Esthwaite Water (ESTH)
- Blelham Tarn (BLEL)
- Approximate grid references provided for each site
- Data files:
  - Windermere_fish_annual_catches.csv: CPUE by species (Arctic charr, perch, pike), by basin and year; formats differ by method (nets, anglers, traps)
  - Cumbrian_Lakes_phyto_allsites.csv: phytoplankton counts by taxon (cells/ml), month/year, site, analyst, counting chamber, and form (CELL/COLO)
  - Cumbrian_Lakes_zoo_allsites.csv: zooplankton counts by group (e.g., Daphnia, Bosmina, total calanoids/cyclopoids), by month/year, site, and analyst
  - Cumbrian_Lakes_chl_allsites.csv: chlorophyll a concentration (mg/m3) by date, month, year, site, and extraction method

## Sampling Design and Collection Methods
- Frequency: weekly to biweekly sampling at the deepest point of each lake
- Phytoplankton and chlorophyll:
  - Water samples fixed with Lugol’s iodine for counts; separate samples for chlorophyll
  - Phytoplankton counted in Lund chambers; dominant species data aggregated to genus level for consistency
  - Chlorophyll extracted from filtered samples (methanol) and measured spectrophotometrically
- Zooplankton:
  - Species-level counts (Windermere NB) and aggregate filter counts for all lakes
  - Net tows over upper 40 m; samples preserved (ethanol/formalin); counts via stereozoom microscopy
- Fish data:
  - Arctic charr: anglers’ catch per unit effort (CPUE) 1966–present; gill netting on spawning grounds 1940–present
  - Perch: standardized traps from 1943–present
  - Pike: gill nets 1944–present
  - Gill nets (pike) standardized since 1982: 64 mm bar mesh, 40 m x 3 m nets, set at multiple sites, with defined weekly rotation and effort
  - Annual CPUEs calculated by basin and year for each species and method

## Analytical Methods and Data Processing
- Phytoplankton data: counts summed to genus level to mitigate analyst differences; time span utilized 1978–2003/2005 depending on species
- Chlorophyll data: concentration used from 1964–2009
- Zooplankton data: species-level (1979–2010) and total crustacean counts (1964–2009)
- Fish data: annual mean CPUEs computed for each species, basin, and year across 1940–2013
- Documentation notes include methodological references and historical context for sampling approaches

## Data Access and Reuse Considerations
- The dataset is provided to describe data used in Burthe et al. (2015); direct contact with original authors is strongly recommended prior to re-use
- Original datasets originated with the FBA and later CEH; data governance, metadata, and sharing practices are highlighted as important considerations
- Several CSV files have varying formats and field definitions; users should reference the column descriptions in each file for appropriate interpretation

## References
- Le Cren, E. D. (2001); The Windermere perch and pike project
- Lund, J.W.G. (1949); Studies on Asterionella
- Talling, J.F. (1974, 2003); Methods for measuring primary productivity and phenology in English lakes
- Thackeray, S.J. et al. (2013); Food web de-synchronization in England’s largest lake
- Winfield, I.J. et al. (2008a, 2008b); Studies on Arctic charr and northern pike in Windermere