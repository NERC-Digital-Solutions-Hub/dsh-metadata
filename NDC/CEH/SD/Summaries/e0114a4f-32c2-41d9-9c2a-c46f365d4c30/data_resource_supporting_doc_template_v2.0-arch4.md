# Emissions of Ammonia (NH 3 ) from Agriculture in South Asia in 2015.

## Overview
- Global and regional emission dataset for gaseous ammonia (NH3) from agricultural sources in SAARC for the year 2015.
- Purpose: to better represent NH3 emissions in South Asia with regionally specific data, including sub-national fertiliser statistics.

## Data Specifications

- Spatial coverage and resolution
  - Region: SAARC countries (Afghanistan, Bangladesh, Bhutan, India, Maldives, Nepal, Pakistan, Sri Lanka)
  - Domain bounds: xmin 60.5°, xmax 97.4°, ymin -0.7°, ymax 38.5°
  - Grid: 0.1° × 0.1°
  - Coordinate system: WGS84
  - Non-domain cells set to NA

- Temporal coverage
  - Annual NH3 emissions for the year 2015
  - Data produced in 2022–2023

- File format and naming
  - GeoTIFF (.tif)
  - Example files:
    - NH3_CRB_SouthAsia_2015_gm2_0.1.tif (crop residue burning)
    - NH3_CRR_SouthAsia_2015_gm2_0.1.tif (crop residues left in fields)
    - NH3_GRM_SouthAsia_2015_gm2_0.1.tif (livestock grazing and manure applications)
    - NH3_MNM_SouthAsia_2015_gm2_0.1.tif (livestock management — housing, storage)
    - NH3_SFA_SouthAsia_2015_gm2_0.1.tif (synthetic fertilisers)

- Units and NA handling
  - Units: grams NH3 flux per square metre per year (g m^-2 yr^-1)
  - No-data values indicated as NA

## Data Model and Sub-sectors
- Five sub-sectors representing agriculture-related NH3 sources:
  - Crop residue burning (CRB)
  - Crop residues left in fields (CRR)
  - Livestock management (housing/storage/manure handling) (GRM)
  - Livestock grazing and manure applications (MNM)
  - Application of synthetic fertilisers (SFA)

## Methodology and Source Data

- Foundation: bottom-up calculations using activity data and emission factors.
- Core reference frameworks:
  - EDGAR v6.1 methodology
  - IPCC 2006 Guidelines and IPCC 2019 Refinement
  - EMEP/EEA air pollutant emission inventory guidebooks (2019, 2023)
- Region-specific data integration:
  - Sub-national fertiliser statistics
  - Crop surfaces reweighted to EarthStat and FAOSTAT national totals
- Sub-sector specifics:
  - CRB: burnt crop fractions by crop, with India-specific burnt crop set; emission factors (EFs) as mean of multiple MCE values
  - CRR: emissions from crops left in field, EF determined by above-ground dry matter N-content
  - GRM and MNM: N-flow approach using excretion rates, management-stage losses, and distribution over country-level livestock data
  - SFA: NH3 from fertiliser application, distribution of total N application across crops, EF per fertiliser type, soil pH effects

## Input Data and Data Provenance
- Inputs include: crop distributions, FAOSTAT crop totals, region-specific crop and fertiliser data, livestock populations and management practices, nitrogen content, and soil data.
- Comprehensive references and data sources listed (FAOSTAT, EarthStat, IPCC guidelines, EDGAR, EEA guidebooks, and numerous cited studies).

## Quality Control and Validation
- Checks for extreme values and NA locations.
- Calculated sectoral totals and sense-checked against non-spatial calculations.
- Spatial distributions validated against original (non-spatial) estimates and compared with other NH3 agriculture estimates.

## Access, Discoverability, and Metadata
- GeoTIFF format with clearly named files enabling sub-sector access.
- Clear documentation of input data sources, methodologies, and regional scope.
- Spatial and temporal metadata embedded via file naming conventions and accompanying methodological notes.

## Governance and Stewardship for Data Leaders

- Data system thinking
  - Provides a region-specific NH3 emission dataset aligned with international methodologies, enabling integration with broader emissions inventories.
- Data quality and usability
  - Transparent bottom-up approach with detailed input data provenance and QA steps.
- Metadata and discoverability
  - Consistent file naming and documentation facilitate discoverability and reuse across partner networks.
- Sustainability and updates
  - While current release is for 2015, framework supports updating with newer years and regional refinements as data become available.
- Collaboration and community alignment
  - Uses widely adopted methods (EDGAR, IPCC, EMEP/EEA) to support interoperability with other datasets and governance networks.

## Use Cases and Value for Data Strategy

- Policy and planning
  - Supports assessment of NH3 emissions from agriculture in South Asia to inform air quality and environmental policy.
- Data integration
  - Can be combined with other pollutant inventories (e.g., NOx, PM) for comprehensive atmospheric modelling.
- Sectoral insights
  - Differentiates emissions by agricultural practices (burning, field residues, livestock, fertiliser use) enabling targeted mitigation strategies.
- Gap analysis and coordination
  - Highlights data gaps at finer granularities (e.g., sub-national granularity for certain sectors) and opportunities for cross-country data harmonization.

## Challenges and Gaps Relevant to Data Leaders

- Data granularity and gaps
  - Sub-national fertiliser usage and crop data may be unevenly available; fragmentation across sources can hinder rapid overview of available data.
- Access barriers
  - While not explicitly noted here, some inputs (e.g., certain fertiliser details or management practices) may be difficult to obtain or verify across all SAARC countries.
- Metadata depth
  - While methodology is detailed, ongoing stewardship would benefit from machine-readable metadata and a centralized data catalog for easier discovery and governance.
- Data standardization
  - Potential need for harmonizing sector definitions and emission factors across national datasets to maintain consistency with EDGAR and IPCC frameworks.