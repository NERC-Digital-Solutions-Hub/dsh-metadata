# NPPMF_CropPollinationPilot_2015_TransectData_SupportingInformation

## Overview
- Data describe insects visiting flowers of three crops: apples, field beans, and oilseed rape.
- Collected from 13 flowering crop fields by teams based at the University of Reading and the James Hutton Institute (JHI) in Scotland.
- Data collection involved a mix of recorders: novices, experienced researchers, and farmers/agronomists.
- Not all data recorders sampled every transect on every day; transects varied by day and field.

## Methodology
- Pre-survey: detailed written transect protocols provided to recorders.
- Transect setup: four 50 m straight-line transects per field, surveyed along a crop tramline.
- Observation: moving observation area 1 m ahead and 1 m to the side; total survey time per transect = 10 minutes.
- Environment: weather data captured with a handheld Kestrel weather recorder before each transect or once per survey day.
- Floral density:
  - Oilseed rape and beans: floral density estimated by counting plants per m2 at three locations along the transect, plus flowers per plant from five random plants to estimate total flowers per m2.
  - Apples: density estimated by counting trees along the transect and assessing flowers on three trees; total flowers estimated by multiplying the average per-tree flower count by the number of trees.
- Data structure: includes field/site codes, recorder identity and type, transect identifiers, start/finish times, and environmental context.

## Data Structure and Variables
- Core columns and definitions:
  - Crop, Site (e.g., RD for Reading, JHI for James Hutton Institute), Date
  - Recorder (unique code) and Recorder type (Novice, Researcher, Farmer/Agronomist)
  - Transect, Start time, Finish time
  - Temp C, Av wind mph, Max wind mph, Cloud %
  - Flowers/m2, Flowers/transect
  - Pollinator counts by group/species: Honeybee; Bombus spp. (various species lists); Andrena sp.; Helictid sp.; Solitary bee unknown/unidentified; Hoverfly unknown/unidentified; Other Diptera; Butterfly; Moth; Coleoptera; Other invertebrate
- Data recording notes:
  - Temperature and wind data may be per transect or daily; some values marked NA.
  - Flowers/transect calculated as Flowers/m2 multiplied by transect length (50 m); apples use-tree-based estimation.
  - For apples, the flowers per transect are derived from counts on three trees and scaled to total trees along the transect.
- Data coverage and quality:
  - No explicit quality assurance performed (as per the document).
  - Some records have incomplete weather data or missing transects/fields.

## Field and Sampling Design
- Field sites: two principal teams (Reading RD and JHI) across 13 crop fields.
- Sampling framework:
  - 4 transects per field, surveyed by different recorders.
  - transects are fixed 50 m lines along crop tramlines.
  - Temporal coverage: surveys conducted on different days; not all transects sampled every day.
- Recorder diversity:
  - Mix of novice public participants, professional researchers, and farming professionals, introducing variability in data collection experience.

## Quality Assurance and Metadata
- Quality Assurance: explicitly noted as not performed for this dataset.
- Metadata richness:
  - Comprehensive column headers with explicit definitions and notes on data collection methods.
  - Documentation of recorder types and sampling procedures aids reproducibility and comparability.
- Data issues to consider for monitoring frameworks:
  - Variability in recorder expertise and sampling effort.
  - Incomplete data across transects and days.
  - Missing or NA weather measurements in some records.
  - The need for robust metadata and data governance to facilitate data sharing and reuse.

## Implications for Monitoring Frameworks
- Demonstrates a field-level monitoring protocol that can inform environmental health monitoring design:
  - Standardized transect-based sampling, explicit observation areas, and parallel collection of biotic (insect visitors) and abiotic (weather, floral density) data.
  - Clear data lineage (who collected what, when, and where) enhances transparency and accountability.
- Highlights governance and practical challenges:
  - Importance of training and consistent methods to reduce variability in data collected by different recorder types.
  - Metadata completeness and the inclusion of QA processes are critical for data usability in policy monitoring.
  - Data sharing considerations: openly sharing underlying data and ensuring data management standards are in place can be barriers without proper governance.
- Lessons for policy-oriented monitoring:
  - When designing monitoring frameworks, plan for data availability across sites and times, metadata completeness, and data quality controls.
  - Ensure mechanisms to manage incomplete data and to transform raw observations into comparable indicators (e.g., standardized pollinator counts, floral density metrics).
  - Consider documenting and addressing potential silos and ensuring cross-institutional data integration and governance.

## Relevance to Policy and Decision-Making
- Provides a concrete example of how pollinator visitation data can be structured and analyzed to assess pollination dynamics across crop types.
- Illustrates the level of detail needed in protocols, data fields, and provenance to support evidence-based decisions in environmental health monitoring.
- Underlines the balance between rapid, open data sharing and the practical constraints of data quality and metadata availability.