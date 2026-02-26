# Termite abundance and ecosystem processes in Maliau Basin, 2015-2016

## Study context and aims
- Conducted in lowland, old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia (2014–2017 sampling with drought and non-drought periods around 2015–2016).
- Eight plots (50 x 50 m): four termite suppression plots and four control plots, separated by at least 100 m.
- Termite suppression used integrated pest management: removal of mounds, soil treatment with imidacloprid, and deployment of poison baits (toilet paper rolls with fipronil solutions) across plots; suppression maintained until July 2017.
- Main objective: examine the role of termites in ecosystem processes and how termite suppression interacts with drought to influence decomposition, invertebrate communities, plant survival, and soil properties.

## Experimental design and sampling regime
- Plots: central 50 x 50 m core sampled; 4 termite suppression plots with an 80 x 80 m treated area (due to 15 m buffer zones) and 4 control plots.
- Treatments and timeline:
  - Termite suppression applied Oct 2014; re-poisoned every 6 months.
  - Poisons used: imidacloprid (soil) and fipronil (TPRs and TBs) with integrated pest management.
- Sampling methods and timing:
  - Termite abundance and community composition: Jones and Eggleton transect method; sampling in June 2015 and October 2016.
  - Leaf litter depth and decomposition: drought and non-drought periods; depth measurements across multiple transects per plot; decomposition bags deployed during the 2015 drought and 2016 non-drought.
  - Invertebrates: leaf litter 1 m2 samples collected in 2016; Winkler extraction for 3 days; identification by order and abundance.
  - Seedling survival: transplant experiment with Agelaea borneensis; monitored during non-drought (baseline 2015) and drought (June 2016) and follow-up non-drought (June 2017) periods.
  - Soil moisture: measured in March 2016 and October 2016 at 25 grid points per plot.
  - Soil nutrients: Plant Root Simulator (PRS) probes for nitrate, ammonium, and multiple nutrients; measurements in March 2016 (drought) and October 2016 (non-drought).
  - Termite feeding activity: untreated toilet paper rolls (TPRs) scored for termite attack on a 0–5 scale monthly; cumulative consumption recorded.
  - Rainfall/climate context: heavy reliance on Standardised Precipitation Index (SPI) derived from Danum Valley rainfall data; monthly rainfall and SPI computed for control plots to relate termite activity to moisture.

## Data files collected (12 CSVs)
- termite_hits_on_T_and_C_plots.csv — termite hit rate data across plots and sampling dates; includes plot, date, treatment, termite genus, hits, SPI, and season (Wet/Dry).
- Leaf_litter_depth.csv — leaf litter depth measurements by plot, line, date, and treatment.
- Leaf_litter_invertebrates.csv — 1 m2 leaf litter samples with abundance data by various invertebrate groups (plus termites) across plots and treatments.
- Non_target_invertebrates_all_years.csv — non-termite invertebrate counts by year, plot treatment, taxon (variable) and value (with log transformation available).
- Litter_mass_loss.csv — decomposition data from litter bags (drought vs non-drought); includes plot, bag type (open/closed), plot treatment, mass loss and proportion.
- Seedling_survival_nondrought.csv — seedling survival data during the non-drought period; columns include plot, Alive_2016, Alive_2017, Treatment.
- Seedling_survival_drought.csv — seedling survival data during the drought period; columns include plot, Alive_2016, Treatment (plus survival indicators).
- Soil_moisture.csv — soil moisture (%) by plot, treatment, condition (season), and date.
- Soil_nutrients.csv — nutrient levels (NO3–, NH4+, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, Al) measured by PRS probes; includes plot, Treatment, Condition, and unit details.
- Termite_cumulative_attack.csv — monthly cumulative termite attack (TPR consumption) per plot; includes Month, Cumulative_consumption, plot, Treatment.
- Termite_hits_on_C_plots_SPI.csv — termite hits on control plots with SPI context; includes Plot, Total hits, Date, SPI, Wet.dry.
- Location_of_plots.csv — GPS coordinates and elevation for plot corners; includes Plot_code, Plot_Name, Latitude, Longitude, Elevation.

## Data structure and variable details
- Plots and treatments:
  - Plot codes include CC, GC, KC, DC with corresponding names (Control and Ant/Termite contexts).
  - Treatments: Termite (suppressed) vs C (Control).
- Temporal coverage:
  - Sampling spanned June 2015, October 2016 for termites; drought period around 2015; drought and non-drought data for litter, soils, seeds, and nutrients.
- Measurements and scales:
  - Termite activity: qualitative hits and toxin exposure; standardized indices (SPI) to link rainfall with termite activity.
  - Soil and litter processes: moisture (%), nutrients (via PRS probes), leaf litter depth (cm), litter mass loss (grams and proportion).
  - Biotic responses: seedling survival (binary alive/dead across years), non-target invertebrate abundances, decomposition rates, and termite community composition.

## Analytical opportunities and considerations
- Assess the impact of termite suppression on:
  - Termite community composition and feeding activity over time.
  - Leaf litter decomposition rates and soil nutrient dynamics under drought vs non-drought.
  - Leaf litter invertebrate communities and overall biodiversity (including non-targets).
  - Seedling survival under drought conditions and the potential buffering role of termites.
- Explore correlations between environmental drivers and biological responses:
  - SPI-derived drought intensity and termite activity vs decomposition and soil nutrient turnover.
  - Soil moisture and nutrient availability as mediators between termite activity and ecosystem processes.
- Integrate multiple data streams to build predictive models:
  - Use the 12 datasets to model how termite suppression affects ecosystem processes across plots and years.
  - Compare control vs suppression plots under differing rainfall regimes to infer termite-mediated resilience or vulnerability to drought.
- Data considerations for analysts:
  - Multiple datasets with different scales and sampling schemes require careful data merging and standardization.
  - Handling of missing data across years and plots; alignment of terms across datasets (e.g., plot codes, treatment labels, and time stamps).
  - Cross-referencing with external rainfall SPI data to interpret seasonal effects.

## Provenance and references
- Primary data collection and methods align with Jones and Eggleton (2000) termite sampling protocol and Vicente-Serrano et al. (2010) SPI drought index to contextualize rainfall and drought conditions.
- Location and sampling are anchored in the Maliau Basin Conservation Area, Sabah, Malaysia, with explicit plot-level coordinates and elevation data provided.

## Access, notes, and potential limitations
- Data are organized into 12 CSV files with explicit column definitions, enabling cross-dataset analyses.
- The dataset captures a unique integration of termite suppression experiments with drought context, but users should account for the complexity of multiple sampling schemes and potential edge effects despite core plot sampling.
- Temporal gaps exist between sampling events; interpret results within the cited sampling windows and drought periods.