# NPPMF_CropPollinationPilot_2015_TransectData_SupportingInformation

## Overview
- Dataset on insects observed visiting flowers of three crops: apples, field beans, and oilseed rape.
- Collected from 13 flowering crop fields by teams at the University of Reading and the James Hutton Institute (Scotland).
- Data gathered by a mix of recorders with varying experience (novice, researchers, farmers/agronomists); not all recorders sampled every transect or field each day.

## Methodology
- Transect surveys: moving observation area 1 m ahead and 1 m to the side, along a 50 m straight transect down a crop tramline over 10 minutes.
- At each field site: 4 transects surveyed by different individuals.
- Weather data captured with a Kestrel weather reader before each transect or once per day.
- Floral density measurements:
  - Oilseed rape and beans: plants per m² counted at three transect locations; flowers per plant counted on 5 plants per location to estimate flowers per m².
  - Apples: number of trees along the transect counted; flowers on 3 trees along the transect used to estimate density.
- Site coding: Crop, Site (RD = Reading team, JHI = James Hutton Institute), Date, Recorder, Recorder type.
- Core timing fields: Start time, Finish time.
- Weather and environment fields: Temp C, Av wind mph, Max wind mph, Cloud %.
- Sampling effort details: Transect identifiers and the specific transect within the field.

## Dataset Structure and Key Variables
- Core fields:
  - Crop, Site, Date, Recorder, Recorder type, Transect, Start time, Finish time.
- Weather and environmental measures:
  - Temp C, Av wind mph, Max wind mph, Cloud % (with notes on NA/missing values and variability in per-transect versus per-day recording).
- Floral and visitation metrics:
  - Flowers/m2, Flowers/transect.
  - Pollinator counts by taxon: Honeybee; Bombus spp. (terrestris/lucorum, hortorum, pratorum, pascuorum, lapidarius); Bombus unknown/unidentified; Andrena sp.; Helictid sp.; Solitary bee unknown/unidentified; Hoverfly unknown/unidentified; Other Diptera; Butterfly; Moth; Coleoptera; Other invertebrate.
- Data provenance:
  - Records linked to crop field, site code, date, and recorder (with a descriptor of recorder type).

## Quality Assurance and Data Quality
- Explicit QA not performed for this dataset (No specific quality assurance documented).
- Variability introduced by:
  - Mixed recorder experience levels (novice to expert).
  - Incomplete sampling (not all recorders sampled all transects or days).
  - Missing environmental data (NA values for Temp, Wind, etc., in some transects/days).
  - Differences in data collection approaches between crops (e.g., density estimation methods differ by crop).

## Data Governance and Stewardship Considerations
- Recording of metadata is essential to interpret variability:
  - Recorder identifiers, recorder type, and field/site codes for traceability.
  - Clear transect identifiers and timing to enable replication and re-analysis.
  - Explicit handling and documentation of NA values and when data were collected (per transect vs. per day).
- Standardization needs:
  - Harmonization of species naming and taxonomic resolution for pollinators.
  - Consistent units and calculation methods (e.g., Flowers/transect derived from Flowers/m2 and transect length; ensure reproducibility across crops).
- Data quality improvements:
  - Implement lightweight QA steps (range checks, cross-field consistency, outlier review).
  - Consider follow-up for missing weather data or incomplete transect coverage.
- Data accessibility and reuse:
  - Documentation of sampling effort and limitations to inform downstream analyses (e.g., pollinator visitation studies, weather-flower interactions).
  - Ensure metadata supports discovery, interoperability, and proper contextualization for large datasets.

## Limitations and Challenges
- Incomplete picture of user needs and priorities may apply to downstream users.
- Timeliness and completeness of data submission (some recorders may not have provided full transect coverage or all fields).
- Diverse systems/formats due to multi-institutional collaboration complicates standardization.
- Large data volume with per-transect variation and potential gaps due to NA values.

## Potential Uses and Implications
- Analyses of pollinator visitation patterns across crops and sites.
- Investigations of relationships between weather variables, floral density, and pollinator activity.
- Baseline for improving transect-based pollination surveys and informing pollination management in agriculture.
- Framework for data governance in multi-institution ecological datasets, emphasizing metadata, QA, and standardization.