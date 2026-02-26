# NPPMF_CropPollinationPilot_2015_TransectData_SupportingInformation

## Overview
- Dataset documenting insects visiting flowers of apples, field beans, and oilseed rape.
- Collected from 13 flowering crop fields by teams from the University of Reading and the James Hutton Institute (Scotland).
- Data collected by multiple recorder types: novice public participants, professional researchers, and farmers/agronomists.
- Transects were sampled with varying coverage (not all recorders sampled every transect every day).

## Data scope and collection
- Crops: apples, field beans, oilseed rape.
- Sites: 13 crop fields across two institutions (Reading and JHI).
- Transects: four transects per field site, surveyed along a 50 m line over 10 minutes.
- Observations: recorded insects visiting flowers within a moving observation area (1 m ahead and 1 m to the side).
- Weather data: recorded with a Kestrel device before each transect or once per survey (temp, wind, etc.).
- Floral density measures:
  - Oilseed rape and beans: plants per m^2 at three locations; flowers per plant on five plants per location; total flowers per m^2 estimated.
  - Apples: number of trees along transect; flowers counted on three trees per transect to estimate density.
- Data recorders: coded by field/site, recorder type, and transect.
- Data coverage notes: not all transects were sampled by all recorders on any given day; some data fields may be NA.

## Data structure and fields (key columns)
- Crop, Site, Date, Recorder, Recorder type (Novice, Researcher, Farmer/Agronomist)
- Transect, Start time, Finish time
- Weather and environmental: Temp C, Av wind mph, Max wind mph, Cloud %
- Floral data: Flowers/m2, Flowers/transect
- Pollinator counts: Honeybee; Bombus (multiple species); Andrena sp.; Helictid sp.; Solitary bee unknown; Hoverfly unknown; Other Diptera; Butterfly; Moth; Coleoptera; Other invertebrate
- Quality Assurance: No specific QA performed

## Methodology in brief
- Transects conducted along crop tramlines with standardized protocol.
- Observers recorded all flower-visiting insects within defined sampling area during a 10-minute traversal per transect.
- Floral density and abundance estimates derived differently by crop type (beans/oilseed vs. apples).
- Data collected by teams with varying experience levels, introducing potential variability in sampling effort and identifications.

## Data quality and limitations
- Variation in recorder expertise (novice, researcher, farmer/agronomist) may affect identification accuracy and sampling consistency.
- Not all transects sampled by all recorders; potential coverage gaps across days/fields.
- Some fields show NA values for weather measures when data were not recorded per transect or per day.
- No explicit quality assurance procedures documented for this dataset.

## Data governance, stewardship, and use implications
- Metadata provides clear field-level context (site, recorder type, transect, timing, weather, floral density estimates).
- For effective reuse, standardization of species naming, units, and QA flags would enhance discoverability and comparability.
- Suitable for analyses of pollinator visitation patterns relative to weather, floral density, and transect-level effort, with caution due to variable recorder experience and incomplete coverage.
- Data would benefit from versioning, data dictionary, and guidance on data provenance and updates.

## Relevance to Data Leaders
- Demonstrates end-to-end data collection across a multi-site study with diverse data collectors.
- Highlights the importance of documenting data governance elements: purpose, scope, sampling methods, metadata, and quality considerations.
- Illustrates challenges in achieving data standardization, discoverability, and access when data originate from multiple institutions and varying contributor expertise.
- Provides a concrete example to inform future practices around data ownership, collaboration, and ensuring data assets meet user needs through metadata richness and transparently reported limitations.

## Opportunities and recommendations for improvement
- Implement a basic QA framework and data quality flags (e.g., data completeness, outlier checks, recorder confidence).
- Develop a comprehensive data dictionary and standardized units (especially for weather and floral density measures).
- Capture recorder identifiers and training level to support provenance and short- and long-term comparability.
- Improve metadata to include data collection dates, sensor calibration details, and transect-level effort notes.
- Consider data integration strategies to link with related datasets (e.g., broader pollinator networks, crop management data) to maximize usefulness for data-driven decision making.