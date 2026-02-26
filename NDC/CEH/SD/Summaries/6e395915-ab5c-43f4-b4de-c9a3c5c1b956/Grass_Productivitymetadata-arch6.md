# Grass_Productivity.csv

## Overview
- Dataset documenting grass productivity biomass under different nutrient treatments.
- Experimental framework: small-scale field plot experiment with controlled nutrient applications and two harvests.
- Data intended to enable self-service analysis of biomass response to N and P treatments over time.

## Experimental design
- Plot layout: 1 x 1 metre quadrats randomly selected.
- Within each quadrat: 5 individual swards sampled (total of 45 swards across 9 quadrats).
- Treatments (9 samples per treatment): 
  - Water (deionised)
  - Nitrogen (N) at 150 kg N/ha
  - Phosphorus (P) at 30 kg P/ha
  - Nitrogen + Phosphorus (N + P) at 150 kg N/ha + 30 kg P/ha
- Initial condition: an initial biomass cut recorded as control.
- Sampling regime: two harvests
  - First_cut recorded on 23/09/2016
  - Second_cut recorded on 23/10/2016

## Nutrient solutions and application details
- Nitrogen source: ammonium nitrate (NH4NO3)
- Phosphorus source: sodium phosphate (Na2HPO4)
- For each treatment, 20 mL of the corresponding solution was applied per sward.

## Collection methods and processing
- Biophysical sampling: swards cut to 10 x 10 x 10 cm within each 100 cm^2 sward and harvested at ~1 cm height.
- In-field measurement: fresh weight recorded (grams).
- Lab processing: samples oven-dried at 80°C for 24 hours, then re-weighed to determine dry weight.
- Samples were stored in a controlled environment (field capacity after overnight soaking, glasshouse conditions: 16°C day / 10°C night).

## Data structure and variables
- File: Grass_Productivity.csv
- Core variables (per record):
  - Transect: transect identifier
  - Row: row number
  - Treatment: one of Water, N, P, N + P
  - First_cut: biomass (grams per 100 cm^2) harvested on 23/09/2016
  - Second_cut: biomass (grams per 100 cm^2) harvested on 23/10/2016
- Nature and units: grams of dry weight per 100 cm^2
- Notes on data structure: rows and transects are coded; each row corresponds to a specific sward within a quadrat, with associated treatment and two harvest measurements.

## Location and metadata references
- Plot locations referenced in Plot_locations.csv
- Description of Plot_locations.csv available in Plot_locations_metadata.rtf
- For precise location mapping, coordinates may be in Cage data accompanying the row/transect layout.

## Quality, metadata, and documentation
- Field and lab instrumentation: balances used; monthly calibration by laboratory technicians.
- Analytical method: fresh weight measured in-field; dry weight determined post-oven-drying (80°C, 24 hours).
- Reported values: dry biomass per 100 cm^2; two harvest timepoints documented.
- Quality control notes: NA (no explicit QC measures documented beyond standard calibration and processing steps).