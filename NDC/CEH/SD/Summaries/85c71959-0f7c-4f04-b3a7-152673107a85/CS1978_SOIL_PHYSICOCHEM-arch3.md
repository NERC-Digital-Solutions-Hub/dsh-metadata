# Soil physico-chemical properties 1978 [Countryside Survey], Great Britain Version: 1: 02-6-2016

- A historical dataset from the Countryside Survey (Great Britain) capturing soil physico-chemical properties observed in 1978.
- Provides measurements for pH and loss on ignition (LOI) across up to 256 1-km squares (1197 plots) in the top 15 cm of soil.
- Includes derived soil carbon indicators and land classification context to support environmental health monitoring.

## Data content and structure

- Dataset file: CS1978_SOIL_PHYSICOCHEM.csv
- Key variables (columns):
  - SQUARE: 1-km square sampling site code
  - PLOT: Plot identifier within each square
  - YEAR: Survey year (1978)
  - PH: Soil pH (measured in water)
  - LOI: Loss on ignition percentage
  - C_CONC_LOI: Carbon concentration calculated from LOI (g/kg), using 0.55 × LOI
  - C_STOCK_LOI: Carbon stock calculated from LOI (t/ha), using 0.55 × LOI
  - LC07: ITE Land Class 2007 description
  - LC07_NUM: Numeric code for LC07
  - COUNTRY: England (ENG), Scotland (SCO), or Wales (WAL)
  - COUNTY07: County or equivalent area
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Dataset scope: 1197 soil plots across 256 1-km squares, sampling top 15 cm of soil in 1978.

## Measurement methods

- LOI methods:
  - 10 g soil samples (top 15 cm) dried at 375°C for 16 hours
  - 1 g sub-sample combusted at 550°C for 3 hours
  - LOI (%) calculated from weight loss
  - Conversion to soil carbon concentration uses a bespoke factor: 0.55 (replacing the earlier 0.5 value used in CS initially)
- Soil pH methods:
  - pH measured in a suspension of de-ionised water
  - Sample: 10 g soil with 25 ml de-ionised water (soil:water ratio 1:2.5)
  - Shake, rest 30 minutes, read pH after a further 30 seconds
- Data provenance and lineage:
  - LOI method and pH method are based on established laboratory procedures (references provided in the documentation)

## Derived metrics and data use

- Derived carbon metrics:
  - C_CONC_LOI represents soil carbon concentration (g/kg) derived from LOI using 0.55×LOI
  - C_STOCK_LOI represents soil carbon stock (t/ha) derived similarly
- Contextual data:
  - Land classification (LC07 and LC07_NUM) provides land-use context
  - Country, county, and environmental zone descriptors (EZ_DESC_07) offer geographic and policy-relevant framing

## Data governance, usage, and access

- Acknowledgement and rights:
  - All use of Countryside Survey data must be acknowledged
  - Acknowledgement text required: “Countryside Survey data owned by NERC - Centre for Ecology and Hydrology” with copyright notes
- Data sharing and openness:
  - Data usage is tied to public acknowledgement and rights held by NERC CEH; public sharing of datasets is expected but subject to attribution requirements
- Data quality and metadata:
  - The documentation notes the use of a bespoke conversion factor for carbon calculations
  - Data structure includes explicit column definitions and survey year, enabling traceability
  - Metadata completeness is essential for verifying suitability for monitoring frameworks

## References and resources

- Countryside Survey methodologies and soil reports (2007 data lineage and technical reports cited)
- Key sources for LOI and pH methods and land classification references:
  - ITE Merlewood Land Classification of Great Britain (Bunce et al.)
  - Countryside Survey: Soils Report from 2007 (CS Technical Report)
  - Soil survey laboratory methods (Avery & Bascomb)
- Links and DOIs provided in the dataset documentation for deeper methodological and historical context

## Relevance for monitoring frameworks

- Provides baseline soil health indicators (pH, LOI-derived carbon concentration and stock) across Great Britain from 1978
- Supports long-term environmental health monitoring by enabling comparisons with later CS iterations (e.g., 1998, 2007) through consistent or transparently adjusted carbon conversion
- Geographic and environmental context (LC07, country, county, EZ) aids in segmentation of monitoring outcomes by land class and administrative region
- Emphasizes data governance requirements (acknowledgement, data rights) that are critical for reproducibility and stakeholder trust in monitoring outputs