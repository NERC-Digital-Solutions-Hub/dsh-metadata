# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Pollinator abundance data.

## Experimental design
- Based on Professor Ronald Good’s extensive Dorset botanical survey (1931–1939); archive publicly available via Dorset Environmental Records Centre.
- Use Good’s identified calcareous grassland, heathland, and woodland sites from the 1930s as a baseline to select current survey sites and assess how ecosystem services change with habitat condition.
- Subsampled Good-identified sites to create a panel representing habitat types: 13 calcareous grassland, 13 heathland, and 12 woodland.
- Subsampling leveraged multiple data sources to classify current habitat types, including UK Land Cover Map 2007, Natural England Priority Habitat Inventory, SSSIs, Horsfall (1981), Dorset Heathland survey (Rose et al., 2000), and Higher Level Stewardship schemes.
- Habitat gradients defined for each type, representing degradation or restoration relative to the 1930s baseline (e.g., calcareous: improved grassland; restoring calcareous grassland; calcareous grassland of SSSI quality).
- Gradient categories also specified for heathland (e.g., coniferous plantation on heathland; high-gorse heathland; heathland with SSSI quality) and woodland (e.g., coniferous plantation; broadleaf woodland; ancient woodland of SSSI quality).
- Selection aimed to cover a range of new habitat types across degradation/restoration gradients, with notes to avoid ancient woodland plantations in some cases and to identify SSSI-quality sites where applicable.

## Collection methods
- Sample squares of 50m x 50m randomly assigned within the original Good survey area using ArcGIS.
- Field surveys conducted across 2017 and 2018 with multiple visits to assess condition, quality, and ecosystem provisioning.
- Pollinator abundance collected through two 50m transects per site; butterflies recorded to species level within a 5m box; bees, hoverflies, flies, and beetles recorded to species within a 2m box; plant species foraging on recorded.
- Transects conducted on three dates per site; timing varied by habitat: calcareous (June–August), heathland (May, August, September), woodland (May–July).
- Weather and timing recorded: date, start/end times, weather conditions (cloud cover, temperature); weather criteria for transects included dry calm conditions, minimum 13°C, 13–16°C with <40% cloud, wind ≤5 on Beaufort scale; transects run between 10:00 and 16:00.
- Data collection fields include detailed metadata (site, habitat, survey date, transect, grid reference, times, sunshine, cloud cover, insect presence, activity, flower species, insect taxonomy, caste/gender, and counts).

- Data structure and standardisation
  - Data are stored with explicit column definitions (e.g., Site_no, Habitat, Date_of_survey, Transect_no, Grid_ref, Start_time, End_time, %_Sunshine, %_Cloud_cover, Insect_seen_Y_N, Activity_when_seen, Flower_species_foraging_on, Order, Insect_name, Caste_or_gender, Number_seen).
  - A habitat lookup table maps 1940 habitat categories to 2017 gradient categories to define the site condition gradient.

## Quality Control
- Data collected by experienced field ecologists; the same team conducted all surveys to ensure consistency.
- In-field data recorded directly into spreadsheets; subsequent checks for anomalies to maintain data reliability and consistency.

## References
- Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
- Natural England (2014) Sites of Special Scientific Interest and historical monuments. https://www.gov.uk/sites-of-special-scientific-interest-and-historical-monuments
- Natural England (2015) Priority Habitats' Inventory version 2.1. http://www.gis.naturalengland.org.uk/pubs/gis/gis_register.asp
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125