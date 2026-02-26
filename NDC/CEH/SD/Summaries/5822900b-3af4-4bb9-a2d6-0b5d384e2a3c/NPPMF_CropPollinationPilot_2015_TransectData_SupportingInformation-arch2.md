# NPPMF_CropPollinationPilot_2015_TransectData_SupportingInformation

## Overview
- Contains data on insects visiting flowers of three crops: apples, field beans, and oilseed rape.
- Collected from 13 flowering crop fields by teams at the University of Reading and the James Hutton Institute (Scotland).
- Data gathered by a mix of recorders (novice, researchers, farmers/agronomists); not all recorders sampled all transects on every day.

## Study design and data collection
- Transect surveys: observers record all flower-visiting insects in a moving area 1m ahead and 1m to the side along a 50m straight line transect over 10 minutes.
- At each field site, 4 transects were surveyed by different recorders.
- Weather data captured with a Kestrel weather recorder before every transect or once during the survey.
- Floral density measurements:
  - Oilseed rape and field beans: estimate flowers per square metre by counting plants per m2 at three transect locations; count flowers per plant on five random plants per location; compute total flowers per m2.
  - Apples: count trees along the transect; estimate density using flowers on three trees along the transect.
- Data coverage notes: multiple recorders involved; some recorders were novice; not all transects were sampled on every field/day.

## Data structure and variables
- Core identifiers:
  - Crop, Site (e.g., RD = Reading team, JHI = James Hutton Institute), Date, Recorder (unique code), Recorder type (Novice, Researcher, Farmer/Agronomist), Transect, Start time, Finish time.
- Weather and habitat context:
  - Temp C, Av wind mph, Max wind mph, Cloud %.
- Floral density and pollinator metrics:
  - Flowers/m2, Flowers/transect.
- Pollinator counts (by taxa):
  - Honeybee; Bombus terrestris/lucorum; Bombus hortorum; Bombus pratorum; Bombus pascuorum; Bombus lapidarious; Bombus hortorum (listed twice in the header); Bombus unknown/unidentified; Andrena sp.; Helictid sp.; Solitary bee unknown/unidentified; Hoverfly unknown/unidentified; Other Diptera; Butterfly; Moth; Coleoptera; Other invertebrate.
- Quality Assurance: No specific quality assurance was performed for the dataset.

## Quality and limitations
- No formal quality assurance performed, which has implications for data reliability and subsequent analyses.
- Variation in recorder expertise (novice to professional) and incomplete sampling across transects and days may affect consistency and comparability.

## Data management and accessibility
- The document provides column headers and descriptions to standardise interpretation.
- While it notes standardised data collection practices and storage/upload expectations in general, explicit instructions for dataset storage, versioning, or portal submission for this specific file are not detailed.

## Potential uses for environmental analysts
- Assess pollinator visitation patterns across different crops and field conditions.
- Explore relationships between pollinator counts, weather variables, and floral density.
- Establish baseline pollination activity for apples, beans, and oilseed rape to inform sustainability and agricultural policy evaluations.
- Facilitate cross-study comparisons by using standardised field definitions and measurement approaches.

## Considerations and caveats
- When integrating with other datasets, account for potential biases due to varied recorder expertise and incomplete transect coverage.
- The lack of QA suggests a need for data cleaning and validation prior to high-stakes analyses or policy reporting.
- Metadata completeness (e.g., occasional NA values for weather variables) should be considered in analyses and when calculating derived metrics.