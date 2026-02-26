# Turf2Surf - Nutrient addition experiment

## Overview

- Investigates stoichiometric coupling of C, N, and P by adding C, N, and P to soil cores from different land-use intensities in the Conwy catchment (bog, acid grassland, improved grassland, arable land).
- Includes a pilot study to calibrate sensitivity and inform the main experiment design.
- Main experiment measures soil respiration and N2O fluxes in response to treatments across four sites, with soil cores taken to 100 cm depth (0-15 cm topsoil and 85-100 cm deep).
- Aims to link plant and soil nutrients to ecosystem processes and to feed into the JULES model; data supported by Turf2Surf WP2 and documented for reuse.

## Experimental Design at a Glance

- Pilot experiment (Nov 2013; Dec 2013):
  - Topsoil cores (0-15 cm) from grassland, conifer woodland, and bog (2 replicates per site; 24 cores total).
  - Treatments: C, N, P, CN, CP, NP, CNP, and combinations with C compounds mimicking root exudates.
  - Nutrient additions calibrated using various C quantities and C:N, C:P ratios; glucose, glycine, NH4NO3-N, KH2PO4 used.
  - Incubations at field capacity with artificial rain solution; CO2 samples collected at multiple time points; CO2 measured by GC.
  - Multiple nutrient additions found to stabilize microbial responses; timepoints extended beyond 1 hour for some soils.
- Main experiment (2014):
  - Four sites: Nant-y-Brwn bog, Capel Curig acid grassland, Hiraethlyn acid grassland, Conwy arable field.
  - Intact soil cores (4 cm diameter) taken to 100 cm depth (different corers by site due to soil conditions).
  - Full factorial 8 treatments: control, C, N, P, CN, CP, NP, CNP.
  - Nutrient additions: total 1.20 mg C g-1 dry soil across 3 days (0.4 mg C g-1 per day); N and P added at C:N = 10 and C:P = 70, respectively.
  - Post-addition incubation: measurements at multiple days (4, 5, 6, 8, 10, 12 days) to observe postponed responses; HgCl2 negative control to assess nutrient distribution efficiency.
  - Soil moisture maintained with artificial rain solution; water content adjusted as needed.
  - Gas measurements captured CO2 and N2O production; additional nitrogen mineralization analysis performed after a 4-week flushing period.
  - The incubation period lasted 2 weeks at 10°C for main measurements; samples stored in breathable bags to minimize water loss.
  - Data collected include plant/soil plots co-located with established measurements; cores prepared for dry weight and LOI analyses.

## Data Collection, Measurements & Procedures

- Gas sampling and analysis:
  - Incubation chambers closed; CO2 and N2O samples collected (60 mL) and stored in pre-evacuated vials.
  - CO2 and N2O concentrations measured with gas chromatography, using standards (0-15 ppm for N2O; 250/500/1000 ppm for CO2 calibrations).
- Nutrient additions and leaching:
  - Artificial rain solution used to simulate UK rainfall; leachate collected until ~150 mL; suction applied to drain larger pores.
  - Across pilot and main experiments, nutrient addition volumes were controlled and adjusted for field-capacity losses.
- Nitrogen mineralization:
  - Control cores flushed with artificial rain solution for 4–5 days to remove available N.
  - After flushing, cores incubated for 2 additional weeks at 10°C; extraction with 1 M KCl and analysis for NO3-N and NH4-N.
  - Calculations derive NO3-N, NH4-N, and total mineralizable N per g dry weight and per g organic matter (LOI-adjusted).
- Soil properties:
  - Post-incubation processing includes drying (65°C) for dry weight; LOI determination (375°C) to estimate organic matter.
- Documentation and attribution:
  - Field sampling, lab work, and analysis carried out by named collaborators; data analyses performed by a designated data lead.

## Data Structure and Files

- Three CSV data files:
  - Pilot experiment data: Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-pilot_experiment_(2014).csv
  - Main experiment data: Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-main_experiment_(2014).csv
  - Nitrogen mineralization data: Experimental_dataset_Nitrogen_mineralization_in_topsoil_and_subsoil_cores_from_the_Conwy_catchment_(2014).csv
- Pilot dataset (12 columns; 1-649 rows):
  - Key fields: Campaign, Date, Soil core number, Nutrient treatment, Land use, Incubation chamber, Time point, CO2 concentration, CO2 production, with additional weights and land-use descriptors.
- Main dataset (24 columns; 1-3889 rows):
  - Expanded with: plot number, core number, depth (0-15 cm or 85-100 cm), mercury treatment flag, soil weights (field capacity, pre-incubation, water-added), land-use type, incubation chamber, time points, CO2 and N2O concentrations and productions, total soil dry weight, LOI.
- Nitrogen mineralization dataset (12 columns; 1-25 rows):
  - Includes date, unique core number, plot, nutrient treatment, soil depth, land-use type, NO3-N, NH4-N, total N mineralization (per g dry weight), and per g organic matter (per LOI).

## Data Provenance, Roles & Connections

- Team and roles:
  - Field sampling: Helen C. Glanville, Miles Marshal, Ben Winterbourn, David Pastrana, Maria C. Blanes.
  - Laboratory work and measurements: Maria C. Blanes, David Pastrana, Sabine Reinsch.
  - Calculations and data analysis: Sabine Reinsch.
- Integration with broader goals:
  - Data generated to support linking plant and soil nutrients to ecosystem processes for incorporation into the JULES model (as part of Turf2Surf WP2).
  - Documentation referenced includes Turf2Surf WP2 Supporting documentation for more context.

## Data Management, Metadata, Standards & Reuse

- Metadata and structure:
  - Consistent use of fields for campaign, date, core identifiers, land-use type, depth, nutrient treatments, and gas measurements.
  - Units clearly specified (e.g., CO2/N2O concentrations in ppm; weights in g; LOI in g; depths as 0-15 cm or 85-100 cm).
- Data quality and iteration:
  - Pilot data used to optimize nutrient addition regimes and incubation timing; main experiment expands scale and depth integration.
  - Multiple incubation time points and replicated treatments improve robustness of gas flux responses.
- Documentation and access:
  - Data are accompanied by procedural descriptions and are referenced to Turf2Surf WP2 Supporting documentation; raw data are provided as CSVs for reuse in modelling and further analysis.

## Access, Documentation, and Next Steps

- Data accessibility:
  - Data files and associated methodological descriptions are provided, with explicit file names for pilot, main, and nitrogen mineralization datasets.
  - Further methodological context available in Turf2Surf WP2 Supporting documentation and project materials.
- Reuse and governance:
  - Data designed for modelling applications (e.g., integration with JULES) and cross-site nutrient interaction studies.
  - Users should consider the multi-site, multi-depth design, and the calibration steps from the pilot when performing cross-dataset analyses.