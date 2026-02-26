# Plant material

- Overview
  - Vegetative propagation of Lolium perenne (ryegrass) and Trifolium repens (white clover) from pasture near Edinburgh, UK.
  - Plants randomized between monocultures and mixtures; established in pots for 12 weeks total under ozone exposure.
  - Four solardomes used to control ozone: two continuous 30 ppb controls and two with episodic rural ozone profiles (30 ppb with peaks up to 80–100 ppb).

- Experimental design and treatments
  - Pots: large containers (approx. 35.5 x 45 x 25 cm) with drainage; each pot contained 12 plants (4 central Trifolium repens, 8 surrounding Lolium perenne).
  - Treatments per dome: three pots of L. perenne monoculture, three pots of T. repens monoculture, and three pots of the L. perenne + T. repens mixture, allocated randomly to each of four solardomes.
  - Ozone exposure schedule: ramp from 30 ppb to a daily max (80 ppb on days 1 and 4; 100 ppb on days 2–3), held at max for 6 hours, then declined back to 30 ppb; otherwise 30 ppb.
  - Watering: well-watered via mist irrigation plus manual watering during warm periods.

- Measurements and data collection
  - Visual assessments: whole-pot evaluation of senescence and ozone-specific injury (white/pale yellow leaf stippling); thresholds: >25% of leaf injured or senesced considered damaged. Leaf senescence length measured on a subsample of 20 leaves per pot (in mm).
  - Stomatal conductance: measured in Trifolium repens using a porometer on stable meteorological days, 10–11 weeks after exposure; measurements taken from upper canopy (sunlit) and inner canopy (shaded) with six leaves per pot (two leaves per canopy position per dome).
  - Chlorophyll content: SPAD index (chlorophyll a + b) measured on Trifolium repens after 1 and 10 weeks; calibration to mg g^-1 fresh weight using acetone extraction and Lichtenthaler/Welburn equations (r^2 = 0.90) with the relation:
    Chlorophyll content (mg g^-1 FW) = (chlorophyll index × 30.448) + 417.
  - Harvesting: two harvests (Sept 6 after 6 weeks; Oct 16 after 12 weeks); plants cut to 7 cm height; material sorted into layers: outside pot, >14 cm, 7–14 cm, and 0–7 cm (final harvest includes 0–7 cm). Sorting by species and health status (Trifolium leaves: healthy vs injured; Lolium leaves: healthy vs senesced). Biomass determined after drying at 65°C for ≥4 days.

- Data processing and analysis
  - Data structure: dome-level means used for analysis; injury/senescence data arcsine-transformed prior to analysis.
  -Statistical methods:
    - Stomatal conductance: one-way ANOVA (Minitab v14).
    - Other parameters: split-plot or split-split plot ANOVA in Genstat v8; main plot factor = ozone treatment; sub-plots = monoculture vs mixture; sub-sub-plots of canopy position where applicable.

- Data availability and structure
  - Data file: Lolium_and_Trifolium_solardomes_Injury_data.csv
  - Structure: 24 rows, 7 columns
    - Harvest
    - Species
    - Monoculture or mixture
    - Part of canopy
    - Ozone treatment
    - % leaves injured or senesced (determined by biomass)
    - Standard error

- Key notes for data support
  - Visual injury assessment is per pot due to plant intermingling.
  - Canopy-position measurements capture spatial variation in stomatal conductance.
  - Data enable comparison of ozone effects across species, growth forms (monoculture vs mix), and canopy layers.