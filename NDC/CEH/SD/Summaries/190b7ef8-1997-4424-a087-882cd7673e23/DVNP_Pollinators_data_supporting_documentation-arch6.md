# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Pollinator abundance data

## Overview
- Document describes the dataset and methods for pollinator abundance data collected as part of the Dorset Valuing Nature Project.
- Uses a historical baseline from Ronald Good’s 1931–1939 Dorset botanical survey to select sites and assess changes in ecosystem services with habitat condition.
- Sites represent a gradient across calcareous grassland, heathland, and woodland habitats.

## Experimental design
- Good’s survey area used as baseline; sites re-identified and subsampled to match habitat types from the 1930s.
- 13 calcareous grassland, 13 heathland, and 12 woodland sites selected to span a degradation/condition gradient.
- Current habitat types identified using multiple sources: UK Land Cover Map 2007, Natural England Priority Habitat Inventory (2015), SSSIs (2014), Horsfall (1981), Dorset Heathland Survey (Rose et al., 2000), and Higher Level Stewardship data.
- Gradient categories defined for each habitat to reflect transitions from original to degraded or restored states; examples include calcareous grassland variants (e.g., restored, SSSI quality) and heathland/woodland transitions (e.g., coniferous plantation, ancient woodland).

## Data collection methods
- Sample squares of 50m x 50m randomly allocated within the original Good survey area using ArcGIS.
- Field surveys conducted across 2017–2018 to assess condition and ecosystem provisioning.
- Pollinator abundance measured along two 50m transects per site:
  - Butterflies recorded to species within a 5m box; bees, hoverflies, flies, and beetles recorded to species within a 2m box.
  - Insects foraging on plants recorded; plant species foraging on noted.
- Observations on three dates per habitat type:
  - Calcareous grassland: June, July, August.
  - Heathland: May, August, September.
  - Woodland: May, June, July.
- Metadata collected: date, start/end times, weather (cloud cover, temperature), sunshine % at end of transect, fixed weather criteria, and 10:00–16:00 survey window.

## Data structure and content
- Data collected by experienced field ecologists; same team across surveys.
- Data entered into a standardized spreadsheet with defined columns, including:
  - Site number, habitat category, date_of_survey, surveyor, transect_no, grid_ref, start_time, end_time, weather variables, insect seen (Y/N), activity (in flight, at rest, foraging), flower_species_foraging_on, insect_order, insect_name, caste/gender, number_seen.
- A habitat gradient lookup table maps 1940 habitat categories to 2017 classifications (e.g., Calcareous → Calcareous grassland (SSSI quality), Improved grassland, Restoring calcareous grassland; Heathland → Coniferous plantation on heathland, Gorse high heathland, Heathland (SSSI quality); Woodland → Broadleaf woodland, Coniferous plantation, Ancient woodland (SSSI quality)).
- Data quality controls include dataset consistency checks and anomaly screening; data collection performed by the same ecologists to ensure reliability.

## Quality control
- Consistent field team; identical researchers conducted all surveys.
- Data reviewed for anomalies and inconsistencies prior to final compilation.
- Documentation includes detailed data headings, units, and a lookup table to support re-use and integration with other datasets.

## References
- Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
- Natural England (2014) Sites of Special Scientific Interest and historical monuments. https://www.gov.uk/sites-of-special-scientific-interest-and-historical-monuments
- Natural England (2015) Priority Habitats' Inventory version 2.1. http://www.gis.naturalengland.org.uk/pubs/gis/gis_register.asp
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125