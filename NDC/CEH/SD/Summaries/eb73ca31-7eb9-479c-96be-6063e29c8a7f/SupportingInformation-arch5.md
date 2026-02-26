# Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution

## Overview
- Comprehensive modelling study of diffuse rural pollution in Scotland, linking an evidence base with process-based models to assess current and future policy measures (e.g., DP GBRs) against Water Framework Directive objectives.
- Produces spatially explicit emissions by pollutant, sector, source, and delivery pathway; compares against monitoring data and official inventories; supports scenario analysis for policy planning.

## Data landscape and inputs
- Spatial framework and reporting units
  - ~3,300 inland river water bodies and ~15,400 coastal water bodies; results disaggregated by representative farm type and land cover; typical catchment ~20 km2.
- Climate, soils, and landscape
  - Climate surfaces (1961–1990), rainfall/temperatures/rain days at 5x5 km2; soils from James Hutton Institute (dominant textures by 1 km2).
  - Enhanced connectivity framework capturing within-field and slope-to-channel losses; boundary features influence pollutant delivery.
- Land cover and farm structure
  - Land-cover data from Ordnance Survey Strategi and 2010 June Agricultural Census; nine Robust Farm Types (RFT) created from land use and livestock patterns.
- Farm management and material flows
  - Crop yields, fertiliser practices, manure management, and calendars; management workbooks documenting assumptions for transparency.
- Data governance and restrictions
  - Some mitigation-action descriptions withheld for sensitivity; farm-level data licensed; farm management workbooks included in appendices but not fully public; data licensing considerations for census inputs.

## Modelling framework and data architecture
- Core modelling approach
  - Meta-model of export coefficients derived from detailed process-based models to estimate diffuse pollutant emissions by representative farm types, incorporating local soil and climate drivers.
  - Spatially explicit outputs linked to a common coordinate system by source type, area, and delivery pathway.
- Source apportionment and framework
  - Policy measures mapped to auditable mitigation actions (e.g., manure heap relocation, riparian fencing, timing adjustments).
  - For each source area, actions have defined effectiveness; efficiencies constrained by local factors; emissions from actions combined to yield net reductions.
- Farm-to-catchment integration
  - Framework Model couples farm outputs with spatial databases of crop areas, livestock, and inputs for each water body; scenario analyses model different uptake levels.
  - Mitigation-action database records action targets and effectiveness.
- Outputs and reporting
  - Emissions by pollutant, farm type, source area, and delivery pathway; supports interrogation by coordinates and action.
  - Validation through Harmonised Monitoring Scheme data; accounts for non-agricultural sources (urban, septic tanks, bank erosion).
  - Outputs feed into river-flow and in-channel retention models and WFD chemical thresholds to project ecological status under realistic uptake scenarios.

## Verification, uncertainty, and data governance
- Verification data sources
  - OSPAR-COM measurements (nitrate, phosphorus, suspended solids) with adjustments for organic content to compare to mineral sediment in the model.
  - In-channel retention models (Behrendt & Optiz, 2000; Vanoni, 1975) to align modeled delivery with observed outputs.
  - Faecal indicator organisms (FIO) comparisons with Kay et al. (2008) and Tetzlaff et al. (2012) for Dee and North Esk catchments.
- Uncertainty and interpretation
  - Acknowledge uncertainties in emission factors and coefficients; emphasis on relative changes due to mitigation actions rather than absolute fidelity.
  - Differences with official inventories (e.g., indirect N2O via leaching) attributed to methodological choices (FracLeach) and inclusion of compaction/poaching effects.
- Data governance and stewardship
  - Restricted disclosure of certain mitigation-action descriptions; licensing constraints on census and farm data; careful handling of sensitive inputs in repositories.
  - Emphasizes robust provenance, metadata, and data lineage to support reproducibility and policy evaluation.

## Outputs and implications for data management
- Policy-relevant results
  - National emissions by pollutant with sectoral contributions (e.g., agriculture as major source for nitrate, phosphorus, sediment; STWs and urban sources for FIOs).
  - Spatial and farm-type breakdowns show which land uses and management practices drive emissions; detailed apportionment by source area, pathway, and form (e.g., soil, fertiliser, grazing, surface runoff).
  - Agri-environment and mitigation scenarios illustrate potential reductions under different uptake levels.
- Data products and traceability
  - Large, diverse datasets (climate, soils, land cover, census, farm management) integrated into a reproducible framework; requires clear metadata, provenance trails, and versioning.
  - Spatial alignment on 1 km2 grids and river/water body boundaries is essential for reproducibility and stakeholder trust.
  - Sensitive items (mitigation-action specifics) kept private with documented justification and controlled access.
- Practical data stewardship considerations
  - Documentation of data sources, coordinate systems, model inputs/outputs, and assumptions is critical for reproducibility and verification against monitoring data.
  - Excel-based workbooks provide transparency but should be complemented with machine-readable metadata and accessible data dictionaries.
  - Authority and licensing constraints necessitate explicit governance around sharing, access controls, and data curation practices.

## Data stewardship challenges and considerations
- Incomplete understanding of user needs and priorities
- Timely acquisition and standardization of data from multiple sources and formats
- Aligning diverse systems, databases, and formats (climate, soils, census, management records)
- Handling large, complex datasets with spatial and temporal detail
- Updating legacy or outdated databases with interoperable, shareable formats
- Balancing transparency with sensitivity for certain mitigation-action details

## Key datasets and provenance (highlights)
- Climate: 1961–1990 CRU/MET Office surfaces
- Soils: James Hutton Institute SSK1B
- Land cover: OS Strategi; 2010 JAC census data
- Farm structure: Nine Robust Farm Types; land use and livestock distributions
- Management: Crop yields, fertiliser patterns (BSFP 2010), manure practices
- Validation: HMS (hydrometric and pollutant monitoring data); OSPAR-COM measurements
- Retention models: Behrendt & Optiz (phosphorus and nitrate), Vanoni (sediment)
- Faecal indicators: Kay et al. (2008); Tetzlaff et al. (2012)
- Inventory benchmarks: Thistlethwaite et al. (2010) for greenhouse gases; IPCC-based methods with Scotland-specific adjustments