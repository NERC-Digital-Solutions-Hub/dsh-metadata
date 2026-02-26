Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sediment stability by Cohesive Strength Meter (CSM) in salt marsh and mud flat habitats

## Overview
- Dataset measuring surface sediment stability using a Cohesive Strength Meter (CSM).
- Sampling across 22 CBESS quadrats at multiple sites, including salt marsh and adjacent mudflats.
- Sites located in Essex (south-east England) and Morecambe Bay (west England); samples collected in winter and summer 2013 (and across multiple seasons for Essex).
- Lead staff: David M. Paterson.

## Study design and locations
- Sites and habitats:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) — heavily grazed by Brent geese.
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP) — grazed by pink-footed geese or lightly grazed.
  - Habitats include saltmarsh and mudflat; Essex mudflats are more erosive, Morecambe Bay mudflats more depositional.
- Spatial details:
  - Each CBESS site includes a salt marsh and a mudflat with three sampling locations per site.
  - Precise sample locations and site coordinates are documented.

## Instrumentation and measurement method
- Instrument: Cohesive Strength Meter (CSM) to determine sediment erosion threshold via a controlled water jet.
- Procedure:
  - The CSM delivers a series of jets; resistance to erosion is inferred from changes in light transmission within a test chamber.
  - Measurements are recorded for each jet pulse; results are converted to stagnation pressure (Nm^-2) to quantify sediment stability.
- Calibration:
  - Machines vary in efficiency; calibration based on jet volume rather than firing pressure to ensure comparability.
  - Calibration process involves weighing jets, plotting jet output against firing pressure, and deriving a calibration equation for each CSM.
  - Critical erosion threshold defined as a 10% drop in light transmission; results expressed as stagnation pressure using the machine-specific calibration.
- Data processing:
  - Transform raw jet data into stagnation pressure; remove anomalous jets (timing errors) before calibration.
  - QA steps include checking for outliers, re-running data where needed, and documenting replicates.

## Data and metadata
- Variables observed: sediment stability (erosion threshold) as measured by CSM.
- Data formats and structure:
  - Data stored as CSV files with defined headers and fields (site, location, habitat, quadrat number, season, replicate details, etc.).
  - Dataset fields include replicate measurements, mean and standard deviation of stagnation pressure, and metadata descriptors.
- Documentation and provenance:
  - Detailed metadata descriptions accompany the dataset, including site names, habitats, quadrat numbers, seasonal timing, and measurement procedures.
  - Original data are linked to calibration and QA procedures for traceability.

## Data quality, sharing, and governance
- Quality assurance:
  - Calibration every six months; monitor for performance changes; re-calibrate if campaigns require precise results.
  - QA includes data checks for mathematical consistency, outlier assessment, and re-runs for validation.
- Data sharing and openness:
  - Data are documented with thorough metadata; standardization across machines is addressed via calibration.
  - Potential barriers include ensuring datasets meet governance standards and enabling public sharing of underlying data.
- Data management notes:
  - Metadata completeness and the ability to verify dataset suitability are emphasized.
  - Data transformations and formats (CSV) are specified to support interoperability.

## Temporal and ecological context
- Temporal coverage:
  - Winter and summer sampling in 2013 for Essex and Morecambe Bay; seasonality captured to reflect sediment dynamics.
- Ecological context:
  - Grazing regimes and inundation characteristics differ between Essex and Morecambe Bay, influencing sediment stability and erosion thresholds.
  - Differences in mudflat composition (sand content) and coastal dynamics between sites are acknowledged.

## Relevance for monitoring frameworks and policy
- What it provides:
  - A quantitative, replicable measure of sediment stability across contrasting coastal habitats, useful for erosion risk assessments and habitat management decisions.
- Policy and governance implications:
  - Highlights the importance of machine calibration, metadata, and data governance to ensure comparability and reliability for monitoring frameworks.
  - Demonstrates potential data-sharing barriers and the need for standardized metadata to support multi-site comparisons.
  - Supports evidence-based decisions on coastal protection, restoration, and grazing management by linking habitat condition to erosion risk metrics.

## Challenges and considerations for implementation
- Data compatibility:
  - Variation between CSM machines requires robust calibration to enable cross-site comparability.
- Metadata and accessibility:
  - Comprehensive metadata is essential to verify data suitability and enable reuse; public sharing requires governance controls.
- Gaps and accessibility:
  - Seasonal coverage and site-specific environmental factors must be considered when extrapolating findings to broader policy contexts.
- Data governance:
  - Clear processes for data storage, sharing, and updating are necessary to maintain data quality over time.