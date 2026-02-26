# Grass_Productivity.csv

## Overview
- Document describes an experimental study designed to measure grass productivity under different nutrient treatments within fixed sampling units.
- Aims to quantify biomass production and provide data suitable for monitoring environmental inputs (water, nitrogen, phosphorus) and their effects on productivity.

## Experimental design and sampling regime
- Sampling area: 1 x 1 square metre quadrat (randomly selected).
- Within each quadrat: 9 swards (each 10 x 10 x 10 cm).
- Sub-samples: 5 swards per quadrat (total of 45 swards across treatments).
- Spatial structure recorded via Row and Transect identifiers; precise locations linked to Plot_locations.csv.

## Treatments
- Water (deionised water)
- Nitrogen (N): 150 kg N/ha (NH4NO3)
- Phosphorus (P): 30 kg P/ha (Na2HPO4)
- N + P: 150 kg N/ha + 30 kg P/ha
- Control: initial biomass cut (no treatment)

## Application details
- First application date: 18/08/2016
- Second application date: 24/09/2016
- Application volume: 20 mL of each solution
- Control condition: initial biomass cut used as baseline

## Collection and processing methods
- Harvest: swards cut to 10 x 10 x 10 cm using a spade; all vegetation within quadrat collected.
- Fresh weight measured in the field; samples transported to lab.
- Lab processing: dried in an oven at 80°C for 24 hours; dry weight reweighed.
- Initial weights recorded for each sample (wet and dry weights).

## Field and laboratory conditions
- Swards soaked in water overnight; drained for 48 hours to establish field capacity.
- Temp control: glasshouse conditions with 16°C day / 10°C night.
- Instruments: balances calibrated monthly by laboratory technicians.

## Nature and units of recorded values
- Primary output: grams dry weight per 100 cm² (g/100 cm²).
- Data includes:
  - First_cut: biomass cut on 23/09/2016 (g per 100 cm²)
  - Second_cut: biomass cut on 23/10/2016 (g per 100 cm²)
  - Associated identifiers: Transect, Row, Treatment

## Data structure and metadata references
- Grass_Productivity.csv records: Transect, Row, Treatment, First_cut, Second_cut.
- Location details linked via Plot_locations.csv; description of Plot_locations.csv provided in Plot_locations_metadata.rtf.

## Quality control and data governance
- Calibration: balances calibrated monthly.
- Quality control field: not explicitly detailed (Quality Control: NA in the document).
- Metadata availability: plot location metadata and descriptions referenced (Plot_locations.csv and Plot_locations_metadata.rtf).
- Data sharing and governance considerations highlighted for environmental monitoring contexts (implications for data openness and metadata completeness).