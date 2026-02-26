# Plant material

## Aim
- Investigate the effects of ozone exposure on two pasture species, Lolium perenne and Trifolium repens, in monoculture and in mixture.
- Assess ozone-induced injury and senescence, stomatal conductance, and chlorophyll content.
- Harvest and quantify biomass at two time points; capture canopy-position variation and produce a dataset suitable for statistical analysis.

## Experimental design
- Large pots (35.5 cm x 45 cm x 25 cm) lined with perforated plastic to constrain roots.
- Each pot contains 12 plants: four central Trifolium repens surrounded by eight Lolium perenne.
- Monocultures (Lolium or Trifolium) and mixtures were prepared, with three pots per treatment.
- Four solardomes used for ozone exposure over twelve weeks, starting 26 July 2002.
- Two harvests: 6 September (intermediate) and 16 October (final).
- Plants kept well-watered via mist irrigation; additional hand watering during warm periods.

## Ozone exposure
- Four solardomes: two controls with ozone in charcoal-filtered air (continuous 30 ppb, O3(30)); two with episodic rural ozone profile (O3(30+peaks)).
- Ozone generation and monitoring:
  - Generated from oxygen; ozone measured every 30 minutes with a Dasibi analyser.
  - Continuous monitoring sample times: minimum 3.5 minutes per dome.
- Concentration schedule:
  - Maximum 80 ppb on days 1 and 4; maximum 100 ppb on days 2 and 3.
  - Ramp from 30 ppb to max over 2 hours, sustain max for 6 hours, then decline to 30 ppb over 2 hours.
  - Otherwise, 30 ppb outside the exposure periods.

## Visual assessments
- Whole-pot visual estimates of senescence and ozone-specific injury (white or pale yellow leaf stipples) due to combined effects.
- Leaves classified as senesced or injured if >25% of leaf area affected; otherwise healthy.
- Senescence in Lolium perenne documented as progression from leaf tip along blade.
- For a sub-sample, senesced leaf length (mm) measured on 20 randomly chosen leaves per pot.

## Harvests
- Plants cut back to 7 cm on 6 September and 16 October (post six and twelve weeks of ozone exposure).
- Harvested in layers:
  - Outside pot perimeter
  - >14 cm above soil
  - 7–14 cm above soil
  - 0–7 cm above soil (only at final harvest)
- Material separated by species and health status (healthy vs ozone-injured leaves for Trifolium repens; healthy vs senesced for Lolium perenne).
- Biomass determined after drying at 65°C for at least 4 days.

## Stomatal conductance measurements
- Measured on Trifolium repens with a porometer (Delta-T AP4).
- Conducted during stable conditions after 10–11 weeks of exposure.
- Measurements taken on six leaves per dome (two leaves per pot) from the upper (sunlit) and inner (shaded) canopy positions.

## Chlorophyll content
- Chlorophyll a + b measured with a SPAD meter (CCM-200) after 1 week and 10 weeks.
- "Typical" leaves used; some ozone injury present.
- Calibration against acetone-extracted chlorophyll (absorbance at 470, 646, 663 nm) using Lichtenthaler and Wellburn (1983) equations:
  - Chlorophyll content (mg g−1 FW) = (chlorophyll index × 30.448) + 417
- Chlorophyll index values converted to mg g−1 fresh weight via the calibration.

## Statistical analysis
- Dome means used as the observational unit; data averaged per solardome before analysis.
- Visually injury and senescence data arcsine-transformed prior to analysis.
- Stomatal conductance: one-way ANOVA.
- Other comparisons: split-plot or split-split plot ANOVA (main plot = ozone treatment; sub-plots = monoculture/mixture; sub-sub-plots = canopy position where applicable).

## Data structure
- Data file: Lolium_and_Trifolium_solardomes_Injury_data.csv
  - 24 rows, 7 columns
  - Columns include: Harvest, Species, Monoculture or mixture, part of canopy, Ozone treatment, % leaves that were injured or senesced, standard error