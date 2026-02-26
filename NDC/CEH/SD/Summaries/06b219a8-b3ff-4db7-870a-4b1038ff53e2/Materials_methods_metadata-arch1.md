# Materials and methods, and metadata for Global data for soil water, groundwater and riverine freshwater DO14C data taken from 'Linking soil solution and riverine DO14C to soil carbon turnover', Adams et al, 2019 Biogeochemistry.

## Overview
- Presents global data for dissolved organic 14C (DO14C) in soil water, groundwater, and riverine freshwater, compiled to study soil carbon turnover.
- Data span through multiple sources and time periods:
  - Soil solution DO14C and DOC concentration: 1989–2015
  - Groundwater DO14C: 1988–2008
  - Riverine DO14C (compiled from Marwick et al. 2015 and additional data): 1962–2015
- Data gathering included literature compilation and digitisation of graphed results when needed (ENGAUGE digitiser).
- Where available, river discharge data were included for single sites with multiple observations.
- Aimed to enable analysis of carbon age, source, and transport from soils to rivers, with metadata to support reproducibility.

## Data compilation and sources
- Literature data compiled for:
  - DOC concentration [DOC] and DO14C in soil solutions
  - Groundwater DO14C
  - Riverine DO14C (built on Marwick et al. 2015 data with additions)
- Data digitised from published figures when necessary; discharge data included for selected sites.
- Metadata and site classifications prepared to enable cross-dataset analyses (land use, vegetation, etc.).

## New river surface water measurements (TableS3_River_Surface_Water_New)
- Fieldwork conducted in the UK (2013–2015) by:
  - Centre for Ecology & Hydrology (CEH), Lancaster
  - James Hutton Institute (JHI), Aberdeen
  - University of East Anglia (UEA), Norwich
- Sampling and handling:
  - New or acid-washed equipment; radiocarbon tracer-free laboratories
  - Sample collection in HDPE bottles; filtration through pre-combusted filter papers; filtrates stored in clean glass bottles
  - Additional samples for DOC concentration measured with elemental analysers
- Laboratory processing:
  - Filtrates transported to NERC Radiocarbon Facility (East Kilbride) for carbonate removal, organic carbon recovery, and CO2 preparation for AMS
  - Archived samples also included from Norwegian and US rivers (1960s–1970s)
  - Standards and process blanks used to monitor accuracy and precision
- Carbon and isotopic analyses:
  - δ13C measured by dual-inlet mass spectrometry; corrections applied to DO14C data
  - In cases of high δ13C indicating carbonate residues, re-analysis performed with purge to pH 2
  - Graphite targets for 14C analysis prepared via iron/zinc reduction; AMS performed at SUERC
  - Some δ13C values derived from AMS rather than independent mass spectrometry and used for correction, with caveats noted
  - DO14C results converted to Δ14C, with decay corrections relative to the oxalic acid modern standard (1950 baseline)
- Precision:
  - Overall analytical precision ≈ 0.45 pMC (1σ), combining AMS statistics and lab processing uncertainties

## Site information and land classification
- Land classes assigned per TableS1_Soil_water_data.csv, using source references for site specifics.
- Pure status defined as at least 90% vegetation type (forest or wetland) within catchments.
- NSN category includes natural or semi-natural landscapes (e.g., mixed landscapes, unfertilized grasslands/heathlands).
- Land_class categorisations used to test hypotheses when discharge data were quantified; qualitative land-use descriptions not used in those tests.

## Data processing, analysis, and quality
- Statistical analyses performed in Microsoft Excel:
  - T-tests and linear regressions
  - Normality and homoscedasticity checks; log-transformations applied when necessary
- Data sources and analyses were cross-checked, and datasets created with metadata to support discovery and reuse.

## Data tables and metadata
- TableS1_Soil_water_data.csv: soil-water data with columns for location, country, coordinates, date, vegetation, land_class, soil, depth, [DOC], 13C, delta14C, and notes; includes references.
- TableS2_Groundwater_data.csv: groundwater data with columns for location, country, coordinates, date, aquifer, [DOC], 13C, delta14C, notes, and references.
- TableS3_River_Surface_Water_New.csv: new UK river-surface-water data with columns such as Data_line, Country_or_Region, Site, year, Lat, Long, [DOC]_mg/L, delta13C_‰, delta14C_‰, Land_class, Publication_code, and references.
- TableS3_Marwick_River_Surface_Water.csv: river surface water data from Marwick et al. (2015) with corresponding column headings.
- TableS3_Extra_Published_River_Surface_Water_Data.csv: additional published river surface-water DO14C data, with a comprehensive set of columns (country/region, site, year, coordinates, [DOC], delta13C, delta14C, Land_class, References, etc.) and notes.
- Column heading explanations provided for each CSV to aid interpretation, including exact meanings for data fields, units, and any data-specific notes.

## References and data provenance
- The document includes extensive references validating data sources for Tables S1 and S2 (soil and groundwater data) and Tables S3 (river data), including major works on riverine DO14C and methodological guidance for radiocarbon analysis.
- Key cited works and projects include Marwick et al. (2015), PROTOS (Mulder et al. 2000), and numerous radiocarbon/isotopic studies across global river systems, soils, and peatlands.
- Data and metadata are intended to be discoverable and reusable, with explicit links to original publications for traceability.