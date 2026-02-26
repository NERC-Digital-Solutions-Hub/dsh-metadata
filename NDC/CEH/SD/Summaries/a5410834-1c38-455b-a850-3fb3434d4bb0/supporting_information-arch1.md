# Supporting document for
# 'Nitrous oxide emissions and associated microbial diversity, soil biochemical properties and crop growth and yield from a field trial of winter barley with the addition of microplastics, Abergwyngregyn, UK, 2020-2021'

## Overview
- Field trial conducted Sep 2020 to Jul 2021 at Henfaes Research Centre, Abergwyngregyn, North Wales (53°14'29"N, 4°01'15"W).
- Objective: assess effects of conventional versus biodegradable microplastics on N2O emissions, microbial community composition, soil biochemical properties, and crop growth/yield.
- Experimental design: randomised block with three treatments (conventional microplastic, biodegradable microplastic, control) and four replicates per treatment (n = 4).

## Experimental design and treatments
- Treatments:
  - Conventional microplastic (polyethylene, PE) powder, 40–48 μm, 100 kg/ha, applied to 0–10 cm soil.
  - Biodegradable microplastic (PHBV; ENMAT Y1000), 1–15 μm, 100 kg/ha, applied to 0–10 cm soil.
  - Control (no microplastic).
- Layout: plots arranged in a randomised block design; 10 plots per block? (exact block count not specified; four replicates per treatment).

## Data collection and measurements (in situ and lab)
- In-field measurements:
  - N2O flux using a mobile gas chromatograph (GC) system; 8 flux measurements per 24 h period.
  - Soil moisture ( Acclima sensors ), air temperature, and rainfall (weather station) data collected continuously or at frequent intervals.
  - Weather data stored as CSV (date, time, air_temp, rainfall).
- Laboratory analyses:
  - Soil pH and electrical conductivity (EC) measured on 0–10 cm soil samples.
  - Soil ammonium (NH4+) and nitrate (NO3−) content via 1:5 soil extracts and calibration curves.
  - Microbial community composition via 16S rRNA gene sequencing (Illumina MiSeq); ASV counts and taxonomic tables produced.
  - Crop measurements: growth metrics (SPAD leaf chlorophyll, plant height) and harvest/yield metrics (stem_count, grain_per_ear, ear_weight, straw_weight, grain_weight).

## Data processing and workflows
- N2O data:
  - Flux calculated from GC measurements using Flux.NET.
  - Cumulative N2O flux determined by trapezoidal integration in Excel.
- Microbial data:
  - Sequencing reads processed with Python; filtering performed in QIIME v1.3.1 to generate ASV count table and taxa table.
- Data management:
  - Datasets prepared as CSV files and deposited for access through the project data portal (EIDC).

## Data resource layout
The data resource comprises 10 files:
- crop_harvest.csv
- crop_yield.csv
- n2o_cumulative.csv
- n2o_flux.csv
- soil_n.csv
- soilph_ec.csv
- weather.csv
- wfps.csv
- asv_count_table.csv
- taxa_table.csv

## File-level summaries (key columns and content)
- crop_growth.csv (growth-related measurements):
  - Columns: date, Variable, date (units), treatment, plot, spad (leaf chlorophyll content), plant_height (cm).
  - Note: 264 rows; some plant height measurements are missing due to small plants.
- crop_yield.csv (yield components):
  - Columns: treatment, plot, stem_count, grain_per_ear, ear_weight (g, dry weight), straw_weight (kg/ha), grain_weight (g per 100 grains).
  - Rows: 12 entries covering treatments/plots.
- n2o_cumulative.csv (cumulative N2O flux):
  - Columns: date, time, chamber, treatment, cumulative_flux (mg N2O-N m−2).
  - Rows: 17843; some early timepoints have missing data.
- n2o_flux.csv (N2O flux per measurement):
  - Columns: date, time, chamber, treatment, flux_best (μg N2O-N m−2 h−1).
  - Rows: 17843; derived from individual flux measurements.
- soil_n.csv (soil inorganic N):
  - Columns: date, treatment, plot, nitrate (NO3−) (kg NO3−-N ha−1), ammonium (NH4+) (kg NH4+-N ha−1).
  - Rows: 552.
- soilph_ec.csv (soil pH and EC):
  - Columns: date, time, treatment, ph, ec.
  - Rows: 386.
- weather.csv (meteorological data):
  - Columns: date, time, air_temp (°C), rainfall (mm).
  - Rows: 11623.
- wfps.csv (water-filled pore space):
  - Columns: date, time, treatment, plot, wfps (%).
  - Rows: 221859.
- asv_count_table.csv (amplicon sequence variant counts):
  - Columns: asv, control_1..4, conventional_1..4, biodegradable_1..4 (counts per ASV per replicate).
  - Rows: 2796.
- taxa_table.csv (taxonomy for ASVs):
  - Columns: asv, Domain, Phylum, Class, Order, Family, Genus, Species.
  - Rows: 2796.
Notes:
- Some metadata and naming inconsistencies exist (e.g., crop_growth.csv described in text but listed as crop_harvest.csv in the file list). The document provides growth (SPAD, height), yield, N2O, soil chemistry, weather, soil moisture, and microbiome data across these files.

## Sampling regime, equipment, and methods
- N2O flux:
  - Frequency: 8 measurements per 24 hours.
  - Equipment: Gas chromatograph system (mobile GC) with Flux.NET processing.
- Soil moisture, air temperature:
  - Frequency: every 30 minutes; devices include Accilima sensors.
- Soil chemistry:
  - pH, EC, NH4+, NO3−: measured weekly (reducing to fortnightly after 28/05/2021).
  - Sample origin: soil 0–10 cm; extraction and calibration for inorganic N.
- Crop metrics:
  - SPAD (chlorophyll) and plant height: measured weekly, later fortnightly after 11/06/2021.
  - Harvest: end of trial; two 50 cm × 10 cm areas per plot used for main harvest measurements.
- Microbial analysis:
  - 16S rRNA gene sequencing on Illumina MiSeq; end-of-trial sampling for microbial DNA; data processed to ASV and taxon tables.

## Location and environmental context
- Site: Henfaes Research Centre, Abergwyngregyn, North Wales.
- Coordinates: 53°14'29"N, 4°01'15"W.
- Important dates include establishment of microplastics (16/09/2020), sowing (16/10/2020), fertilizer applications (26/10/2020; 25/03/2021; 19/04/2021), greenhouse gas chamber adjustments, sampling changes (28/05/2021; 11/06/2021), bird-related plot damage (21/06/2021; 21–25/06/2021), and final sampling/archive (25/06/2021).

## Data provenance and accessibility
- Data produced through field measurements and laboratory analyses, with explicit processing steps (GC flux to cumulative flux, 16S sequencing data processing).
- Deposited in the Environmental Data and Information Centre (EIDC) data portal.
- References for methods include:
  - Marsden et al., 2018 (N2O emissions and measurement approaches)
  - Miranda et al., 2001 (nitrate/nitrite detection)
  - Mulvaney, 1996 (inorganic nitrogen methods)

## Potential analyses and use cases for analysts
- Assess how conventional vs biodegradable microplastics influence:
  - N2O emissions (flux and cumulative flux) and emission factors.
  - Soil inorganic N pools (NO3−, NH4+) and soil chemical properties (pH, EC).
  - Soil moisture dynamics and water-filled pore space in relation to N2O flux.
  - Microbial community structure and ASV-level changes; associations with N2O flux and soil chemistry.
  - Crop growth metrics (SPAD, height) and yield components (stem_count, grain_per_ear, ear_weight, straw_weight, grain_weight).
- Develop predictive models linking N2O flux to environmental variables, plastic treatment, and microbial metrics.
- Conduct correlation analyses between microbial taxa (or ASVs) and N2O emissions or soil biogeochemical properties.
- Use spatial/temporal data (date, treatment, plot) to explore treatment-by-time interactions and potential lag effects.

## Endnotes and constraints
- Field disruption: significant bird damage around 21–25 June 2021 affected harvest feasibility in some plots; some data collection may have been curtailed or altered near the end of the trial.
- Data completeness: some measurements have missing values (e.g., plant height due to small plants; early cumulative flux data gaps).
- Scale considerations: local field scale; data may require careful normalization and handling of replicates for cross-study comparability.

## References for context
- Marsden, K.A., Holmberg, J.A., Jones, D.L., Chadwick, D.R. (2018). Sheep urine patch N2O emissions are lower from extensively-managed than intensively-managed grasslands. Agric. Ecosyst. Environ. 265, 264-274.
- Miranda, K.M., Espey, M.G., Wink, D.A. (2001). A Rapid, Simple Spectrophotometric Method for Simultaneous Detection of Nitrate and Nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L. (1996). Nitrogen-Inorganic Forms, in Methods of Soil Analysis. John Wiley & Sons.