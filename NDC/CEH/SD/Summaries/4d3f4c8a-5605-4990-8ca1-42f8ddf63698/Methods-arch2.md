# EIDC dataset 1: Caterpillar counts from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Purpose and context
- Uses standardized data to monitor environmental health and policy performance over time, focusing on the potential impacts of artificial light at night (ALAN) on moth caterpillars.
- Builds on methods and concepts from the Science Advances study Is street lighting detrimental to local insect populations (2021).

## Field sites and design
- Matched-pairs design comparing lit vs unlit sections within two habitat types: hedgerows and grass margins.
- 26 lit-unlit site pairs (plus one triplet with two lit sections of different light types); all pairs had identical habitat apart from ALAN, separated by ≥60 m (median ~118 m).
- Lighting treatments reflect current regional technologies: LED, high-pressure sodium (HPS), and low-pressure sodium (LPS); lit transects illuminated for at least five years, full-night operation.
- Sites were selected to minimize urbanization confounds via GIS overlays; urbanization measures were not strong predictors of caterpillar abundance in this design.
- Light intensity measured in lux at five points along each transect; measurements recorded at heights relevant to caterpillars (hedgerows: 1.25 m; grass margins: 0.25 m).

## Lighting characterization
- Spectral data collected for grass margins using a portable spectrometer; LED spectra estimated with Correlated Colour Temperature (CCT) values (LED 2700–4000 K; HPS ~2200 K; LPS ~1800 K); spectral data for hedgerows not available.
- Lux values varied by habitat type and lighting type, with unlit transects typically <0.01 lux on overcast nights.

## Sampling methods
- Caterpillar sampling used two methods to target two feeding guilds:
  - Hedgerow beating (spring) for deciduous-wood feeders.
  - Sweep net sampling (winter) for nocturnal grass/low-vegetation feeders.
- Sampling windows:
  - Hedgerow: mid-May 2019 and April 2020 (late spring and early spring periods chosen to minimize phenological artefacts).
  - Grass margins: December 2018 to April 2019 (mild nights; later converted times after sunset).
- Sampling protocol:
  - Beating: three points per transect (14 m long); multiple beating methods (drainpipes or beating tray) depending on hedge structure.
  - Sweep netting: standardized 14 m transects; continuous figure-of-eight sweeps; repeated visits to each site (most sites sampled ~4 times).
- Environmental data collected alongside caterpillars: time after sunset, temperature, transect length, and distance between lit/unlit transects.
- Specimen handling: all caterpillars retained (n = 826 grass margins; n = 1021 hedgerows) and identified by the lead author; some early-2020 samples not retained due to COVID-19 restrictions.

## Taxonomy and data products
- Hedgerow caterpillars: predominantly winter-flying geometrids and some micromoths; grouped into 20 taxonomic units.
- Grass-margin caterpillars: predominantly winter-flying noctuids; grouped into 16 taxonomic units.
- A subset of day-flying Lepidoptera (34 individuals) recorded due to potential nocturnal larval exposure to ALAN.
- Main outputs:
  - Hedgerow counts data: Boyes_et_al_2021_hedgerow_counts.csv
  - Grass margin counts data: Boyes_et_al_2021_grass_counts.csv
- Field-site metadata: Boyes_et_al_2021_field_sites_data.csv documenting site-level attributes and sampling context.

## Data structure and metadata
- Key columns in count data include:
  - Visit_ID, Site_ID, Site_Name, Date, DaysSince
  - Treatment_1 (lit/unlit) and Treatment_2 (lighting type: unlit, LED, HPS, LPS)
  - Time, Sunset, MinsPastSunset, Temp_Degree_Celsius
  - TransectOffset, All_Cats, DiurCats, NonDiurCats
  - Dist_between_trans, urbanization metrics (p100, p250, p500 for 100/250/500 m radii)
  - Hedge_Height, Dom_plant_species
- Field-site data includes coordinates, light type, transect centroids, mean illumination per habitat type, urban metrics, and distances between transects.

## Quality control and standardization
- Matched-pair selection based on a predefined criteria set to ensure comparability.
- All sampling conducted on the same nights to control for temperature effects.
- Standardized sampling protocols and data entry with dropdown menus; data entered within 24 hours of field visits.
- Specimens identified by an expert; data checks for outliers performed post-entry.
- Data stored as CSVs designed for easy integration into analyses and portals.

## Limitations and caveats
- Lux is a human-vision proxy and may not fully capture ecologically relevant light spectra experienced by caterpillars.
- Spectral data were only available for grass margins, not hedgerows; calibrations of spectral measurements were not fully standardized.
- Despite careful matching, some microclimatic or habitat variables could differ between lit and unlit transects.

## Relevance for environmental monitoring
- Provides a robust, standardized dataset suitable for time-series analyses of ALAN effects on larval Lepidoptera.
- Enables cross-study comparisons and integration with broader environmental monitoring datasets.
- Data are prepared for upload to appropriate data portals, with clear metadata and data dictionaries to facilitate reuse.

## References and related work
- Contextualized within literature on light pollution and insect population dynamics (e.g., Boyes et al. 2021; Longcore & Rich 2004; Maudsley et al. 2002; Merckx & Van Dyck 2019; Porter 2010).