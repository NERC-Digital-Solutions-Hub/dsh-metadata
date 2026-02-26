# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Pollinator abundance data.

## Aim
- Establish a baseline of pollinator abundance linked to habitat condition across calcareous grassland, heathland, and woodland in Dorset.
- Build on Professor Ronald Good’s 1931–1939 botanical survey; use his site identifications to select current survey sites representing a degradation/restoration gradient.
- Enable analysis of how ecosystem services (pollinators) change with habitat condition by comparing historic baseline with current data.

## 1. Experimental design
- Baseline and archive: Good’s 1937 Dorset botanical survey provides the historical framework; archive is public via Dorset Environmental Records Centre (DERC).
- Site selection: Subsampled Good-identified calcareous grassland, heathland, and woodland sites to create a gradient of habitat condition. 13 calcareous grassland, 13 heathland, and 12 woodland sites were selected.
- Data sources for contemporary habitat classification: UK Land Cover Map 2007, Natural England Priority Habitat Inventory (2015), Sites of Special Scientific Interest (SSSIs, 2014), Horsfall (1981), Dorset Heathland survey (Rose et al., 2000), and Higher Level Stewardship schemes (see table 1 for details).
- Gradient categorisation (examples by habitat):
  - Calcareous: Improved grassland; Restoring calcareous grassland; Calcareous grassland (SSSI quality); maintenance/restoration assignments (e.g., HK6, HK7).
  - Heathland: Coniferous plantation on heathland; Gorse high heathland; Heathland (SSSI quality).
  - Woodland: Coniferous plantation; Broadleaf woodland; Ancient woodland (SSSI quality); with attention to avoiding ancient woodland plantations.
- Outcome: A structured dataset spanning three habitat types across a condition/degradation gradient to examine changes in pollinator communities.

## 2. Collection methods
- Plot design: 50m x 50m sample squares randomly assigned within the original Good survey area using ArcGIS.
- Survey timing: Conducted across 2017 and 2018 with multiple visits per site.
- Pollinator recording:
  - Butterflies: recorded to species within a 5m box along each transect, in flight or nectaring.
  - Bees, hoverflies, flies, beetles: recorded to species within a 2m box along the 50m transect while foraging.
  - Plant-pollinator interactions: plant species insects were foraging on recorded.
- Transects:
  - Two 50m transects per site walked at a steady pace.
  - Three survey dates per habitat type:
    - Calcareous grassland: June, July, August.
    - Heathland: May, August, September.
    - Woodland: May, June, July.
- Environmental data: Date, start/end times (HHMM), weather conditions (cloud cover %, temperature) at end of transect.
- Weather criteria and timing: Surveys conducted only under dry, calm conditions with:
  - Minimum 13°C; within 13–16°C if applicable.
  - Cloud cover ≤ 40%.
  - Wind ≤ Beaufort scale 5.
  - Time window 10:00–16:00.
- Data capture: Field data entered into a standardized spreadsheet with predefined columns (see Data schema section for details).

## 3. Quality Control
- Personnel: Data collected by experienced field ecologists; the same team conducted all surveys to ensure consistency.
- Data integrity: Field-recorded data checked for anomalies and consistency.
- Documentation: Clear definitions for column headings and units to support reproducibility and cross-site comparisons.

## 4. Data structure and lookup (key details)
- Field schema: Includes Site_no, Habitat, Date_of_survey, Survey_month, Surveyor, Transect_no, Grid_ref, Start_time, End_time, %_Sunshine, %_Cloud_cover, Insect_seen_Y_N, Activity_when_seen, Flower_species_foraging_on, Order, Insect_name, Caste_or_gender, Number_seen, among others.
- Habitat gradient mapping: A lookup table translating 1940 habitat classifications (as identified by Good) to 2017 observed habitat categories and gradient statuses (e.g., Calcareous grassland (SSSI quality), Restoring calcareous grassland, Coniferous plantation, Gorse high heathland, Ancient woodland (SSSI quality), etc.). This enables alignment of historical habitat type with contemporary condition and SSSI designations.
- Habitat scope: 38 total sites across three habitat types (13 calcareous grassland, 13 heathland, 12 woodland) representing the full gradient of condition from degradation to restoration or high-quality habitat.

## 5. References
- Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
- Natural England (2014) Sites of Special Scientific Interest and historical monuments. https://www.gov.uk/sites-of-special-scientific-interest-and-historical-monuments
- Natural England (2015) Priority Habitats' Inventory version 2.1. http://www.gis.naturalengland.org.uk/pubs/gis/gis_register.asp
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125