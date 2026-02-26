# Plant material

- Lolium perenne (L. perenne) and Trifolium repens (T. repens) were vegetatively propagated from pasture turf near Edinburgh, UK. Plants from different parents were randomized across competition (monoculture vs mixture) and ozone treatments; established for ~8 weeks before planting into monocultures or mixtures.
- Experimental unit: large pots with 12 plants (4 central T. repens surrounded by 8 L. perenne) arranged in either monoculture or mixed canopies.

## Experimental design

- Four solardomes (large hemispherical glasshouses) used, with randomized block design.
- Each solardome contained:
  - 3 pots of L. perenne monoculture
  - 3 pots of T. repens monoculture
  - 3 pots of a L. perenne and T. repens mixture
- Ozone treatment setup:
  - Two domes as controls with ozone in charcoal-filtered air (continuous O3)
  - Two domes with episodic rural ozone profile
  - Ozone regimes: maximum 80 ppb on days 1 and 4; 100 ppb on days 2 and 3; otherwise 30 ppb
- Ozone concentrations measured every 30 minutes in each dome

## Ozone exposure regime

- Ozone profiles designated as O3(30) and O3(30 + peaks)
- Exposure pattern: ozone ramped from 30 ppb to daily max over 2 hours, held at max for 6 hours, then decreased back to 30 ppb over 2 hours

## Harvests and sample processing

- Two harvests: at 6 weeks and 12 weeks after start of exposure
- Harvesting layers:
  - Material outside pot perimeter
  - Material > 14 cm above soil
  - Material between 7 and 14 cm above soil
  - Final harvest added 0–7 cm layer
- Material sorted by species at harvest; T. repens separated into stolons, flowers, leaves; L. perenne sorted into leaves and stems (no stems were identified for the latter)
- Drying and analysis:
  - Dry all material at 65°C for ≥4 days to determine dry weight
  - Subset of L. perenne leaf material ground and dried at 105°C for CHNS analysis (C and N content)

## Physiological measurements

- Leaf sampling: representative leaves of different ages; Leaf 1 = newest fully expanded leaf; Leaf 2 = second newest; minimum of six leaves per measurement day
- A–Ci curves (photosynthetic rate vs. substomatal CO2) collected after ozone exposure at two time points (4 weeks and 10–11 weeks) using PP-Systems CIRAS I
  - Light: 1000 μmol m−2 s−1 PAR
  - CO2 series: 0, 50, 100, 200, 400, 600, 800, 1000, 1500, 2000 ppm
  - Calculations performed with CIRAS software using Farquhar et al. (1981) framework
- A–Q curves (photosynthesis vs. light) conducted for both species at 1000 ppm CO2 and PAR steps up to 2000 μmol m−2 s−1
- Parameters derived:
  - Maximum electron transport rate (Jmax) from A–Ci curve asymptote (Ci > 500 ppm) using the Farquhar model
  - Vc,max estimated from initial slope of A vs Ci (Ci up to 300 ppm)
  - Data per plant used to fit the Farquhar et al. (1980) model of photosynthesis

## Statistical analysis

- Data aggregation: values averaged per solardome for analysis
- Analyses performed:
  - One-way ANOVA (Minitab) for Jmax (within ozone effects; no monoculture vs mixture comparison in this test)
  - GLM regression (SPSS) for comparing A vs Ci relationships between treatments
  - Split-plot and split-split-plot ANOVA (Genstat) with:
    - Main factor: ozone treatment
    - Subplot: monoculture vs mixture
    - Sub-subplot: canopy position for biomass partitioning
- Data structure notes:
  - Data structured per solardome for ACi-related analyses
  - Separate data structures for biomass and canopy distribution

## Datasets and data structure

- Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv
  - 220 rows, 7 columns
  - Columns: Species, Leaf number, number of weeks since start of exposure, Treatment, dome.pot, Ci (ppm), A corrected for leaf area (μmol m−2 s−1)
- Lolium_and_Trifolium_solardomes_biomass_data.csv
  - 16 rows, 6 columns
  - Columns: Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight (g per pot, cutting height 7 cm), standard error
- Lolium_and_Trifolium_solardomes_clover_distribution_data.csv
  - 28 rows, 6 columns
  - Columns: Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error
- Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv
  - 32 rows, 6 columns
  - Columns: Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error

- Notes
  - All datasets include measurements linking species, canopy composition, and ozone treatment to physiological and biomass responses
  - Data and metadata are structured to support cross-comparison of monoculture vs mixture under ozone exposure and to facilitate replication and re-analysis by others in the field