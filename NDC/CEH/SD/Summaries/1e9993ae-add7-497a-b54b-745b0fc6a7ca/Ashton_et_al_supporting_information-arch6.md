# Termite abundance and ecosystem processes in Maliau Basin, 2015-2016 L. A. Ashton , H. M. Griffiths, C. L. Parr, T. A. Evans and P. Eggleton

## Overview of datasets
- Twelve comma-separated value (CSV) files detailing termite abundance, leaf litter dynamics, invertebrate communities, seedling survival, soil moisture and nutrients, decomposition, termite attack metrics, climatic context (SPI), and plot locations.
- Datasets capture both termite suppression and control plots across drought and non-drought periods (2015–2016) in lowland rainforest of Maliau Basin, Sabah, Malaysia.
- Primary aim: investigate the role of termites in ecosystem processes under drought and non-drought conditions.

## Experimental design and sampling regime
- Site: eight 50 x 50 m experimental plots within a 42-hectare area; four termite suppression plots and four control plots, separated by at least 100 m.
- Treatment: termite suppression using two poison-bait types (imidacloprid via soil application after mound removal; fipronil delivered via half toilet paper rolls and tea bags), plus 23 ppm imidacloprid soil treatment; additional buffer zones create 80 x 80 m treated area; managed with integrated pest management.
- Sampling periods:
  - Termite-focused sampling: June 2015 and October 2016 using Jones and Eggleton transect method.
  - Drought vs non-drought periods: drought 2015–2016 window; non-drought sampling in 2016–2017.
  - Other ecological measurements (leaf litter, seedlings, soils) collected during drought and non-drought phases (e.g., leaf litter March 2016 and October 2016; seedling survival in 2015–2017; soil moisture/nutrient sampling in 2016).
- Plot localization: GPS coordinates provided for plot corners; water and rainfall context gathered from regional data.

## Data collection methods
- Termite abundance and activity:
  - Termite_hits_on_T_and_C_plots.csv: termite encounters by genus with transect sampling.
  - Termite_cumulative_attack.csv: cumulative termite feeding via untreated transparent paper rolls (TPRs) across plots.
  - Termite_hits_on_C_plots_SPI.csv: termite hits on control plots; rainfall context via SPI.
- Leaf litter and decomposition:
  - Leaf_litter_depth.csv: leaf litter depth along transects within plots during drought and non-drought.
  - Leaf_litter_invertebrates.csv: 1 m² leaf litter samples collected for Winkler extraction; identification by order.
  - Litter_mass_loss.csv: decomposition bags (open vs closed) across plot treatments; mass loss and proportional loss.
- Invertebrate communities:
  - Non_target_invertebrates_all_years.csv: non-termite invertebrate orders across years and treatments.
  - Leaf_litter_invertebrates.csv: abundance by major invertebrate groups (multiple taxa and functional groups).
- Plants and soil responses:
  - Seedling_survival_nondrought.csv and Seedling_survival_drought.csv: seedling mortality outcomes over time for a monocot/protean species transplanted into plots.
  - Soil_moisture.csv: soil moisture collected at 25 grid points per plot (March 2016 and October 2016).
  - Soil_nutrients.csv: plant-available nutrient proxies (NO3-, NH4+, P, K, Ca, Mg, Mn, Al, Fe, Zn, B, etc.) using PRS resin probes across drought and non-drought periods.
- Climatic context:
  - Termite_hits_on_C_plots_SPI.csv: SPI values by sampling period linked to plot data.
  - Location_of_plots.csv: latitude, longitude, and elevation for plot corners.
- Data structure notes: each file includes standard fields (Plot/Treatment/Date or Time) with dataset-specific columns (e.g., genus, depth_cm, Alive_2016, etc.).

## Data structure and metadata
- Termite_hits_on_T_and_C_plots.csv: Plot, date, Treatment, genus (e.g., Bulbiter, Coptoter, Dicuspid, etc.), hits, SPI, Wet.dry.
- Leaf_litter_depth.csv: Time, Plot, LINE, Depth_cm, Treatment.
- Leaf_litter_invertebrates.csv: Plot, Treatment, Distance, and abundance for numerous groups (e.g., Coleoptera, Diptera, Formicidae, Termites, etc.).
- Non_target_invertebrates_all_years.csv: Year, Treatment, variable, value, log.
- Litter_mass_loss.csv: Condition, Plot, Bag-treatment, Plot-treatment, Mass_loss, Proportion.
- Seedling_survival_nondrought.csv: plot, Alive_2016, Treatment, alive.2017.
- Seedling_survival_drought.csv: plot, Alive_2016, Treatment.
- Soil_moisture.csv: plot, treatment, soil_moisture, condition, date.
- Soil_nutrients.csv: plot, Treatment, Condition, nutrients (NO3_N, NH4_N, Ca, Mg, K, P, Fe, Mn, Zn, B, Al).
- Termite_cumulative_attack.csv: Month, Cumulative_consumption, plot, Treatment.
- Termite_hits_on_C_plots_SPI.csv: Plot, Total, Date, SPI, Wet.dry.
- Locations_of_plots.csv: Plot_code, Plot_Name, Latitude, Longitude, Elevation.
- Note: minor naming variations exist (e.g., Locations_of_plots vs Location_of_plots; some column headings use singular/plural forms).

## Data quality, sharing, and caveats
- Data collected across drought and non-drought periods to enable comparative analyses of termite roles in ecosystem processes.
- Edge effects avoided by focusing on core 50 x 50 m plots; comprehensive replication across four suppression and four control plots.
- Some related plots (ant suppression) are described but not included in the dataset.
- Data cover multiple taxonomic groups and environmental variables, enabling multi-domain analyses but requiring careful alignment by plot, date, and treatment.

## Potential data uses for data support
- Integrate across datasets to assess how termite suppression influences:
  - Leaf litter decomposition and nutrient cycling (Litter_mass_loss, Soil_nutrients, Leaf_litter_depth).
  - Soil moisture dynamics and plant-available nutrients under drought vs non-drought conditions (Soil_moisture, Soil_nutrients).
  - Plant reproduction and survival responses (Seedling_survival_nondrought, Seedling_survival_drought).
  - Community ecology: termite communities, non-target invertebrates, and changes in leaf litter invertebrate assemblages (Termite_hits_on_T_and_C_plots, Non_target_invertebrates_all_years, Leaf_litter_invertebrates).
- Examine climate and rainfall context effects via SPI and precipitation on termite activity (Termite_hits_on_C_plots_SPI, SPI data).
- Spatial analyses using plot locations to map treatment effects and microhabitat variation.
- Development of data products and dashboards enabling self-service exploration by plotting metrics by plot, treatment, and time.
- Data supports broader investigations of termite roles in mitigating drought effects on tropical rainforest ecosystem processes.