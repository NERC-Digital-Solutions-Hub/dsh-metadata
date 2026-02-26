# Plant material L. perenne and T. repens plants were vegetatively propagated from turf samples of pasture managed for silage near Edinburgh, UK (Grid reference NT245642).

## Experimental design
- Plants: Lolium perenne (ryegrass) and Trifolium repens (white clover) propagated from pasture turf; randomised between different competition and ozone treatments.
- Setup: Large containers (solardomes) with drainage holes lined with perforated plastic; each pot contained 12 plants (4 central, 8 surrounding). Each solardome included three pots of L. perenne monoculture, three pots of T. repens monoculture, and three pots of a mixed culture (4 central T. repens; 8 surrounding L. perenne).
- Duration: Exposure for 12 weeks starting 26 July 2002; two harvest periods (26 July–6 Sept; 7 Sept–16 Oct).
- Plant care: Maintained well-watered via mist irrigation at 04:00, with additional hand watering as needed.

## Ozone exposure
- Design: Four solardomes in a randomised block; ozone generated from oxygen; two domes served as controls (30 ppb O3) using charcoal-filtered air; two domes received an episodic rural ozone profile (O3(30+peaks)).
- Targets: Maximum ozone concentrations reached 80 ppb on days 1 and 4, and 100 ppb on days 2 and 3; ramped up over 2 hours, held for 6 hours, then tapered over 2 hours; otherwise maintained at 30 ppb.
- Monitoring: Ozone measured every 30 minutes with an ozone analyser; continuous control via mass flow controllers; calibration of equipment performed as part of protocol.

## Harvests
- Timing: Harvests at 6 weeks and 12 weeks post-exposure.
- Method: Plants harvested in layers (outside pot perimeter; >14 cm above soil; 7–14 cm; and for final harvest additionally 0–7 cm). Material sorted by species and plant part (T. repens stolons, flowers, leaves; L. perenne leaves and stems; stems absent above 7 cm for L. perenne).
- Processing: Samples dried at 65°C for at least 4 days to determine biomass; subsamples of L. perenne leaf material ground and dried at 105°C for CHN analysis (C and N content) using an automated analyser.

## Physiological measurements
- Leaves: Representative leaves chosen based on age; Leaf 1 = newest fully expanded leaf; Leaf 2 = second newest.
- Sample size: Minimum of six leaves per measurement day, same physiological stage.
- A-Ci curves: Net CO2 assimilation (A) vs substomatal CO2 (Ci) to assess photosynthetic efficiency and capacity; measured with CIRAS I and 1000 μmol m-2 s-1 PAR, CO2 stepped from 0 to 2000 ppm.
  - Levels: Ci steps at 0, 50, 100, 200, 400, 600, 800, 1000, 1500, 2000 ppm.
  - Calculations: A and Ci derived with CIRAS software; data used to parameterize Farquhar model; Jmax estimated from A-Ci curve asymptote (Ci > 500 ppm) using a specified method; T-dependent I* used to adjust calculations.
- A-Q curves: Light response curves (A-Q) with CO2 fixed at 1000 ppm and PAR steps from 10 to 2000 μmol m-2 s-1 to derive photosynthetic parameters; used to complement A-Ci data.
- Analysis: Comparisons of Vc,max (via initial slope of A vs Ci for Ci up to 300 ppm) and Jmax across treatments.

## Statistical analysis
- Data aggregation: For each parameter, values averaged per solardome, then used for analyses.
- Tests:
  - One-way ANOVA (Minitab) for Jmax by ozone treatment (no monoculture vs mixture comparison).
  - GLM regression (SPSS) for comparing A vs Ci relationships between treatments.
  - Split-plot and split-split-plot ANOVA (Genstat) with main factor of ozone and subplot of growth form (monoculture vs mixture); canopy position included as a sub-sub plot for biomass analyses.
- Data structure notes:
  - Data used include A-Ci and CHN-derived measurements, with separate datasets for biomass and canopy distribution.

## Data structures (datasets and fields)
- Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv
  - 220 rows, 7 columns
  - Columns: Species, Leaf number, number of weeks since start of exposure, Treatment, dome.pot, Ci, A corrected for leaf area
- Lolium_and_Trifolium_solardomes_biomass_data.csv
  - 16 rows, 6 columns
  - Columns: Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight (g per pot, cutting height 7cm), standard error
- Lolium_and_Trifolium_solardomes_clover_distribution_data.csv
  - 28 rows, 6 columns
  - Columns: Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error
- Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv
  - 32 rows, 6 columns
  - Columns: Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error

## Particular challenges and data governance considerations
- Challenges highlighted in related aims include incomplete user needs, timely data provision, meeting metadata standards by data creators, interoperability across different systems/formats, handling large datasets, and updating legacy databases.
- For data stewardship: the dataset is organized with explicit structure, clearly labeled files, and well-defined variables and measurement units; includes calibration and processing details (e.g., instrument models, curve-fitting methods) to support reproducibility; metadata should capture experimental conditions, treatment schedules, and data processing steps; data sharing should ensure access to the three CSV datasets and their documentation, with clear provenance and potential for reanalysis of photosynthesis parameters (A, Ci, Jmax, Vc,max) and biomass distribution by canopy layer and species.