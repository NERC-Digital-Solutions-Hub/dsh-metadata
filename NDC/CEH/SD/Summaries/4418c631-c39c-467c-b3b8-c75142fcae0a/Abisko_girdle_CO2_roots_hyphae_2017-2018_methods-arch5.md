# Methods for site descriptions, CO 2 efflux, root and hyphae ingrowth at a subarctic treeline, Abisko.

## Overview
- Document describes a girdling experiment near the Abisko Scientific Research Station, Sweden, measuring soil CO2 efflux, root ingrowth, and ectomycorrhizal (ECM) hyphal production.
- Data supporting Parker et al. (2020) are in two CSV files: Primetime_Abisko_2017_2018_NP2020_CO2efflux.csv and Primetime_Abisko_2017_2018_NP2020_roots_hyphae.csv.

## Site, experimental design and setup
- Location: forest-tundra ecotone 3–4 km south of Abisko Scientific Research Station (68°18 N, 18°49 E, ~600 m a.s.l.).
- Habitat: mountain birch forest (Betula pubescens ssp czerepanovii) and willow thickets (Salix lapponum).
- Plot structure: 0.88 km2 area with 5 willow plots (W) and 6 mountain birch plots (B); each plot divided into paired sub-plots (Birch: B1-6; Willow: W1-5).
- Pre-treatment setup (June 2017): central 3 m radius used for measurements; birch plots radii ≈ 10 m; willow plots ≈ 2 m; outer perimeters separated by 10–20 m, with 300–1100 m between pairs.
- Treatments: within each pair, one sub-plot girdled (G) and one control (C); girdling performed mid-June 2017.
- Girdling details:
  - Birch: all stems >1 cm diameter girdled within the 10 m radius; 4–8 cm of bark removed around the circumference down to xylem, ~30 cm above ground, severing phloem connections.
  - Willow: every willow stem girdled ~10–20 cm above ground; resprouts removed if observed.
  - Willow plots were trenched around the perimeter and lined with plastic to prevent root intrusion; birch plots were not trench-backed.
- Collars for CO2 measurements: three 5 cm tall, 15 cm inner-diameter PVC collars installed within 1 m of one central tree per birch plot and within central 1 m radius of willow plots; secured with plumber’s putty to seal soil surface.

## Data collection and measurements

- Soil CO2 efflux
  - Timing: two measurements after snowmelt (9–12 June 2017) before girdling; post-girdling measurements conducted across 10 dates in birch plots and 9 dates in willow plots during 2017, plus 10 dates in both in 2018.
  - Instrument: EGM-5 infrared gas analyser with CPY-5 darkened chamber.
  - Method: measure CO2 efflux from each collar; compute flux from linear CO2 rise over 90 seconds; replicate flux per plot = average of three collars.
  - Sampling design: if possible, covers all plots on the same day; order alternated to minimize temporal bias.

- Root ingrowth (root production)
  - Method: cylindroid fiber-glass mesh bags (6 cm deep, 2 mm mesh) filled with ericaceous peat collected on-site.
  - Deployment: one root ingrowth bag inserted per CO2 collar area, vertically into top 6 cm of organic soil, 30 cm from each collar.
  - Incubation: 96 days (2017) and 102 days (2018) per season; retrieved by cutting around bag, washing roots, drying at 60°C for 72 h, and weighing dry mass; carbon content measured with elemental analyser.

- Hyphal production (ectomycorrhizal fungi)
  - Method: sand-filled ingrowth bags (5 × 5 cm nylon mesh, 37 μm) filled with 18 g autoclaved Lake Torneträsk sand; bags thinner (0.5 cm) to ease fungal colonization.
  - Deployment: under litter layer, 30 cm from each CO2 collar, on the opposite side from root bags.
  - Incubation and processing: bags retrieved and sand processed to extract hyphae; hyphae-C content measured with elemental analyser after subtracting blank samples from non-field controls.

## Data files, provenance and references
- CO2 efflux data: Primetime_Abisko_2017_2018_NP2020_CO2efflux.csv
- Root and hyphae data: Primetime_Abisko_2017_2018_NP2020_roots_hyphae.csv
- Related publication: Parker et al. (2020) https://nph.onlinelibrary.wiley.com/doi/full/10.1111/nph.16573

## Quality assurance and data integrity
- Pre-girdling comparisons: paired t-tests on sub-plot characteristics showed no significant differences between girdled and control sub-plots prior to treatment.
- Collar seal validation: effectiveness demonstrated by systematic increases in CO2 concentration when a closed chamber is attached to collars.
- Replication and timing: multiple collars per plot; dates of measurement spread to capture growing-season dynamics; efforts made to randomize sampling order to minimize bias.

## Data governance and stewardship considerations
- Metadata needs:
  - Clear plot identifiers (B1-6, W1-5), girdling status (G/C), central tree references, collar IDs, and precise dates.
  - Context on plot sizes, distances between plots, and trenching status (especially for willow plots).
  - Description of girdling methods and timings, as well as leaf phenology notes (birch leaves present in 2018; willow leaves absent after girdling).
- Data standards:
  - Standardize units for CO2 efflux (likely mass-based flux per area per time), root/hyphae dry mass (g), and carbon content (% or g C).
  - Explicit variable definitions and calculation methods (e.g., how replicate flux is averaged across collars).
  - Document data provenance and processing steps (e.g., how collar data were quality-filtered and how blanks were treated for hyphae analyses).
- Data publication and access:
  - Ensure CSV files are versioned and accompanied by metadata describing methods, site specifics, and equipment.
  - Include cross-links to related publications (e.g., Parker et al. 2020) for context and reuse.
- Limitations and usability:
  - Note potential site-specific challenges (remote subarctic conditions, large plot distances, trenching in willow plots) that may affect generalizability.
  - Highlight gaps such as the absence of certain measurements in some plots or dates, and the 2018 differences in plant phenology.

## References
- Parker et al. (2020). Methods and data usage: https://nph.onlinelibrary.wiley.com/doi/full/10.1111/nph.16573