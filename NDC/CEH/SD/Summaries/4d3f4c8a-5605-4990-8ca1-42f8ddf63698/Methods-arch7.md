# EIDC dataset 1: Caterpillar counts from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Overview
- Dataset compares moth caterpillar communities at lit vs unlit transects in hedgerows and grass margins using a matched-pairs design.
- Lit transects used current lighting technologies (mostly LED and HPS; a few LPS) with five-year continuity.
- Includes spatially explicit methods and measurements to disentangle ALAN effects from urbanisation.
- Spectral data collected for grass margins; lux-based light intensity measurements at canopy-relevant heights.
- Data intended for GIS-enabled analysis of spatial patterns and lighting effects on insect communities.

## GIS and sampling design (spatial framework)
- Street-light locations overlaid on satellite imagery to identify lit/unlit linear habitat sections.
- Virtual site visits (Google Street View) followed by in-person checks to confirm comparable habitat.
- Matched lit/unlit transects: median 118 m apart (range 60–527 m); straight-road alignment to minimise microclimate differences.
- Habitat controls: no hedgerow trees differ between paired transects; grass margins matched for vegetation height; exclusion of nearby high-quality habitats.
- Urbanisation metrics derived from CEH 2017 landcover; radii buffers of 100, 250, and 500 m used to quantify surrounding urban area (p100/p250/p500 and LitUnlit equivalents).

## Field sampling design and methods
- Two sampling guilds:
  - Hedgerow beating (spring) for woody/deciduous feeders.
  - Grass-margin sweep netting (winter) for noctuid grass feeders.
- Sampling schedule aligned with moth caterpillar phenology to reduce artefacts.
- Transect specifications: typically 14 m length, three sampling points per transect, with equipment adapted to hedge structure.
- Light measurements: lux readings at five points along each transect, at heights relevant to caterpillars (1.25 m for hedges; 0.25 m for grass margins); readings taken on cloudy/new-moon nights.
- Time and condition data recorded: time after sunset, temperature, transect offset, and relative distance between lit/unlit transects.

## Data collection and structure
- Two main count datasets:
  - Boyes_et_al_2021_hedgerow_counts.csv
  - Boyes_et_al_2021_grass_counts.csv
- Field-site metadata:
  - Boyes_et_al_2021_field_sites_data.csv
- Key fields include:
  - Site identification (Visit_ID, Site_ID, Site_Name)
  - Treatment (Lit/UL; LED/HPS/LPS)
  - Temporal context (Time, Sunset, MinsPastSunset)
  - Environment (Temp_Degree_Celsius, Dist_between_trans)
  - Caterpillar totals by category (All_Cats, DiurCats, NonDiurCats)
  - Habitat metrics (Hedge_Height, Dom_plant_species; vegetation height for grass margins)
  - Urban context (p100/p250/p500_urban, Lit100s/urban, Unlit100s/urban, etc.)
  - Spatial coordinates for transect centroids (Lit_transect_lat/long, Unlit_transect_lat/long)

## Lighting, spectra, and interpretation
- Lighting treatments characterized by lamp type (LED, HPS, LPS) and relative spectral output.
- Spectral data (Grass margins only) collected with Ocean Optics USB2000+VIS-NIR-ES; CCT values estimated:
  - HPS ~ 2200 K
  - LPS ~ 1800 K
  - LED 2700–4000 K (warm white to neutral white)
- Notes on lux vs ecological relevance:
  - Lux reflects human vision; spectral differences may affect insects differently despite similar lux.
  - Spectral data not calibrated; readings provide relative rather than absolute spectral quantities.

## Data quality, matching, and management
- Matched-pair design established via predefined criteria; all sites sampled on the same nights where possible.
- Standardised field forms and Excel-based data capture with automated calculations.
- Post-collection quality checks include cross-checking entries and outliers; samples stored at -20°C (except some 2020 samples due to COVID-19 restrictions).

## Data availability and formats
- Main datasets available as CSV files:
  - Hedge rows: Boyes_et_al_2021_hedgerow_counts.csv
  - Grass margins: Boyes_et_al_2021_grass_counts.csv
- Site metadata: Boyes_et_al_2021_field_sites_data.csv
- Documentation includes detailed column descriptions and data structure for integration into GIS workflows.

## Practical implications for GIS work
- Enables creation of spatial layers for lit/unlit transects, with precise coordinates, lengths, and centroids.
- Supports calculation of urban exposure metrics around transects using 100/250/500 m buffers.
- Facilitates join operations between caterpillar counts and lighting/land-cover attributes for spatial analyses of ALAN effects.
- Provides a framework to reproduce matched-pairs analyses across habitat types (hedgerows vs grass margins) in GIS.

## Limitations and cautions
- Lux as a proxy for ecologically relevant lighting may not capture spectral ecological effects.
- Spectral data limited to grass margin sites; hedgerow spectra not characterized.
- Uncalibrated spectrometer readings; caution when comparing across lamps without calibration.

## References
- Boyes et al. (2021) Is light pollution driving moth population declines? A review of causal mechanisms across the life cycle.
- Longcore & Rich (2004); Maudsley et al. (2002); Merckx & Van Dyck (2019); Porter (2010); Staley et al. (2016).