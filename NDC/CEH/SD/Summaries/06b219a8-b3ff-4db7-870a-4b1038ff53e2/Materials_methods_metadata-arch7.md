# Materials and methods, and metadata for Global data for soil water, groundwater and riverine freshwater DO14C data taken from 'Linking soil solution and riverine DO14C to soil carbon turnover', Adams et al, 2019 Biogeochemistry.

## Overview
- Compiles global data on dissolved organic carbon (DOC) concentrations and DO14C (radiocarbon content) for soil water, groundwater, and riverine freshwater.
- Builds on literature datasets (soil solution DOC and DO14C 1989–2015; groundwater 1988–2008; river data extending 1962–2015, incorporating Marwick et al. 2015) with additional data to broaden temporal coverage.
- Includes new UK river-water measurements (2013–2015) to augment existing datasets.
- Data prepared for GIS-like use with location and environmental attributes to support analyses of soil carbon turnover.

## Data coverage and types
- Literature data for:
  - DOC concentration in soil solutions (DOC) and DO14C in soil water.
  - Groundwater DOC and DO14C.
  - Rivers: DO14C and DOC, with sampling dates spanning 1962–2015 (enhanced by post-Marwick data).
- New river surface-water measurements (TableS3_River_Surface_Water_New) from UK sampling campaigns (2013–2015).
- River data supplemented by archived samples from Norway and the US (1960s–1970s) with methods adapted for carbon isotope analyses.

## Data sources and data compilation
- Compilation derived from multiple literature sources; where needed, data digitized from graphs using Engauge Digitizer.
- River data assembled from Marwick et al. (2015) and expanded with additional published/unpublished data (PROTOS, PhD theses, etc.).
- Land-class and site information assigned from provided tables (e.g., TableS1_Soil_water_data.csv) and source references.

## Sampling, measurement, and laboratory methods
- New UK river sampling (2013–2015) conducted by CEH, JHI, and UEA with stringent sample handling:
  - New or acid-washed equipment; radiocarbon-tracer-free labs.
  - Filtration and sample preservation protocols with pre-cleaned bottles and filters.
  - DOC measurements via Vario EL and Thermo Flash elemental analysers.
- Radiocarbon (14C) analyses:
  - CO2 recovered from organic carbon, converted to graphite targets for AMS at SUERC (East Kilbride).
  - δ13C measured by dual-inlet mass spectrometry (Thermo Fisher Delta V) for 14C correction; in some samples δ13C = -25‰ VPDB used for correction when high δ13C suggested carbonate carryover.
  - Corrections applied to account for radioactive decay since 1950 (Stuiver and Polach standards).
  - Precision: ~0.45 pMC (1σ), with explicit reporting of measurement statistics and lab processing uncertainties.
  - Purging to remove inorganic carbon; select samples reanalyzed with lower pH to improve purge efficiency.
- Archived samples from Norway and the US processed with adapted purification and pre-treatment steps before combustion.

## Site information and metadata
- Land class assignment follows a defined scheme (TableS1_Soil_water_data.csv), with categories including:
  - Pure vegetation types (≥90% forest or wetland) vs. NSN (natural or semi-natural), F (forest-related) and W (wetland-related) etc.
  - Discharge data used for hypothesis testing only when quantified.
- Sampling site details include location, country, latitude, longitude, date, vegetation, land_class, soil type, sampling depth, and reference.
- For rivers, site-level data include site name, country/region, year, coordinates, [DOC] concentration, δ13C, Δ14C, land_class, and publication codes.

## Data attributes and CSV table structure
- TableS1_Soil_water_data.csv (Soil water data)
  - Key columns: Location, Country, lat, long, date_yr, vegetation, Land_class, soil, depth_cm, [DOC], 13C, delta14C, Reference, Notes.
- TableS2_Groundwater_data.csv (Groundwater data)
  - Key columns: Location, Country, lat, long, Date_yr, aquifer, [DOC], 13C, delta14C, Reference, Notes.
- TableS3_River_Surface_Water_New.csv (New UK river data)
  - Key columns: Data_line, Country_or_Region, Site, year, Lat, Long, [DOC]_mg/L, delta13C_‰, delta14C_‰, Land_class, Publication_code.
- TableS3_Marwick_River_Surface_Water.csv (Marwick et al. river data)
  - Data_line plus publication-specific columns for river surface-water DO14C, DOC, and related metadata.
- TableS3_Extra_Published_River_Surface_Water_Data.csv (Additional published river data)
  - Comprehensive set of river data with site, year, coordinates, [DOC]_mg/L, delta13C, delta14C, Land_class, References, and other notes.

## Data quality, standards, and integration
- Data quality relies on cross-study standardization attempts (e.g., consistent radiocarbon calibration, δ13C corrections, and decay adjustments).
- Data integrate multiple resolutions and methods (literature compilations, digitized graphed data, and new standardized UK measurements).
- Acknowledges potential inconsistencies due to disparate data sources, varying sampling schemes, and use of multiple reference materials.
- GIS-ready attributes include precise spatial coordinates, land-use classifications, and vegetation/soil context to support spatial analyses of soil-water–carbon turnover.

## GIS relevance and use cases
- Enables mapping and spatial analysis of DO14C and DOC distributions across soil, groundwater, and river systems.
- Facilitates linking soil carbon turnover estimates to hydrological pathways and land-use types.
- Supports provenance tracking of carbon through soil-to-river networks and assessment of carbon age (Δ14C) in freshwater systems.
- Useful for policy-relevant visuals and public-facing map products describing carbon dynamics in different landscapes.

## References and data provenance
- Core data originate from Adams et al., 2019 Biogeochemistry and related literature datasets (Buckingham 2008; Marwick et al. 2015; PROTOS project; numerous radiocarbon studies).
- Tables include explicit source citations and publication codes to trace data lineage and enable reproducibility.