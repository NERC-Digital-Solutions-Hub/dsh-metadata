# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Eddy Covariance Flux Data for Abbotts Hall, Essex

## Overview
- Eddy covariance flux dataset focusing on Abbotts Hall, Essex, within the CBESS project.
- Provides half-hourly averaged flux and meteorological data collected between 15/12/2012 and 27/01/2015.

## Location and Site Context
- Location: Abbotts Hall, Essex (AH) at 51°47'9"N, 0°52'1"E.
- Site context: Salt marsh (Abbotts Hall) in Salcott Channel, part of a network of connected marshes; sheltered from certain wind directions with dendritic drainage and clay/organic sediments.

## Data Collected and Variables
- Fluxes and meteorological variables recorded, including:
  - Air temperature (T_air), soil temperatures at 10 cm, 20 cm, 30 cm (T_soil_10cm, T_soil_20cm, T_soil_30cm)
  - Relative humidity (RH), Vapour Pressure Deficit (VPD)
  - Net radiation (Net_rad), Photosynthetically active radiation (PAR)
  - Precipitation (Precip), Wind speed (Wind_Spd), Wind direction (Wind_Dir)
  - Latent energy (LE) and its filled value (LE_Filled), LE quality control (LE_QC)
  - CO2 flux (Fc), its filled value (Fc_Filled), CO2 flux QC (Fc_QC)
  - Sensible heat (H) and its filled value (H_Filled), H QC (H_QC)
  - Modelled respiration (Resp), u* friction velocity (ustar), Monin-Obukhov stability (MO)
- Temporal resolution: Fluxes at 10 Hz (via CSAT3A anemometer on a CS CPEC200 system) and other variables at 1/60 Hz (every minute) via CS CR1000 with multiplexer.
- Time reference: mean values at the middle of each half-hour bin (e.g., 00:15 for 00:00–00:30).

## Instrumentation and Data Collection
- Field system: Campbell Scientific CPEC200 Closed Path Eddy Covariance.
- Data logger: CS CR3000 for fluxes; CS CR1000 with multiplexer for other variables.
- Ancillary sensors: Vaisala HMP155A (air humidity/temperature), EM L ARG100 tipping bucket rain gauge, Kipp and Zonen NR Lite (net radiation), Skye Instruments SKP215 (PAR), CS 107 thermistors for soil temperatures.
- Data processing tools: EdiRe and Matlab for flux processing.
- Data are subject to corrections for frequency losses (WPL) and, for CO2 fluxes, storage terms.

## Data Processing, Quality Control, and Gap Handling
- Quality control: Flux QC flags based on diagnostic flags from gas analyser and anemometer; additional reality checks grouping fluxes into 15 radiation bins with outlier clipping (within-bin data beyond 3.5 SD flagged as QC=1 and beyond 5 SD as QC=2; data affected by tower wind shadow QC=3). QC=0 represents best data.
- Gap filling: Performed with the REddyProc R package using QC=0 data.
- Processing specifics: Fluxes corrected for frequency losses and WPL; CO2 fluxes also corrected for storage terms.
- Data quality and processing documentation are described in detail, with recording and binning methodologies explained.

## Gaps, Limitations, and Data Quality Notes
- Gaps occur due to sensor malfunctions or power loss to the system.
- Data flags provide an indicator of data quality; lower QC values signal higher confidence.
- Basic reality checks and model-based respiration are applied to nocturnal CO2 fluxes using Lloyd & Taylor 1994.

## Data Formats and Structure
- Primary data format: CSV.
- Metadata structure includes a comprehensive field description, with columns for Year, Month, Day, Hour, Minute, and a range of observed and modelled variables.
- Field descriptors include location, site, habitat, scale, and sensor readings, enabling reproducibility and interoperability.

## Dataset Field Descriptions and Coding
- Field-level details cover:
  - Temporal fields (Year, Month, Day, Hour, Minute)
  - Spatial/site fields (Site, Location, Habitat)
  - Measurements and units for each variable (e.g., T_air in °C, PAR in μmol m−2 s−1, Fc in μmol m−2 s−1)
  - Quality control flags for each flux (QC codes 0–3)
  - Modelled variables (Resp, u*, MO) and their corresponding labels
- The dataset uses descriptive header and row ordering to facilitate sorting and interpretation.

## Data Governance, Stewardship, and Access Considerations
- Responsibility: Data are associated with dedicated staff (e.g., Timothy Hill) and follow standardized QA/QC procedures.
- Sharing and dissemination: Datasets are uploaded to relevant portals and catalogues, with metadata and data lineage documented to support discovery and reuse.
- Updates and reproducibility: Processing steps (WPL corrections, gap filling, respiration modeling) are specified to enable replication and auditing of results.

## Key Takeaways for Data Stewards
- Ensure continued adherence to documented QC procedures, including per-bin radiation QC and shadowing considerations.
- Maintain complete metadata, including precise instrument configurations, temporal references, and processing steps (EdiRe/Matlab workflow, gap filling with REddyProc).
- Monitor and document data gaps, sensor health, and power supply reliability to support data governance and upgrade planning.
- Preserve CSV data format continuity and ensure header/field documentation remains synchronized with any schema changes.
- Facilitate discoverability by aligning portal uploads with existing CBESS data catalogs and providing clear provenance (staff responsible, site context, instrumentation, and processing methods).