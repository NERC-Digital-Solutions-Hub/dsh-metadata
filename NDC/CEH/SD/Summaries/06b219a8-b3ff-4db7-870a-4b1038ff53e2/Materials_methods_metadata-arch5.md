# Materials and methods, and metadata for Global data for soil water, groundwater and riverine freshwater DO14C data taken from 'Linking soil solution and riverine DO14C to soil carbon turnover', Adams et al, 2019 Biogeochemistry

## Overview
- Compiles literature data for dissolved organic carbon (DOC) concentration and DO14C in soil solutions, groundwater, and rivers, covering 1962–2015 (river data) and 1988–2015 (soil and groundwater data).
- New UK river-water measurements (2013–2015) contributed by CEH, JHI, and UEA, with full laboratory processing and radiocarbon analysis.
- Data are organized into CSV datasets with extensive metadata and column heading explanations to support discovery, reuse, and governance.

## Data scope and time coverage
- Soil water DOC concentration and delta14C data: 1989–2015.
- Groundwater DOC concentration and delta14C data: 1988–2008.
- River DO14C data: literature+archived data spanning 1962–2015; includes PROTOS and Marwick et al. (2015) datasets with additions.
- Additional published river data (Extra Published River Surface Water Data) and Marwick River datasets included for broad coverage.

## Data sources and provenance
- Literature compilations built from multiple sources, with digitization of graphed results as needed (ENGAUGE tool).
- New river-water data (TableS3_River_Surface_Water_New) from UK-based campaigns; extensive documentation of sampling, filtration, storage, and processing.
- Archived samples and historical datasets incorporated (Norwegian, US rivers; PROTOS).
- Data lineage documented via extensive reference lists (Buckingham 2008; Marwick et al. 2015; numerous radiocarbon/isotopic studies).

## Data collection and processing workflows
- Sampling and handling
  - Soil and water samples collected with careful contamination controls; blank and field protocols described in TableS3 data documentation.
  - New river samples collected in HDPE bottles; filtration with pre-combusted filter papers; processing in tracer-free labs.
- Laboratory processing
  - DOC quantification performed with elemental analyzers (CEH and JHI) and specific sample handling steps.
  - Radiocarbon (14C) analyses performed at the Scottish Universities Environmental Research Centre AMS Laboratory (East Kilbride) with graphite targets prepared by iron/zinc reduction.
  - δ13C measurements conducted via dual-inlet mass spectrometry; corrections applied for 14C adjustments.
- Data adjustments and quality control
  - 14C data decay-corrected to modern standard (AD 1950 oxalic acid) per Stuiver & Polach (1997).
  - For some samples, δ13C values were used to correct to δ13C = -25 ‰ VPDB when 13C measurements were problematic.
  - Precision reported as 1σ, averaging 0.45 pMC (range 0.35–0.70 pMC); QA included use of process-blanks and standards; some samples re-analyzed to ensure purge completeness (pH adjustments).

## Data structure and metadata standards
- Tables and column headings
  - TableS1_Soil_water_data.csv: site location, country, lat/long, date, vegetation, land_class, soil type, depth, [DOC], 13C, delta14C, notes, reference.
  - TableS2_Groundwater_data.csv: site, country, lat/long, date, aquifer, [DOC], 13C, delta14C, notes, reference.
  - TableS3_River_Surface_Water_New.csv: data_line, country/region, site, year, lat/long, [DOC]_mg/L, delta13C_‰, delta14C_‰, land_class, publication_code.
  - TableS3_Marwick_River_Surface_Water.csv; TableS3_Extra_Published_River_Surface_Water_Data.csv: similarly structured with detailed column headings.
- Metadata detail
  - Column heading explanations provided for TableS1 and TableS2 (location, country, coordinates, date, vegetation, land_class, sample measurements, references).
  - Detailed explanations for TableS3 datasets (data_line, site, year, coordinates, DOC, δ13C, Δ14C, land use, publication code, and related notes).
  - Full references accompany each dataset and data line.

## Data quality, uncertainty, and QA
- Analytical precision for Δ14C/14C corrections documented; overall 0.45 pMC precision.
- Calibration and correction steps (δ13C corrections, pMC to Δ14C conversions) explicitly described.
- Purging and acidification steps used to remove inorganic carbon; re-analysis performed when purge incomplete.
- Data digitization from published graphs acknowledged; standardized processing to enable comparability across studies.

## Site information and land-use metadata
- Sites categorized by land_class and habitat type (pure forest, wetland, natural/sem natural NSN, etc.).
- Land_class data used to support analyses of carbon source and aging in riverine systems.
- Discharge data used to test select hypotheses where available.

## Data governance, sharing, and updates
- Emphasis on ensuring datasets meet standards (accuracy, metadata, formats) and on capturing provenance.
- Systems in place to respect sharing limitations and to enable dataset updates and versioning.
- Documentation supports reuse by data creators/sharers and data users, aligning with the Data Steward aim to enable discovery and usability.

## Challenges and considerations for Data Stewards
- Incomplete understanding of user needs and priorities.
- Timely acquisition of data from producers.
- Encouraging metadata completeness and standardization across diverse systems/formats.
- Handling large datasets and legacy/non-interoperable databases.
- Ensuring continual updates and licenses when sharing data across portals and catalogs.

## References and data sources
- Comprehensive references for soil water, groundwater, riverine DO14C data, including Buckingham (2008), Marwick et al. (2015), PROTOS project materials, and numerous radiocarbon/isotopic studies.
- Datasets pull from theses, journal articles, and project reports, with clear attribution in each table’s references section.