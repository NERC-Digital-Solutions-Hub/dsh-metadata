# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Pollinator abundance data.

## Scope and purpose
- Documents the pollinator abundance dataset from the Dorset Valuing Nature Project field component.
- Uses Professor Ronald Good’s 1931–1939 Dorset botanical survey as a baseline to select survey sites and assess how ecosystem services relate to habitat condition.
- Archive is publicly accessible via the Dorset Environmental Records Centre (DERC).

## Experimental design
- Good’s historic survey provides a reference framework; sites are subsampled from Good-identified calcareous grassland, heathland, and woodland.
- Subsampling draws on multiple data sources to identify current habitat types and create a comparable gradient of degradation.
- Aims to compare pollinator assemblages across habitat types and degradation gradients.

## Site selection and habitat gradients
- Sites selected to represent a range of new habitat types across a condition gradient.
- Habitat categories and gradients are defined for 1940 (Good) vs 2017 conditions:
  - Calcareous: calcareous grassland (SSSI quality), improved grassland, restoring calcareous grassland, and calcareous grassland with SSSI indicators.
  - Heathland: coniferous plantation on heathland, gorse high heathland, and heathland (SSSI quality).
  - Woodland: coniferous plantation, broadleaf woodland, and ancient woodland (SSSI quality).
- 13 calcareous grassland sites, 13 heathland sites, and 12 woodland sites were surveyed.
- Ancient woodland plantations were excluded; some sites are designated as SSSIs.

## Collection methods
- Sample squares of 50 m x 50 m randomly assigned within the Good survey area using ArcGIS.
- Field surveys conducted in 2017 and 2018 with multiple visits.
- Pollinator sampling:
  - Two 50 m transects per site; butterflies recorded to species level within a 5 m box; bees, hoverflies, flies, and beetles recorded to species within a 2 m box while foraging.
  - Plant species each insect was foraging on recorded.
- Transect timing and weather:
  - Dates for calcareous grassland: June, July, August; heathland: May, August, September; woodland: May, June, July.
  - Data collected: date of survey, start/end times, and weather (cloud cover, temperature).
  - Surveys conducted under fixed weather criteria: dry, calm, minimum 13°C; 13–16°C, cloud ≤ 40%, wind ≤ Beaufort 5; survey window 10:00–16:00.

## Data capture and metadata
- Data collected by experienced field ecologists; same team conducted all surveys.
- Data entered into spreadsheets exactly as recorded in the field.
- Data columns documented, including:
  - Site, habitat classification, date of survey, surveyor initials, transect number, grid reference (10 km resolution), start/end times, sunshine and cloud cover, presence of insects, activity, flowering plant foraging on, insect taxonomy (order to species where possible), caste/gender, and counts.
- A lookup table maps habitat classifications from 1940 to 2017 (e.g., Calcareous -> Calcareous grassland (SSSI quality), Improved grassland, Restoring calcareous grassland, Ancient woodland, etc.).

## Quality Control and data standards
- Data collected by the same experienced ecologists to ensure consistency and reliability.
- Routine checks for anomalies in the dataset.
- Metadata and units standardized across pollinator files; grid references standardized to 10 km resolution.

## Data provenance and references
- Primary sources and references:
  - Good, R. (1937) on Dorset botanical survey.
  - Horsfall, A. (1981) on habitat change in northeast Dorset.
  - Natural England (2014, 2015) on SSSIs and Priority Habitats Inventory.
  - Rose, et al. (2000) on changes in Dorset heathlands.
- Archival and data sources underpin habitat gradient definitions and site selection.

## Data sharing and access
- Data are organized for upload to relevant portals and catalogue holdings to ensure discoverability and reuse.
- Documentation includes field procedures, data structure, and provenance to support future data sharing and interoperability.

## Governance considerations for Data Stewards
- Ensure alignment with data governance: provenance, dataset versioning, and clear metadata.
- Maintain linkage between 1940 baseline classifications and 2017 data for reproducibility.
- Manage permissions and embargo status as needed given source data (e.g., SSSI-related information) and ensure proper attribution to sources.

## Caveats and limitations
- Habitat classification relies on multiple historical and contemporary data layers; potential misalignment across time periods.
- Data reflect surveys conducted within specific weather windows and seasons, which may influence detectability of certain pollinators.
- Not all insect taxa may be identifiable to species due to field constraints; some identifications use higher taxonomic levels where necessary.
- Ancient woodland plantations were excluded, which should be considered in cross-dataset comparisons.

## References
- Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
- Natural England (2014) Sites of Special Scientific Interest and historical monuments. https://www.gov.uk/sites-of-special-scientific-interest-and-historical-monuments
- Natural England (2015) Priority Habitats' Inventory version 2.1. http://www.gis.naturalengland.org.uk/pubs/gis/gis_register.asp
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125