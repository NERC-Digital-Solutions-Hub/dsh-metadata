# Termite abundance and ecosystem processes in Maliau Basin, 2015-2016

## Overview and purpose
- A data-oriented study in lowland, old-growth rainforest (Maliau Basin, Sabah, Malaysia) examining the role of termites in ecosystem processes during drought and non-drought periods.
- Eight 50x50 m plots established in Oct 2014: four termite suppression plots and four control plots; suppression maintained until Jul 2017 with integrated pest management.
- Data collected across multiple ecological facets (termites, leaf litter dynamics, invertebrates, seedling survival, soil moisture and nutrients) to assess termite influence on decomposition, soil processes, and plant recruitment under drought stress.

## Experimental design and sampling regime
- Plots: 8 total (4 termite suppression, 4 control) within a 42-ha area; core plots (50x50 m) sampled to avoid edge effects; 100 m spacing between treatment types.
- Termite suppression: removal of mounds, soil application of imidacloprid (23 ppm) to mound areas, and deployment of treated toilet paper rolls (TPRs) and tea bags (TBs) containing fipronil; repeated approximately every 6 months; total treated area ≈ 80x80 m per plot.
- Sampling periods: June 2015 and Oct 2016 for termite community composition; drought period in 2015–2016 and non-drought period in 2016–2017.
- Additional data streams collected to link termite activity with ecosystem processes (leaf litter, soil moisture, nutrients, seedling survival, and invertebrate communities).

## Data collection methods
- Termite abundance: Jones and Eggleton transect method; termite encounters recorded on suppression and control plots.
- Leaf litter depth: in situ measurements across multiple transects within plots during drought (Mar 2016) and non-drought (Oct 2016).
- Leaf litter invertebrates: 1 m² samples per plot in 2016; Winkler extraction for 3 days; identification to order.
- Decomposition: litter bags (open and closed) with Shorea johorensis leaves; 112-day exposure during drought (Aug 2015) and non-drought (Jul 2016).
- Non-target invertebrates: leaf litter samples across 2014–2016; Winkler extraction.
- Seedling survival: Agelaea borneensis transplanted July 2015; monitored 2016 (drought) and 2017 (non-drought) with alive/dead status.
- Soil moisture: Delta-T HH2 meter; 25 points per plot across two sampling periods (Mar and Oct 2016).
- Soil nutrients: PRS resin probes for NO3-, NH4+, P, K, Ca, Mg, Mn, Al, Fe, Zn; deployed across two sampling windows (Mar 2016 and Oct 2016).
- Termite feeding activity: untreated toilet paper rolls (TPRs) placed on each plot; scored for termite attack on a 0–5 scale; cumulative consumption recorded.
- Rainfall and drought index: Daily rainfall data from Danum Valley; 3-month Standardised Precipitation Index (SPI) calculated to characterize drought conditions.
- Plot locations: GPS coordinates for plot corners; ancillary data include a parallel ant-suppression experiment for context.

## Data structure and content (12 CSV files)
- termite_hits_on_T_and_C_plots.csv
  - Plot, date, Treatment, counts by termite genus, hits, SPI, Wet.dry (season)
- Leaf_litter_depth.csv
  - Time, Plot, LINE, Depth_cm, Treatment
- Leaf_litter_invertebrates.csv
  - Plot, Treatment, Distance, abundances by groups (e.g., Coleoptera, Diptera, Formicidae, Termites, etc.)
- Litter_mass_loss.csv
  - Condition (Drought/non-drought), Plot, Bag-treatment (open/closed), Plot-treatment, Mass_loss (g), Proportion
- Non_target_invertebrates_all_years.csv
  - Year, Treatment, variable (taxon), value, log
- Seedling_survival_nondrought.csv
  - plot, Alive_2016, Treatment, alive.2017
- Seedling_survival_drought.csv
  - plot, Alive_2016, Treatment
- Soil_moisture.csv
  - plot, treatment, soil_moisture (%), condition, date
- Soil_nutrients.csv
  - plot, Treatment, Condition (drought/non-drought), nutrients (NO3-, NH4+, Ca, Mg, K, P, Fe, Mn, Zn, etc.), units
- Termite_cumulative_attack.csv
  - Month, Cumulative_consumption, plot, Treatment
- Termite_hits_on_C_plots_SPI.csv
  - Plot, Total, Date, SPI, Wet.dry
- Locations_of_plots.csv
  - Plot_code, Plot_Name, Latitude, Longitude, Elevation

Notes on data design
- Common keys: Plot, Treatment, Date or Time, and season indicators (Wet.dry, Condition) enabling cross-dataset integration.
- Units vary by dataset (e.g., mass in grams, depth in cm, percent soil moisture, 0–5 attack scale).

## Relevance for environmental monitoring and analysis
- Provides a multi-ecosystem, drought-aware dataset to quantify termite roles in decomposition, soil nutrient dynamics, and plant recruitment.
- Enables standardized assessment of environmental health indicators across a common framework (plots, treatments, time, and climate context via SPI and rainfall).
- Supports cross-dataset analyses by design (e.g., linking termite activity to soil moisture, nutrient availability, leaf litter decomposition, and seedling survival).

## Analytical opportunities and outputs (for Analysts Monitoring the Environment)
- Compare termite suppression vs control effects on decomposition rates, soil moisture retention, and nutrient cycling under drought versus non-drought.
- Assess community responses: termite diversity, leaf litter invertebrates, and non-target invertebrates across treatments and seasons.
- Link rainfall drought index (SPI) to termite activity and ecosystem processes to understand climate-ecosystem interactions.
- Map and visualize spatial patterns using Locations_of_plots.csv alongside plot-level measurements.
- Develop standardized dashboards or reports summarizing termite-driven ecosystem effects over time.

## Data quality, access, and usage notes
- Data collection followed standardized methods (e.g., Jones and Eggleton transects, Winkler extraction) to ensure comparability across plots and years.
- Edge effects minimized by focusing sampling within core plots and by maintaining consistent plot management.
- Data are available as 12 CSV files with clearly defined column headings and units; designed to be integrated with climate indices (SPI) and other environmental datasets.
- For broader data value, consider integrating with external datasets (e.g., additional climatic variables or regional biodiversity datasets) and sharing via environmental data portals.

## References and methodological notes
- Sampling methodology reference: Jones, D.T. and Eggleton, P. (2000) Sampling termite assemblages in tropical forests: testing a rapid biodiversity assessment protocol.
- Drought index reference: Vicente-Serrano, S.M. et al. (2010) A multiscalar drought index sensitive to global warming: the standardized precipitation evapotranspiration index.