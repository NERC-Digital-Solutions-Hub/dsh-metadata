# NPPMF_CropPollinationPilot_2015_TransectData_SupportingInformation

## Overview
- Dataset on insects observed visiting flowers of three crops: apples, field beans, and oilseed rape.
- Collected from 13 flowering crop fields by teams at the University of Reading and the James Hutton Institute (Scotland).
- Data collected by diverse recorders (novice, researchers, farmers/agronomists); not all recorders sampled all transects on any given day.

## Sampling Design and Field Protocol
- Transect method: moving observation area 1 m ahead and 1 m to the side; along a 50 m straight transect down a crop tramline over 10 minutes.
- At each field site, 4 transects were surveyed by different recorders.
- Weather data captured with a Kestrel weather recorder before each transect or once during the survey day.
- Floral density:
  - Oilseed rape and beans: estimated by counting plants per m² at three transect locations; flowers per plant counted on five plants per location to estimate flowers per m².
  - Apples: estimated density by counting flowers on five random trees along the transect and multiplying by the total number of trees on the transect.

## Data Variables and Schema
- Field identifiers:
  - Crop, Site (RD = Reading, JHI = James Hutton Institute), Date, Transect, Start time, Finish time.
- Recorder details:
  - Recorder (unique code), Recorder type (Novice, Researcher, Farmer/Agronomist).
- Environmental and sampling metrics:
  - Temp C, Av wind mph, Max wind mph, Cloud % (NA where missing).
  - Flowers/m2 (average flowers per m² along transect).
  - Flowers/transect (Flowers/m2 × 50 for most crops; apples use tree-based estimator).
- Pollinator counts (onflowers per transect):
  - Honeybee; Bombus spp. (terrestris/lucorum, hortorum, pratorum, pascuorum, lapidarious); Bombus unknown/unidentified.
  - Andrena sp.; Helictid sp.; Solitary bee unknown/unidentified.
  - Hoverfly unknown/unidentified; Other Diptera; Butterfly; Moth; Coleoptera; Other invertebrate.
- Notes on data quality:
  - Some temperature/wind/cloud records missing (NA) or provided per transect/day, leading to non-uniform coverage.

## Data Collectors and Recorder Types
- Recorder types include: Novice (public), Researcher (professional), Farmer/Agronomist (professionals with no prior survey experience).
- Data recorded by multiple individuals across sites (RD and JHI).

## Data Quality and Limitations
- No specific quality assurance was performed on the data.
- Data heterogeneity due to varied recorder experience and sampling effort.
- Incomplete coverage: not all recorders sampled every transect; some fields may have partial data for certain days or transects.
- Data standards and spatial granularity are limited to field-site and transect identifiers; explicit geographic coordinates are not provided in this description.

## GIS Relevance and Potential Uses
- Suitable for map-based visualization of pollinator visitation across crops, sites, and dates.
- Allows integration with weather and floral density metrics to explore relationships between environmental conditions and pollinator activity.
- Can support spatial analyses at the field/site level, with transect-level observations, though precise geolocation data would be needed for fine-grained mapping.
- Useful for quality checks and provenance: recorder type and site information help assess data reliability and sampling effort.