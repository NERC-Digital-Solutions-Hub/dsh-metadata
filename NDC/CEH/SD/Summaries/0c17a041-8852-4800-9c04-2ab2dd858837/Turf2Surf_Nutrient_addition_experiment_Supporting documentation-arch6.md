# Turf2Surf - Nutrient addition experiment

- Purpose: Assess stoichiometric coupling of carbon (C), nitrogen (N) and phosphorus (P) additions on soil respiration and N2O fluxes across different land-use types in the Conwy catchment; link findings to ecosystem processes for integration with a model (JULES).

## Experimental design

- Pilot experiment (Nov 2013 – Dec 2013)
  - Topsoil (0–15 cm) cores from grassland, conifer woodland, and bog; two replicates per site.
  - Treatments included varied C, N, P additions, C:N and C:P ratios, C compounds (glucose, glycine, root-exudate mimics), and combinations (CN, CP, NP, CNP).
  - Gas measurements (CO2) taken at multiple times after incubation to determine incubation duration needed for reliable signals (bog required ~2 h; grassland/conifer ~1 h).
  - Incubations used a rain solution to reach field capacity; leachate collected; samples stored for GC analysis of CO2.
  - A mercury (HgCl2) negative control was used to evaluate nutrient distribution within cores.

- Main experiment (Jan 2014 – Feb 2014)
  - Four field sites: bog, acid grassland, improved grassland, and arable field; intact cores to 100 cm depth (4 cm diameter; 216 cores total), with top 0–15 cm and bottom 85–100 cm used.
  - Full factorial design with eight nutrient treatments: control, C, N, P, CN, CP, NP, CNP.
  - C additions totaling 1.20 mg C g-1 dry soil distributed over 3 days; N and P added to match C:N = 10 and C:P = 70.
  - Post-addition incubations conducted at multiple time points (4, 5, 6, 8, 10, 12 days) to capture delayed responses; additional incubations for investigation of shifted responses (1–3 days after second addition).
  - Negative control with HgCl2 added for 3 consecutive days to gauge nutrient distribution effects.
  - Gas measurements included CO2 and N2O fluxes; soil water content maintained with artificial rain solution.

- Nitrogen mineralization (Nmin)
  - Measured on control cores after flushing leached cores with artificial rain solution for 4–5 days, followed by a 4-week incubation at 10°C.
  - Nmin values derived from nitrate and ammonium in 1 M KCl extracts; biomass and organic matter content also assessed.

## Data collection and methods

- Incubation and moisture
  - Core handling: stored at 4°C for up to 1 week; field capacity achieved using perforated racks and rain solution; cores weighed before and after incubation with adjustments for added solutions.
  - Rain solution composition (all in meq L⁻¹): Ca²⁺ 17.6, Mg²⁺ 30.1, Na⁺ 125, Cl⁻ 140, SO4²⁻ 57.2; pH 4.55.

- Gas sampling and analysis
  - CO2 and N2O sampled from sealed incubation chambers; samples collected in 60 mL syringes, injected into pre-evacuated 20 mL vials.
  - CO2 measured by gas chromatography; N2O measured concurrently with CO2 using standard curves (5–15 ppm).
  - Time points varied by site (bog vs others) but followed a structured protocol to capture production rates.

- Soil and chemical analyses
  - Weighed cores used to determine dry weight; total soil dry weight and soil organic matter (LOI) determined gravimetrically.
  - Nitrogen mineralization: extraction with 1 M KCl; nitrate and ammonium quantified.
  - Soil depths examined: 0–15 cm (topsoil) and 85–100 cm (deep soil) for core analyses.

- Data structure and documentation
  - Three datasets produced:
    - Pilot experiment data: Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-pilot_experiment_(2014).csv
    - Main experiment data: Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-main_experiment_(2014).csv
    - Nitrogen mineralization data: Experimental_dataset_Nitrogen_mineralization_in_topsoil_and_subsoil_cores_from_the_Conwy_catchment_(2014).csv
  - Pilot file: 12 columns, 1–649 rows (fields include campaign, date, soil core number, nutrient treatment, weights, land use, incubation details, CO2 production).
  - Main file: 24 columns, 1–3889 rows (includes campaign, date, core/plot identifiers, nutrient treatments, depth, weights, land use, incubation times, CO2 and N2O data, soil weight, LOI).
  - Mineralization file: 12 columns, 1–25 rows (NO3-N, NH4-N, total mineralization, and related measurements by depth and land use).

## Data fields and structure (highlights)

- Core and treatment identifiers
  - Campaign, Date, Unique core number, Plot number, Land use type, Incubation chamber, Time point and Time (min).
- Measurements
  - CO2 concentration and CO2 production; N2O concentration and N2O production.
- Physical and chemical context
  - Weight at field capacity, weight before incubation, weight after water adjustments, total dry weight, total LOI (organic matter).
  - Soil depth category (0–15 cm; 85–100 cm).
- Soil chemistry and mineralization
  - Mineralizable NO3-N and NH4-N per g dry soil and per g organic matter; total N mineralization per g dry soil and per g organic matter.
- Metadata
  - Land-use type categories (Bog, Acid grassland, Improved grassland, Arable).
  - Incubation times, searchable with time since chamber closure.

## Data provenance and personnel

- Field collection and site work
  - Helen C. Glanville, Miles Marshal, Ben Winterbourn, David Pastrana, Maria C. Blanes.
- Laboratory work
  - Maria C. Blanes, David Pastrana, Sabine Reinsch.
- Data analysis
  - Sabine Reinsch.
- Purpose alignment
  - WP2 of Turf2Surf aims to connect plant and soil nutrients to ecosystem processes to inform JULES modeling.

## Reuse, outputs and documentation

- Data are organized to enable self-serve exploration of how C, N, and P additions affect soil respiration and N2O fluxes across depths and land uses.
- Outputs anticipated: data-driven insights for nutrient dynamics, potential dashboards or pivot analyses, and inputs for ecosystem process modeling (JULES).
- Related documentation: Turf2Surf WP2 Supporting documentation (referenced for additional methodological details).