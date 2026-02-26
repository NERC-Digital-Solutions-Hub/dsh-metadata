# Turf2Surf - Nutrient addition experiment

## Aim
- Assess stoichiometric coupling of carbon (C), nitrogen (N), and phosphorus (P) and how soil respiration and N2O flux respond to C and nutrient additions across soils of different land-use intensities.
- Use pilot results to inform nutrient addition levels and timing for the main experiment.
- Generate standardized data suitable for linking to ecosystem process modelling (e.g., JULES) and support environmental monitoring through well-documented datasets.

## Scope and setting
- Conducted within the Turf2Surf project in the Conwy catchment.
- Four sites representing different land-use types: bog, acid grassland, improved grassland, and arable land.
- Goals include measuring soil respiration and N2O fluxes, along with C, N, and P dynamics, across topsoil and subsoil layers.

## Experimental design

### Pilot experiment (topsoil 0–15 cm)
- Sites: Aber Henfaes farm (grassland), Clocaenog forest (conifer woodland), bog near Aber Henfaes.
- Treatments: Varied C, N, and P additions, including combinations (C, N, P, CN, CP, NP, CNP) and C compounds mimicking root exudates.
- C additions: 0.4 mg C/g soil or 1.2 mg C/g soil; N added as NH4NO3-N; P as KH2PO4; C:N and C:P ratios explored.
- Measurements: CO2 production via gas sampling at multiple time points after incubation; used to calibrate incubation times (bog required ~2 h; grassland/conifer ~1 h).
- Additional step: A second nutrient addition event performed to activate microbial communities; included a mercury (HgCl2) negative control to assess nutrient distribution.
- Moisture management: Cores kept at field capacity with artificial rain solution to mimic UK rainfall; water loss accounted for by weight adjustments.

### Main experiment
- Sites and soils: Nant-y-Brwn bog; Capel Curig acid grassland; Hiraethlyn acid grassland; Conwy arable field.
- Core sampling: Intact soil cores (4 cm diameter) to 100 cm depth; top 0–15 cm and bottom 85–100 cm separated; 216 cores prepared in perforated racks to collect leachate.
- Treatments: Full factorial of eight nutrient treatments (Control, C, N, P, CN, CP, NP, CNP).
- C and N/P rates: Total C addition 1.20 mg C g-1 dry soil over 3 days (0.4 mg C g-1 per day); N and P added in ratios based on pilot results (C:N = 10; C:P = 70).
- Incubation schedule: After first 3 days of additions, incubations at 4, 5, 6, 8, 10, and 12 days to capture delayed responses; mercury control included for a short period.
- Moisture management: Hydration adjusted with artificial rain solution every other day to maintain moisture.

## Measurements and methods

### Gas measurements
- CO2 and N2O measured from identical incubation samples.
- Sample collection: 60 mL gas samples, sealed in 20 mL pre-evacuated vials; staged transfers ensure representative concentrations.
- Analysis: CO2 via gas chromatography (GC) with Porapak QS column; N2O quantified with appropriate standards.
- Time points: Pilot phase used 0, 1–3 hours post-closure depending on site; main phase used standardized incubation times per site.
- Standards: CO2 standards at 250, 500, 1000 ppm; N2O standards at 5, 10, 15 ppm.

### Nitrogen mineralization (Nmin)
- Measured on control cores after flushing leached soil with artificial rain solution for 4–5 days.
- Incubation duration: 4 weeks at 10°C.
- Extraction: 10 g moist soil extracted with 100 mL 1 M KCl; nitrate (NO3–) and ammonium (NH4+) quantified.
- Calculations: Total N mineralization derived from NO3– and NH4+; also expressed per g dry weight and per g organic matter (acid-insoluble LOI-based OM assessment).

### Data collection and personnel
- Field sampling: Helen C. Glanville, Miles Marshal, Ben Winterbourn, David Pastrana, Maria C. Blanes.
- Laboratory work: Maria C. Blanes, David Pastrana, Sabine Reinsch.
- Calculations and data analysis: Sabine Reinsch.
- Purpose: Link plant and soil nutrient data to aboveground and belowground ecosystem processes for integration into JULES modelling.

## Data products and structure

### Data files
- Pilot experiment data: Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-pilot_experiment_(2014).csv
- Main experiment data: Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-main_experiment_(2014).csv
- Nitrogen mineralization data: Experimental_dataset_Nitrogen_mineralization_in_topsoil_and_subsoil_cores_from_the_Conwy_catchment_(2014).csv

### Dataset structures
- Pilot dataset (12 columns; 1–649 rows)
  - Campaign, Date, Soil core number, Nutrient treatment, Weight at field capacity, Weight before incubation, Land use, Incubation chamber, Time point, Time since closure, CO2 concentration, CO2 production, etc.
- Main dataset (24 columns; 1–3889 rows)
  - Campaign, Date, Core number, Plot number, Soil depth, Land use, Incubation chamber, Carbon/Nitrogen/Phosphorus additions (presence/absence), Weights (field capacity, before incubation, after water addition), Mercury flag, N2O concentration and production, CO2 concentration and production, Total dry weight, LOI/OM indicators, etc.
- Nitrogen mineralization dataset (12 columns; 1–25 rows)
  - Date, Unique core number, Plot number, Nutrient treatment, Soil depth, Land use, NO3-N, NH4-N, Total N mineralization, NO3-N per g dry weight, NH4-N per g dry weight, Total N mineralization per g OM.

## Data accessibility and purpose
- The datasets are designed to be standardised, well-documented, and suitable for monitoring environmental nutrient dynamics and for informing ecosystem process models (e.g., JULES).
- The documentation references further details in Turf2Surf WP2 Supporting documentation.