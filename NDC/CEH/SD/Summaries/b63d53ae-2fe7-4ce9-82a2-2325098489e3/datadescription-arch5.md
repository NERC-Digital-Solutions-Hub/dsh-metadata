# EIDC dataset: Tritrophic phenology and associated data from 44 sites in Scotland, 2014-2021

## Overview and scope
- Multi-site, multi-year dataset describing interactions among trees, caterpillars, and birds across 44 woodland sites in Scotland (Edinburgh to Dornoch) from 2014 to 2021.
- Data collected include: temperature, tree phenology, caterpillar abundance/mass, blue tit nestbox phenology, nestlings, and adult blue tit metrics.
- Fieldwork varied by year (e.g., 2020 COVID-19 disruptions with later start and reduced data collection in southern sites).

## Data collected and variables
- Temperature
  - Hourly air temperatures recorded at two loggers per site (approx. 1.5 m above ground, north side of tree trunks).
  - Data cover mid-February to mid-June; logged as hourly values.
- Tree phenology (Tree_Phenology)
  - For a representative set of deciduous taxa per site.
  - Phenophases tracked: first budburst (fbb), complete budburst (cbb), first leaf (flf), complete leaf (clf).
  - Taxon may be species or genus; records linked by site, year, and TreeID.
- Caterpillars (Branch_Beating)
  - Branch beating at selected trees starting after 45% of trees reached first leaf.
  - Counts of caterpillars dislodged and total mass (grams); mass < 0.02 g recorded as < 0.02 g.
  - Additional fields: date, weather, recorder, notes, mass uncertainty.
- Blue tit nestbox phenology (Bird_Phenology)
  - Nestbox-level breeding data: first egg date, clutch size, first incubation date, hatching, and fledging outcomes.
  - Includes a clutch swap treatment variable for experimental manipulation in 2017–2019.
  - Hatching records, incubation status, and timing data with multiple visit dates.
- Nestlings (Nestlings)
  - Individual nestling data across visits: dates, mass (g) on first/second visit, wing length (mm), ringer IDs.
  - Outcomes include fledging status per nestling.
- Adults (Adults)
  - Adult blue tit measurements: ring ID, age, sex, wing length (mm), mass (g), capture date/time, ringer ID.
- Metadata and linkage
  - All files share site identifiers (three-letter site code) and year; datasets can be combined by site and year.
  - Unique IDs: TreeID for trees, box for nestboxes; data matrices are designed to be joined across files via site/year and IDs.

## Data structure and file layout
- Total of 7 CSV files:
  - site_details: site, Name, MeanLat, MeanLong, MeanElev.
  - temperatures: site, Year, X46–X163 (hourly temperature data); NA where missing.
  - Tree_Phenology: Year, site, TreeID, taxon, fbb, cbb, flf, clf.
  - Branch_Beating: Year, site, treeID, taxon, date, weather, recorder, caterpillar, caterpillar.mass, notes, mass.uncertain.
  - Bird_Phenology: Year, site, box, species, fed (first egg date), cs (clutch size), fki (first incubation), clutch_swap_treatment, Hatching_first_recorded, uhe, v1date, v1alive, v1time, v2date, v2alive, v2time, suc (fledged), etc.
  - Nestlings: Year, site, box, ring, v1date, v1mass, v1ringer, v2alive, v2date, v2mass, v2wing, v2ringer, fledged.
  - Adults: ring, year, site, box, age, sex, wing, mass, date, time, ringer.
- Data can be merged across files using site code and year; the same site-year combination appears in multiple files with consistent IDs.

## Data quality, provenance, and governance
- Data provenance
  - Authors affiliated with the University of Edinburgh; multiple studies cited (Shutt et al. 2018, 2019; Macphie et al. 2020; Phillimore et al.).
  - Measurements follow standardized protocols described in accompanying literature.
- Data quality and caveats
  - 2020 field season affected by COVID-19: partial data collection; southern sites (22 of 44) received regular visits, others may have missing data.
  - Some variables use ordinal or categorical representations (e.g., weather, clutch_swap_treatment) that require careful interpretation in analyses.
  - Missing data represented as NA or special codes (e.g., -999 in Bird_Phenology) and should be excluded or handled appropriately in analyses.
  - Mass measurements for caterpillars with very small weights may be recorded as <0.02 g.
  - Clutch swap treatments in Bird_Phenology require control/adjustment in analyses to avoid confounding.
- Data stewardship considerations
  - Clear site coding (three-letter codes) and year keys facilitate data discovery and integration.
  - Documentation provides detailed column definitions to support reproducibility and metadata quality.
  - Updates and versioning implied by annual data collection; researchers should note year-specific changes (e.g., COVID-19 impacts, trek timing).

## Access, use, and updates
- Data are organized for portal upload and cataloguing as part of a data sharing workflow.
- Users should account for:
  - Potential data gaps due to 2020 disruption.
  - Variable definitions that may differ slightly across years or in nested subdatasets.
  - The need to align early- and late-year sampling windows when combining across years.
- Potential reuse
  - Cross-trophic phenology analysis (temperature, tree phenology, caterpillar abundance, bird breeding phenology and success).
  - Spatial comparisons across 44 sites and temporal trends across 2014–2021.
  - Studies incorporating climate and habitat gradients, and the effects of road proximity on phenology.

## Limitations and caveats
- Incomplete data for certain years/sites (notably 2020 disruptions).
- Some phenology and breeding metrics may be affected by experimental treatments (e.g., clutch swaps) requiring adjustment in analyses.
- Data are longitudinal but nested (trees within sites), necessitating appropriate statistical models to account for hierarchical structure.

## References and related publications
- Macphie, K., Samplonius, J.M., Hadfield, J.D., Pearce-Higgins, J. & Phillimore, A.B. (2020). Among tree and habitat differences in the timing and abundance of spring caterpillars. EcoEvoRxiv.
- Shutt, J.D., Bolton, M., Benedicto Cabello, I., Burgess, M.D. & Phillimore, A.B. (2018). The effects of woodland habitat and biogeography on blue tit territory occupancy and productivity along a 220 km transect. Ecography.
- Shutt, J.D., Burgess, M.D. & Phillimore, A.B. (2019a). A spatial perspective on the phenological distribution of the spring woodland caterpillar peak. American Naturalist.
- Shutt, J.D., Cabello, I.B., Keogan, K., Leech, D.I., Samplonius, J.M., Whittle, L. et al. (2019b). The environmental predictors of spatio-temporal variation in the breeding phenology of a passerine bird. Proceedings of the Royal Society B.