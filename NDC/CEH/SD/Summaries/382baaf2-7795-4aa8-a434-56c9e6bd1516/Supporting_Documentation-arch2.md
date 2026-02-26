# Brief description of methods

- Experiment location: Abergwyngregyn, North Wales, UK (Orthic Podzol soil, pH 5; lat 53.2389, lon -4.0185).
- Plant material: Leontodon hispidus (Rough Hawkbit) and Succisa pratensis (Devil's-bit Scabious) grown from plug plants and planted in April 2016.
- Experimental design: 1 m square blocks arranged in nine Free Air Ozone Enrichment (FAOE) rings (4 m diameter) with a Latin square layout; species alternating within blocks.
- Treatments:
  - Ozone: Low (mean 24 ppb), Medium (mean 40 ppb), High (mean 57 ppb).
  - Nitrogen: Yes (40 kg N ha-1 yr-1) or No (none) during the first year.
  - Ring assignment of ozone levels: A1, B2, C3 = Low; A3, B1, C2 = Medium; A2, B3, C1 = High.
- Growth conditions: Natural irrigation; no supplementary watering except with N addition.
- Measurements (over three growing seasons): 
  - Growth and physiology: leaf ground cover, leaf litter, flowering, chlorophyll index, photosynthesis (Asat) and stomatal conductance (gs).
  - Methods: Asat and gs measured on healthy leaves with LI-COR 6400XT; standard chamber conditions applied.
- Quality controls:
  - Ozone levels monitored with calibrated Thermo 49i analyser.
  - LI-COR 6400XT pre-measurement checks for chamber conditions (temperature, light, pressure, flow) and gas leaks; CO2 and H2O checks.
  - Data visually inspected for outliers/unusual values.

## Experimental setup and timeline

- Planted in April 2016; three-year ozone exposure with and without nitrogen in year one.
- Ring infrastructure and arrangement documented with figures (layout and ring design).
- Ozone delivered from an O3 generator using ambient oxygen; rings monitored to ensure target concentrations.

## Data files and structure

There are five CSV data files, each with descriptive headers:

- Asat_gs.csv
  - Variables: Date, Ring, Nitrogen, Ozone, Species, Asat (µmol CO2 m-2 s-1), gs (mmol H2O m-2 s-1)
  - Notes: Measurements of light-saturated photosynthesis and stomatal conductance on healthy leaves; standard chamber conditions described.

- Chlorophyll.csv
  - Variables: Date, Ring, Nitrogen, Ozone, Species, Chl (chlorophyll index)
  - Notes: Chlorophyll index measured on healthy leaves with Opti-Sciences CCM200 meter; NA indicates missing.

- FlowerStems.csv
  - Variables: Date, Ring, Nitrogen, Ozone, Species, No_FlowerStems
  - Notes: Count of flowering stems.

- LeafCover.csv
  - Variables: Ring, Nitrogen, Ozone, Species, Cover, PurpleCover, FrostDamage
  - Notes: Leaf cover assessed via 100-square grids; October 2016 measurements for cover and damage; frost damage measured January 2017; NA indicates not applicable (e.g., no damage observed for Leontodon).

- WeightLitter.csv
  - Variables: Month, Year, Ring, Nitrogen, Ozone, Species, Litter
  - Notes: Monthly oven-dried litter weight (g) from July 2016 to February 2017; NA indicates missing.

## Data context for environmental analysts

- Standardized data collection and quality assurance enable cross-study comparison and time-series analysis of ozone and nitrogen effects on plant physiology and morphology.
- Dense metadata within each file facilitates integration with other environmental datasets (e.g., atmospheric chemistry, microclimate) for monitoring ecosystem responses to air quality changes.
- Data storage and accessibility considerations aligned with monitoring responsibilities, supporting transparency and reuse.