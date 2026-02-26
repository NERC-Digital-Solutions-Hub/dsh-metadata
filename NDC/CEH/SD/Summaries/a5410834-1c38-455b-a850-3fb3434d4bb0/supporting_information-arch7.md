# Supporting document for
'Nitrous oxide emissions and associated microbial diversity, soil biochemical properties and crop growth and yield from a field trial of winter barley with the addition of microplastics, Abergwyngregyn, UK, 2020-2021'

## Overview
- Field trial (Sep 2020–Jul 2021) comparing conventional vs biodegradable microplastics against a control to assess N2O emissions, microbial diversity, soil biochemistry, and crop performance.
- Field site: Henfaes Research Centre, Abergwyngregyn, North Wales (53°14'29"N, 4°01'15"W).
- Experimental design: randomised block with three treatments (conventional microplastic, biodegradable microplastic, control) and four replicates per treatment (n=12 plots).
- Data collected in field and lab, spanning gas flux, soil properties, climate, crop metrics, and microbial community data.
- Primary data products prepared for GIS-friendly use (per-plot, per-date data) and deposited outputs for N2O flux; sequencing data processed into ASV counts and taxonomic tables.

## Experimental design and field site
- Location and coordinates provided; field plots arranged in a randomised block design.
- Plot layout described (Figure 1 referenced) with 3 treatments × 4 replicates.
- Key dates and activities documented (seeding, microplastics application, fertilizer events, gas chamber installation, sampling events, harvest activities).

## Data collection and measurement
- In-field measurements:
  - N2O flux: mobile gas chromatograph system; measurements aggregated to compute cumulative flux.
  - Soil moisture: Acclima sensors (30-minute intervals).
  - Weather: Rainfall and air temperature from weather station (time-stamped data).
  - Additional in-field measurements: SPAD leaf chlorophyll, plant height, crop harvest area.
- Laboratory analyses:
  - Soil pH and electrical conductivity (EC) measured from 0–10 cm depth.
  - Soil ammonium (NH4+) and nitrate (NO3−) quantified via microplate method with calibration curves.
  - Crop yield components: stem count, grains per ear, ear weight, straw weight, grain weight per plot.
  - Crop growth details captured in notebooks and transcribed to CSV.
- Microbial analyses:
  - 16S rRNA gene sequencing (Illumina MiSeq) to profile microbial communities.
  - Raw reads processed with Python and QIIME v1.3.1 to produce ASV count table and taxa table.
- Data processing workflows:
  - N2O flux: peak areas from GC data exported to Flux.NET (v3.3) and cumulative flux calculated via trapezoidal integration in Excel.
  - Data compiled into per-measurement CSV files for deposition (including N2O flux and cumulative flux).

## Data resource layout (files and contents)
- The data resource comprises 10 CSV files:
  - crop_harvest.csv: contains date, treatment, plot, and harvest-related variables (e.g., SPAD and plant height data, with some height measurements blank due to very small plants).
  - crop_yield.csv: per-plot yield metrics including stem_count, grain_per_ear, ear_weight, straw_weight, grain_weight.
  - n2o_cumulative.csv: cumulative N2O flux by date/time and chamber, with units of mg N2O-N m^-2.
  - n2o_flux.csv: N2O flux estimates per measurement (flux_best) with date, time, chamber, treatment, and flux rate.
  - soil_n.csv: soil NO3− and NH4+ contents by date, plot, and treatment.
  - soilph_ec.csv: soil pH and EC by date, time, plot, and treatment.
  - weather.csv: daily weather records (date, time, air_temp, rainfall).
  - wfps.csv: water-filled pore space over time by plot and treatment.
  - asv_count_table.csv: ASV counts per sample with columns for control, conventional, and biodegradable replications.
  - taxa_table.csv: taxonomic assignment per ASV (domain to species) with SILVA v138-based taxonomy.
- Data characteristics:
  - n2o_flux and n2o_cumulative: 17843 rows each.
  - soil_n: 552 rows.
  - soilph_ec: 386 rows.
  - weather: 11623 rows.
  - wfps: 221859 rows.
  - asv_count_table and taxa_table: 2796 rows, 13 and 8 columns respectively.
- Additional context:
  - Several outputs were prepared with specific formatting (e.g., .chr intermediate file for N2O flux processing; final CSVs deposited to EIDC).
  - Table references for sampling regime and plotting described in the dataset narrative (e.g., sampling frequency and measurement methods for each variable).

## Spatial, temporal, and data quality considerations for GIS
- Spatial: study plots arranged in a randomised block design within a defined field site; plot identifiers and treatments available to enable per-plot spatial joins and map-layer creation.
- Temporal: extensive time series across the trial (dates and times for flux, weather, soil properties, and growth metrics); data are aligned by date and plot, enabling spatiotemporal mapping of N2O flux and soil conditions.
- Data provenance and processing: detailed methodological notes on measurement techniques and data transformations (e.g., N2O flux calculation in Flux.NET, DNA sequencing pipeline with QIIME) support traceability and reproducibility for GIS analyses and data integration with other spatial datasets.
- Data standards: CSV format; explicit units for each variable; date formats specified (dd/mm/yyyy where applicable); depth specification for soil samples (0–10 cm). Taxonomic data aligned to SILVA v138 framework.

## Access, usage, and references
- Data deposition: N2O-related outputs prepared for deposit in EIDC.
- Key methodological references:
  - Marsden et al. 2018 for N2O emission measurement in related grassland contexts.
  - Miranda et al. 2001 for nitrate/nitrite detection method.
  - Mulvaney 1996 for inorganic soil nitrogen methods.
- These data and methods enable GIS-enabled analyses of spatial patterns in N2O emissions, soil properties, crop performance, and microbial community structure under microplastic treatments.