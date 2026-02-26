# Termite abundance and ecosystem processes in Maliau Basin, 2015-2016

## Purpose and scope
- Investigates the role of termites in ecosystem processes under drought and non-drought conditions in lowland rainforest, Maliau Basin, Sabah, Malaysia.
- Uses a controlled experimental design with termite suppression versus control plots to assess impacts on termite abundance, leaf litter dynamics, soil properties, seedling survival, and broader invertebrate communities.
- Data are intended to support data-driven understanding of termite-mediated effects and to enable reuse by others studying tropical forest resilience and ecosystem processes.

## Experimental design and sampling regime
- Eight plots within a 42-hectare area: four termite suppression plots and four controls, each 50 x 50 m; suppression plots include 80 x 80 m treated area with buffers.
- Termite suppression applied from Oct 2014 to July 2017 using imidacloprid soil treatment and fipronil-treated toilet paper rolls and tea bags; integrated pest management with six-monthly re-poisoning.
- Edges avoided by sampling only in core 50 x 50 m plots; plots separated by at least 100 m.
- Data collection occurred across drought and non-drought periods (2015–2017), with specific timepoints described for each dataset.

## Datasets included (data files)
- termite_hits_on_T_and_C_plots.csv: termite hit rate data by plot, treatment, genus, and sampling date.
- Leaf_litter_depth.csv: leaf litter depth measurements per plot and line across drought and non-drought periods.
- Leaf_litter_invertebrates.csv: abundance by invertebrate groups from leaf litter samples using Winkler extractions.
- Litter_mass_loss.csv: decomposition rates from litter bags (open vs closed mesh) on termite suppression and control plots during drought and non-drought periods.
- Non_target_invertebrates_all_years.csv: non-termite invertebrate counts by year and plot treatment.
- Seedling_survival_nondrought.csv: binary survival data for transplant seedlings during non-drought periods.
- Seedling_survival_drought.csv: seedling survival data during drought period.
- Soil_moisture.csv: soil moisture measurements on a 25-point grid per plot during drought and non-drought periods.
- Soil_nutrients.csv: plant-available nutrient measurements (PRS probes) across drought and non-drought periods.
- Termite_cumulative_attack.csv: monthly cumulative termite feeding activity on plots via untreated trunk, expressed as a consumption score.
- Termite_hits_on_C_plots_SPI.csv: termite hits on control plots with corresponding SPI-derived rainfall context.
- Location_of_plots.csv: GPS locations (latitude, longitude, elevation) for plot corners; includes notes on the relationship to arks of parallel ant-suppression plots.

## Data collection methods and structure (highlights)
- Termite abundance and encounters: transect-based sampling (Jones and Eggleton method) conducted June 2015 and Oct 2016.
- Leaf litter measurements: depth recorded via multiple transects per plot; decomposition assessed using macroinvertebrate-excluded and accessible bags placed at drought and non-drought times.
- Invertebrate surveys: Winkler extraction from leaf litter; identification to order; counts by year and plot.
- Seedling experiments: Agelaea borneensis transplanted in a grid (n=25 per plot); survival tracked at multiple intervals during drought and non-drought periods.
- Soil moisture and nutrients: moisture measured with Delta-T HH2; PRS membranes deployed for two weeks in drought and non-drought windows; measurements at 10 cm depth; nutrients include NO3, NH4, Ca, Mg, K, P, Fe, Mn, Zn, B, Al.
- Termite activity: untreated chewable cellulose traps (TPRs) scored for termite attack on a 0–5 scale; monthly replacements.
- Rainfall context: daily rainfall data from Danum Valley; SPI calculated to reflect drought intensity.

## Metadata and data quality considerations
- Data are organized into twelve CSV files with explicit column definitions per file (plot codes, treatment, date, taxa groups, abundance/counts, soil measurements, etc.).
- Columns include clear identifiers (Plot, Treatment, Date, Time) and measurement units (e.g., Depth_cm, Mass_loss in grams, % soil moisture, nutrient units for PRS probes).
- Provisions for edge-case notes (e.g., “Location_of_plots.csv” indicates absence of ant suppression data on ant plots but included for completeness).
- Key references for provenance and methods cited (Jones & Eggleton 2000; Vicente-Serrano et al. 2010 SPI).

## Governance, sharing, and reuse considerations for Data Stewards
- Data are structured to support reuse in studies of termite roles in ecosystem processes, drought impacts, and tropical forest resilience.
- Metadata provides sufficient context to reproduce analyses or integrate with similar datasets (sampling design, treatment meaning, plot naming conventions, and sampling dates).
- Data sharing considerations:
  - Clearly defined data ownership and acknowledgement (authors listed).
  - Data are organized as CSV files suitable for ingestion into common data portals and catalogs.
  - Locations provided for plots enable spatial analyses but note that ant suppression plots are not part of this dataset.
- Potential data governance actions:
  - Establish a dataset-level metadata record (README) detailing data collection protocols, quality checks, units, and data lineage.
  - Maintain a data update plan if future re-sampling or re-analysis is planned (e.g., re-poisoning schedules, additional sampling rounds).
  - Ensure proper attribution to original authors and sources in any data sharing or publication.

## Endnotes and references
- Data are designed to support analysis of termite roles in drought-related ecosystem changes and to enable cross-study comparisons with clearly documented methods and variables.
- References cited for methodology and drought context:
  - Jones, D.T. and Eggleton, P. (2000). Sampling termite assemblages in tropical forests: testing a rapid biodiversity assessment protocol.
  - Vicente-Serrano, S.M. et al. (2010). Standardized Precipitation Evapotranspiration Index (SPI).