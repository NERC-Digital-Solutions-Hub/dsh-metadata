# Invertebrate herbivory data across a natural soil temperature gradient in Iceland from May-July 2017

## Overview
- Dataset of environmental data, vegetation cover, and invertebrate herbivory across a natural soil temperature gradient in the Hengill geothermal valley, Iceland.
- Spans May–July 2017 with plots experiencing a temperature gradient from ~5 to 35 °C on average.
- Includes both species-level herbivory data for three focal plants and community-level herbivory, along with soil chemistry, moisture, and vegetation structure data.
- Context: prior work shows phenology shifts and changes in plant and invertebrate diversity with warming, while total plant cover and invertebrate biomass remain largely unchanged across the gradient.

## Study site and design
- 14 experimental plots (66–210 m² each) within a 1 km² area in the Hengill geothermal valley.
- Plots spread across a natural soil temperature gradient; hotspot proximity ensures comparable soil moisture, pH, nitrate, ammonium, and phosphate.
- Stratified experimental approach to capture temperature effects across individuals and communities.

## Focal species and phenology
- Species-focused herbivory assessments on three widespread plants:
  - Cardamine pratensis
  - Cerastium fontanum
  - Viola palustris
- Growth forms differ among species, influencing susceptibility to herbivory.
- Phenology tracked weekly via development stages (1–10, from vegetative growth to full flowering).

## Measurements and data collection
- Soil temperature recorded at 12 cm depth at five points within each community-level quadrat and near each marked individual.
- Soil moisture measured in each community-level quadrat (ML3 ThetaProbe).
- Soil chemistry: five cores per quadrat for pH and nutrient content; nutrients extracted and analyzed:
  - Nitrate and ammonium: 2M KCl extraction (5:1 soil:solution)
  - Phosphate: ammonium lactate–acetic acid buffer (pH 3.75)
  - Colorimetric analysis with detection limits: nitrate/ammonium 0.17 mg/kg; phosphate 0.30 mg/kg
- Soil processing: dried 80 °C for 13 h; a 10 g subsample prepared for pH after dilution and equilibration.
- Vegetation surveys: 50 × 50 cm quadrats to assess functional-group cover (bryophytes, forbs, graminoids, lichens, litter, bare ground) with cover classes (0–1% to 95–100%).
- Plant phenology: weekly assessment of marked individuals’ developmental stage; flowering status recorded.

## Herbivory assessments
- Leaf herbivory quantified as a standing measure of damage on healthy leaves at each sampling.
- Species-level assessments: three time-points per species (late May to early July; ~every two weeks) for marked individuals (30 plants per species per 10 plots).
- Community-level assessments: five 50 × 50 cm quadrats per plot in eight plots; a single date (19 June) when damage was assessed in 100 plants per quadrat grid.
- Damage metric: binary damaged/not damaged per plant at each time-point; damage restricted to defoliation by biting (no mining or galls); damage on wilted leaves excluded; damage on leaves categorized when petiole remained with bite marks.
- Across species, 30–60% of marked plants showed evidence of herbivory at sampling times.

## Data structure and files
- Five CSV files, each row representing one sampling time-point per plant or community.
- Common columns across files: time, date, plot.
- Cardamine pratensis and Cerastium fontanum (cardamine.csv, cerastium.csv):
  - Additional columns: ID, temp (soil temp at 12 cm), phenology, damage (binary), length, stems, leaves, leaves_damaged, pc_leaves_damaged, overall_damage, flowering, num_flowers.
- Viola palustris (viola.csv):
  - Similar columns to cardamine/cerastium with leaves_damaged and flowering as the 9th and 10th columns.
- cover.csv:
  - Additional columns: ID, species (Latin name), temp, cover percentages for moss, lichens, graminoids, forbs, litter, bare ground, flowering.
- herbivory.csv:
  - Additional columns: herbivory (proportion of quadrat plants damaged), cover (moss, lichens, graminoids, forbs, litter, bare ground), temp (average quadrat temperature), pH, moisture, nitrate, ammonium, phosphate.
- Plot and time identifiers follow Warner et al. (2021) coding.

## Potential analyses and uses
- Relate soil temperature gradient to:
  - Species-level herbivory indicators (damage probability, pc_leaves_damaged, overall_damage) across time.
  - Community-level herbivory and its association with quadrat-level plant cover and composition.
  - Plant phenology progression and flowering timing across temperature regimes.
- Examine interactions between soil chemistry (nitrate, ammonium, phosphate, pH), moisture, and herbivory intensity.
- Integrate vegetation structure (functional-group cover) with herbivory to understand how plant community context modulates damage.
- Cross-validate findings with prior work on phenology and community composition responses to soil warming.

## References and context
- Data collection methods and broader context linked to Warner et al. (2021) and related studies on soil warming effects in the Hengill valley.
- Foundational methods for soil analyses referenced (Blakemore et al. 1987; Egnér et al. 1960) and vegetation/phenology assessment approaches (Peet et al. 1998; Turcotte et al. 2014; Turcotte et al. 2014).