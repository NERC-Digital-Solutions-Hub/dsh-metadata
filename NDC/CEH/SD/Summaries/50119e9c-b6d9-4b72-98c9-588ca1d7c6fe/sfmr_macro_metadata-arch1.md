# Macroinvertebrate data from the South Fork McKenzie River in Oregon, USA

- Purpose and scope
  - Assess macroinvertebrate response to wildfire in restored versus unrestored sites along the South Fork McKenzie River.
  - Sampling across three periods: fall 2019 (17 sites), fall 2020 (12 sites), and winter 2021 (10 sites), with 10 samples per site.
  - Data collected include density and biomass, plus species-level and trait information to enable ecological analyses.

- Datasets and file structure
  - SFMR_Macro_Traits: macroinvertebrate taxa traits and taxonomic information (e.g., Insect, Origin, Classification, Order, Family, Genus_species, Lifestage, CodeUnique, FFG, Habit, Tolerance, Voltinism, Seasonal, Drift, Size, Rheophily, Thermal).
  - SFMR_Macro_Coordinates: site-level metadata with MasterSite, Trmt, Restoration, Width_Avg_ft, GPS coordinates, and notes.
  - SFMR_Macro_Samples: site-period measurements including date, transect, environmental covariates (Cover_pct, Temp_C, SISA_pct, substrate percentages, vegetation, BMIwood_pct), physical dimensions (Width_m, Depths), and restoration/treatment information (Post_mos, Post_Fire, Restoration, etc.).
  - SFMR_Macro_Species: species-level data per MasterSite-time, including Density, Biomass_mg, Stage, and Taxon_Wisseman (linked to traits).
  - All four CSV files are designed to be merged on MasterSite and CodeUnique for integrated analyses.

- Sampling design and collection methods
  - 1 ft net samples collected along transects across the river channel (10 samples per site; left bank, center, right bank, equidistant along transect).
  - Filamentous algae not filtered; BMI wood defined as within 1 ft of a large woody object.
  - Pre-restoration transect stakes; post-restoration sites identified primarily by GPS (3–4 m spatial error due to washed-away stakes).
  - Specimens identified to species or genus by Robert Wisseman; trait values drawn from a dedicated expert database.
  - Temperature data: USGS gauge near Cougar Dam used due to handheld device inconsistencies.

- Temporal and spatial coverage
  - 17 sites sampled fall 2019; 12 sites fall 2020; 10 sites winter 2021.
  - Each site contains 10 samples, collected across transects that span LB, Center, RB within each site.
  - Environmental and restoration metadata captured per site, including restoration type and months since restoration (Post_mos).

- Measurements, units, and key covariates
  - Density: individuals per square meter (/#m2); Biomass: dry mass in mg per square meter (mg/m2).
  - Sample standardization: site-scale values standardized to 1 m2 (conversion noted as 1-m2 of bethos per 0.7432 m2).
  - Environmental covariates: Cover_pct, USGS temperature (or Temp_C), Width_m, Depth_max_m, Depth_avg_m; substrate composition (SISA_pct, GR_pct, CO_pct, BO_pct); vegetation categories (NonvascVeg_pct, EmergVeg_pct, AqVeg_pct); BMIwood_pct.
  - Habitat/physical descriptors: stream width, transect position, bank side, and restoration status.
  - Temporal descriptors: Trmt (pre- or post-restoration; or reference unburned site), Post_mos (months since restoration), Post_Fire indicator; Restoration type for Stage 0 activities.
  - Species-level metrics: Density and Biomass_mg per MasterSite per time, Stage (life stage), Taxon_Wisseman (aligned with trait definitions).

- Data quality, limitations, and notes
  - Temperature measurements face inconsistencies from handheld devices; reliance on USGS gauge data for temperature.
  - Post-restoration site identification has GPS-based positioning with a typical 3–4 m error due to washed stakes.
  - Data integration requires careful linking via MasterSite and CodeUnique; some fields may have missing values across years/sites.
  - Trait definitions and column headers are provided to support consistent interpretation and downstream modelling.

- How analysts can use this dataset
  - Merge trait, coordinates, samples, and species data via MasterSite and CodeUnique to build, for example:
    - Taxon-specific and functional-group (FFG) responses to wildfire and restoration.
    - Community composition analyses over time and across restoration treatments.
    - Trait-based analyses (e.g., tolerance, voltinism, rheophily) in relation to environmental covariates (Temp_C, Cover_pct, substrate composition).
  - Model impacts of time since restoration (Post_mos) and treatment (Pre vs Post) on density and biomass, while accounting for spatial variation across sites.
  - Use per-site environmental covariates to explore drivers of macroinvertebrate community structure and functional characteristics.

- Practical considerations for data use
  - Ensure consistent unit handling across datasets (Density, Biomass, area normalization).
  - Align MasterSite and CodeUnique identifiers when integrating traits and species data.
  - Be mindful of GPS precision limitations when mapping site locations; consider incorporating GPS uncertainty in spatial analyses.

- Quick reference to data scope
  - Four CSV files: SFMR_Macro_Traits, SFMR_Macro_Coordinates, SFMR_Macro_Samples, SFMR_Macro_Species.
  - Focused on macroinvertebrate response to wildfire and stage 0 restoration across multiple years and sites, with rich trait and environmental metadata to enable robust analyses.