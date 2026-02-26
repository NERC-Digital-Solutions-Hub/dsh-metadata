# Grass_Productivity.csv

## Overview
- Dataset documents grass productivity under different nutrient and water treatments using a 1 x 1 m quadrat design.
- Within each of 9 quadrats, 5 swards (10 x 10 x 10 cm) were sampled, totaling 45 swards.
- Location references are via Plot_locations.csv; precise row/transect coordinates are provided there.
- Measurements include fresh and dry biomass weights collected at two harvest dates.

## Experimental design
- Quadrat size and selection: 1 x 1 m quadrats randomly selected.
- Sampling within quadrats: 9 swards per quadrat (total of 45 swards across all quadrats).
- Treatments applied (for swards): Water (deionised), Nitrogen (N), Phosphorus (P), Nitrogen + Phosphorus (N + P), plus a Control representing initial biomass cut.
- Nutrient applications:
  - Nitrogen source: ammonium nitrate (NH4NO3)
  - Phosphorus source: sodium phosphate (Na2HPO4)
- Application schedule: First application on 18/08/2016; second on 24/09/2016.
- Application volumes: 20 mL of each solution per sward.

## Data collection and processing
- Field collection: Swards harvested with a spade, cut to 10 x 10 x 10 cm, all vegetation harvested to ~1 cm height.
- Weighing protocol: Fresh weight recorded in the field; samples oven-dried at 80°C for 24 hours then reweighed to obtain dry weight.
- Field-to-lab workflow includes bagging samples and maintaining consistent processing times.

## Measurements and units
- Reported measurements: 
  - Wet weight (initial) per sward
  - Dry weight per sward
  - First_cut and Second_cut biomass (grams per 100 cm^2)
- Final data values are reported as grams per 100 cm^2.
- Time points:
  - First_cut corresponding to 23/09/2016
  - Second_cut corresponding to 23/10/2016

## Data structure and documentation
- Key fields:
  - Transect (number of transect)
  - Row (number of row)
  - Treatment (Water, N, P, N + P)
  - First_cut (g per 100 cm^2)
  - Second_cut (g per 100 cm^2)
  - Initial wet weight (g) and initial dry weight (g) per sward
- Supporting metadata:
  - Plot_locations.csv contains row/transect locations
  - Plot_locations_metadata.rtf provides description for Plot_locations.csv

## Quality control and notes
- Quality Control: not applicable/NA in the provided documentation.
- Documentation gaps to consider for stewardship:
  - Explicit QC procedures and calibration records are not described beyond monthly balance calibrations.
  - Dependency on external location metadata files for precise geolocation and sampling context.