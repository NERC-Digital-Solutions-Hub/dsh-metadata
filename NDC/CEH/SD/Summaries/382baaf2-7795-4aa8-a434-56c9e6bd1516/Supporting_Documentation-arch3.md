# Brief description of methods

- Objective and design
  - Assess environmental health-related plant responses to Free Air Ozone Enrichment (FAOE) across ozone and nitrogen treatment combinations.
  - Two plant species: Leontodon hispidus (Rough Hawkbit) and Succisa pratensis (Devil's-bit Scabious).
  - Experimental setup in North Wales, UK, using nine FAOE rings with a Latin square arrangement of 1 m blocks per ring.
  - Ozone treatments: Low (mean 24 ppb), Medium (mean 40 ppb), High (mean 57 ppb).
  - Nitrogen treatment: 40 kg N ha-1 yr-1 added to one block per ring; other blocks without added N.
  - Study period: planted in April 2016; data collected over three growing seasons; litter measurements July 2016–February 2017.

- Location and environmental context
  - Site: Abergwyngregyn, North Wales, UK.
  - Soil: Orthic Podzol, pH ~5.
  - Coordinates: Latitude 53.2389, Longitude -4.0185.
  - Irrigation relied on natural precipitation; no supplemental watering aside from N addition.

- Treatments and ring layout
  - Rings 4 m diameter; ozone concentrations assigned to rings as:
    - Low: A1, B2, C3
    - Medium: A3, B1, C2
    - High: A2, B3, C1
  - Each ring contains multiple 1 m blocks with species alternated in the Latin square design.

- Measurements and response variables
  - Growth and physiological responses recorded:
    - Leaf ground cover (LeafCover)
    - Leaf litter production (Litter weight after oven-drying)
    - Flowering stems (FlowerStems)
    - Chlorophyll index (Chl)
    - Photosynthesis and stomatal conductance (Asat and gs)

- Measurement conditions and instruments
  - Photosynthesis and stomatal conductance: LI-COR 6400XT; mean chamber conditions—air temp 20°C, CO2 400 μmol mol-1, light 1500 μmol m-2 s-1; RH 60–80%; VPD 0.8–1.2 kPa.
  - Chlorophyll index: Opti-Sciences CCM200 meter.
  - Data checks: ozone levels measured with calibrated Thermo 49i ozone analyser; pre-measurement checks on LI-COR system for chamber temp, light, pressure, flow; checks for CO2 and H2O; data graphically checked for outliers.

- Data files and structure
  - Five CSV data files provided:
    - Asat_gs.csv: Light-saturated photosynthesis (Asat) and stomatal conductance (gs)
      - Columns: Date, Ring, Nitrogen, Ozone, Species, Asat, gs
      - Measurement context: mean chamber conditions as above; healthy leaves
    - Chlorophyll.csv: Chlorophyll index
      - Columns: Date, Ring, Nitrogen, Ozone, Species, Chl
      - Instrument: CCM200; NA for missing measurements
    - FlowerStems.csv: Number of flowering stems
      - Columns: Date, Ring, Nitrogen, Ozone, Species, No_FlowerStems
    - LeafCover.csv: Leaf cover metrics
      - Columns: Ring, Nitrogen, Ozone, Species, Cover, PurpleCover, FrostDamage
      - Method: grids on photographs (100 squares per block); FrostDamage recorded January 2017; Leontodon showed NA for some damage data
    - WeightLitter.csv: Oven-dried litter mass
      - Columns: Month, Year, Ring, Nitrogen, Ozone, Species, Litter
      - Timeframe: July 2016–February 2017
  - Data notes: NA indicates missing measurements in the respective datasets. Leaf damage observed only for some species; certain values for Leontodon may be NA in some records.

- Data provenance and governance
  - Data collection, quality assurance, and transparent reporting implemented via standardized measurement protocols and metadata (e.g., ring, treatment codes, species).
  - Data files include explicit metadata for each column to support reproducibility and secondary analysis.