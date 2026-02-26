# Soil physico-chemical properties 1978 [Countryside Survey], Great Britain

## Overview
- Part of the Countryside Survey (Great Britain) 1978, documenting soil physico-chemical properties: pH and loss on ignition (LOI).
- Data cover up to 256 1km squares across Great Britain, with LOI and pH measurements from 1197 plots in the top 15 cm of soil.
- File and dataset are from the Countryside Survey, owned by NERC - Centre for Ecology & Hydrology.

## Data File and Columns
- Data file: CS1978_SOIL_PHYSICOCHEM.csv
- Key columns:
  - SQUARE: 1km square sampling site code (text)
  - PLOT: Plot identifier within each square (1–5) (number)
  - YEAR: Year of survey (number)
  - PH: Soil pH (number)
  - LOI: Loss on ignition percentage (number)
  - C_CONC_LOI: Carbon concentration from LOI (g/kg) using 0.55 x LOI
  - C_STOCK_LOI: Carbon stock from LOI (t/ha) using 0.55 x LOI
  - LC07: ITE Land Class 2007 (text)
  - LC07_NUM: ITE Land Class 2007 (numeric code)
  - COUNTRY: Country code (England ENG, Scotland SCO, Wales WAL)
  - COUNTY07: County or Council area
  - EZ_DESC_07: Countryside Survey Environmental Zone description (with link to documentation)

## Methods and Conventions
- LOI methods:
  - LOI measured on top 15 cm of soil from samples of 10 g soil (sieved to 2 mm).
  - Drying: 375°C for 16 hours; 1 g sub-sample combusted at 550°C for 3 hours.
  - LOI% used to estimate soil organic matter and soil carbon concentration.
  - Conversion to soil carbon concentration uses a factor of 0.55 (updated from 0.5 after 1998/2007 data analyses).
  - Carbon stock calculated from LOI with the 0.55 factor.
- Soil pH methods:
  - pH measured in a suspension of deionised water.
  - Procedure: 10 g field-moist soil + 25 ml deionised water (soil:water 1:2.5 by weight); stir, stand 30 minutes; read pH after 30 seconds.
  - pH measured in water following a method aligned with Soil Survey of England and Wales procedures.
- Samples and scope:
  - LOI values derived from 1197 plots across 256 1km squares, from the top 15 cm of soil.
- Land classification and references:
  - LC07 and LC07_NUM reference the ITE Land Classification (GB) framework (1996–2007) used for context.
  - EZ_DESC_07 provides environmental zone descriptions with related documentation.

## Data Quality, Provenance and Access
- Acknowledgement requirements:
  - All use of Countryside Survey data must be acknowledged.
  - Acknowledgement statement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © Database Right/Copyright NERC- CEH. All rights reserved.
- Ownership and rights:
  - Data owned by NERC - Centre for Ecology & Hydrology; rights reserved.
- Documentation and references are linked to external sources and publications to support methodologies and classifications.

## Usage Considerations for Data Leaders
- Data system perspective:
  - This dataset exemplifies structured, versioned, survey-based soil properties with derived carbon metrics (C_CONC_LOI, C_STOCK_LOI) and geospatial context (SQUARE, PLOT, COUNTRY, COUNTY07, LC07, EZ_DESC_07).
  - Metadata includes conversion factors and methodological details essential for reproducibility and auditing of carbon estimates.
- Discoverability and metadata:
  - Rich metadata in column definitions and cross-referenced classifications (ITE Land Classification, Environmental Zone) enhance discoverability and interoperability with other Countryside Survey outputs.
- Data gaps and governance:
  - Covers 1978 survey period for Great Britain; note potential gaps beyond the surveyed plots or years.
  - Clear acknowledgement requirements support governance and reuse in reports, analyses, and policy contexts.
- Practical considerations:
  - Carbon values depend on the 0.55 LOI-to-carbon conversion; users should be aware of historical updates to conversion factors (0.5 used previously; 0.55 used for CS estimates).
  - For policy or planning applications, linkage to LC07 and EZ_DESC_07 aids integration with land-use and habitat classifications.

## Publications and References
- Countryside Survey Website and technical reports (overview and methodologies).
- Emmett et al. 2010. Countryside Survey: Soils Report from 2007 (CS Technical Report No. 9/07).
- Bunce et al. various foundational documents on ITE Land Classification of Great Britain (1996, 1981) and related datasets (IZ Land Classification 2007).
- Avery and Bascomb (1974) Soil survey laboratory methods (Vol. 6).
- Carey et al. 2008. Countryside Survey: UK Results from 2007.
- DOIs and links provided for primary data centers and publications.