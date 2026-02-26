# Sunflower seed predation rates in Biodiversity and Ecosystem Function in Tropical Agriculture (BEFTA) plots, Sumatra, Indonesia

## Overview
- Study of granivory (sunflower seed predation) across BEFTA plots in Sumatra, Indonesia.
- Locations: three Pt Ivo Mas Tunggal estates in Riau Province (Ujung Tanjung, Kandista, Libo) with mature and replanted stands.
- Timeframe: data collected in 2014 (mature) and 2016–2017 (mature and replanted).

## Experimental design and sampling regime
- Experimental setup: 18 plots established in 2013 as part of vegetation management research.
- Plot layout: 50 x 50 m plots, with 50 m between plots and approximately 1000 m to the nearest major track on one side.
- Sampling positions: three positions per plot at 45°, 165°, and 285° from compass north.
- Granivory test unit: ten shelled sunflower seeds on a paper disc (~15 cm diameter), covered by a polystyrene plate ~10 cm above soil, protected from rain.
- Treatments (four per replicate): cage + grease, cage only, grease only, open (no protection).
- Test deployment: one test per sampling position per plot; exposure duration ~24 hours.
- Sampling frequency: once in 2014 (mature stands) and five times in 2016–2017 (both mature and replanted stands).

## Measurements
- Response variable: total seeds remaining out of ten, with decimals allowed (e.g., 3.5) to reflect partial consumption.

## Data collection details
- Field procedure includes placement of seeds, application of treatments, and recording of seeds remaining after ~24 hours.
- Rainfall data collected for the 24-hour sampling window (dayrain) at the nearest weather station.
- Notes field: any observations or data entry changes recorded in allnotes.

## Treatments and experimental setup
- Four treatment configurations to isolate predation effects:
  - remain_cage_grease (cage + grease)
  - remain_open (open)
  - remain_cage (cage only)
  - remain_open_grease (open with grease)
- Exclosures and ant-poison context noted for 2016–2017 in BEFTA plots.

## Data quality control
- Basic data checks for impossible values (e.g., more seeds remaining than possible).
- 50% of data entry cross-checked against original field sheets; error rate <1%.
- All changes logged with dataset.

## Data storage and format
- Data stored in three separate CSV files:
  - SunflowerSeedPredationRates_2014.csv (mature stands)
  - SunflowerSeedPredationRates_2016_2017.csv (mature stands)
  - SunflowerSeedPredationRates_replants.csv (replanted stands)
- Format: thin format; one observation per line.
- Key fields/columns include:
  - Estate_abbrev (estate name)
  - Plot_no (three-character plot identifier, e.g., C01)
  - Triplet (plot set identifier; three plots per set)
  - Treatment (how plots have been managed since Feb 2014)
  - Period (discrete sampling period)
  - Position (compass heading where border intercept occurred)
  - Date_set / Time_set (seed placement date/time)
  - Date_coll / Time_coll (seed remaining collection date/time)
  - seedstreat (seed treatment: remain_cage, remain_open, remain_cage_grease, remain_open_grease)
  - seedsremaining (out of ten; decimal values allowed)
  - dayrain (24-hour rainfall from 8am–8am at nearest station)
  - allnotes (field or data-entry observations)
  - SAFE_distance (distance relevant to exclosure/ant-poison context; may indicate data to exclude)

## Miscellaneous and provenance
- Funding reference: NE/P00458X/1.
- Data coverage: BEFTA core plots (2016–2017) and replanted plots (replants dataset).
- Additional plot details (coordinates and plotting notes) are included in the dataset metadata. 

## Usage guidance for analysts
- Suitable for comparing predation rates across treatments, estates, plot types (mature vs replanted), and sampling periods.
- Consider rainfall (dayrain) and treatment interactions when modelling granivory.
- Exercise caution with SAFE_distance in analyses related to exclosures and ant-poison contexts; data there may be less suitable for certain analyses.
- Use the thin-format datasets to merge observations across years and plots; ensure correct interpretation of period, position, and plot identifiers.