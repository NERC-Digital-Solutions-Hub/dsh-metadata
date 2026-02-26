# Plant material

- Objective
  - Compare ozone effects on Lolium perenne (L. perenne) and Trifolium repens (T. repens) grown in monocultures and mixtures, assessing physiological responses, biomass partitioning, and canopy-level distribution under controlled solardome conditions.

- Experimental material and design
  - Plant source and propagation: L. perenne and T. repens vegetatively propagated from pasture turf near Edinburgh, UK; plants randomly allocated to competition and ozone treatments.
  - Establishment: propagated plants grown ~8 weeks before planting into either monocultures or mixtures.
  - Pot setup: large pots with drainage, 35.5 cm x 45 cm x 25 cm; lined with perforated plastic; each pot contains 12 plants (4 central T. repens surrounded by 8 L. perenne).
  - Dome arrangement: four solardomes; randomised block design; 3 pots per species per dome.
  - Exposure period: 12 weeks starting 26 July 2002; two harvest periods (6 weeks and 12 weeks).
  - Watering: mist irrigation at 04:00, with additional hand watering during warm periods.

- Ozone exposure regime
  - Dome treatment groups: two domes as continuous 30 ppb controls (O3(30)); two domes receive episodic rural ozone profiles (O3(30+peaks)).
  - Monitoring: ozone concentrations measured every 30 minutes; analyser calibrated prior to exposure.
  - Concentration schedule: daily maximums of 80 ppb on days 1 and 4, and 100 ppb on days 2 and 3; ramp up from 30 ppb to max over 2 h, hold ~6 h, then return to 30 ppb over 2 h; remaining times at 30 ppb (including days 5–7).
  - Baseline conditions: constant 30 ppb in control domes; other domes follow the program above.

- Harvesting and sample processing
  - Harvest timing: first at ~6 weeks, second at ~12 weeks.
  - Sorting by canopy layer: outside pot perimeter, >14 cm above soil, 7–14 cm above soil; final harvest includes 0–7 cm layer.
  - Species sorting: T. repens separated into stolons, flowers, leaves; L. perenne into leaves and stems (only leaves above 7 cm considered).
  - Biomass processing: material dried at 65°C for ≥4 days; subsamples of L. perenne leaves analysed for carbon and nitrogen content (CHN) after grinding.

- Physiological measurements
  - Leaves: representative leaves from different ages; measurements on at least six leaves per date.
  - A-Ci curves: net CO2 assimilation (A) vs substomatal CO2 (Ci) using PP-Systems CIRAS I; PAR = 1000 μmol m−2 s−1; CO2 steps from 0 to 2000 ppm; A and Ci calculated via CIRAS with Von Caemmerer & Farquhar model.
  - AQ curves: CO2 fixed at 1000 ppm; PAR stepped from 0 to 2000 μmol m−2 s−1.
  - Parameters estimated: maximum electron transport rate (Jmax) from A-Ci asymptote (Ci > 500 ppm) using the Stirling et al. (1997) approach; Vc,max inferred from initial slope of A-Ci up to Ci = 300 ppm.
  - Modelling: Farquhar et al. (1980) model for photosynthesis; I* temperature-adjusted concept used in Jmax calculation.

- Statistical analysis
  - Data aggregation: parameter values averaged per solardome (block) for analysis.
  - Analyses: one-way ANOVA (Jmax) for ozone effect; GLM regression for A vs Ci across treatments; split-plot and split-split-plot ANOVA in Genstat with main factor ozone and subplot factor monoculture vs mixture; canopy position included as sub-sub plot for biomass partitioning.
  - Software: Minitab, SPSS, Genstat used for different analyses.

- Data availability and structure
  - Datasets provided as CSV files:
    - Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv: 220 rows, 7 columns (Species, Leaf number, weeks since exposure start, Treatment, dome.pot, Ci, A corrected for leaf area).
    - Lolium_and_Trifolium_solardomes_biomass_data.csv: 16 rows, 6 columns (Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight per pot, standard error).
    - Lolium_and_Trifolium_solardomes_clover_distribution_data.csv: 28 rows, 6 columns (Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot, standard error).
    - Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv: 32 rows, 6 columns (Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot, standard error).
  - These data enable integration of physiological, biomass, and canopy-distribution measurements across species, treatments, and time points.

- GIS-relevant notes
  - Spatial structure within the experiment is captured via the dome and pot identifiers (dome.pot), along with canopy-part classifications and harvest times, enabling spatial-temporal mapping of ozone effects on biomass and photosynthetic performance.
  - Data cuboids exist for three linked aspects (physiology, biomass, canopy distribution) that can be joined by species, treatment, dome/pot, and harvest date for GIS-enabled visualization and analysis.