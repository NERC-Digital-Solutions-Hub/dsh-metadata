# Post Chernobyl surveys of radiocaesium in soil, vegetation, wildlife and fungi in Great Britain

## Overview
- Documentation of environmental radiocaesium assessment across Great Britain following the Chernobyl incident.
- Datasets capture radiocaesium (primarily Cs-134 and Cs-137) in soil, vegetation, wildlife, and fungi collected from 1986 to 1997.
- Data are intended to inform environmental health monitoring, uptake pathways, and policy decisions.

## Scope of the datasets
- Environmental compartments covered:
  - Soil (top 0–4 cm and below 4 cm)
  - Vegetation (grass/graminaceous plants; including heather, bracken, litter)
  - Wildlife (rabbit, hare, fox, red deer, woodcock, grouse)
  - Fungi (various species)
- Radionuclides measured:
  - Cesium-134 and Cesium-137 (primary focus; activity per unit dry weight or per square metre)
  - Other measurements include K-40, Ru-103, Ru-106, Pu isotopes; activity units include Bq/kg dry weight and Bq/m2
- Data organization:
  - Datasets include detailed field and laboratory measurements with metadata fields (e.g., site codes, sampling dates, specimen types, depths, etc.)
  - Some fields show data quality indicators (e.g., below minimum detectable activity, not analysed)

## Sampling design and compartments
- Field sampling approaches:
  - Vegetation: grassy/graminaceous plants clipped from plots, away from roadsides and overhanging vegetation
  - Wildlife: tissue samples (flesh, gut contents) from various species; stomach/rumen contents collected where applicable
  - Soil: soil cores or blocks from sampling plots, with depth segmentation and horizon notes
- Laboratory analysis:
  - Gamma spectrometry using high-purity Ge detectors
  - Calibration against British Calibration Service standards; decay corrections applied to sampling date
  - Measurements reported as activity concentrations (Bq/kg dry weight for biota/soil; Bq/m2 for deposits)
- Metadata collected:
  - Site and sample identifiers (CEH/ITE codes), latitude/longitude, habitat type, sampling dates
  - Soil properties (pH, texture, LOI, bulk density), vegetation metrics (dry weight), and other contextual variables
- Quality and lineage:
  - QA procedures described (calibration, standards, decay correction)
  - Data may include qualifiers such as MDA (minimum detectable activity), n/a, or notes indicating not analysed

## Data structure and metadata
- File format and labeling:
  - Multiple CSV datasets (e.g., soil, vegetation, animal, fungi data) with extensive column head metadata
  - Columns include: CEH_Code, Site_name, Latitude, Longitude, Location, Sampling_date, Depth, Soil_classification, Soil_pH, Soil_texture, Bulk_density, Veg_kg_DM, Cs134_bqkg_DM_lower, Cs137_bqkg_DM_upper, Cs134_Deposit_Bqm2, Cs137_Veg_Bqm2, 134Cs_0-4cm_soil_bqkg, 137Cs_0-4cm_soil_m, and numerous related fields
- Data provenance and standards:
  - Datasets are sourced from Chaplow et al. (2015) and archived via the NERC Environmental Information Data Centre (EIDC)
  - Measurements standardized to be comparable across compartments and years
- Data quality indicators:
  - Fields reflect data completeness and quality indicators (e.g., MDA denotes below detectable levels; notes indicate “Not analysed,” “Not applicable,” or replication details)

## Temporal and spatial coverage
- Temporal scope:
  - 1986–1987 surveys (soil, vegetation, wildlife)
  - 1989–1990 surveys
  - 1992 surveys
  - 1994–1997 surveys focusing on fungi
- Spatial scope:
  - Great Britain-wide coverage with site-level coordinates and habitat context
  - Data include farm-level groupings and site descriptors

## Key variables and outputs for monitoring frameworks
- Concentration and deposition metrics:
  - Cs-134 and Cs-137 activity concentrations in soil and vegetation
  - Total Cs-134 and Cs-137 deposits per square metre
  - Vegetation and soil Cs concentrations reported in dry weight (Bq/kg DM) or per area (Bq/m2)
- Transfer and uptake indicators:
  - Uptake measurements in wildlife tissues and gut contents
  - Depth-specific soil measurements (0–4 cm vs below 4 cm) to assess vertical distribution
- Supporting context variables:
  - Habitat type, soil classification, pH, texture, LOI, bulk density
  - Sampling dates, geographic location, site identifiers, and project/replicate metadata
- Data governance cues:
  - Emphasis on data openness, clear data lineage, and the need for robust metadata to enable reuse in policy evaluation

## Implications for monitoring frameworks and policy
- Demonstrates end-to-end data flow:
  - Field sampling across multiple environmental compartments
  - Laboratory analysis with QA and calibration
  - Rich metadata enabling cross-component linkage and trend analysis
  - Reporting and data sharing through public repositories
- Highlights key requirements:
  - Standardized units and depths for comparability across time and space
  - Comprehensive metadata to verify data suitability for policy use
  - Data governance practices to address data sharing barriers and ensure up-to-date datasets
- Policy-relevant insights:
  - Multi-compartment contamination data support assessment of exposure pathways and ecosystem transfer
  - Longitudinal datasets enable monitoring of temporal trends post-Chernobyl
  - Documentation of data limitations (e.g., incomplete fields, MDAs) informs interpretation and future monitoring design

## Challenges and considerations for policy-oriented monitoring
- Data availability and access:
  - Potential barriers related to data sharing, metadata completeness, and organizational silos
- Metadata adequacy:
  - Some fields require clarification or transformation to ensure reuse across programs
- Data transformation:
  - Variation in units and measurement depths necessitates careful standardization for policy reporting
- Governance and openness:
  - Need for transparent data governance to ensure datasets are stored, shared, and kept up to date by at-source standards

## Relevance to monitoring framework design
- Serves as a comprehensive example of multi-environment radiological monitoring data from field to repository
- Illustrates the importance of:
  - Clear sampling design and compartment definitions
  - Standardized measurement protocols and QA
  - Rich, machine-readable metadata to enable policy analysis and comparability
  - Open data practices and governance to maximise policy impact and reuse