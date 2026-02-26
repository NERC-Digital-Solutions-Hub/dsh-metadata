# Invertebrate herbivory data across a natural soil temperature gradient in Iceland from May-July 2017

## Overview
- Dataset of environmental data, vegetation cover, and invertebrate herbivory at 14 experimental plots in Hengill geothermal valley, Iceland, collected May–July 2017.
- Plots span a natural soil temperature gradient from ~5 to ~35 °C and are located within 1 km2 with similar soil moisture, pH, nitrate, ammonium, and phosphate.
- Builds on prior work showing warming effects on phenology and plant/invertebrate diversity, while total plant cover and invertebrate biomass remain largely unchanged across temperatures.
- Focuses on three common plant species (Cardamine pratensis, Cerastium fontanum, Viola palustris) to assess species- and community-level herbivory across the gradient.
- Data collection supports analyses of how soil temperature, phenology, and vegetation composition influence invertebrate herbivory.

## Study design and sampling regime
- 14 plots (66–210 m2) established in May 2017 within Hengill valley to represent the temperature gradient; within-plot variation in temperature included where possible.
- Species-level herbivory: 30 individuals per species sampled per plot in a stratified random design across the temperature gradient (three focal species).
- Community-level herbivory: five 50 × 50 cm quadrats marked at random in eight plots to capture full temperature gradient.
- Temporal design: herbivory assessed across multiple time-points—species-level surveys every two weeks from late May to early July; community-level assessment on a fixed date.
- Environmental measurements taken at or near sampling points to characterize microclimate and soil chemistry.

## Measurements and variables
- Soil temperature: measured at 12 cm depth at five points per community quadrat and near each marked plant.
- Soil moisture: percentage moisture measured in each community quadrat.
- Soil chemistry: five cores per quadrat analyzed for pH, nitrate, ammonium, and phosphate using standard extraction methods.
- Nutrient analysis: nitrate and ammonium via 2M KCl extraction; phosphate via ammonium lactate–acetic acid buffer; detection limits specified.
- Plant phenology: weekly assessment of floral development stages for each marked plant (10-stage scale from vegetative growth to full flowering and wilting).
- Vegetation cover: visual percent cover of functional groups (bryophytes, forbs, graminoids, lichens, litter, bare ground) within quadrats.
- Herbivory assessment:
  - Species level: binary damage (damaged/not damaged) on marked individuals; three time-points per species between May 30 and July 2.
  - Community level: damage assessed as proportion of damaged plants out of 100 in 19 June survey; only healthy leaves used for assessment; damage defined as bite marks with intact petiole; excludes leaf wilt damage.

## Data structure and files
- Five CSV data files:
  - cardamine.csv and cerastium.csv: species-level data for Cardamine pratensis and Cerastium fontanum with columns including:
    - time, date, plot (common across files)
    - ID (unique plant identifier)
    - temp (soil temperature at 12 cm)
    - phenology (development stage)
    - damage (binary herbivory indicator)
    - length (longest vegetative structure, cm)
    - stems, leaves
    - leaves_damaged, pc_leaves_damaged (percentage)
    - overall_damage (percentage of photosynthetic tissue damaged)
    - flowering (status: Y/N/B/S/W)
    - num_flowers
  - viola.csv: species-level data for Viola palustris with columns 4–10 similar to the above, plus pc_leaves_damaged and flowering as columns 9 and 10.
  - cover.csv: quadrat- and plant-level cover data with columns:
    - time, date, plot
    - ID (individual plant)
    - species (Latin name)
    - temp (soil temperature)
    - moss, lichens, graminoids, forbs, litter, bare_ground (percent cover)
    - flowering (as above)
  - herbivory.csv: quadrat-level herbivory data with columns:
    - time, date, plot
    - herbivory (proportion of plants with herbivory within the quadrat)
    - moss, lichens, graminoids, forbs, litter, bare_ground (quadrats’ cover)
    - temp (average soil temperature within quadrat)
    - pH, moisture, nitrate, ammonium, phosphate (soil chemistry in mg kg-1)
- Column numbering is provided in the dataset descriptions to aid data interpretation.

## Methods and quality considerations
- Standardized protocols for environmental measurements and plant assessments to enable comparability across plots and time.
- Use of stratified random sampling for species-level measurements to represent temperature variation.
- Phenology and herbivory scoring follow published scales and defensible criteria to minimize misattribution of damage (e.g., excluding wilted leaves, requiring intact petioles for certain damage categorizations).
- Numerical data include explicit measurement depths, sampling intervals, and analytical detection limits for nutrients.

## Context and related work
- The dataset ties into broader studies on how soil temperature and plant community changes influence herbivory and ecosystem functioning in warming environments.
- References to prior work provide methodological grounding and context for interpretation, including Robinson et al. (2018), Valdés et al. (2019), Warner et al. (2021), and foundational methods for soil and vegetation measurements.

## Potential uses for monitoring and policy analysis
- Track environmental condition indicators across a natural warming gradient in a Arctic-like ecosystem.
- Enable standardised, time-series analyses of herbivory responses to soil warming, phenology shifts, and vegetation changes.
- Facilitate data integration with other environmental monitoring datasets for cross-site comparisons and synthesis.
- Support quality assurance and transparency goals by providing well-documented, reproducible measurement protocols and clearly defined data structures.