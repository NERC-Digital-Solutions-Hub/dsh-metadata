# EIDC dataset 1: Caterpillar counts from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Aim
- Provide a dataset assessing the effects of artificial light at night (ALAN) on moth caterpillar communities.
- Compare lit versus unlit transects across two habitats (hedgerows and grass margins) using matched-pairs design.
- Use data to support analyses of long-term lighting treatments (LED, HPS, LPS) on caterpillars, with careful data quality and structure for reuse.

## Study design and sampling framework
- Matched-pairs design: 26 lit-unlit site pairs and one triplet (unlit with two lit sections) across hedgerows and grass margins.
- Habitat sampling methods:
  - Hedgerows: daytime beating for woody-plant feeders.
  - Grass margins: winter sweep-netting for grass- and low-vegetation feeders.
- Site matching criteria:
  - Lit and unlit transects geographically close (median 118 m; range 60–527 m).
  - Similar microclimate and vegetation within each pair; hedgerow trees, hedge height/width considered, and adjacent high-quality habitats avoided.
- Lighting context:
  - Treatments reflect current regional lighting: predominantly LED and HPS, with two LPS sites.
  - Lit transects had been illuminated with the same treatment for at least five years; no part-night operation during sampling.
- Urbanization controls:
  - GIS analyses indicated urbanization at various scales did not predict caterpillar abundance.
- Lighting measurements:
  - Lux readings at five points along each transect, at heights relevant to caterpillar perception ( hedgerows: 1.25 m; grass margins: 0.25 m).
  - Spectral data collected for grass margins; CCT values reported for lamp types (LED ~2700–4000 K; HPS ~2200 K; LPS ~1800 K).

## Caterpillar sampling and sampling design
- Sampling windows:
  - Hedgerows: spring visits (mid-May 2019 and April 2020) to bracket spring-time caterpillar activity.
  - Grass margins: winter sampling (Dec 2018–Apr 2019) after sunset to capture nocturnal feeders.
- Sampling methods:
  - Hedgerows: three points per transect; 14 m segments; beating using drainpipes or beating trays; multiple instars collected.
  - Grass margins: transects along verges or margins; continuous sweeps with a 50 cm net; repeated visits due to low counts.
- Temporal considerations:
  - Night sampling occurred after sunset (21:00–06:30), with recordings of time relative to sunset and temperature.
- Taxonomic units:
  - Hedgerow caterpillars: 20 taxonomic units (includes fully described species/genera and some undetermined).
  - Grass margins: 16 taxonomic units.
  - Additional day-flying Lepidoptera (34 individuals) included due to potential nocturnal larval impacts.
- Sample sizes:
  - Grass margins: 826 caterpillars collected.
  - Hedgerows: 1021 caterpillars collected.
- Special notes:
  - One site had changes during the study period (new street lights installed) and was treated accordingly in analyses.
  - Seasonal sampling chosen to minimize phenological artefacts related to ALAN.

## Measurements and data collection specifics
- Light measurements:
  - Lux readings across transects; hedgerow transects average lux 5.7 (range 1.42–15.84) and grass margins average lux 2.2 (range 0.18–7.14) for lit sections.
  - Unlit transects typically <0.01 lux.
  - Within habitat type, LED vs HPS readings were not significantly different.
- Spectral data:
  - Grass margin spectra recorded with Ocean Optics USB2000+VIS-NIR-ES; LED CCT estimated 2700–4000 K; HPS ~2200 K; LPS ~1800 K.
  - Spectral data limited to grass margins due to equipment availability.
- Data quality and timing:
  - All sampling conducted on the same nights within site pairs to control temperature.
  - Standardized data entry and quality checks; specimens stored at -20°C (except some 2020 samples due to COVID-19 access limits).

## Data structure and files
- Main data files:
  - Boyes_et_al_2021_hedgerow_counts.csv: hedgerow caterpillar counts by sampling event.
  - Boyes_et_al_2021_grass_counts.csv: grass margin caterpillar counts by sampling event.
- Field site data:
  - Boyes_et_al_2021_field_sites_data.csv: site-level information, including light type, transect centroids, urban metrics, and transect distances.
- Key data columns (examples):
  - Visit_ID, Site_ID, Site_Name, Date, DaysSince, Treatment_1 (Lit/Unlit), Treatment_2 (Unlit, LED, HPS, LPS), Time, Sunset, MinsPastSunset, Temp_Degree_Celsius, TransectOffset, All_Cats, DiurCats, NonDiurCats, Hedge_Height, Dom_plant_species.
  - Urban metrics: p100/p250/p500 urban area proportions around transect centroids; 100/250/500 m radius metrics.
  - Lighting details: Lit_transect_centroid coordinates and unlit transect coordinates; light type and mean illumination in hedgerow and grass margin contexts.
- Documentation and references:
  - Data linked to Boyes et al. 2021 and relevant foundational references on ecological light pollution.

## Accessibility, use, and limitations
- Data are prepared for secondary analysis of ALAN effects on Lepidoptera, enabling comparisons across lit vs unlit conditions and across habitat types and lamp technologies.
- Limitations:
  - Lux is a human-vision-based measure; spectral differences may affect caterpillars differently.
  - Spectral data are limited to grass margins; hedgerows lack spectral measurements in this dataset.
  - Some field data were not retained due to COVID-19 restrictions.
- References included for context and methodology:
  - Boyes et al. 2021 (Is light pollution driving moth population declines? A review of causal mechanisms across the life cycle).
  - Additional methodological references on ecological lighting and hedgerow sampling.