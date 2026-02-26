# Invertebrate herbivory data across a natural soil temperature gradient in Iceland from May-July 2017

## Overview
- Dataset of environmental data, vegetation cover, and both community- and species-level invertebrate herbivory.
- Collected May–July 2017 across 14 experimental plots in the Hengill geothermal valley, Iceland.
- Plots span a soil temperature gradient (about 5–35 °C on average) within 1 km² area; sites share similar soil moisture, pH, nitrate, ammonium, and phosphate.
- Focuses on a low Arctic plant community dominated by herbaceous perennials and bryophytes; vegetation and phenology responses to warming explored in related studies (e.g., Warner et al. 2021).

## Study setting and design
- 14 plots (66–210 m²) established in May 2017 to evenly distribute focal plant species across the temperature gradient and maximize within-plot temperature variation where possible.
- Focal plant species with widespread occurrence across the gradient: Cardamine pratensis, Cerastium fontanum, Viola palustris.
- Species-level herbivory assessments: 30 individuals per focal species per plot in 10 plots.
- Community-level herbivory assessments: five 50 × 50 cm quadrats in eight plots that best captured the full gradient.
- Soil temperature recorded at 12 cm depth at five points per community quadrat and near each marked individual during every herbivory survey.
- Soil moisture measured in each community quadrat; soil pH and nutrients (nitrate, ammonium, phosphate) analyzed from five soil cores per quadrat.
- Plant phenology tracked weekly; aboveground vegetation cover estimated for each quadrat; flowering stages categorized with a 10-stage scale.

## Measurements and variables
- Plant-level data (for Cardamine pratensis, Cerastium fontanum, Viola palustris):
  - ID (unique plant identifier), temp (soil temperature 12 cm depth), phenology (development stage), damage (binary herbivory indicator), length (longest vegetative structure, cm), stems, leaves, leaves_damaged, pc_leaves_damaged, overall_damage (percentage of photosynthetic tissue damaged), flowering status, num_flowers.
  - Viola data includes pc_leaves_damaged and flowering columns similar to the other two species.
- Community-level data (cover context):
  - ID, species, temp (soil temperature near individual), and percentage cover for moss, lichens, graminoids, forbs, litter, bare ground, plus flowering indicator.
- Herbivory context (quadrats):
  - herbivory (proportion of plants within the quadrat showing herbivory), cover for moss/lichens/graminoids/forbs/litter/bare ground, temp (average soil temperature across five points in the quadrat), pH, moisture, nitrate, ammonium, phosphate (mg/kg).
- Temporal coverage:
  - Species-level surveys conducted every two weeks from 30 May to 2 July (three time points per species); community-level herbivory assessed 19 June.
- Data structure:
  - Five CSV files, each row representing a sampling time-point for a plant individual or community quadrat.
  - Common initial columns across files: time (sampling time-point), date, plot (coded as per Warner et al. 2021).
  - File-specific columns as described above.

## Data files and structure (columns at a glance)
- cardamine.csv and cerastium.csv:
  - Additional columns: ID, temp, phenology, damage, length, stems, leaves, leaves_damaged, pc_leaves_damaged, overall_damage, flowering, num_flowers.
- viola.csv:
  - Similar to the species files with pc_leaves_damaged and flowering as the 9th and 10th columns.
- cover.csv:
  - Additional columns: ID, species, temp, moss, lichens, graminoids, forbs, litter, bare_ground, flowering.
- herbivory.csv:
  - Additional columns: herbivory, moss, lichens, graminoids, forbs, litter, bare_ground, temp, pH, moisture, nitrate, ammonium, phosphate.
- All files use units such as °C for temperature; percent for cover and moisture; mg kg⁻¹ for soil nutrients.

## Data collection methods and quality notes
- Standardized methods for soil temperature (12 cm depth), soil moisture (Delta-T devices), soil pH, and nutrient extraction/measurement (colorimetric methods with specified detection limits).
- Phenology staged using a defined 10-point scale; damage assessed as presence/absence of herbivory on healthy leaves, excluding wilted or damaged leaves where attribution was uncertain.
- Defoliation noted only if part of the leaf petiole remained with bite marks to avoid overestimation.
- Data are designed to enable self-serve analyses of how soil temperature and vegetation context relate to herbivory across species and at the community level.
- Related publications provide broader analyses of temperature effects on plant- and invertebrate-associated communities (e.g., Warner et al. 2021; others cited in the dataset).

## Potential uses for Data Support purposes
- Build dashboards or data products enabling exploration of herbivory patterns across a natural warming gradient.
- Cross-compare species- and community-level herbivory with soil temperature, moisture, pH, and nutrient profiles.
- Analyze phenology interactions with herbivory intensity and plant growth attributes (length, leaves, flowering).
- Promote data reuse by integrating with related spatial/temporal warming studies in Arctic or geothermal-gradient contexts.
- Validate or extend findings from Warner et al. (2021) on soil temperature, phenology, and plant community effects on invertebrate herbivory.