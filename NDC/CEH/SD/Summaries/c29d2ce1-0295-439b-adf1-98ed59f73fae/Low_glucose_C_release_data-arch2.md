# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a low glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Purpose and scope
- Document time-series measurements of microbial carbon mineralization (14CO2 evolution) from soil under varying nitrogen (N) and phosphorus (P) treatments with a fixed low glucose carbon source.
- Conducted in the Conwy catchment, North Wales, UK, 2015.
- Data intended to support environmental monitoring by comparing carbon release under standardized nutrient amendments and glucose addition, enabling assessment of microbial activity and environmental health over time.

## Experimental design and treatments
- Treatments (Low concentration glucose, fixed carbon addition of 0.006 mM): 
  - Control (no N, no P)
  - N addition only
  - P addition only
  - N and P addition
- For each treatment, 42 soil samples were prepared.
- Soil material: 5 g per sample (dry weight equivalent), with soil cores collected and subdivided by depth (see depths below).
- Nutrient additions:
  - N addition: 33.33 units (e.g., mg/kg or equivalent per protocol)
  - P addition: 3.53 units
  - For N&P treatment: both N and P added (33.33 and 3.53 respectively)
- Plot locations and borehole context described in Plot_locations.csv; additional details in Plot_locations_metadata.rtf.

## Soil sampling and preparation
- Depth intervals (cm): 0–15, 15–30, 50–100, 100–150, 150–200, 250–300.
- Depth-based grouping for analysis: topsoil (0–30 cm), midsoil (50–100 cm), subsoil (100–300 cm).
- Samples sieved to 5 mm to remove stones and plant material and improve homogeneity, minimizing disturbance to microbial communities.

## Carbon mineralization measurement
- 14C-glucose labeled substrate added to soil surface; 5 g soil placed in sterile 50 mL tubes.
- NaOH trap (1 M) placed to capture evolved 14CO2.
- Tubes sealed and incubated at 10°C (representing mean annual catchment temperature).
- NaOH traps replaced at multiple time points: 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 hours; then weekly up to 6 weeks after labeling.
- Captured 14CO2 quantified by mixing trap with liquid scintillation fluid and counting with a scintillation counter.

## Data structure and metadata
- Column structure for measurements:
  - Transect (refers to Cage location in Plot_locations.csv)
  - Row (refers to Cage location in Plot_locations.csv)
  - Depth (cm, soil depth sampled)
  - Timepoint columns: 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 hours
  - DPM counts for each timepoint
  - BLANK columns: DPM counts from blank traps
  - STD1_HMWC, STD2_HMWC+N, STD3_HMWC+N+P, STD4_HMWC+P (DPM counts for standards)
  - Empty cells indicate missing data
- Metadata and quality control:
  - Quality control and reference data are provided in Low_glucose_C_release_data_metadata.csv
  - Column names and descriptions are documented in the same metadata file
- Supporting location data:
  - PlotLocations: Plot_locations.csv (borehole locations)
  - PlotLocations metadata: Plot_locations_metadata.rtf

## Data management and access
- Primary application data file: Low_glucose_C_release_data.csv
  - Contains treatment, sample count (e.g., 42 per treatment), soil mass, glucose addition, and N/P addition details per sample
- Supporting accessibility:
  - Plot_locations.csv and Plot_locations_metadata.rtf describe sampling sites
  - Metadata file Low_glucose_C_release_data_metadata.csv provides data structure and variable descriptions

## Quality, standards and reproducibility
- Use of standardized sampling depth grouping and consistent incubation temperature (10°C) to enable comparability across samples and depths.
- Inclusion of blank controls and standard counts (DPM) for calibration and quality assurance.
- Time-resolved measurements spanning short (0.5–6 h) to long-term (up to 1008 h) intervals to capture initial and sustained mineralization dynamics.

## Relevance for environmental monitoring
- Provides a standardized, time-resolved view of soil microbial carbon mineralization under nutrient amendments, useful for:
  - Assessing soil microbial response to N and P inputs
  - Comparing carbon release dynamics across soil depths and soil carbon pools (topsoil to subsoil)
  - Supporting interpretation of environmental health, carbon cycling processes, and potential policy relevance for nutrient management

## Key considerations and use cautions
- Missing data indicated by empty cells; users should account for gaps in timepoints or depths.
- Depth grouping may affect interpretation when comparing topsoil, midsoil, and subsoil responses.
- Data interpretation should reference the associated Plot_locations and metadata to ensure correct spatial context.