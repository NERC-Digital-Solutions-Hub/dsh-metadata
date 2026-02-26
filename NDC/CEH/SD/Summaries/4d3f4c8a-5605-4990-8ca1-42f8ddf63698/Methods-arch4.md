# EIDC dataset 1: Caterpillar counts from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

- Purpose and basis
  - Dataset derived from a study on how artificial light at night (ALAN) affects moth caterpillar communities.
  - Methods align with the Science Advances 2021 study on light pollution and insect populations.
  - Designed to disentangle ALAN effects from urbanisation by using matched lit/unlit transects across two habitat types.

- Study design and site pairing
  - Matched-pairs design across two habitats: hedgerows and grass margins.
  - 26 lit/unlit site pairs plus one triplet where lit sections differed by street light type.
  - Pairs selected from GIS overlays of street lights; verified with Google Street View and on-site checks.
  - Criteria to ensure comparability: transects within ~60–527 m apart (median 118 m), straight road alignment, similar vegetation structure, and consistent agricultural management within pairs.
  - Exclusions: hedgerow trees differing between lit/unlit within a pair (n=8) and sites adjacent to high-quality habitat (n=2).

- Lighting treatments and environmental context
  - Lit transects illuminated by peak regional lighting technologies: LED, HPS, and two LPS sites.
  - Lit sections had maintained lighting for at least five years; entire night-time illumination (no part-night lighting).
  - Lux measurements taken at five points along each transect, vertical heights 1.25 m (hedgerows) and 0.25 m (grass margins).
  - Spectral data collected for grass margins only; CCT values used to contextualize color temperature:
    - HPS ~2200 K, LPS ~1800 K; LEDs estimated 2700–4000 K.
  - Urbanisation context captured as area-based metrics within 100/250/500 m radii around transect centroids.

- Caterpillar sampling methods
  - Hedge row sampling: beating in spring to target woody-plant feeders.
    - Sampling times: mid-May 2019 and mid-April 2020 (end/start of spring caterpillar activity).
    - Three transect points per transect; two hardware methods (drainpipes for box hedges, beating trays) to dislodge caterpillars.
    - Focus on more mature instars (late spring sampling targeted 4th/final instar; early spring targeted 1st/2nd instar) to minimize phenological bias.
  - Grass margins sampling: sweep netting for nocturnal grass-feeding caterpillars in winter.
    - Sampling window: December 2018–April 2019, typically after sunset (21:00–06:30), on mild nights (min temp ≥ 6°C).
    - 14 m transects; continuous 2D sweep pattern; transects separated by ~10 minutes per lit/unlit pair.
    - Most sites sampled ~4 times; one site had a shorter sampling period due to lighting changes.
  - Sample handling: all caterpillars preserved for later identification; total counts reported per transect.

- Taxonomic resolution and data scope
  - Hedge rows: 20 taxonomic units (mostly winter-flying geometrids and some micromoths).
  - Grass margins: 16 taxonomic units (noctuids; some day-flying larvae included due to nocturnal larval stages).
  - Included 34 day-flying Lepidoptera caterpillars in analyses.
  - Total counts: grass margins (n=826) and hedgerows (n=1021) across sampling events.

- Data quality control and management
  - Standardised data collection forms; data entered into Excel with dropdowns to ensure consistency.
  - Data entry completed within 24 hours of field visits; subsequent double-checking for errors and outliers.
  - Specimens stored at -20°C (except some 2020 samples not retained due to COVID-19 restrictions).
  - Documentation and metadata aligned with dataset files and accompanying descriptions.

- Data structure and files
  - Main data files:
    - Boyes_et_al_2021_hedgerow_counts.csv (hedgerow caterpillar counts)
    - Boyes_et_al_2021_grass_counts.csv (grass margin caterpillar counts)
  - Field site metadata:
    - Boyes_et_al_2021_field_sites_data.csv
  - Key data columns (examples):
    - Visit_ID, Site_ID, Site_Name, Date, DaysSince, Treatment_1 (Lit/UL), Treatment_2 (LED/HPS/LPS), Time, Sunset, MinsPastSunset, Temp_Degree_Celsius, Dist_between_trans, All_Cats, DiurCats, NonDiurCats, Hedge_Height, Dom_plant_species
    - Light_Type, Lit_transect_centroid/eastings/northings/lat/long, Unlit_transect_centroid/eastings/northings/lat/long
    - Urban metrics: Lit/Unlit 100/250/500 m urban area and proportion (Lit100s/urban, etc.)
  - Data collection controls:
    - Transect length, vegetation height matching, dominant plant species, and habitat consistency within pairs.

- Limitations and considerations
  - Lux measures reflect human vision; ecological relevance may differ due to spectral sensitivity of insects.
  - Spectral data limited to grass margins due to instrument access; lighting spectra across hedgerows assumed similar.
  - Spatial matching aimed to separate ALAN effects from urbanisation, though complete decoupling is challenging.

- References and context
  - Primary linkage: Boyes, D. H. et al. (2021) Is light pollution driving moth population declines? A review of causal mechanisms across the life cycle.
  - Related methodological references on ecological light pollution and hedgerow sampling.

- Practical relevance for data governance
  - Demonstrates robust data lifecycle: design-based pairing, standardized field methods, rigorous QA/QC, structured metadata, and clear data file organization.
  - Provides rich variables for evaluating data usability, discoverability, and reusability in a data strategy context (e.g., documentation of data provenance, data lineage, and interoperability across datasets).