# NPPMF_CropPollinationPilot_2015_TransectData_SupportingInformation

## Overview
- Dataset on insects observed visiting flowers across three crops: apples, field beans, and oilseed rape.
- Collected from 13 flowering crop fields by teams at the University of Reading and the James Hutton Institute (Scotland).
- Data gathered by individuals with varying levels of experience (novice public data collectors, researchers, farmers/agronomists).
- Not all recorders sampled all transects; transect sampling was uneven across fields and days.

## Methodology and Data Collection
- Transect protocol:
  - Recorders observed all flower-visiting insects within a moving area 1 m ahead and 1 m to the side.
  - Each transect: 50 m straight along a crop tramline, surveyed for 10 minutes.
  - At each field site, 4 transects were surveyed by different recorders.
- Weather data:
  - Collected with a Kestrel weather recorder before each transect (or once during the day for some surveys).
- Floral density data:
  - Beans and oilseed rape: estimate flower density by counting plants per m2 at three transect locations and counting flowers on 5 plants per location to estimate flowers per m2.
  - Apples: estimate density by counting trees along the transect and counting flowers on 3 trees to estimate density.
- Site and data identifiers:
  - Site: codes RD (Reading) or JHI (James Hutton Institute); site number identifies the field.
  - Date, Recorder (unique code), and Recorder type (Novice, Researcher, Farmer/Agronomist).
  - Transect identifier; start and finish times.
- Variables recorded (sample of columns):
  - Temperature (Temp C), Average wind (Av wind mph), Maximum wind (Max wind mph), Cloud cover (%).
  - Flowers/m2 and Flowers/transect (derived from floral density measurements).
  - Insect counts by taxa: Honeybee; Bombus spp. (multiple taxa or groups); Andrena sp.; Helictid sp.; Solitary bee unknown/unidentified; Hoverfly unknown/unidentified; Other Diptera; Butterfly; Moth; Coleoptera; Other invertebrate.
- Quality Assurance:
  - No specific quality assurance was performed for this dataset.

## Variables and Column Descriptions (highlights)
- Core fields: Crop, Site, Date, Recorder, Recorder type, Transect, Start time, Finish time.
- Environmental metrics: Temp C, Av wind mph, Max wind mph, Cloud %.
- Floral metrics: Flowers/m2, Flowers/transect.
- Pollinator counts: Honeybee and multiple taxa/groups of Bombus spp., Andrena sp., Helictid sp., Solitary bee unknown/unidentified, Hoverfly unknown/unidentified, Other Diptera, Butterfly, Moth, Coleoptera, Other invertebrate.

## Data Quality, Limitations, and Considerations for Use
- Patchy data: varying sampling effort across recorders, transects, and days; not all fields have complete coverage.
- Granularity mismatches: weather data can be per-transect or per-day; some records have NA values.
- Taxonomic resolution: counts include several broad groups and some unidentified categories.
- No explicit QA: potential data quality issues due to mix of novice and expert recorders and inconsistent procedures.

## Potential Analyses and Data Products for Data Support
- Descriptive summaries by crop and site (e.g., total pollinator visits per transect, per crop).
- Relationships between pollinator counts and environmental variables (temperature, wind, cloud cover).
- Per-transect derived metrics:
  - Flowers/m2, flowers/transect.
  - Pollinator abundance by taxa per transect.
- Cross-field and cross-crop comparisons of pollinator assemblages.
- Data products for end users:
  - Dashboards or pivot-table style views enabling exploration by site, date, crop, and pollinator group.
  - Visualizations of temporal or spatial patterns in pollinator visits.

## Data Preparation and Use Recommendations for Data Support
- Standardize units and ensure consistent interpretation across transects (e.g., harmonize weather measurements and per-transect vs per-day values).
- Create a clean master key (e.g., Crop + Site + Date + Transect) to enable join/aggregation across variables.
- Document data quality checks and fill/flag missing values clearly for end users.
- Consider consolidating Taxa names and handling unidentified categories to improve comparability across datasets. 
- Provide metadata on recorder type and transect coverage to contextualize variability in counts.