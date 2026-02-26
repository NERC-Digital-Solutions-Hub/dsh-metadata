# Supporting document for
"Nitrous oxide emissions and associated microbial diversity, soil biochemical properties and crop growth and yield from a field trial of winter barley with the addition of microplastics, Abergwyngregyn, UK, 2020-2021"

## Executive overview
- Purpose: Field trial to assess the impact of conventional vs biodegradable microplastics on N2O emissions, soil biology, biochemical properties, and barley crop performance.
- Setting: Henfaes Research Centre, Abergwyngregyn, North Wales (randomised block design; 3 treatments with 4 replicates).
- Data scope: In-field measurements and lab analyses spanning gas flux, soil chemistry, microbial communities, weather, and crop metrics; data are organized into multiple CSV files with detailed metadata.
- Data handling: Data processed and integrated with specialized software; results prepared for deposit in the EIDC data repository.

## Study design and scope
- Design: Field trial conducted Sept 2020 – July 2021; randomised block with three treatments (conventional microplastics, biodegradable microplastics, control) and four replicates per treatment.
- Location: 53°14'29"N, 4°01'15"W, North Wales.
- Treatments and sampling: Comprehensive sampling across topsoil (0–10 cm) with repeated measurements through the growing season, including pre-harvest and post-harvest periods.

## Data collected and targets
- In situ measurements:
  - Nitrous oxide (N2O) fluxes using a mobile gas chromatograph system; 8 measurements per 24 hours; flux calculated via Flux.NET and cumulative flux estimated by trapezoidal integration.
  - Soil moisture (Accilima sensors), rainfall, and air temperature (weather station) with high-frequency logging.
  - Plant health proxies: SPAD (leaf chlorophyll) and crop height.
  - GHG monitoring apparatus includes greenhouse gas chambers and plot-specific monitoring extensions.
- Laboratory analyses:
  - Soil chemistry: pH, electrical conductivity (EC), ammonium (NH4+), nitrate (NO3−) via standard extraction and spectrophotometric methods; data generated as calibration-curve-based concentration values.
  - Microbial community: 16S rRNA gene sequencing (Illumina MiSeq); downstream processing with Python and QIIME v1.3.1 to produce ASV count tables and taxonomic classifications.
  - Crop yield components: stem count, grain per ear, ear weight, straw weight, grain weight, and 100-grain weight.
- Sampling regime: Detailed schedule of activities and measurements (Table 1); sampling depth 0–10 cm for soil analyses; ferreted into multiple timepoints and measurement types (Table 3).

## Data processing and analysis pipeline
- N2O data: Peak area integration in Peak490Win10Canabis, export to .CHR, processing in Flux.NET, export to Excel and then to .csv for EIDC.
- Microbial data: 16S sequencing reads processed to ASV count tables and taxa tables; alignment to SILVA v138 references via QIIME v1.3.1 and custom Python scripts.
- Soil and plant data: Field notes transcribed into Excel, then exported as .csv files for integration.
- Data standards: Explicit metadata descriptors accompany each file (date, time, treatment, plot, and measurement-specific fields).

## Data resources and file structure
- The data resource comprises 10 primary files:
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
- Each file includes clearly defined columns (e.g., date, time, treatment, plot, and measurement-specific variables such as nitrate, ammonium, ph, ec, N2O flux, etc.).
- Additional context: Table 1 (key dates), Table 2 (microplastics characteristics), and Table 3 (sampling regime and methods) provide methodological and scheduling details.
- Data gaps: Some rows/fields are blank where measurements were not possible (e.g., certain plant growth measurements due to small plants).

## Data management, quality and governance
- Data management: Data are organized by measurement type and linked through consistent identifiers (date, time, treatment, plot) to enable multi-omics and multi-parameter analyses.
- Documentation: Methodological references accompany the dataset (Marsden et al. 2018; Miranda et al. 2001; Mulvaney 1996).
- Access and deposition: Data prepared for deposition in the EIDC repository, enabling discoverability and reuse.
- Reproducibility considerations: Detailed sampling schedules, measurement methods, and data processing workflows support replicability and secondary analyses.

## Practical implications for data leaders
- End-to-end data system view: This project demonstrates integration of field and laboratory data across disciplines (gas fluxomics, soil chemistry, microbiomics, agronomy) with standardized data formats.
- Metadata and discoverability: Explicit metadata fields and documentation facilitate data discovery, interpretation, and reuse by policy colleagues and cross-institutional partners.
- Data quality and gaps: Acknowledges measurement gaps and potential data quality considerations across high-frequency time-series data and complex sequencing outputs.
- Collaboration and standards: Use of established software (Flux.NET, QIIME v1.3.1) and references highlights the importance of standardized tooling and community resources to support a robust data ecosystem.