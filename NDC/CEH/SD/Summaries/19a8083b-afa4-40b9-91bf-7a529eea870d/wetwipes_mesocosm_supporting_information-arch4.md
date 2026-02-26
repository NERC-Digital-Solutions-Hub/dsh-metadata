# What has been recorded and what form does the data take?

- Five CSV files are included in the dataset:
  - Dry_weight_sand_used_in_wet_wipes_mesocosm.csv (223 B)
  - Background_bacterial_concentrations_in_wet_wipes_mesocosm.csv (333 B)
  - Water_characteristics_used_in_wet_wipes_mesocosm.csv (217 B)
  - Tensile_strength_of_wet_wipes_in_wet_wipes_mesocosm.csv (3.6 KB)
  - Bacterial_concentrations_in_wet_wipes_mesocosm.csv (7.25 KB)

# Where and when were the data collected?

- Mesocosm study conducted at the University of Stirling
- Data collected between May and August 2023

# Experimental design

- Three commercial wet wipe brands representing different advertised compostability:
  - A: non-compostable (contains plastic)
  - B: home compostable
  - C: commercially compostable
- Wet wipes cut into replicate 7 × 7 cm squares
- Sequence of treatments to simulate bathroom to beach journey: flushed, discharged from WWTP into seawater, then beach sand
- Experimental workflow:
  - Placed in tap water with sterile human feces and E. coli inoculum
  - Transfer to effluent from a WWTP with additional E. coli
  - Incubation steps (48 h, then 24 h in seawater)
  - Transferred to beach sand mesocosms
  - Mesocosms constructed from drainpipes filled with sand and covered to prevent loss

# How were the data collected?

- Weekly sampling over 15 weeks
- For each wipe type:
  - Four wipes per week were collected per replicate
  - Loose sand shaken off; wipes placed in PBS; vortexed
  - E. coli enumerated by vacuum filtration onto selective media; CFU counted after incubation
  - Wipes dried; tensile strength measured with a digital force meter

# Why were the data collected?

- To study sewage-associated plastic waste as reservoirs for fecal bacteria, potential human pathogens, and antimicrobial resistance genes
- To fulfil UKRI NERC grant requirements:
  - Microbial hitchhikers of marine plastics: the survival, persistence & ecology of microbial communities in the Plastisphere (NE/S005196/1)
  - NERC-GCRF SPACES project (NE/V005847/1)

# Who was responsible for the collection and interpretation of data?

- Rebecca Metcalf

# Completeness. Are any data absent from the dataset?

- Data were checked for anomalies; no data are reported as absent

# Data file contents

- Replicates are consistent across all data files
- Dry_weight_sand_used_in_wet_wipes_mesocosm.csv
  - Data on the dry weight of sand used for the mesocosms
- Background_bacterial_concentrations_in_wet_wipes_mesocosm.csv
  - Background bacterial concentrations used in the mesocosms
- Water_characteristics_used_in_wet_wipes_mesocosm.csv
  - Water characteristics of water types used in the mesocosms
- Tensile_strength_of_wet_wipes_in_wet_wipes_mesocosm.csv
  - Tensile strength of wet wipes (sampled weekly)
- Bacterial_concentrations_in_wet_wipes_mesocosm.csv
  - Bacterial concentrations of E. coli on the wet wipes (sampled weekly)

- Variable and data structure notes:
  - Rep, variables describing replicates
  - Measurements include: Foil_weight (g), Sand_weight_start (g), Sand_weight_end (g), Difference (moisture content in g), Percentage_change
  - Source of E. coli; Water_type; pH; Salinity
  - Timepoint/Week/Date; Wipe_type
  - For bacterial data: CFU_per_ml, CFU_per_wipe
  - Tensile Strength (N) data include Week, Date, Rep, Wipe_type, Tensile Strength (N)
  - Data tables align by Replicate (Rep) across files

- Note: The dataset provides both environmental context (water/sand conditions) and biological measurements (E. coli CFUs) alongside physical properties (tensile strength) to facilitate integrated analysis.