# EIDC dataset: Tritrophic phenology and associated data from 44 sites in Scotland, 2014-2021

## Overview
- Longitudinal, multi-taxa dataset covering 44 woodland sites in Scotland from 2014 to 2021.
- Data collected on tree phenology, caterpillars, and blue tit breeding, plus environmental temperature.
- Data organized into seven CSV files, with consistent site and year identifiers to enable integration across datasets.

## Data collection and sampling design
- Sites and nestboxes:
  - Started with 30 woodland sites; expanded to 44 sites by 2017, most with eight nestboxes per site.
  - Site selection favored spatial spacing and proximity to major roads (M90, A9).
  - Visits typically every 2 days from April to mid-June; fieldwork in 2014-2016 began mid-March; 2020 fieldwork delayed to May due to COVID-19, with southern (22) sites visited regularly.
- Temperature:
  - Hourly air temperature recorded at two loggers per site, positioned at ~1.5 m above ground on opposite ends of each site.
  - Data span mid-February to mid-June; NA values indicate missing readings.
- Tree phenology:
  - Representative deciduous taxa sampled; phenophases recorded: first budburst, complete budburst, first leaf, complete leaf.
  - Phenology data stored per tree (Tree_Phenology) with taxon and ordinal day measurements.
- Caterpillars (branch beating):
  - Branch beating conducted on branches of trees with accessible live growth; sampling began after 45% of trees showed first leaf.
  - Branches beaten every four days; caterpillars dislodged and counted if >1 mm diameter.
  - From 2017, samples weighed; <0.02 g recorded as <0.02 g; caterpillar mass logged and notes captured for issues.
- Blue tit breeding:
  - Nestbox visits every 2 days until first egg; subsequent visits record incubation, clutch size, hatching, and fledging data.
  - Nestlings weighed and wing-length measured at specified days; adults weighed, morphometrics recorded; nestlings and adults have separate data files.
  - Clutch treatments noted for 2017–2019 clutch swap experiments; outcomes may require controls or exclusion in analyses.

## Data files and structure
- 7 CSV files, which can be joined by site and year; same site/year can be combined across files using standardized identifiers.
- site_details
  - site, Description: three-letter site code; Name/Description: sampling location name; MeanLat/MeanLong/MeanElev: site coordinates and elevation.
- temperatures
  - site, Description; year; X46–X163: hourly temperature data by ordinal day (46 to 163); NA where data missing.
- Tree_Phenology
  - year, site, TreeID (unique per tree per site); taxon; fbb (first budburst), cbb (complete budburst), flf (first leaf), clf (complete leaf) – all in ordinal days.
- Branch_Beating
  - year, site, treeID, taxon; date (ordinal day); weather; recorder; caterpillar (count); caterpillar.mass; notes; mass.uncertain.
- Bird_Phenology
  - year, site, box (nestbox number); species; fed (first egg date); cs (clutch size); fki (first incubation date); clutch_swap_treatment; Hatching_first_recorded; uhe (unhatched eggs); v1date/v1alive/v1time; v2date/v2alive/v2time; suc (fledging success); data use notes (-999 to be excluded in analyses).
- Nestlings
  - year, site, box; ring; v1date; v1mass; v1ringer; v2alive; v2date; v2mass; v2wing; v2ringer; fledged.
- Adults
  - ring; year; site; box; age; sex; wing; mass; date; time; ringer.
- Notes on data structure
  - Tree_ID combined with site yields a unique tree identifier; nestbox IDs combined with site yield unique nestbox identifiers; values such as -999 indicate exclusions; NA denotes missing observations.

## Data quality and limitations
- Data completeness affected by COVID-19 in 2020; southern sites (22) received regular visits, while other locations had gaps.
- Some years require careful handling of clutch treatment data (possible exclusion or control in analyses).
- Branch mass measurements include <0.02 g entries; interpretation requires awareness of detection limits.

## Usage guidance and outputs
- Potential data products include dashboards, pivot tables, and self-serve analyses enabling exploration of tri-trophic phenology relationships across sites and years.
- Outputs can be enhanced by incorporating the included notes and ensuring proper treatment of missing data, clutch treatments, and year-specific sampling variation.

## References
- Macphie, K., Samplonius, J.M., Hadfield, J.D., Pearce-Higgins, J. & Phillimore, A.B. (2020). Among tree and habitat differences in the timing and abundance of spring caterpillars. EcoEvoRxiv.
- Shutt, J.D., Bolton, M., Benedicto Cabello, I., Burgess, M.D. & Phillimore, A.B. (2018). The effects of woodland habitat and biogeography on blue tit territory occupancy and productivity along a 220 km transect. Ecography.
- Shutt, J.D., Burgess, M.D. & Phillimore, A.B. (2019a). A spatial perspective on the phenological distribution of the spring woodland caterpillar peak. American Naturalist.
- Shutt, J.D., Cabello, I.B., Keogan, K., Leech, D.I., Samplonius, J.M., Whittle, L. et al. (2019b). The environmental predictors of spatio-temporal variation in the breeding phenology of a passerine bird. Proceedings of the Royal Society B.