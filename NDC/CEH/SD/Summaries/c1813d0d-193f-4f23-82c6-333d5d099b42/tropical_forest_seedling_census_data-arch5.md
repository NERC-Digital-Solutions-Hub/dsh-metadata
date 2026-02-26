# Study site

- Location: Danum Valley Conservation Area (DVCA), unlogged primary forest, Sabah, Malaysia; adjacent partially logged Ulu Segama Forest Reserve (USFR).
- Area and climate: DVCA covers ~438 km2 with lowland dipterocarp forest and lower montane rainforest; USFR adjacent region sampled was logged 1981–1993. Mean annual rainfall ~2305 mm; mean daily temperature ~25.8°C.
- Landscape context: DVCA borders a large logging concession; USFR experienced interim silvicultural interventions including Reduced Impact Logging (RIL) trials and restoration efforts as part of rainforest rehabilitation projects.

## Study design and sampling

- Seedling plots: 1 m2 plots established in September–October 2019 within both DVCA (87 plots, primary forest) and USFR (96 plots; 52 actively restored, 44 naturally regenerating).
- Comparison framework: primary forest (unlogged) vs. logged forest (regeneration, with restoration subset).
- Data collection window: Mast fruiting event followed by four seedling censuses from Sep 2019 to Mar 2021.
- Census cadence: Four rounds (Census 1: Sep–Oct 2019; Census 2: Nov–Dec 2019; Census 3: Jan–May 2020; Census 4: Feb–Mar 2021).
- Typology and identification: Each fruit/seedling identified to species level in the field; unidentified species classified as morphospecies.
- Datasets: Counts of fruits and seedlings by species and plot across four censuses.

## Dataset structure and content

- Primary dataset: Danum_Valley_Seedling_Census.csv
- Core columns and meaning:
  - Forest: Primary (unlogged) or Logged (regeneration status)
  - Management: Management regime (Natural Regeneration or Active Restoration)
  - Seedling.Plot: Identifier for each 1 m2 plot
  - Family: Plant family name
  - Species: Scientific species name (unidentified species labeled as morphospecies)
  - Date.1 / Date.2 / Date.3 / Date.4: Census dates
  - Count.1 / Count.2 / Count.3 / Count.4: Counts of individuals at each census
- Dataset scope:
  - DVCA: 87 seedling plots
  - USFR: 96 seedling plots (52 actively restored; 44 naturally regenerating)
- Data granularity: Counts per species per plot per census; includes both fruit and seedling counts during the mast event.
- Metadata level: Explicit column descriptions and field-level definitions; dates and counts aligned with census events.

## Data collection methods and quality

- Field procedures: Species-level identification conducted in the field; morphospecies used where species could not be resolved.
- Temporal coverage: Four census rounds spanning Sep 2019–Mar 2021, enabling analysis of regeneration dynamics across restoration status and forest type.
- Data quality notes: Possible unidentified taxa (morphospecies) and potential variability in identification effort between plots; data are organized with explicit census dates and counts for reproducibility.

## Temporal and spatial scope

- Temporal: Four censuses between Sep 2019 and Mar 2021, aligned with mast fruiting dynamics.
- Spatial: Two forest contexts within a single study area: DVCA (primary forest) and adjacent USFR (logged forest with restoration trial).

## Data governance and sharing considerations

- Provenance: Collected under ForestGEO Danum Valley 50 ha network and INDFORSUS restoration project; data reflect both natural regeneration and active restoration treatments.
- Documentation: Includes clear schema for the CSV file and explicit definitions for each column, supporting interoperability and re-use.
- Considerations for data stewards:
  - Harmonize species identifications across plots and censuses; address morphospecies where present.
  - Track restoration status and logging history alongside ecological measurements to enable comparative analyses.
  - Ensure consistent date formats and census labeling to facilitate time-series analyses.
  - Plan for updates or additional censuses to maintain longitudinal continuity.

## Key takeaways for data stewardship

- The dataset provides a longitudinal view of seedling and fruit counts by species across primary and selectively logged forests, with clear separation between natural regeneration and active restoration plots.
- The data schema is concise but requires careful handling of morphospecies and consistent census dating for robust cross-plot comparisons.
- Excellent for studying the impacts of logging and restoration on seedling recruitment and forest regeneration within a well-documented experimental context.