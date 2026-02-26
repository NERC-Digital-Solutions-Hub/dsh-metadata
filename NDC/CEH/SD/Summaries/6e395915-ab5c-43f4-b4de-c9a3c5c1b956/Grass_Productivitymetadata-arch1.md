# Grass_Productivity.csv

## Overview
- A from-experiment dataset detailing biomass productivity under different nutrient treatments.
- Experimental setup uses 1 x 1 m quadrats with 9 swards per quadrat, each sward 10 x 10 x 10 cm, totaling 45 swards.
- Treatments: Water (de-ionised), Nitrogen (N) 150 kg N/ha, Phosphorus (P) 30 kg P/ha, N + P (150 kg N + 30 kg P/ha), and Control (initial biomass cut).
- Replication: 9 samples per treatment (total 45 swards across 5 treatments).
- Measurements are biomass-related and standardized to grams dry weight per 100 cm^2 (per 10 x 10 cm sward).

## Experimental design and sampling regime
- Quadrats: 1 m x 1 m (randomly selected) with 9 swards sampled per quadrat.
- Within-quadrat sampling: 5 swards per quadrat recorded, yielding 45 swards total for the experiment.
- Nutrient applications: Water, N, P, or N + P applied as solutions.
- Application details:
  - Nitrogen source: Ammonium nitrate (NH4NO3)
  - Phosphorus source: Sodium phosphate (Na2HPO4)
  - First application: 18/08/2016
  - Second application: 24/09/2016
  - Volume: 20 mL of each solution per sward
- Field conditions: Swards soaked to field capacity then maintained in a glasshouse at 16°C (day) / 10°C (night).

## Treatments and sampling specifics
- Treatments and replicate count:
  - Control (initial biomass cut): 9 samples
  - Water: 9 samples
  - Nitrogen (N): 9 samples
  - Phosphorus (P): 9 samples
  - Nitrogen + Phosphorus (N + P): 9 samples
- Within each treatment, biomass measurements are taken as two cuts:
  - First_cut: biomass cut in g per 100 cm^2 on 23/09/2016 (not applicable for Control)
  - Second_cut: biomass cut in g per 100 cm^2 on 23/10/2016

## Collection, processing and measurements
- Harvesting: Swards cut with a spade and transported to the lab; cut to 10 x 10 x 10 cm; all vegetation within quadrat harvested to ~1 cm height.
- Weighing and drying:
  - Fresh weight recorded in the field.
  - Samples oven-dried at 80°C for 24 hours, then reweighed to determine dry weight.
- Units: Dry weight measured as grams per 100 cm^2 (g/100 cm^2), reflecting biomass productivity per 10 x 10 cm sward.

## Data structure and variables
- Core variables (Grass_Productivity.csv):
  - Transect: Number of transect (within-plot position)
  - Row: Row number within the plot
  - Treatment: Water, N, P, N + P, or Control
  - First_cut: Biomass cut in g/100 cm^2 on 23/09/2016 (n/a for Control)
  - Second_cut: Biomass cut in g/100 cm^2 on 23/10/2016
- Nature of recorded values: Grams dry weight per 100 cm^2
- Initial measurements: Table-like data provide initial wet and dry weights for some rows (per 100 cm^2) prior to treatments; useful as baseline references.

## Metadata and related data
- Location data: For row and transect locations, refer to Plot_locations.csv.
- Location metadata: Plot_locations_metadata.rtf describes Plot_locations.csv contents.
- Cage coordinates: Location references point to Cage coordinates for precise row/transect positioning.
- Data provenance and reproducibility: Data sources and methodologies are logged (calibration of balances monthly; sample processing steps).

## Quality control and notes
- Balances calibrated by laboratory technicians monthly.
- Quality control field notes include: NA (no explicit quality-control metrics beyond calibration and standard procedure), but processing steps are standardized (fresh weight → oven-dry → dry weight).
- Data interpretation considerations:
  - First_cut is not applicable for Control.
  - Biomass expressed as dry weight per 100 cm^2, enabling comparability across sward sizes and treatments.
  - Data can be used to compare productivity across N, P, and N+P under controlled field-capacity and glasshouse conditions, with baseline for initial biomass.

## How analysts can use this dataset
- Compare biomass productivity across nutrient treatments (N, P, N+P) relative to Water and Control.
- Assess treatment effects on two harvest times (First_cut vs Second_cut) where applicable.
- Normalize biomass to 100 cm^2 to compare across swards and quadrats.
- Integrate with Plot_locations.csv to analyze spatial patterns (row/transect alignment, potential spatial autocorrelation).
- Use available metadata to document data lineage, reproducibility, and to locate raw measurement details or cross-reference with other plots or trials.