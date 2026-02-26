# Predicting spatially heterogeneous invasive spread: Pyracantha angustifolia invading a dry Andean valley in northern Argentina

- Purpose: Describes field data collection and datasets for analyzing fecundity, plant size, environmental conditions, and potential spread of Pyracantha angustifolia in a dry Andean valley.

- Study area and design:
  - Location: Tafi Del Valle, Tucuman, northern Argentina.
  - Time: Field data collected in May 2019.
  - Sites and plots: Ten sites, with three circular plots (20 m diameter) per site, randomly selected centers, separated by at least 20 m (30 plots total; ~9,426 m2).
  - Plot-level data: GPS coordinates and elevation recorded; habitat type categorized as grassland, shrubland, or rocky.

- Target species and measurements:
  - Species: Pyracantha angustifolia.
  - Abundance by plot: Counts of saplings (>10 cm tall, non-reproductive) and reproductive adults.
  - Individual-level data for reproductive adults: Basal stem diameter, plant height, canopy diameter (measured in four cardinal directions); evidence of grazing; fruit sampling within a defined canopy segment.
  - Fruit and seeds: Fruit production estimated per plant by sampling one-eighth of the canopy area and multiplying by eight; seeds counted per fruit (consistently five seeds per fruit in samples); total fruits and seeds per plant estimated from counts and proportion counted.
  - Age estimation: Ground-level stem blocks collected from 32 shrubs; cross-sections prepared and growth rings counted by four observers to estimate age.

- Habitat and environmental context:
  - Habitat types documented per plot (grassland, shrubland, rocky).
  - Additional plot-level indicators recorded (presence of Cotoneaster, cattle and horse dung, grazing activity).

- Data files included (contents and structure):
  - RawFecundityData.csv: 
    - Fields include Date, Site, Plot, latitude, longitude, Elevation, Habitat_type, Cotoneaster_presence, Cotoneaster_count, Cattle_dung, Horse_dung, Grazing, Sapling_count, Adult_count, Plant_number, Plant_grazed, Basal_stem_circumference, Basal_stem_diameter, Rosette_Diameter_1-4, Average_Rosette_Diameter, Height, Number_of_Fruits, Proportion_counted, Total_fruit, Total_seeds.
    - Purpose: raw measurements linking plant size and environmental context to fecundity outcomes.
  - FruitCounts.csv:
    - Fields: Sample_ID, Seed_count.
    - Purpose: seed counts per sampled fruit to support total seed estimates.
  - DendrochronologyPyrcantha.csv:
    - Fields: Sample_ID, circumference, count1–count4 (growth rings counted by four observers), mean_count.
    - Purpose: age estimation reliability for sampled shrubs via ring counts.
  - diameter (file): 
    - Appears to contain diameter-related measurements; included as a dataset file (exact columns not listed in summary).
  - Data accessibility: All datasets are freely available; data last modified 09/12/2020; contact details provided for dataset origin.

- Data provenance and quality considerations:
  - Multi-observer validation for growth ring counts to improve age estimates.
  - Combined datasets available with explicit metadata for reproducibility and reusability (e.g., site, plot, habitat, plant measurements, and fecundity estimates).
  - Data designed to enable analyses of correlations between plant size, habitat type, grazing pressure, and fecundity, as well as age-related growth patterns.

- Potential analyses and use cases for analysts:
  - Examine relationships between plant size metrics (basal diameter, height, canopy, rosette size) and fecundity (fruit and seed counts).
  - Assess how habitat type and grazing presence influence reproductive output and growth.
  - Model age distribution and growth using dendrochronology data and cross-observer reliability assessments.
  - Develop spatially explicit models of invasive spread by linking plot-level fecundity to environmental context and geography.
  - Integrate multiple datasets (size, age, fruit counts, seeds) to estimate potential spread rates and identify growth hotspots.