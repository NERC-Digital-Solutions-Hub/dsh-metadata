# EIDC dataset 2: Caterpillar masses from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

- Purpose and design
  - Dataset compares moth caterpillar communities and masses between lit and unlit transects in two habitat types: hedgerows and grass margins.
  - Matched-pairs design across 26 lit/unlit site pairs (plus one triplet) to isolate artificial light at night (ALAN) effects from urbanisation.
  - Sites are linear habitat strips with ≥60 m separation between lit and unlit sections; median transect separation is 118 m (range 60–527 m).

- Field sites and GIS context
  - Regions: Oxfordshire, Buckinghamshire, and Berkshire (southern England, UK).
  - GIS-informed site identification: street-light datasets overlaid on satellite imagery to locate potential transects; 153 locations visited virtually, 153 in person to confirm matching criteria.
  - Habitat controls: transects paired for comparable habitat; hedgerow trees presence recorded within 30 m; vegetation height compared at grass margins; sites with adjacent high-quality habitat or differing dominant plant composition excluded.
  - Habitat criteria: transects along straight roads (allowing up to 25° angle difference); lit/unlit transects geographically close (median 118 m).

- Lighting treatments and spectral characterization
  - Lighting types across lit transects: LED (14), HPS (11), LPS (2).
  - Illumination duration: lit transects remained fully lit throughout the night; no part-night lighting or dimming during sampling.
  - Lux measurements: five points per transect, at heights 1.25 m (hedgerows) and 0.25 m (grass margins); lit transects showed mean lux values with notable range (hedgerows 1.42–15.84 lux; grass margins 0.18–7.14 lux); unlit transects <0.01 lux (on overcast nights).
  - Spectral data: Ocean Optics USB2000+VIS-NIR-ES used for grass margins; CCT values: HPS ~2200 K, LPS ~1800 K, LEDs ~2700–4000 K (warm to neutral white); notes that lux is a proxy and spectral differences may affect ecologies differently.
  - CCT and spectral differences are contextualized to interpret potential biological responses beyond simple light intensity.

- Caterpillar sampling methods
  - Hedgerow (spring): beating method to sample deciduous woody feeders; 3 points per transect along a 14 m section; two beating approaches (drainpipes or beating tray) depending on hedge structure; sampling aimed at end of spring leaf-out period to minimize phenological artefacts.
  - Grass margins (winter): sweep netting for noctuid caterpillars on grasses and low-growing plants; transects typically 14 m, sometimes longer if habitat allowed; sampling conducted after sunset across multiple visits (mean total visits per site higher due to low catch rates).
  - Sampling timing: late-spring hedgerow sampling (May 2019, April 2020) and winter grass-margin sampling (Dec 2018–Apr 2019); sampling nights chosen to maintain comparable temperatures and conditions.
  - Temperature and time data: each sampling event recorded minutes past sunset and air temperature.

- Data collected and structure
  - Caterpillar data
    - Hedge data: 20 taxonomic units (including species, genera, family-level identifications, and unknowns); mass measurements for each caterpillar (mg); total caterpillars per transect recorded; separate mass datasets for hedgerows.
    - Grass margin data: 16 taxonomic units; 34 day-flying Lepidoptera included due to potential nocturnal larval exposure to ALAN; mass measurements recorded; total counts per transect.
    - Overall: 826 grass-margin caterpillars and 1021 hedgerow caterpillars weighed; mean masses: grass margins ~98 mg, hedgerows ~43 mg.
    - IDs: provisional IDs (Provisional_ID) and broader taxonomic resolution (ID2) stored for each specimen.
    - Visit and site references: Visit_ID, Site_ID, Sample_number per grass margin sample, and site-level identifiers.
  - Field sites data
    - Site metadata: Old_Site_ID, SiteID_Fig, Sampling_meth (Grass margin, Hedgerow, or both), Site_Name.
    - Lighting and location: Light_Type (unlit, LED, HPS, LPS); geospatial centroids for lit and unlit transects (E/N, lat/long); distance between transects (Dist_between_trans).
    - Habitat measurements: hedgerow characteristics (dominant plant species, hedge height/width), grass margin vegetation height (within 10 cm equivalence between lit/unlit).
    - Urban context metrics: area classifications within 100/250/500 m radii around transects classified as urban; proportions of urban landcover within those radii (Lit/unlit variants).
    - Spatial extents: Lit_transect_centroid and Unlit_transect_centroid coordinates; various radius-based landcover summaries (100/250/500 m) and proportions (Lit100s/urban, Lit250s/urban, Lit500s/urban, Unlit100s/urban, Unlit250s/urban, Unlit500s/urban).
  - Data storage and QA
    - Main datasets: Boyes_et_al_2021_hedgerows_mass.csv and Boyes_et_al_2021_grass_mass.csv.
    - Field sites data: Boyes_et_al_2021_field_sites_data.csv.
    - QA: standardized data collection forms, routine data entry checks within 24 hours of field visits, double-checking for outliers and transcription errors; most samples preserved at -20°C (COVID-19 interrupted some retention).

- How to use the dataset with GIS
  - Map lit vs unlit transects across hedgerow and grass-margin habitats to visualize spatial patterns in caterpillar masses.
  - Combine with urbanization and land-use rasters at multiple buffer scales (100/250/500 m) to assess potential confounding factors and interaction effects.
  - Analyze relationship between light type (LED/HPS/LPS), lux levels, and caterpillar mass distributions, accounting for sampling method and habitat type.
  - Integrate taxonomic-unit data to create spatially-enabled biodiversity indicators by habitat and light treatment.
  - Reproduce the matching approach (overlay street-light data, virtual site visits, in-person validation) for consistent GIS-based study designs.

- References and caveats
  - Core study context: Boyes et al. 2021 on how light pollution may drive moth population declines; caution on lux as a proxy for ecological illumination due to spectral differences.
  - Supplementary methodological references on sampling and hedgerow management and related ecological considerations.