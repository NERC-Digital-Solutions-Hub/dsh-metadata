# What has been recorded and what form does the data take?

## Overview
- A mesocosm study at the University of Stirling (May–Aug 2023) examining the persistence of wet wipes in beach sand and the survival of E. coli on wipe surfaces.
- Three wet wipe brands representing different compostability categories:
  - A: non-compostable (containing plastic)
  - B: home compostable
  - C: commercially compostable
- Experimental flow: wipes were cut to 7 × 7 cm squares and simulated journey from toilet to beach:
  - Flushed in 10 L tap water with 250 g sterile human feces and E. coli inoculum (1 × 10^3 CFU/ml)
  - Transferred to 2 L WWTP effluent with E. coli inoculum (5 × 10^3 CFU/ml)
  - Incubated (48 h, 15 °C, 80 rpm)
  - Transferred to 2 L seawater, incubated 24 h (15 °C, 80 rpm)
  - Moved to beach sand mesocosms (constructed from drainpipes, 10 cm sand depth)
- Weekly sampling over 15 weeks; four replicates per wipe type per week.

## Data files (five CSVs)
- Dry_weight_sand_used_in_wet_wipes_mesocosm.csv
- Background_bacterial_concentrations_in_wet_wipes_mesocosm.csv
- Water_characteristics_used_in_wet_wipes_mesocosm.csv
- Tensile_strength_of_wet_wipes_in_wet_wipes_mesocosm.csv
- Bacterial_concentrations_in_wet_wipes_mesocosm.csv

## Data collection and methods
- Sampling: weekly, four wipes per wipe type selected, removed from mesocosm.
- Preparation: sand shaken off; wipes placed in sterile PBS, vortexed; E. coli quantified by vacuum filtering through 0.45 μm membranes and plating on MLGA; CFU counted after 24 h at 37 °C.
- Wet wipe analysis: wipes dried; tensile strength measured with a 50 N digital force meter to determine force required to break each wipe.
- Measurements span multiple data aspects:
  - Dry weight of sand used, background bacterial concentrations, water characteristics, tensile strength, and bacterial concentrations on wipes.

## Purpose and context
- To study whether sewage-associated plastic waste can act as reservoirs for faecal bacteria, potential human pathogens, and antimicrobial resistance genes.
- Aligns with UKRI NERC grants: NE/S005196/1 (Microbial hitchhikers of marine plastics) and NE/V005847/1 (SPACES project).

## Data stewardship and quality
- Responsible for collection and interpretation: Rebecca Metcalf.
- Completeness: no missing data reported; data checked for anomalous values and upper/lower limits.
- Data provenance: data described with clear replication structure across files; replicates consistent across data files.

## Data contents and variable descriptions
- Replicates and timing:
  - Timepoint/Week/Date, Wipe_type, Rep (replicate)
- Measurements per file:
  - Dry_weight_sand_used_in_wet_wipes_mesocosm.csv: dry sand weight per mesocosm
  - Background_bacterial_concentrations_in_wet_wipes_mesocosm.csv: background E. coli levels in mesocosms
  - Water_characteristics_used_in_wet_wipes_mesocosm.csv: pH, salinity, and other water characteristics by mesocosm
  - Tensile_strength_of_wet_wipes_in_wet_wipes_mesocosm.csv: tensile strength (N) per wipe, weekly sampling
  - Bacterial_concentrations_in_wet_wipes_mesocosm.csv: CFU per ml and CFU per wipe on wet wipes, weekly sampling
- Example variable descriptions include:
  - Rep, Wipe_type, Timepoint, Date
  - CFU_per_ml, CFU_per_wipe
  - Tensile Strength (N)
  - pH, Salinity
  - Sand_weight_start_(g), Sand_weight_end_(g), Difference_(moisture content), Percentage_change
  - Source of E. coli, Water_type, Dilution

## Potential analyses and uses
- Compare persistence and colonisation across wipe types (A, B, C) and compostability categories.
- Assess relationship between tensile strength and bacterial survival on wipes.
- Examine trends over time (weeks) in bacterial concentrations and environmental parameters.
- Integrate sand, water, and background data to model reservoirs and exposure risk in beach environments.
- Use the datasets as inputs for replication-based statistical models or predictive analyses related to environmental microbiology and plastics in marine contexts.