# What has been recorded and what form does the data take?

- Study focus: Persistence of wet wipes in beach sand and survival of Escherichia coli on wipe surfaces.
- Data format: Five CSV files providing replicate-based measurements and observations from a mesocosm experiment.
  - Dry_weight_sand_used_in_wet_wipes_mesocosm.csv
  - Background_bacterial_concentrations_in_wet_wipes_mesocosm.csv
  - Water_characteristics_used_in_wet_wipes_mesocosm.csv
  - Tensile_strength_of_wet_wipes_in_wet_wipes_mesocosm.csv
  - Bacterial_concentrations_in_wet_wipes_mesocosm.csv
- File sizes suggest compact per-measurement records, with consistent replication across files.

## Study location and timeframe

- Location: Mesocosm study conducted at the University of Stirling.
- Period: May to August 2023.

## Experimental design

- Wipe brands and compostability classes:
  - A: non-compostable (plastic-containing)
  - B: home compostable
  - C: commercially compostable
- Wipe samples: Cut into 7 × 7 cm squares.
- Experimental flow to simulate real-world pathway:
  - Toilet flushing into 10 L tap water with 250 g sterile feces + E. coli inoculum
  - Transfer to 2 L WWTP effluent with E. coli inoculum
  - Incubation and transfer to 2 L seawater
  - Final transfer to beach sand mesocosms
- Sand mesocosms: Constructed from drainpipes filled with beach sand, covered to prevent sand loss while allowing drainage.

## Data collection and measurements

- Sampling schedule: Weekly timepoints over 15 weeks; four wipes per type per timepoint.
- E. coli enumeration: Vortexing in PBS, filtration through 0.45 μm membranes, culture on MLGA plates; CFU counted after 24 h at 37 °C.
- Wet wipe strength: Tensile strength measured with a 50 N digital force meter.
- Data capture: Replicates maintained across all data files; measurements include CFU counts, tensile strength, and sand/ water characteristics.

## Variables and data content (high-level)

- Sand and water context:
  - Dry weight of sand used
  - Water type, pH, salinity
  - Background bacterial concentrations
- Wipe-specific measurements:
  - Wipe type, replicate, week/date, tensile strength (N)
  - Bacterial concentrations on wipes (CFU per wipe, CFU per ml)
  - CFU per ml in wash or rinse steps as applicable
- Experimental details:
  - Replicate identifiers, timepoint (week), date
  - Dilution factors used for microbiological assays
- Units and descriptions are documented per file (e.g., grams for weights, CFU for bacteria, Newtons for tensile strength).

## Data provenance, purpose, and funding

- Purpose: Assess sewage-associated plastic waste as reservoirs for fecal bacteria, potential pathogens, and antimicrobial resistance genes.
- Funders and project alignment:
  - UKRI Natural Environment Research Council (NERC) grants: Microbial hitchhikers of marine plastics; SPACES project (NE/S005196/1; NE/V005847/1).
- Lead data curator: Rebecca Metcalf.
- Data completeness: Checked for anomalies; no missing data reported.

## Data quality and usability for GIS

- Structure suitable for GIS-informed data products:
  - Time-series and replicate-based measurements can be joined or joined-with-attributes to create spatial-temporal maps if coupled with location metadata or beach-site attributes.
  - Variables such as pH, salinity, and bacterial concentrations can be mapped across timepoints or by wipe type to visualize spatially-relevant trends if linked to sampling locations or beach segments.
- Integration considerations:
  - Data exist across multiple related files; join keys include Replicate, Wipe_type, Week/Date, and Timepoint.
  - Consistency across replicates is noted; careful alignment of the timepoints and dilution factors is needed for cross-file aggregation.
- Limitations for GIS:
  - No explicit geographic coordinates are provided; spatial analysis would require attaching site-level location data or linking to beach locations outside the dataset.
  - The mesocosm setup is a controlled environment, so GIS products would primarily support process visualization, risk assessment, or scenario mapping rather than natural dune/beach ecology.

## Practical implications for map-based data products

- Potential maps and layers:
  - Temporal maps of CFU_per_wipe or CFU_per_ml by wipe type over the 15-week period (if geo-referenced to sampling locations or experimental bays).
  - Spatial proxies of sand characteristics (dry weight, moisture-related metrics) linked to time since exposure.
  - Tensile strength trends by wipe type across weeks as a supplementary layer for material performance vs microbial contamination.
- Suggested GIS workflow:
  - Import CSVs, create relational joins on Rep, Wipe_type, Week/Date.
  - Normalize CFU data where appropriate and create time-enabled layers.
  - Overlay with environmental attributes if location or site metadata is available or combined with beach-specific context.