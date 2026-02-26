# Raw data sets on the behaviour and distribution of Lepidoptera (butterflies and day flying moths) at the Stonehenge Landscape in 2011

## Overview and purpose
- Provides raw data on Lepidoptera behaviour and distribution at the Stonehenge Landscape in 2011, with accompanying botanical data (flowering units and percent cover).
- Data quality assurance performed to identify outliers and anomalies using species occurrence expectations and exploratory analysis.
- Documented background, study design, and data collection methods to enable reuse and interpretation.

## Study site and sampling design
- Location: Stonehenge World Heritage Site, Wiltshire, UK; four chalk grassland fragments (Full-moon Bank, Luxenborough Bank, Winterbourne Stoke Group, Fargo Barrow) within the Stonehenge Landscape estate.
- Landscape features: small fragments (0.22–1.98 ha) of ancient chalk grassland on slopes with burial mounds; management involves sown chalk grassland seed mixtures.
- Survey layout:
  - 14 survey boundaries (20 m x 20 m) placed on fragment-adjacent land cover boundaries; two boundaries per fragment edge when edges run north–south; Fargo Barrow had two boundaries due to size.
  - Control surveys in continuous habitat within fragments and adjacent land cover, with a dummy boundary for comparison.
- Boundaries and controls used to assess Lepidoptera behaviour at habitat edges versus interior/other land-cover types.

## Data collection methods and structure
- Lepidoptera surveys (May–July; 10:00–16:00) aimed to sample across different times of day to reduce time-of-day effects.
- Methodology:
  - 20 m x 20 m survey areas centered on each boundary or control.
  - Flight paths of individual Lepidoptera tracked for up to 3 minutes per individual; stops longer than 3 minutes or movements beyond 20 m from the boundary end the observation for that individual.
  - Each boundary surveyed for a total of 20 minutes per month (May, June, July) with equal effort on chalk grassland and adjacent land cover.
  - Exiting behaviour categorized as: crossing, following, avoiding; if no exit or path too convoluted, then staying.
  - Attempts to minimize pseudoreplication by selecting different species or sexes for each flight path and spacing replicates by about 15 days.
  - Weather criteria aligned with UK Butterfly Monitoring Scheme standards.
- Vegetation and nectar data:
  - Four 0.5 m x 0.5 m quadrats per boundary (two on chalk side, two on adjacent land cover) to measure vegetation height/density, bare ground, and nectar resources (flowering units; families: Asteraceae, Fabaceae, Dipsacaceae).
  - Botanical surveys conducted twice between May and August.
- Auxiliary data:
  - Wind speed and direction from the nearest meteorological station (Boscombe Down, ~6.5 km away) recorded hourly.
- Data content and codification:
  - Datasets include “DATA Lepidoptera Behaviour” and “DATA Resources Behaviour” with standardized columns and codes (e.g., DATE, TEMP, WIND SPEED, WIND DIRECTION, REP, MATRIX TYPE, LOCATION, SURVEY, SIDE OF LOCATION, SHELTERED/EXPOSED, START/END TIME, SPECIES, SPECIES CODE, SEX, BEHAVIOUR, HABITAT TYPE START/END, MOVEMENT DIRECTION, NOTES; for resources: quadrat measures, drop disc, bare ground, dead vegetation, plant/resource codes, flowering units).
  - Data dictionaries and column keys provided (e.g., table 1-2, 1-3, 1-4, 1-5, and 1-6 references) to interpret fields and codings.
- Location and identifiers:
  - Location codes for fragments (e.g., WSG, Fargo, Full, Lux) and edge/centre designations; grid references in British National Grid (BNG) format included in the datasets.

## Nomenclature and data dictionaries
- Lepidoptera nomenclature follows standard field guides; plant nomenclature follows Stace (2010).
- Tables provided for:
  - Lepidoptera species surveyed with scientific names, common names, and abbreviated species codes (e.g., Ads.sta = Forester, Pie.nap = Green-veined White).
  - Flowering plant species with scientific names and abbreviated codes (e.g., Agr.eup = Agrimony, Cam.glo = Clustard Bellflower).
- Key lists and codes enable consistent data entry and cross-dataset linking.

## Metadata and data quality considerations
- Data quality assurance included checks for outliers and anomalies using pivot tables and exploratory analysis (details not shown).
- Specimen capture/recapture not used; measures taken to minimize pseudoreplication by species/sex rotation and time spacing between replicates.
- Weather and site conditions are captured to support contextual interpretation (temperature, cloud cover, wind, shelter/exposure).
- Metadata coverage includes:
  - Date, time windows, location boundaries, side of location, habitat type, boundary status (edge, restoration, arable, chalk).
  - Replicate numbers, boundary/control designation, and measurement units.

## Data governance, storage, and sharing considerations for Data Stewards
- Structure is designed for sharing with clear data dictionaries, standardized codes, and explicit field definitions.
- Datasets align with published methodologies, enabling replication and secondary analysis.
- Key governance actions:
  - Preserve and publish the two primary data sheets (Lepidoptera Behaviour; Resources Behaviour) with their respective field definitions.
  - Maintain the species and plant nomenclature tables and their codes to ensure interoperability with other datasets.
  - Document all measurement methods, boundary definitions, replication cadence, and weather/edge conditions as provenance.
  - Ensure careful handling of boundary vs control designations and habitat categories to support edge-effect analyses.
  - Include references to governing standards (e.g., Pollard & Yates 1993) for weather/season criteria to support reuse.

## Limitations and considerations for reuse
- Data pertain to a specific year (2011) and site (Stonehenge Landscape chalk grassland fragments); applicability to other sites or years requires caution due to local habitat and management differences.
- Pseudoreplication controls described are important for correct interpretation of behavioural categories.
- Some data fields reference tables or figures (e.g., figures showing boundary setups) that should be consulted for precise replication of methods.

## References and nomenclature sources
- Field and nomenclature references underpinning species and plant identifications, as well as survey design and vegetation measurement methods (e.g., Hardy et al. 2007; Langmaid et al. 1989; Pollard & Yates 1993; Stace 2010; Stewart et al. 2001).