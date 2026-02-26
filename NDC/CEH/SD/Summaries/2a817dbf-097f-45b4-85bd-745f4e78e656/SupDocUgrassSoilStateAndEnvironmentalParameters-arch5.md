# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands: Soil state and environmental parameters across geo linked sampling locations

## Executive summary
- Dataset of soil state and environmental parameters from 32 UK grassland sites, spanning paired intensive and extensive management and contrasting low/high pH parent soils.
- Winter and spring 2015–2016 sampling; cores collected along a 100 m land-use interface with five paired replicates per site.
- Subsamples analyzed for total nitrogen, total carbon, total organic carbon, total phosphorus, soil pH, soil moisture, loss on ignition, sand/silt/clay texture, FT-IR spectra, and bulk density.
- Stored frozen at -20°C prior to processing; analyses conducted across multiple CEH laboratories and collaborators.
- Data compiled into an Excel workbook and exported as a CSV for deposition into the EIDC data repository.
- Project context: part of the NERC U-GRASS Soil Security Programme, addressing soil biodiversity, biogeochemical processes, and soil ecosystem services under varying management and climatic scenarios.

## Project context and provenance
- Project: U-GRASS – Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands.
- Authors and institutions: Griffiths, R.I.; Puissant, J.; Dos Santos Pereira, G.; Goodall, T.I. (Centre for Ecology & Hydrology, UK; multiple CEH sites).
- Funding and program: NERC Soil Security Programme, NE/M017125/1.
- Data lineage:
  - Soil samples collected from 32 UK grassland sites; stored frozen at -20°C prior to analysis.
  - Analyses performed for chemical, physical, molecular, and functional characteristics at designated CEH labs (Lancaster, Wallingford) and NRMs; results compiled into Excel and exported as CSV for EIDC deposition.

## Protocols and sampling design
- 2.1 Soil sampling: 32 sites with land-use contrast (low vs. high intensity). Soil cores (15x5 cm) collected along 100 m interface at 25 m intervals, 5 paired replicates per site; sampling Nov 2015–Feb 2016; cores stored at -20°C.
- 2.2 Total Nitrogen, total Carbon, total organic Carbon: measured by oxidation and detection (Elementar Vario EL) after ball milling and oven-drying; decarbonated samples for total organic C.
- 2.3 Total Phosphorus (P): H2O2/H2SO4 digestion, selenium/lithium sulfate, colorimetric analysis on a SEAL discrete analyser; molybdenum blue complex measured at 880 nm.
- 2.4 Soil pH: measured in deionised water (25 mL water to 10 g soil) with pH electrode after equilibration.
- 2.5 Soil moisture and Loss on ignition (LOI): LOI as proxy for organic matter; moisture by drying at 105°C; LOI by combustion at 375°C.
- 2.6 Sand, silt, clay and texture: texture analysis by NRMs; percentages sum to 100%.
- 2.7 FT-IR spectra: mid-IR MIR-ATR on dried, milled samples; spectral regions used to estimate clay bonds, saturated carbon, and carbonate content.
- 2.8 Bulk Density: derived from core weight and volume, corrected for moisture and stone volume.
- Data collection spanned multiple laboratories and instruments; detailed methods ensure traceability to specific analyses.

## Data structure and content
- 3. Data Structure: single flat CSV file.
- 450 data rows, 19 columns.
- Key fields:
  - id: unique dataset row identifier
  - latitude, longitude: GPS coordinates (described as X/Y)
  - organic_C, total_C, total_N: percent mass measurements
  - total_P: mg/kg
  - pH: soil pH in water
  - soil_moisture, LOI: percent moisture and organic matter by LOI
  - sand, silt, clay: soil texture percentages
  - FT-IR related fields: clay1_IR, clay2_IR, clay_quality_IR, sat_C_IR, calc_IR (areas under specific FT-IR peaks)
  - bulk_density: g/cm3
- NA indicates missing data.
- Data descriptors align units and descriptions with each field (e.g., percent, mg/kg, pH units).

## Associated files and data access
- Analysis outputs: UgrassSoilStateAndEnvironmentalParameters.csv
- Data deposition: designed for deposition into the EIDC data repository, enabling discovery and reuse.
- Data scope supports cross-site comparisons of soil state and environmental parameters under different management regimes.

## Data governance and stewardship considerations
- Provenance and versioning: traceable processing chain from field sampling to lab analyses to CSV deposition; potential for re-use with proper citation of methods and authors.
- Metadata and interoperability: consistent field naming and units; requires a thorough data dictionary and methods metadata to ensure cross-dataset compatibility.
- Data quality: multi-lab analyses and diverse measurement techniques; explicit QA/QC steps are described in methods, but explicit QA metrics or data validation notes are not detailed in the summary—would benefit from a dedicated quality flag schema.
- Data availability and limitations: dataset includes precise geolocation and multiple derived measures; consider disclosure limitations or embargo settings if sharing site-level coordinates publicly.
- Update and maintenance: dataset captures a specific time window (2015–2016); future updates would need clear versioning and change logs to maintain dataset integrity.
- Accessibility for Data Stewards: well-structured protocol details, clear variable definitions, and explicit data lineage support discoverability, reproducibility, and governance.

## Potential use cases for data stewards
- Ensure consistent metadata and data dictionaries accompany the CSV for discoverability.
- Maintain provenance links to protocols and laboratories for auditability.
- Facilitate data integration with other soil datasets by aligning units and descriptors.
- Monitor data quality and completeness (e.g., flagged missing values in FT-IR fields or bulk density).
- Manage licensing, access controls, and embargo guidelines if needed for geographic-sensitive data.