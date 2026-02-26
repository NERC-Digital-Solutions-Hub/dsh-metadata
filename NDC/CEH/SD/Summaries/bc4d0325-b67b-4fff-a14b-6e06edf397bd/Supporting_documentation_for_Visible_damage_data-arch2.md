# Lolium_and_Trifolium_solardomes_Injury_data.csv

## Study aim and environmental monitoring context
- Controlled ozone exposure experiment to assess the health responses of pasture species (Lolium perenne and Trifolium repens) under standardized conditions.
- Data are collected to enable monitoring of environmental health effects over time and to support policy-relevant interpretations of ozone impacts on mixed plant communities.

## Plant material and experimental setup
- Plant material: Lolium perenne and Trifolium repens propagated from turf samples near Edinburgh, UK.
- Experimental units: Large pots with 12 plants each (four central Trifolium repens surrounded by eight Lolium perenne).
- Configurations: Monocultures (Lolium or Trifolium), and mixed cultures (four central Trifolium with eight surrounding Lolium).
- Randomization: Different parent plants randomized across competition (monoculture vs mix) and ozone treatments.
- Growth period: Approximately eight weeks establishment before exposure; two harvests during ozone exposure (intermediate and final).

## Ozone exposure and treatments
- Experimental domes: Four solardomes used; two domes serve as controls, two as ozone treatments.
- Ozone delivery:
  - Controls: Ozone added to charcoal-filtered air to achieve baseline 30 ppb.
  - Treatments: Two patterns:
    - O3(30): 30 ppb baseline with continuous monitoring.
    - O3(30+peaks): Episodic rural ozone profile with weekly peaks.
- Concentration timeline within days:
  - Target daily maximums of 80 ppb on days 1 and 4; 100 ppb on days 2 and 3.
  - Ramp up from 30 ppb to daily maximum over 2 hours, hold 6 hours, ramp down over 2 hours; otherwise 30 ppb.
- Monitoring: Ozone concentrations measured every 30 minutes in each dome.

## Measurements and data collection
- Visual assessments (whole-pot level):
  - Senescence and ozone-specific injury assessed by appearance (white/pale yellow stipples).
  - Classification criteria: leaves categorized as healthy, injured (>25% of leaf area injured), or senesced (>25% senesced).
  - For Lolium perenne, senescence length measured on a sample of leaves.
- Harvests and biomass:
  - Two harvest times after ozone exposure (6 weeks and 12 weeks).
  - Layered harvesting: outside pot perimeter, >14 cm, 7–14 cm, and finally 0–7 cm (for final harvest).
  - Species separation at harvest; distinguishing healthy vs ozone-injured leaves for Trifolium repens and healthy vs senesced for Lolium perenne.
  - Drying: 65°C for at least 4 days; biomass determined after drying.
- Physiological measurements:
  - Stomatal conductance: Measured in Trifolium repens using a porometer (Delta-T AP4) at stable weather conditions, in upper (sunlit) and inner (shaded) canopy positions; six leaves per pot per canopy position.
  - Chlorophyll content: Measured with SPAD meter (SPAD CCM-200) after 1 week and 10 weeks of ozone exposure; calibration to reflect actual chlorophyll content via acetone extraction and spectrophotometry; equation provided relates SPAD index to chlorophyll content (mg g-1 FW).
- Data handling:
  - Fresh material sorted into component species and health status during harvest.
  - Data are recorded as dome-level means for subsequent analysis.

## Data structure and analysis
- Data processing:
  - All parameter values averaged to produce a mean per solardome for analysis.
  - Proportional data (injury/senescence) arcsine transformed before analysis.
- Statistical methods:
  - Stomatal conductance: One-way ANOVA (Minitab).
  - Other parameters: Split-plot or split-split plot ANOVA (Genstat).
  - Experimental factors: Main plot = ozone treatment; sub-plots = monoculture vs mixture; sub-sub-plots = canopy position when applicable.
- Data availability:
  - Injury data stored in a CSV with structure: Harvest, Species, Monoculture or mixture, part of canopy, Ozone treatment, % leaves injured or senesced, plus standard error (24 rows, 7 columns).

## Relevance to monitoring and data stewardship
- Emphasizes standardized, repeatable methodologies suitable for time-series environmental health monitoring.
- Facilitates integration with other datasets through consistent treatment definitions (ozone regimes, canopy positions, harvest layers) and explicit data structure (injury percentages with standard errors).
- Encourages accessibility of underlying data via clear data conventions and documentation of measurements and analysis approaches.