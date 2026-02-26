# Grass_Productivity.csv

- Purpose and scope
  - Dataset from a grass productivity experiment using 1 x 1 meter quadrats with randomized treatments.
  - Within each quadrat (n = 9), five 10 x 10 x 10 cm swards were sampled (total 45 swards) to assess biomass under different nutrient treatments.
  - Two harvest events: First_cut on 23/09/2016 and Second_cut on 23/10/2016; values reported as grams of dry weight per 100 cm².

- Spatial and geographic context
  - Row and transect locations are defined in Plot_locations.csv.
  - Precise positioning within rows/transects referenced via Cage coordinates.
  - See Plot_locations_metadata.rtf for description of Plot_locations.csv.

- Experimental design and treatments
  - Sampling area: 1 x 1 m quadrats randomly selected.
  - Treatments applied to swards: Water (control/deionised water), Nitrogen (N: 150 kg N/ha), Phosphorus (P: 30 kg P/ha), and N + P (150 kg N/ha + 30 kg P/ha).
  - For comparison, an initial biomass cut (control) was recorded; there were 9 samples per treatment.

- Application details
  - Each solution applied in 20 mL volumes.
  - First application date: 18/08/2016; second application date: 24/09/2016.

- Collection and laboratory methods
  - Swards harvested with a spade; within-quadrat vegetation trimmed to 1 cm height and weighed fresh.
  - Samples oven-dried at 80°C for 24 hours and reweighed to obtain dry weight.
  - Initial wet/dry weights recorded for context; dry weight used for productivity metrics.

- Data structure and key variables
  - Primary fields: Transect (transect number), Row (row number), Treatment (Water, N, P, N + P).
  - Biomass measures: First_cut and Second_cut (g per 100 cm²) corresponding to 23/09/2016 and 23/10/2016, respectively.
  - Units: Dry weight in grams per 100 cm².

- Quality control and documentation
  - Balances calibrated monthly by laboratory technicians.
  - Quality control section marked as NA; supporting metadata references include Plot_locations.csv and Plot_locations_metadata.rtf.

- Practical considerations for GIS work
  - Spatial mapping relies on Plot_locations.csv and Cage coordinates for precise geolocation within rows/transects.
  - Data is nested (quadrats -> swards; multiple treatments per plot), with per-sward biomass per 100 cm², enabling high-resolution spatial analysis at 10 x 10 cm scales within quadrats.
  - Time-series aspect: two harvest dates allow assessment of temporal changes in productivity across treatments.
  - Harmonization notes: ensure consistent interpretation of units (g per 100 cm²) and align records to plotting coordinates via the referenced location files.