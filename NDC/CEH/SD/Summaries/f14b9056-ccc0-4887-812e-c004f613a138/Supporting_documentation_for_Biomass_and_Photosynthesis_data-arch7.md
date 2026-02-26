# Plant material

## Overview
- Study of ozone effects on Lolium perenne (L. perenne) and Trifolium repens (T. repens) grown in pots, with randomised placement across different competition treatments and ozone exposure.
- Plants were vegetatively propagated from pasture near Edinburgh, UK (Grid NT245642) and established for ~8 weeks before exposure.
- Experiments included monocultures and mixtures, with data collected on biomass, canopy distribution, and physiological responses.

## Experimental design and setup
- Large pots (35.5 cm x 45 cm x 25 cm) lined with perforated plastic to prevent root escape; each pot held 12 plants (4 central, 8 surrounding).
- Pots arranged as: in mixtures, four central plants were T. repens and eight surrounding were L. perenne; monocultures comprised only one species.
- Four solardomes used in a randomised block design; conditions except rainfall approximated ambient air.
- Exposure period: 12 weeks starting 26 July 2002, split into two harvest periods (26 July–6 Sept; 7 Sept–16 Oct).
- Well-watered using mist irrigation (04:00 daily, plus hand watering as needed).

## Ozone exposure protocol
- Four solardomes with ozone generated from oxygen; two domes served as controls with ozone in charcoal-filtered air (30 ppb).
- Two domes used episodic rural ozone profile (O3(30+peaks)).
- Maximum daily ozone: 80 ppb on days 1 and 4; 100 ppb on days 2 and 3; other times held at 30 ppb.
- Ozone measured every 30 minutes in each dome; dome air concentrations controlled via LabView and mass-flow controllers.

## Harvesting and sample processing
- Harvests: plants trimmed to 7 cm on 6 Sept and 16 Oct.
- Layered harvest: outside pot perimeter, >14 cm above soil, 7–14 cm above soil; final harvest included 0–7 cm layer.
- Biomass sorted by species and plant part at harvest:
  - T. repens: stolons, flowers, leaves.
  - L. perenne: leaves and stems (no stems separated for >7 cm material).
- Samples dried (65°C, minimum 4 days) to determine biomass; a subsample of L. perenne leaf material analyzed for C and N (CHNS analysis).

## Physiological measurements
- Measurements on representative leaves and repeated across days; “Leaf 1” = newest fully expanded leaf and “Leaf 2” = second newest.
- A-Ci curves (photosynthesis vs. substomatal CO2) measured after exposure using CIRAS I with 1000 µmol m−2 s−1 PAR; CO2 series: 0, 50, 100, 200, 400, 600, 800, 1000, 1500, 2000 ppm.
- AQ curves (photosynthetic capacity) measured with CO2 at 1000 ppm and light stepped from 0 to 2000 µmol m−2 s−1.
- Data used to fit Farquhar model of photosynthesis; Jmax estimated from A-Ci curve asymptote (Ci > 500 ppm); Vc,max inferred from initial slope (Ci ≤ 300 ppm).
- Calculations followed established methods (Stirling et al. 1997; Farquhar et al. 1980/1988 references).

## Data architecture and datasets
- Data structures described for four CSV datasets:
  - Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv
    - Columns: Species, Leaf number, number of weeks since start of exposure, Treatment, dome.pot, Ci (ppm), A corrected for leaf area (µmol m−2 s−1)
    - 220 rows, 7 columns
  - Lolium_and_Trifolium_solardomes_biomass_data.csv
    - Columns: Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight (g per pot, cutting height 7 cm), standard error
    - 16 rows, 6 columns
  - Lolium_and_Trifolium_solardomes_clover_distribution_data.csv
    - Columns: Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error
    - 28 rows, 6 columns
  - Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv
    - Columns: Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error
    - 32 rows, 6 columns

## Statistical analysis
- Per-parameter means calculated per solardome before analysis.
- Analyses included:
  - One-way ANOVA (Minitab) for Jmax (no monoculture vs mixture comparison within this test).
  - GLM regression (SPSS) for A vs Ci across treatments.
  - Split-plot and split-split-plot ANOVA (Genstat) with main factor: ozone treatment; subplot: monoculture vs mixture; canopy position as a sub-sub plot for biomass data.

## Geographic and temporal context
- Location: near Edinburgh, UK (grid reference NT245642).
- Exposure span: 12 weeks starting 26 July 2002; two harvests during and after the exposure period.

## GIS relevance and potential data products
- The datasets provide spatially explicit information at the pot level within four domes, enabling:
  - Mapping of ozone exposure regimes over time and across treatments (monoculture vs mixture).
  - Spatial distribution of biomass by species and by canopy layer, enabling 3D or layered map representations of the canopy structure within each pot.
  - Visualization of physiological responses (A-Ci and Jmax) by treatment, canopy position, and harvest time.
  - Integration with precise geolocation (field origin near Edinburgh; grid NT245642) for contextual GIS analyses or embeddable data-rich map layers in policy or outreach visuals.
- Data structure indicates compatibility with GIS-friendly formats for multi-attribute, time-series mapping (e.g., per-sample or per-pot layers keyed by dome.pot, harvest, species, and treatment).