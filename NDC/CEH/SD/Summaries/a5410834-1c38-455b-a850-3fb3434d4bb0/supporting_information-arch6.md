# Supporting document for "Nitrous oxide emissions and associated microbial diversity, soil biochemical properties and crop growth and yield from a field trial of winter barley with the addition of microplastics, Abergwyngregyn, UK, 2020-2021"

## Overview
- Field trial (Sept 2020 – July 2021) in North Wales to compare conventional microplastic, biodegradable microplastic, and control on N2O emissions, microbial diversity, soil biochemistry, and crop growth/yield.
- Experimental design: randomised block with three treatments and four replicates per treatment (n=4).

## Experimental design and data collection
- Location: Henfaes Research Centre, Abergwyngregyn (53°14'29"N, 4°01'15"W).
- Measurements in situ: N2O flux, soil moisture, rainfall, air temperature.
- Laboratory analyses: soil pH, electrical conductivity (EC), ammonium, nitrate, microbial community composition, and crop yield.
- Methods of key measurements:
  - N2O flux: mobile gas chromatograph; data processed to compute flux per sample and cumulative flux (via trapezoidal integration).
  - Soil moisture: Acclima sensors.
  - Weather: rainfall and air temperature from weather station.
  - Soil pH/EC: manual measurements input to Excel, exported as CSV.
  - Ammonium/Nitrate: microplate method; Gen5 software; data converted to mg/kg using calibration curves; CSV output.
  - Crop growth: field notes → Excel to CSV.
  - Crop yield: field notes → Excel to CSV.
  - Microbial community: 16S sequencing (Illumina MiSeq); raw reads processed with Python and QIIME v1.3.1; outputs ASV count table and taxa table (CSV).

## Data resource layout (files and general content)
- The data resource consists of 10 CSV files:
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
- Highlights by file:
  - crop_growth.csv: 5 columns, 264 rows; captures date, treatment, plot, SPAD (leaf chlorophyll), and plant_height (plant height); some plant height measurements are blank due to small plants.
  - crop_yield.csv: 7 columns, 12 rows; metrics per plot including stem_count, grain_per_ear, ear_weight, straw_weight, grain_weight.
  - n2o_cumulative.csv: 5 columns, 17,843 rows; date, time, chamber, treatment, cumulative_flux (N2O-N, mg m^-2).
  - n2o_flux.csv: 5 columns, 17,843 rows; date, time, chamber, treatment, flux_best (N2O-N, μg m^-2 h^-1).
  - soil_n.csv: 5 columns, 552 rows; nitrate and ammonium contents per plot, date, treatment.
  - soilph_ec.csv: 5 columns, 386 rows; pH and EC with date, time, and treatment.
  - weather.csv: 4 columns, 11,623 rows; date, time, air_temp (°C), rainfall (mm).
  - wfps.csv: 5 columns, 221,859 rows; date, time, treatment, plot, wfps (%).
  - asv_count_table.csv: 13 columns, 2,796 rows; counts of Amplicon Sequence Variants (ASVs) by treatment replication (control_1–4, conventional_1–4, biodegradable_1–4).
  - taxa_table.csv: 8 columns, 2,796 rows; Taxonomic assignations (Domain, Phylum, Class, Order, Family, Genus, Species) for each ASV.
- Notes:
  - Data are organized with columns for date and time, treatment, and plot, plus variable-specific measurements (e.g., SPAD, plant_height, nitrate, ammonium, etc.).
  - Some spatial-temporal gaps exist (e.g., plant_height blanks when plants were too small).

## Data processing, provenance, and derived metrics
- N2O flux and cumulative flux:
  - In-field measurements using a mobile GC;-derived flux values are integrated to obtain cumulative N2O flux.
  - Derived in Excel and deposited as CSV (n2o_flux.csv and n2o_cumulative.csv).
- Microbial data:
  - 16S sequencing data processed with Python and QIIME v1.3.1; outputs include asv_count_table.csv and taxa_table.csv representing abundance and taxonomy by sample.
- Data provenance:
  - Data flow from field measurements and lab assays to CSV files, then to higher-level aggregates (e.g., cumulative N2O) and availability in the data resource layout.
  - Data deposited for reuse in Ethically Important Data Repository (EIDC).

## Sampling regime and experimental details (metadata references)
- Table 1: Key dates for setup, management, and data collection (e.g., microplastic application, barley sowing, greenhouse gas chamber setup, fertilizer applications, bird-related disturbances, harvest events).
- Table 2: Microplastic characteristics and application details:
  - Conventional powder (PE): 40–48 μm, 100 kg/ha, applied to 0–10 cm soil.
  - Biodegradable powder (PHBV): 1–15 μm, 100 kg/ha, applied to 0–10 cm soil.
- Table 3: Sampling regime and methods:
  - N2O flux: 8 measurements per 24 h; gas chromatography system; sampling frequency.
  - Soil moisture: every 30 minutes; Acclima sensors.
  - Air temperature: every 30 minutes; meteorological station data.
  - Soil pH, EC, NH4+, NO3−: frequent measurements with weekly to fortnightly updates; extraction and analysis methods described.
  - Leaf SPAD: weekly to fortnightly (post-11/06/2021).
  - Crop height: weekly to fortnightly.
  - Microbial community composition: end of trial (soil 0–10 cm; -80°C storage prior to freeze-drying).
  - Crop harvest: at end of trial (two 50 cm × 10 cm areas per plot).

## Use cases and data products for end users
- Potential dashboards and analyses:
  - Compare N2O flux and cumulative flux across treatments and replicates over time, with weather context.
  - Link soil properties (pH, EC, nitrate, ammonium) and soil moisture to N2O emissions.
  - Assess crop growth metrics (SPAD, height) and yield components (ear weight, grain count, grain weight) by treatment.
  - Explore microbial community patterns (ASV counts and taxonomic assignments) in relation to microplastic treatment and soil chemistry.
- Data integration points:
  - Merge weather.csv with N2O flux and soil moisture to study environmental drivers.
  - Join crop_yield and crop_growth with soil_n and soilph_ec for agronomic interpretation.
  - Combine ASV_count_table.csv and taxa_table.csv with soil properties to explore links between microbial diversity and soil chemistry.

## References
- Marsden et al. 2018. Sheep urine patch N2O emissions are lower from extensively-managed than intensively-managed grasslands. Agric. Ecosyst. Environ. 265, 264-274.
- Miranda et al. 2001. A rapid spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney 1996. Methods of Soil Analysis (inorganic forms).