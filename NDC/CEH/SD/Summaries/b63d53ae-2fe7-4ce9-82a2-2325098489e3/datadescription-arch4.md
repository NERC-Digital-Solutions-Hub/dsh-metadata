# EIDC dataset: Tritrophic phenology and associated data from 44 sites in Scotland, 2014-2021

## Overview
- A multi-taxa, tritrophic dataset spanning 44 sites in Scotland (2014–2021) that records temperature, tree phenology, caterpillar abundance/mass, and blue tit breeding phenology and morphology.
- Data collected from nestbox-equipped woodland sites to study interactions among trees, herbivores (caterpillars), and a key passerine (blue tit).

## Study design and sampling
- Initial sampling: 30 woodland sites with eight 26 mm Schwegler 1B nestboxes per site (2014); sites chosen for spacing and proximity to M90/A9 roads.
- Field schedule: visits every 2 days from early April to mid-June (early years started mid-March); in 2020, fieldwork paused until May due to COVID-19, with southern 22 sites sampled regularly.
- Site evolution: by 2017, 44 sites with most having eight nestboxes.

## Data collected by component

- Temperature
  - Hourly air temperatures recorded at two loggers per site (DS1922 L thermochrons) placed high on tree trunks, one at each end of the site, ~1.5 m above ground.
  - Data span mid-February to mid-June; loggers positioned to capture site-wide temperature variation.

- Tree phenology
  - Sampled representative deciduous taxa per site; taxon can be species or genus (e.g., Alder, Oak, Willow, Birch).
  - Phenophases recorded at each visit: first budburst (fbb), complete budburst (cbb), first leaf (flf), complete leaf (clf).
  - Tree_ID provides a unique identifier per tree within a site; data stored in Tree_Phenology.

- Caterpillars
  - Branch beating conducted on trees with accessible live branches; sampling begins once 45% of trees show first leaf.
  - Beating protocol: 30 strikes per sample; caterpillar counts recorded; mass collected and weighed from 2017 onward using Triton scales.
  - Caterpillar mass < 0.02 g recorded as < 0.02 g; notes capture any weighing issues; data stored in Branch_Beating.

- Blue tit data (Bird Phenology and Metrics)
  - Nestbox visits every two days until first egg date; daily egg-laying assumed at 1 egg/day.
  - Post-egg data: first incubation date, clutch size, hatch date; nestlings ringed and weighed multiple times (day 6 post-hatching; day 12); wing length measured; adults weighed and morphometrics recorded when captured at the nest.
  - Breeding success quantified as number of fledglings.
  - Data distributed across three files: Bird_Phenology (nestbox-level phenology and treatment), Nestlings (individual nestling measurements), Adults (adult morphometrics and identification).

## Data structure and files
- Seven CSV files, designed to be joinable by site and year (and by tree/nest identifiers where applicable).
  - site_details: site code, site name, mean latitude, longitude, elevation.
  - temperatures: site, year, hourly temperature columns (X46–X163); NA where data are missing.
  - Tree_Phenology: year, site, TreeID, taxon, fbb, cbb, flf, clf.
  - Branch_Beating: year, site, treeID, taxon, date, weather, recorder, caterpillar count, caterpillar.mass, notes, mass.uncertain.
  - Bird_Phenology: year, site, box, species, fed (first egg date), cs (clutch size), fki (first known incubation), clutch_swap_treatment, Hatching_first_recorded, uhe (unhatched eggs), v1date, v1alive, v1time, v2date, v2alive, v2time, suc (fledged).
  - Nestlings: year, site, box, ring, v1date, v1mass, v1ringer, v2alive, v2date, v2mass, v2wing, v2ringer, fledged.
  - Adults: ring, year, site, box, age, sex, wing, mass, date, time, ringer.
- Common keys
  - Site: three-letter code used consistently across all files.
  - Year: data collection year.
  - TreeID / box: enable linking to individual trees or nestboxes within a site.

## Data quality, limitations, and notes
- Data gaps and NA values exist where measurements were not recorded or were invalid (e.g., COVID-19 disruptions in 2020 led to partial data).
- Taxa records sometimes reflect genus-level taxonomy rather than species (e.g., some tree taxa).
- Branch mass recordings include a threshold (<0.02 g) when weighing did not register.
- Clutch treatment (clutch_swap_treatment) indicates experimental manipulation in nestboxes (2017–2019) and should be controlled for in analyses or nests excluded if necessary.
- Data collected are intended to be combined by site and year; longitudinal cross-site comparisons are supported through consistent coding.

## Access, use, and governance considerations for Data Leaders
- Clear metadata and consistent coding across files support data discoverability, interoperability, and reuse within and beyond the project network.
- The dataset enables integration of multi-taxa phenology with microclimate data to study trophic interactions and phenological mismatches.
- Potential for cross-network collaboration: harmonize with other datasets to build broader baselines, address data gaps, and improve sector-wide data standards and discovery.

## References
- Macphie, K., Samplonius, J.M., Hadfield, J.D., Pearce-Higgins, J. & Phillimore, A.B. (2020). Among tree and habitat differences in the timing and abundance of spring caterpillars. EcoEvoRxiv.
- Shutt, J.D., Bolton, M., Benedicto Cabello, I., Burgess, M.D. & Phillimore, A.B. (2018). The effects of woodland habitat and biogeography on blue tit territory occupancy and productivity along a 220 km transect. Ecography.
- Shutt, J.D., Burgess, M.D. & Phillimore, A.B. (2019a). A spatial perspective on the phenological distribution of the spring woodland caterpillar peak. American Naturalist.
- Shutt, J.D., Cabello, I.B., Keogan, K., Leech, D.I., Samplonius, J.M., Whittle, L. et al. (2019b). The environmental predictors of spatio-temporal variation in the breeding phenology of a passerine bird. Proceedings of the Royal Society B.