# Plant species cover and carabid beetle species counts (2018) and bird species counts 14 5 5 (2019) in ungrazed native reforestation areas and grazed/ungrazed unforested and mature forest areas in the Scottish Highlands

## Overview
- A biodiversity assessment across native reforestation sites in the Scottish Highlands, focusing on plants, carabid beetles, and birds.
- Aims to evaluate biodiversity value of reforestation relative to unforested and mature Caledonian Pineforest habitats under different grazing pressures (grazed vs ungrazed).
- Data collected in 14 fenced reforestation sites (1990–2012) within Glen Affric and Glen Moriston; accompanying unforested and mature-forest plots used for comparison.
- Plot design includes 10 × 10 m plots for plants and carabids and 50 m radius plots for birds; surveys conducted in summer 2018 (plants and carabids) and 2019 (birds).

## Study area and experimental design
- Locations: Glen Affric and Glen Moriston, central Scottish Highlands; landscape includes mature Caledonian pineforest, conifer plantations, heathland, and regenerating native forest.
- Fencing and grazing: Sites fenced to exclude deer grazing; grazing pressure varies in surrounding landscape.
- Treatments and matching:
  - Three forest statuses represented: reforestation (newly established), unforested (unplanted), mature forest.
  - Two grazing statuses: grazed and ungrazed.
  - All combinations represented except reforestation × grazed (deer pressure prevents this pairing).
  - Reforestation plots were matched to nearby unforested grazed and unforested ungrazed plots; five pairs of plots in mature forest (grazed vs ungrazed) to capture target habitat.
- Plot spacing: Plant and carabid plots are 30–400 m apart within a site; bird plots require 150–450 m separation between centers; some plots located in different places between survey types to maintain spacing.

## Data collection methods
- Plant surveys (2018):
  - 3 randomly placed 1 × 1 m quadrats per plot; percent cover using DOMIN scale.
  - Full plot species list recorded; vascular plants to species level; some non-vasculars identified to genus/morphospecies.
- Carabid beetle surveys (2018):
  - Six pitfall traps per plot (two traps per plant quadrat); traps deployed with propylene glycol/water, covered, emptied over time.
  - Specimens identified to species level; voucher specimens archived.
- Bird surveys (2019):
  - Two 15-minute surveys per plot, conducted morning (6:00–11:30) with settling period.
  - Identified visually or by vocalizations; two observers covered ~50% of plot each; weather noted; some plots excluded due to logistics.
- Temporal scope:
  - Plant and carabid data collected in summer 2018; bird data collected in summer 2019.

## Data structure and files (GIS-ready attributes)
- plant_carabid_plot_locations.csv
  - Spatially locates 10 × 10 m plots for plants and carabids.
  - Fields include: Site, Plot type (reforestation/forests/grazed/ungrazed/mature), Forest_status, Grazing_status, Year established, Grid_ref (OS National Grid), Pitfalls_0/1/2/3 dates.
- bird_plot_locations.csv
  - Spatially locates 50 m radius plots for birds.
  - Fields include: Site, Plot type, Forest_status, Grazing_status, Year, Grid_ref, Weather_1/Weather_2.
- plants.csv
  - Species-level plant data per plot/quadrat, including Date, Quadrat ID, Species (binomial), DOMIN percent cover, Seedling_frequency, etc.
- carabids.csv
  - Carabid species counts per plot per time (pitfall sampling occasion); fields include Time (sampling occasion), Species, Frequency.
- birds.csv
  - Bird sightings per plot per survey, including Date, Time, Species, How_recorded, Distance from plot center, etc.

## GIS-ready considerations and spatial specifics
- Spatial granularity:
  - Plants and carabids: 10 × 10 m plot geometry; 50 m radius for birds.
- Spatial references:
  - Plot locations include grid_ref in OS National Grid, enabling precise mapping and cross-reference with site coordinates (latitude/longitude provided in site table).
- Sites and treatments:
  - 14 reforestation sites with paired unforested plots (grazed and ungrazed) and 3 sites with mature forest plots (two grazed, two ungrazed per site; 5 total pairs).
  - Table 2 (affixed in the study) provides year of establishment, number of trees planted, planting methods, and presence of mature forest for each site.
- Data provenance:
  - Data collected by multiple authors; references cited for methods and context (plant/technique scales, carabid taxonomy, vegetation classifications).

## Potential GIS applications and data products
- Map-based biodiversity comparisons across habitat types (reforestation vs unforested vs mature forest) and grazing regimes.
- Spatial visualization of species richness and composition for plants, carabid beetles, and birds by plot.
- Landscape-scale analysis of restoration outcomes, plot-level biodiversity metrics, and habitat suitability for Caledonian Pineforest restoration.
- Integrated GIS layers:
  - Plot polygons (10 × 10 m) with attributes: site, forest_status, grazing_status, year_established.
  - Bird survey buffers (50 m radius) with attributes: bird_species_counts, survey_weather, survey_dates.
  - Point/area data for plant species cover per quadrat with DOMIN scales.
  - Pitfall trap locations with collection dates and species frequencies.
- Temporal analysis of changes between 2018 (plants/carabids) and 2019 (birds) within matched treatment plots.

## Notes on scope and limitations
- Not all sites/bands were surveyed in every year (e.g., 2019 bird surveys excluded for sites 3, 4, 6, and 16).
- Some plots are within mature Caledonian Pineforest remnants; adjacent landscapes include productive plantations and heathland, which may influence observed biodiversity.
- The dataset emphasizes fenced, ungrazed reforestation areas and their comparison to grazed/unfenced states to isolate grazing and restoration effects.

## References and context
- Contextual background on historical forest cover and deer-mediated regeneration; related prior studies cited for methodology and interpretation (e.g., deer management, pinewood dynamics, and vegetation classification standards).
- Appendix 1 lists roles of authors for design, data collection, and background material.