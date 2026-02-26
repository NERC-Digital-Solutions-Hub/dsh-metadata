# Brief description of methods

- Study purpose and setup
  - Investigates effects of Free Air Ozone Enrichment (FAOE) and nitrogen addition on two plant species: Leontodon hispidus (Rough Hawkbit) and Succisa pratensis (Devil's-bit Scabious).
  - Location: Abergwyngregyn, North Wales, UK (Orthic Podzol soil, pH 5; coordinates 53.2389, -4.0185).
  - Plants grown from plug plants in April 2016; arranged in 1 m square blocks with a Latin square design within nine 4 m diameter FAOE rings.
  - Treatments: Low, Medium, High ozone (24, 40, 57 ppb respectively) with/without nitrogen addition (40 kg N ha-1 yr-1) during the first year.
  - Natural irrigation; no supplemental watering except for nitrogen treatment.

- Experimental design and layout
  - Nine FAOE rings used to apply ozone treatments; rings labeled to deliver Low, Medium, High ozone across blocks (A1, B2, C3 for Low; A3, B1, C2 for Medium; A2, B3, C1 for High).
  - Each ring contains plant blocks; one block in each relevant subset receives nitrogen.

- Data collection and recorded variables
  - Growth and physiology metrics recorded over three growing seasons:
    - Leaf ground cover
    - Leaf litter
    - Flowering (flowering stems)
    - Chlorophyll index
    - Photosynthesis (Asat) and stomatal conductance (gs)
  - Instruments and conditions:
    - Asat and gs measured with LI-COR 6400XT under mean chamber: 20°C, CO2 400 µmol mol-1, light 1500 µmol m-2 s-1, relative humidity 60–80%, vapor pressure deficit 0.8–1.2 kPa.
    - Chlorophyll index measured with Opti-Sciences CCM200 meter.
    - Growth and other measurements linked to ring, nitrogen, ozone treatment, and species.

- Quality control (QC)
  - Ozone levels monitored with calibrated Thermo 49i analyser.
  - LI-COR 6400XT pre-measurement checks for chamber conditions; checks for leaks and CO2/H2O concentrations.
  - Data graphically checked for outliers and unusual values.

- Data files and metadata
  - Five CSV data files:
    - Asat_gs.csv: Light-saturated photosynthesis (Asat) and stomatal conductance (gs)
      - Key columns: Date, Ring, Nitrogen, Ozone, Species, Asat (µmol CO2 m-2 s-1), gs (mmol H2O m-2 s-1)
      - Measurement conditions: mean chamber temp 20°C, CO2 400 µmol mol-1, light 1500 µmol m-2 s-1, humidity 60–80%, VPD 0.8–1.2 kPa
    - Chlorophyll.csv: Chlorophyll index (Chl)
      - Key columns: Date, Ring, Nitrogen, Ozone, Species, Chl
      - Measured with Opti-Sciences CCM200; NA indicates missing
    - FlowerStems.csv: Number of flowering stems
      - Key columns: Date, Ring, Nitrogen, Ozone, Species, No_FlowerStems
    - LeafCover.csv: Leaf cover and damage indicators
      - Key columns: Ring, Nitrogen, Ozone, Species, Cover (percentage), PurpleCover (damaged leaf percentage), FrostDamage (frost-damaged leaf percentage)
      - Leaf cover assessed from grids overlaid on photos; October 2016
    - WeightLitter.csv: Dried litter weight
      - Key columns: Month, Year, Ring, Nitrogen, Ozone, Species, Litter (grams)
      - Litter measured monthly from July 2016 to February 2017; oven-dried at 60°C
  - Common fields across files: Ring (FAOE ring), Nitrogen (YES/NO), Ozone (Low/Medium/High), Species (Succisa or Leontodon)
  - Handling of missing data: NA used where measurements were not available

- Data considerations and potential uses
  - Enables self-serve analysis of treatment effects on photosynthesis, chlorophyll content, flowering, leaf morphology, and litter production.
  - Facilitates data integration across multiple response variables and treatments for broader policy or ecological insights.
  - Suitable for exploring data quality, treatment interactions, and time-series patterns across three growing seasons.