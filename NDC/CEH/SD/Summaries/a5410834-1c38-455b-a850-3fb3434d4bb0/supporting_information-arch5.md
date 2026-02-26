# Supporting document for
'Nitrous oxide emissions and associated microbial diversity, soil biochemical properties and crop growth and yield from a field trial of winter barley with the addition of microplastics, Abergwyngregyn, UK, 2020-2021'

## Purpose and scope
- Describes a field trial (Sept 2020 – July 2021) assessing the effects of conventional vs biodegradable microplastics on N2O emissions, microbial diversity, soil biochemistry, and crop growth/yield.
- Location: Henfaes Research Centre, Abergwyngregyn, North Wales.
- Experimental design: randomised block with three treatments (conventional microplastic, biodegradable microplastic, control) and four replicates per treatment (n=4).

## Data collection and measurements
- In-field measurements:
  - N2O flux using a mobile gas chromatograph system; data processed to generate cumulative and per-measurement flux values.
  - Soil moisture (Acclima sensors), rainfall, and air temperature (weather station).
- Laboratory measurements:
  - Soil pH and electrical conductivity (EC).
  - Soil ammonium and nitrate via microplate method with Gen5 software and calibration curves.
  - Crop growth metrics (SPAD chlorophyll, plant height) and crop yield (two middle-plot areas).
  - Microbial community composition via 16S rRNA gene sequencing (Illumina MiSeq); data processed with Python and QIIME v1.3.1 to produce ASV counts and taxonomic assignments.
- Data recording and transfer:
  - Field observations logged in notebooks; processed into Excel and CSV files for deposition.
  - N2O data exported through multiple software steps (Peak490Win10Cannabis → Flux.NET → Excel → CSV; cumulative flux via trapezoidal integration in Excel).

## Data resource layout and file types
- Data resource comprises 10 CSV files (plus related growth data noted):
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
- Additional dataset referenced:
  - crop_growth.csv (5 columns, 264 rows) detailing plant growth measurements; notes that plant height measurements include blanks due to small plants early in the trial.
- Dataset contents (high-level):
  - crop_harvest.csv: harvest-level metrics by plot/treatment.
  - crop_yield.csv: yield components (stem_count, grain_per_ear, ear_weight, straw_weight, grain_weight) by plot/treatment.
  - n2o_cumulative.csv: date, time, chamber, treatment, and cumulative N2O flux (mg N2O-N m^-2).
  - n2o_flux.csv: date, time, chamber, treatment, and flux values (best estimate).
  - soil_n.csv: nitrate and ammonium contents by date, treatment, plot.
  - soilph_ec.csv: soil pH and EC by date, time, treatment.
  - weather.csv: date, time, air_temp and rainfall.
  - wfps.csv: date, time, treatment, plot, and water-filled pore space percentage.
  - asv_count_table.csv: counts of Amplicon Sequence Variants (ASVs) by treatment replication.
  - taxa_table.csv: taxonomic assignments (domain to species) for ASVs (SILVA v138), with some blanks at lower taxonomic levels.
- Data columns and units are explicitly described for each file (e.g., NO3-N and NH4-N contents in kg N ha^-1, SPAD as unitless, plant_height in cm, etc.).

## Data production and processing details
- N2O data: collected with a mobile GC system; processed through Flux.NET; cumulative flux calculated in Excel.
- Soil chemistry: performed with standard extraction and colorimetric/igen-based methods; calibration curves used to convert readings to mg/kg.
- Microbial data: raw 16S reads processed in Python and QIIME v1.3.1 to generate ASV count tables and taxa tables.
- Metadata and provenance:
  - Key dates and activities captured (Table 1) detailing management actions and sampling milestones.
  - Microplastic treatments characterized (Table 2) with material type, size, and application rate (100 kg/ha) in the top 0–10 cm.
  - Sampling regime and methods summarized (Table 3), including measurement frequency, equipment, and analysis methods.
- Data deposition: outputs prepared for deposit in the EIDC data repository.

## Metadata, standards, and provenance considerations
- Documentation provides explicit data dictionaries and file-level metadata (dates, treatments, plots, measured variables, units).
- Taxonomic data linked to SILVA v138 databases; acknowledges blanks where taxonomic resolution is unavailable.
- References for methods and analysis techniques included (Marsden et al. 2018; Miranda et al. 2001; Mulvaney 1996).

## Governance, sharing, and stewardship considerations
- Data are organized into discrete, well-described CSV files enabling discoverability and reuse.
- Data sharing via EIDC implies a governance workflow for access, versioning, and updates; consider clear licensing, embargo, and provenance records.
- Large datasets (e.g., wfps with 221,859 rows) highlight needs for scalable storage, efficient retrieval, and clear data transfer processes.
- Potential data stewardship tasks:
  - Ensure metadata completeness (sampling dates, treatment codes, plot identifiers, units, methods).
  - Maintain consistent units and formats across all files (e.g., date formats, concentration units).
  - Enforce interoperability practices for multi-source data (field measurements, lab assays, sequencing data).
  - Track data processing steps (software versions: Flux.NET 3.3, QIIME v1.3.1, Python scripts) for reproducibility.
  - Document data quality checks and any data cleaning performed (outliers, missing values, calibration adjustments).
  - Plan for updates and synchronization across the 10 data files when new measurements or revisions occur.

## Key takeaways for data stewardship
- The dataset provides a comprehensive, multi-method capture of a field trial, combining environmental measurements, soil chemistry, crop performance, and microbial sequencing.
- It is structured into clearly delineated CSV files with explicit variable definitions and units, suitable for reuse and secondary analyses.
- Governance considerations center on metadata completeness, data provenance, handling of large files, and clear deposit/sharing pathways (EIDC), ensuring the data remain discoverable, interoperable, and up to date.