# Termite abundance and ecosystem processes in Maliau Basin, 2015-2016

## Overview
- Study site: lowland, old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia.
- Timeframe: plots established Oct 2014; termite suppression maintained until July 2017; data collection focused on 2015 and 2016.
- Objective: understand the role of termites in ecosystem processes and how they interact with drought conditions.
- Data assets: twelve CSV datasets describing termite activity, leaf litter dynamics, invertebrate communities, seedling survival, soil moisture and nutrients, decomposition, and spatial information.
- Data structure aims to support cross-cutting analysis of termite suppression effects and drought-related ecosystem responses.

## Experimental design and data collection
- Experimental design: eight 50 x 50 m plots within a 42-ha area; four termite suppression plots and four control plots, separated by at least 100 m.
- Treatments: imidacloprid soil application to suppress termites, plus targeted use of toilet paper rolls (TPRs) and tea bags (TBs) with fipronil; integrated pest management to avoid over-application.
- Plot layout: core sampling within 50 x 50 m plots to minimize edge effects; suppression maintained across duration.
- Sampling timeline and methods:
  - Termite abundance and community composition: Jones and Eggleton transect method in 2015 and 2016.
  - Leaf litter depth and decomposition: destructive measurements and litter bags during drought (Mar 2016) and non-drought (Oct 2016).
  - Leaf litter invertebrates: Winkler extraction from 1 m2 litter samples in 2016.
  - Seedling survival: transplantation of Agelaea borneensis seedlings in Jul 2015; survival assessed during drought (2016) and non-drought (2017) with baseline measurements.
  - Soil moisture: 25 points per plot, March 2016 and Oct 2016.
  - Soil nutrients: Plant Root Simulator (PRS) probes for multiple nutrients, Mar 2016 and Oct 2016.
  - Termite feeding activity: untreated toilet paper rolls scored for termite attack (0–5 scale) and replaced monthly.
  - Rainfall context: daily rainfall data used to compute 3-month SPI (drought proxy) for 2016–2017.
  - Spatial data: GPS coordinates for plot corners.

## Datasets and structure
- Twelve CSV files provided:
  - termite_hits_on_T_and_C_plots.csv — termite hit rates by plot, date, treatment, genus, and SPI; season noted.
  - Leaf_litter_depth.csv — leaf litter depth by time, plot, transect line, and treatment.
  - Leaf_litter_invertebrates.csv — abundances by taxonomic groups along transects per plot and treatment.
  - Litter_mass_loss.csv — mass loss and proportion for both open (accessible) and closed (excluded) bags, by plot and treatment.
  - Non_target_invertebrates_all_years.csv — yearly counts by invertebrate orders, with log-transformed values.
  - Seedling_survival_nondrought.csv — seedling survival during non-drought periods (2016–2017 baseline).
  - Seedling_survival_drought.csv — seedling survival during drought periods.
  - Soil_moisture.csv — plot-level soil moisture by treatment, condition, and date.
  - Soil_nutrients.csv — nutrient measures (NO3, NH4, Ca, Mg, K, P, Fe, Mn, Zn, etc.) by plot, treatment, and condition.
  - Termite_cumulative_attack.csv — monthly cumulative termite attack (TPR consumption) by plot and treatment.
  - Termite_hits_on_C_plots_SPI.csv — termite hits on control plots with SPI and rainfall context.
  - Location_of_plots.csv / Locations_of_plots.csv — GPS coordinates (latitude, longitude, elevation) for plot corners; note minor naming variations across files.
- Data columns are described for each file, including plot codes (e.g., CC, GC, KC, DC), treatment (Termite vs C), date or time, and measured variables (e.g., depths, abundances, concentrations, and indices).

## Data quality, standards, and governance
- Strengths: clear documentation of data collection methods, sampling design, and each dataset’s purpose; explicit column headings and units in many files; inclusion of both drought and non-drought contexts and replication across plots.
- Considerations for data leaders:
  - Some naming inconsistencies across files (e.g., Location_of_plots.csv vs Locations_of_plots.csv) that should be harmonized for seamless integration.
  - Variable labels vary slightly (e.g., Alive_2016 vs alive.2017) which may require standardization during aggregation.
  - Ensure a unified data dictionary and data provenance records to support reproducibility and cross-dataset joins.
  - Metadata should capture sampling methods, units, and any data processing steps (e.g., SPI calculation, log transformations).

## Opportunities and uses for Data Leaders
- System-level data integration:
  - Link termite suppression effects to leaf litter dynamics, soil nutrients, moisture, seedling survival, and non-target invertebrates to understand ecosystem-level consequences.
- User needs and governance:
  - Create a data catalog with cross-referenced keys across datasets (plot, date, treatment) to support policy analysis, ecological research, and ecosystem service assessments.
  - Develop data governance practices: versioning, licensing, data provenance, and clear access protocols.
- Analytical opportunities:
  - Causal and correlational analyses of termite suppression on decomposition, nutrient cycling, and plant recruitment under drought vs non-drought conditions.
  - Time-series and spatial analyses leveraging SPI, rainfall data, and plot-level measurements.
- Collaboration and reuse:
  - Harmonize metadata with ecological data standards to facilitate sharing with broader networks; enable co-ownership with partner institutions; prepare reproducible analysis pipelines.

## Archiving, reuse, and next steps
- Confirm availability and access permissions for all 12 data files; consider depositing in a data repository with a DOI and explicit license.
- Provide comprehensive data dictionaries, data provenance, and a readme describing measurement protocols, sampling dates, and any data processing steps (e.g., SPI computation workflow).
- Include example analyses or scripts to promote reproducibility and accelerate reuse by other data leaders and researchers.