# Plant material

- A controlled ozone exposure study with Lolium perenne (ryegrass) and Trifolium repens (white clover) grown from pasture turf samples near Edinburgh, UK. Plants originated from different parents and were randomised across competition treatments and ozone exposure. Individual plants were established for ~8 weeks before forming monocultures and mixtures for ozone exposure.

## Experimental design

- Large pots (35.5 cm x 45 cm x 25 cm) with drainage, lined to prevent roots escaping.
- Each pot contained 12 plants: 4 central Trifolium repens surrounded by 8 Lolium perenne.
- Experimental units: four solardomes containing three pots per treatment (monoculture/mixture), with randomised allocation to treatments.
- Treatments:
  - Ozone exposure: two domes with controls (O3(30): continuous 30 ppb in charcoal-filtered air) and two domes with episodic rural ozone profile (O3(30+peaks)).
  - Within ozone domes: maximum daily ozone concentrations reached 80 ppb on days 1 and 4 and 100 ppb on days 2 and 3; ramped from 30 ppb to max over 2 hours, held for 6 hours, then ramped back to 30 ppb over 2 hours.
  - Other times: 30 ppb baseline in all domes.
- Timeline: ozone exposure for 12 weeks starting 26 July 2002, with two harvests (intermediate 6 Sept, final 16 Oct 2002). Plants were well-watered via mist irrigation and hand watering during warm periods.

## Data collected and measurements

- Visual assessments:
  - Whole-pot scoring for senescence and ozone-specific injury (white/pale yellow leaf stipples). Leaves classified as healthy, injured (>25% of leaf area), or senesced (>25% of leaf area). Senescence length measured as the length of the senesced portion (mm) on a sub-sample of 20 leaves per pot.
- Harvesting and biomass:
  - Two harvest events: 6 Sept (after six weeks) and 16 Oct (after 12 weeks).
  - Plants harvested in layers: outside pot, >14 cm, 7–14 cm, and (at final harvest) 0–7 cm above soil.
  - Material sorted by species and health status (Trifolium repens: healthy vs ozone-injured; Lolium perenne: healthy vs senesced).
  - Biomass dried at 65°C for at least 4 days before weighing.
- Physiological measurements:
  - Stomatal conductance (Trifolium repens) via porometer (Delta-T AP4); measurements at stable weather conditions, for upper (sunlit) and inner (shaded) canopy positions; six leaves per dome (two per canopy position).
  - Chlorophyll content (chlorophyll a + b) via SPAD meter (CCM-200); measurements after 1 week and 10 weeks of ozone exposure. Calibration against acetone-extracted chlorophyll content (mg g-1 FW) using Lichtenthaler and Wellburn (1983) equations; relationship reported as r2 = 0.90, with the equation:
    Chlorophyll content (mg g-1 FW) = (chlorophyll index × 30.448) + 417.

## Data structure and file details

- Data structure: Lolium_and_Trifolium_solardomes_Injury_data.csv
  - Rows: 24
  - Columns: Harvest, Species, Monoculture or mixture, part of canopy, Ozone treatment, % leaves that were injured or senesced (determined by biomass), standard error.
- Data handling:
  - Values aggregated to dome means prior to statistical analysis.
  - Visible injury and senescence data arcsine transformed before analysis.

## Data processing and analysis

- Statistical methods:
  - One-way ANOVA (Minitab 14) for stomatal conductance.
  - Split-plot and split-split-plot ANOVAs (Genstat 8) with:
    - Main plot: ozone treatment
    - Sub-plot: monoculture vs mixture
    - Sub-sub-plot (where appropriate): canopy position
- Data processing notes:
  - Injury and senescence data were arc-sine transformed for analysis, using dome-mean values as the analytical unit.

## Data governance and provenance considerations

- Data provenance:
  - Experiment design, treatment assignments, measurement protocols, and data processing steps are documented (including measurement instruments and calibration references).
  - The primary injury/senescence dataset is summarized per solardome and per treatment, with explicit notes on the calculations (e.g., percentage leaves injured/senesced determined by biomass).
- Metadata and reuse considerations for Data Stewards:
  - Dataset should include: study location and grid reference, plant species, seating arrangement (monoculture vs mixture), pot and dome identifiers, ozone treatment regime, harvest times, measurement instruments/models, calibration relationships (e.g., SPAD calibration to chlorophyll content), data transformations applied, and analysis models used.
  - Potential limitations to document: injury/senescence assessments are made at the pot level due to canopy integration; some measurements (e.g., chlorophyll) reflect “typical” leaves with some ozone injury present; raw per-plant data are not provided in this summary (data are dome-averaged).
  - Suggested data sharing approach: archive the Injury_data.csv with a clear data dictionary, alongside the full measurement protocols, instrument models, calibration details, and analysis scripts or notes to reproduce dome-mean analyses. Include the exact harvest dates, dome identifiers, and treatment labels to ensure discoverability and reproducibility.