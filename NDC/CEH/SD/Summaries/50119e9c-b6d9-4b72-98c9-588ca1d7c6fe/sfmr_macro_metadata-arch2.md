# Macroinvertebrate data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Purpose: Assess macroinvertebrate response to wildfire in restored and unrestored sites of the South Fork McKenzie River.
- Data type: Monitoring
- Size: 140KB
- Interpreted by: All authors

## Study design and sampling
- Sites and timing:
  - Fall 2019: 17 sites, each with 10 samples
  - Fall 2020: 12 sites, each with 10 samples
  - Winter 2021: 10 sites, each with 10 samples
- Sample scope: 10 samples per site along transect (1 ft nets), across the river channel with samples equidistant along the transect
- Restoration context: Samples collected before and after restoration events; restoration type documented as part of Site data (Stage 0 restoration activities)
- Pre/post restoration: Transsects were originally marked with stakes pre-restoration; post-restoration site identification relied on GPS (3–4 m error)
- Post-fire context: Dataset aims to evaluate macroinvertebrate response to wildfire and restoration status (pre/post, post-fire, recovery)
- In-field processing: Samples sorted, identified to species/genus by Robert Wisseman; body length measured; trait data assigned from expert database
- Standardization: Density and biomass values standardized to 1 m2 of benthos (scaling factor 0.7432 m2 for density conversion)

## Data organization and files
The dataset comprises four separate CSV files:
- SFMR_Macro_Traits: macroinvertebrate trait definitions and taxon details (Insect, Origin, Classification, Order, Family, Subfamily_tribe, Genus_species, Lifestage, CodeUnique, FFG, Habit, Tolerance, Voltinism, Seasonal, Drift, Size, Rheophily, Thermal)
- SFMR_Macro_Coordinates: site-level spatial data (ID, MasterSite, Trmt, Restoration, Width_Avg_ft, No_samples, GPS_bank, Lat_WGS84, Long_WGS84, Notes)
- SFMR_Macro_Samples: sample-level metadata (River, OrigSite, Date, Transect, MasterSite, SiteYearSeason, Year, Season, Trmt, Post_mos, Post_Fire, Restoration, H_macro, H_micro, Cover_pct, Temp_C, Width_m, Depth_max_m, Depth_avg_m, SISA_pct, GR_pct, CO_pct, BO_pct, NonvascVeg_pct, EmergVeg_pct, AqVeg_pct, BMIwood_pct, Notes)
- SFMR_Macro_Species: species-level outputs (Year, Season, MasterSite, SiteYearSeason, Density, Biomass_mg, CodeUnique, Stage, Taxon_Wisseman)

## Trait and data definitions
- Trait definitions cover taxonomic and functional attributes, including:
  - Insect, Origin (Aquatic, Terrestrial), Classification, Order, Family, Subfamily_tribe, Genus_species
  - Lifestage (Adult, Larvae, Pupa; Code for unique taxon and lifestage)
  - FFG (Functional Feeding Groups), Habit (BU, CL, CM, SP, SW, UN), Tolerance (TolHigh, TolMod, IntHigh, IntMod), Voltinism (SV, UV, MV), Seasonal (fast, slow, non), Drift (rare, common, usual), Size (sm, med, lg), Rheophily (lentic, both, lotic), Thermal (cold, cool-warm, warm)
- CodeUnique provides a unique taxon code; MasterSite labels consistent site names across datasets
- Species data (SFMR_Macro_Species) includes Density and Biomass (mg) by MasterSite, with Life Stage and Taxon_Wisseman

## Collection methodology details
- Sampling method: 1 ft net, 10 samples per site, across transects; sampling position chosen by eye; independent of transect length
- Habitat notes: Filamentous algae not filtered from nonstock; BMI wood defined as within 1 ft of a large woody object
- Post-restoration identification: GPS-based site ID due to stake loss; 3–4 m spatial error
- Taxonomy and traits: Identified to species or genus by Bob Wisseman; traits drawn from his expert database
- Temperature data: USGS temperature measurements used due to handheld device inconsistencies

## Temporal and spatial coverage
- Temporal: Fall 2019, Fall 2020, Winter 2021
- Spatial: 17 sites (2019), 12 sites (2020), 10 sites (2021); each site sampled with 10 transect samples

## Data use and provenance
- Purpose alignment: Data supports evaluation of environmental health and restoration policy by tracking macroinvertebrate responses to wildfire and restoration over time
- Data quality notes: Temperature inconsistencies acknowledged; GPS-based site localization documented; standardized metrics (density/biomass per m2) applied for comparability
- Accessibility: Four CSV files with standardized columns and defined traits, coordinates, samples, and species data to facilitate analysis and cross-site comparisons