# Invertebrate herbivory data across a natural soil temperature gradient in Iceland from May-July 2017

- ## Overview
  - Dataset of environmental data, vegetation cover, and community- and species-level invertebrate herbivory.
  - Collected May–July 2017 across 14 experimental plots in the Hengill geothermal valley, Iceland.
  - Plots span a soil temperature gradient of ~5–35 °C, with similar soil moisture, pH, nitrate, ammonium, and phosphate.
  - Focus on three widespread plant species (Cardamine pratensis, Cerastium fontanum, Viola palustris) to assess herbivory at species and community levels.
  - Prior related work in the area notes phenology changes and reduced plant/invertebrate diversity with warming, while total plant cover and invertebrate biomass remain largely stable.

- ## Sampling regime and collection methods
  - 14 plots (66–210 m²) within ~1 km² area; plots chosen to distribute focal species across the temperature gradient, with within-plot temperature variation where possible.
  - Species-level herbivory: 30 individuals per focal species per plot marked and monitored; stratified random sampling to cover full temperature range.
  - Community-level herbivory: five 50 × 50 cm quadrats per plot in eight plots chosen to capture the full gradient.
  - Measurements:
    - Soil temperature recorded at 12 cm depth at five points within each quadrat and near each marked individual during every herbivory survey.
    - Soil moisture measured with ML3 ThetaProbe; soil pH and nutrients (nitrate, ammonium, phosphate) via standard extraction and colourimetric methods.
    - Nutrient detection limits noted (nitrate/ammonium ~0.17 mg kg⁻¹; phosphate ~0.30 mg kg⁻¹).
    - Soil dried and analysed for pH after water extraction.
    - Plant phenology staged weekly using a 10-stage scale ( vegetative growth through flowering and wilting).
    - Aboveground vegetation cover estimated in 50 × 50 cm quadrats, by functional groups (bryophytes, forbs, graminoids, lichens, litter, bare ground).
    - Leaf herbivory quantified as a standing damage measure (presence/absence) for individual leaves and plants; damage recorded only on healthy, fully expanded leaves to avoid confounding wilted leaves.
  - Timeframe and frequency:
    - Species-level surveys every two weeks from 30 May to 2 July (three time-points per species).
    - Community-level herbivory assessment on 19 June.
    - All marking and surveys conducted within a 48-hour window per survey per plot/individual.

- ## Data structure and files
  - Data are provided as five CSV files, each row representing a single sampling time-point for a particular plant individual or a vegetation quadrat.
  - Common fields across files: time, date, plot (plot code; codes described in Warner et al. 2021).
  - cardamine.csv and cerastium.csv (species-level data) include:
    - ID (unique plant identifier), temp (soil temperature at 12 cm), phenology (development stage), damage (binary: herbivory present or not),
    - length (longest vegetative structure, cm), stems, leaves, leaves_damaged, pc_leaves_damaged (percent leaves damaged),
    - overall_damage (percent of photosynthetic tissue damaged), flowering (status), num_flowers.
  - viola.csv contains the same columns as above (with pc_leaves_damaged and flowering as the 9th and 10th columns).
  - cover.csv (vegetation cover data) includes:
    - ID (unique plant), species (Latin name), temp (soil temperature near plant,
    - cover proportions for moss, lichens, graminoids, forbs, litter, bare ground, and flowering status.
  - herbivory.csv (community-level herbivory data) includes:
    - herbivory (proportion of plants in the quadrat with herbivory), cover variables (moss, lichens, graminoids, forbs, litter, bare ground),
    - temp (mean soil temperature within the quadrat), and soil chemistry/pH/moisture/nutrient concentrations (nitrate, ammonium, phosphate).
  - File-specific metadata and column positions are described in the dataset documentation; full methodological references are provided.

- ## Context and potential uses for monitoring and policy
  - Provides integrated measures of how soil temperature, plant phenology, vegetation structure, and herbivory respond to a natural warming gradient.
  - Enables examination of links between abiotic conditions (temperature, nutrients, moisture) and biotic responses (herbivory pressure, phenological shifts, plant cover composition).
  - Suitable for informing environmental health monitoring frameworks on:
    - Selection of temperature- and nutrient-related indicators of ecosystem health.
    - Data governance and metadata requirements (clear variable definitions, sampling protocols, and data sharing).
    - Assessing data gaps, integration across datasets, and reporting of complex ecological responses to warming.

- ## References and methods
  - Methods for soil analysis and nutrient extraction referenced (Blakemore et al. 1987; Egnér et al. 1960).
  - Phenology and herbivory assessment approaches cited (Turcotte et al. 2014; related vegetation and warming studies in the Hengill region).
  - Related ecological findings and broader context described in Robinson et al. (2018); Valdés et al. (2019); Warner et al. (2021).