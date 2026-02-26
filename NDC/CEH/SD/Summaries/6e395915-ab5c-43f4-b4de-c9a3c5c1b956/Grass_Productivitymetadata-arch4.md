# Grass_Productivity.csv

## Overview
- Field experiment measuring grass productivity under nutrient treatments.
- Experimental units: 1 x 1 m quadrats with randomized selection; each quadrat contains 5 swards (10 x 10 x 10 cm) for a total of 45 swards across treatments.
- Treatments: Water (de-ionised), Nitrogen (N), Phosphorus (P), and Nitrogen plus Phosphorus (N+P).
- Data captured include biomass weights (fresh and dry) and biomass yields from two sequential harvests.

## Experimental design and sampling
- Quadrat size and layout: 1 x 1 m quadrats; randomly selected.
- Within-quadrat sampling: 9 swards per quadrat (5 swards per sampling unit, total 45 swards).
- Field setup: Swards soaked to establish field capacity, maintained in a controlled glasshouse (16°C day / 10°C night).
- Fieldwork timeline: First application on 18/08/2016; second application on 24/09/2016.
- Harvest dates: First cut on 23/09/2016; second cut on 23/10/2016.
- Biomass processing: Fresh weight measured in the field, samples oven-dried at 80°C for 24 hours, then reweighed to obtain dry weight.

## Treatments and application details
- Nitrogen (N): 150 kg N/ha
- Phosphorus (P): 30 kg P/ha
- N + P: 150 kg N/ha + 30 kg P/ha
- Water: De-ionised water (control)
- Each treatment group includes 9 samples.

## Data collection and processing
- Measurements per sward: fresh weight and dry weight after drying.
- Data captured as grams per sample; initial measurements include wet and dry weights for turf.
- Two biomass harvests per sward corresponding to First_cut and Second_cut (grams per 100 cm²).
- Units: grams (g); biomass values reported as g per 100 cm².

## Data structure and key fields
- Transect: Transect number (categorical/ordinal).
- Row: Row number within transect.
- Treatment: Water, N, P, or N + P.
- First_cut: Biomass after the first harvest (g per 100 cm²).
- Second_cut: Biomass after the second harvest (g per 100 cm²).
- Wet weight: Initial fresh weight of turf (g per 100 cm²) for each sward.
- Dry weight: Initial dry weight of turf (g per 100 cm²) for each sward.
- Additional context: Each row references biomass data per sward within the quadrats; Field-scale sampling details are linked to Plot_locations.csv and related metadata.

## Location and metadata references
- Plot locations: Refer to Plot_locations.csv for row and transect coordinates.
- Plot metadata: See Plot_locations_metadata.rtf for descriptions of Plot_locations.csv.

## Quality control and governance
- Balances/calibration: Balances calibrated monthly by laboratory technicians.
- Quality notes: No explicit quality control (NA) indicated in the documentation.
- Data governance considerations: Metadata completeness (units, per-100 cm² normalization), clear treatment labeling, and linkages to location metadata are essential for interoperability and reuse.

## Key dates and conditions
- First application: 18/08/2016
- Second application: 24/09/2016
- First harvest: 23/09/2016
- Second harvest: 23/10/2016
- Field conditions: Swards maintained at field capacity; glasshouse conditions with controlled temperature.