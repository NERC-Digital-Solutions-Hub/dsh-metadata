# Turf2Surf - Nutrient addition experiment

- A field and incubation study in the Turf2Surf project assessing how carbon (C) and nutrients (N, P) interact to affect soil respiration and gas fluxes (CO2 and N2O) across different land-use types in the Conwy catchment.
- Involves pilot and main experiments using soil cores from four sites and two soil depths, with a full factorial nutrient addition design (eight treatments: C, N, P, CN, CP, NP, CNP, plus controls).

## Overview and aims

- Test sensitivity of top- and sub-soils to varying C and nutrient additions and inform the main experiment.
- Examine stomatal-like responses in soil microbial communities via soil respiration and N2O fluxes under different nutrient regimes.
- Link plant and soil nutrient dynamics to ecosystem processes for incorporation into models (e.g., JULES).

## Experimental design

- Pilot experiment (Nov 2013 → Dec 2013)
  - Topsoil (0–15 cm) cores from grassland, conifer woodland, and bog (Aber Henfaes, Clocaenog, etc.).
  - Treatments: various C sources (glucose, glycine), N, P, and combinations (CN, CP, NP, CNP), plus C:N and C:P ratios, and C compounds mimicking root exudates.
  - Incubation: multiple time points (0, 1–3 hours after nutrient addition; repeated incubations) to determine CO2 emission timing.
  - Measurements: CO2 production via gas chromatography; CO2 sampling in sealed incubation chambers.
  - Purpose: refine nutrient addition regimens and incubation timing for the main experiment.

- Main experiment (Jan–Feb 2014 start; 4-month nutrient additions)
  - Four sites: Nant-y-Brwn bog (bog), Capel Curig acid grassland, Hiraethlyn acid grassland, Conwy arable field.
  - Intact soil cores to 100 cm depth; top 0–15 cm and bottom 85–100 cm (two depths).
  - Treatments: eight factorial combinations (control, C, N, P, CN, CP, NP, CNP).
  - C additions: 1.20 mg C g-1 dry soil total, over three days (0.4 mg C g-1 per day).
  - N and P additions: based on pilot results (C:N = 10, C:P = 70), plus combinations (CN, CP, NP, CNP).
  - Incubation and sampling: gas samples at specific times after chamber closure (bog: ~2 h; others: ~1 h); repeated incubations to capture delayed microbial responses.
  - Negative control: HgCl2 to evaluate nutrient distribution within cores.
  - Measurements: CO2 and N2O fluxes; soil water content maintained with artificial rain solution.

## Measurements and protocols

- Gas measurements
  - CO2 and N2O concentrations measured from incubation samples (60 mL syringed samples, 20 mL injected, remainder flushed into vial).
  - CO2 and N2O quantified with gas chromatography, using calibration standards (ppm ranges provided).
- Nutrient additions and water management
  - Artificial rain solution mimicked UK rainfall; composition provided (Ca2+, Mg2+, Na+, Cl-, SO4 2-, pH 4.55).
  - Soil cores flushed to field capacity, with minimal water loss accounted for in nutrient dosing.
  - Incubations conducted at 10°C; cores stored to minimize water loss between steps.
- Nitrogen mineralization (Nmin)
  - Assessed on untreated control cores after flushing out available N with artificial rain solution for 4–5 days.
  - Incubation continued for 4 weeks at 10°C; post-incubation extraction of nitrate and ammonium with 1 M KCl; soil dry weight and organic matter determined.
- Laboratory work and data handling
  - Collaboration and data processing carried out by project staff; results used to inform model parameterization.

## Sites, land use, and sample structure

- Four main sites representing diverse land uses:
  - Nant-y-Brwn: bog
  - Capel Curig: acid grassland
  - Hiraethlyn: acid grassland
  - Conwy: arable field
- Depths used for analysis:
  - Topsoil: 0–15 cm
  - Deepsoil: 85–100 cm
- Plot/core organization:
  - Intact cores co-located with plots that had existing plant and soil measurements.
  - 216 cores in the main experiment (across land-use types and depths).

## Data files and structure

- Three primary data files (CSV format):
  - Pilot experiment data: Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-pilot_experiment_(2014).csv
  - Main experiment data: Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-main_experiment_(2014).csv
  - Nitrogen mineralization data: Experimental_dataset_Nitrogen_mineralization_in_topsoil_and_subsoil_cores_from_the_Conwy_catchment_(2014).csv
- Pilot dataset (12 columns): campaign, date, soil core number, nutrient treatment, weights at field capacity and before incubation, land-use type, incubation chamber, time point, time since closure, CO2 concentration, CO2 production.
- Main dataset (24 columns): campaign, date, core number, plot number, soil depth (0–15 cm or 85–100 cm), land use, weight measurements, nutrient treatments (C, N, P; and combinations), mercury control indicator, incubation chamber, time point, CO2 & N2O concentrations and productions, total soil dry weight and total LOI weight.
- Nitrogen mineralization dataset (12 columns): date, core number, plot number, nutrient treatment, soil depth, land use, NO3-N, NH4-N, total mineralization, NO3-N and NH4-N per organic matter, etc.
- Notes: Mineralization rates refer to a 4-week incubation period.

## Geography and data integration considerations for GIS

- Spatial context: four study sites within the Conwy catchment; land-use types cover bog, acid grassland, improved grassland, and arable land.
- Depth-resolved data: measurements for topsoil (0–15 cm) and deeper soil (85–100 cm) enable vertical mapping of nutrient responses.
- Time-series potential: multiple incubation time points and repeated incubations allow temporal mapping of gas flux responses to nutrient additions.
- Data alignment: unify core IDs, plots, land-use codes, and depth definitions across pilot and main datasets for GIS layering and agricultural/ ecosystem modelling.
- Data limitations: no explicit geographic coordinates are provided in the data descriptions; GIS implementation would require linking cores to spatial locations via field records or linked plot maps.

## Key takeaways for GIS specialists

- The Turf2Surf nutrient addition study provides rich, depth- and time-resolved data on soil CO2 and N2O fluxes and nitrogen mineralization across four land-use types.
- Eight nutrient treatment combinations enable spatially explicit analyses of how C and nutrients influence microbial respiration and greenhouse gas emissions.
- Data are organized into three CSV files (pilot, main, and nitrogen mineralization) with detailed metadata fields suitable for integrating into GIS workflows, model parameter databases, and map-based visualizations of treatment effects and site comparisons.
- To use in GIS, align plots and cores to spatial features, incorporate depth stratification, and leverage time-point data for animated or multi-layered visualizations of nutrient response patterns.