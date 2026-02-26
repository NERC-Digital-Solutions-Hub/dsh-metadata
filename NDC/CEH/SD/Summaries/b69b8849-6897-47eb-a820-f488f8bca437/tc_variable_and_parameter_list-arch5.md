# PLOT-SCALE SIMULATIONS WITH MAIN-FRAME

- A comprehensive data dictionary for plot-scale simulations using a main-frame model.
- Contains extensive var lists across vegetation, soil biogeochemistry, hydrology, energy balance, and meteorological inputs/outputs.
- Distinguishes between input time series, assigned parameters, internal parameters, and derived/assigned outputs.
- Structured around per-Crown (per vegetation unit), per Plant Functional Type (PFT), and per-soil-layer scales, with numerous high-resolution time series (hourly, daily) and scalar parameters.

## Data architecture and key data types

- Time series data
  - Hourly and daily series for a wide range of state variables and fluxes (e.g., An_H, ANPP_H, NEE, NPP_H/L, LAI_H/L, N2flx, Rainfall, PAR, DQ, DT, SWE, etc.).
  - Many fields are labeled as per-C crown, per-vegetation type, or per-soil-layer, enabling fine-grained temporal tracking.
- Assigned and internal parameters
  - Assigned parameters (e.g., Aice, B_harv_H/L, CT_H/CT_L, Cbare, PFT_opt_H/L) define physical properties, vegetation structure, and optical/biogeochemical parameters.
  - Internal parameters (e.g., Bio_Zs, Damp_Zs, dampening factors, Ks_Zs, Osat) define soil-plant system properties not directly provided by external inputs.
- Input time series and environmental drivers
  - Time series inputs include Ca (CO2), Datam/Date, Lat/Lon, meteorological drivers (U, Ws, Pre, PARB, PARD, N, PAR), and other climate/atmospheric variables.
  - Depositions and fertilization inputs (DepN, DepP, DepK, FertN, FertP, FertK; Fertilization, Nitrogen/Phosphorus/Potassium deposition).
  - Hydrological and soil moisture drivers (Pr, PARB, PARD, Pre, esat/ea, RH, wind, humidity, DeltaGMT, Lat/Lon, Zbas).
- Per-structure and per-layer organization
  - Variables are organized across crowns, soil layers, and layers of plant/soil interactions (e.g., Rg_H/L growth respiration, RA_H/L autotrophic respiration, NPP, NEE, SAI_H/L, SL_H/L, Ws_under, Ks_Zs).

## Metadata, provenance, and data quality

- Clear data provenance signals
  - Distinctions among Input Time series, Assigned Parameter, Internal Parameter, and Output/Computed values.
  - Some fields are explicitly marked not active or not used (e.g., Jxl_H/L not active, Kleaf_H/L not active), signaling potential gaps or deprecated components.
- Units and documentation
  - Broadly SI units with descriptive labels, aiding cross-dataset interoperability.
  - Each variable includes a description and unit, supporting metadata completeness.
- Quality considerations
  - Several variables refer to mass balance checks (e.g., CK1, CK2 (wrong), CkC_ALL, CkC_H, CkC_L) used for numerical QA.
  - Presence of “wrong” or deprecated fields indicates need for versioned metadata and dataset lineage tracking.

## Data lifecycle, updates, and governance

- Lifecycle considerations
  - Large, complex data model spanning multiple harmonized components (vegetation, soils, energy/water fluxes, nutrients).
  - Frequent updates to time-series inputs and parameters necessitate robust version control and dataset lineage.
- Data governance implications
  - Data stewards should standardize naming, units, and metadata conventions across all variables.
  - Maintain a registry of active vs. inactive fields, with rationale and historical context.
  - Ensure reproducibility by recording model version, parameter sets, and input data sources alongside each simulation run.

## Accessibility, discoverability, and reuse

- Discoverability
  - Rich variable-level metadata supports targeted discovery (per crown, per PFT, per soil layer).
  - Time-series data enable re-use for calibration, validation, and scenario analysis.
- Reuse considerations
  - Document data provenance, modeling assumptions, and parameterization schemes to facilitate reuse in other plot-scale contexts.
  - Clearly separate inputs, parameters, and outputs to aid integration with other data management pipelines.

## Common challenges for Data Stewards

- Incomplete user needs and alignment
  - The model includes many specialized fields; ensure metadata captures intended use cases and user requirements.
- Data timeliness and interoperability
  - Heterogeneous time steps (hourly, daily) and multiple scales ( crown, soil layer) demand rigorous temporal alignment and harmonization.
- Metadata completeness and consistency
  - Not all fields are active; maintain an up-to-date inventory of active vs. deprecated fields with rationales.
- System heterogeneity and formats
  - Large, multi-block schema implies diverse data formats; enforce standardized schemas and mapping to common ontologies.
- Data volume and performance
  - Plot-scale simulations generate extensive time-series; plan for storage, indexing, and efficient retrieval.

## Governance recommendations for Data Stewards

- Establish a comprehensive data dictionary and dataset registry
  - Capture dataset name, version, author, modeling context, active fields, and deprecation history.
- Standardize metadata
  - Enforce consistent naming conventions, units, data types, and per-variable descriptions.
- Implement data provenance and lineage
  - Track source (input vs. parameter), versioned model, simulation runs, and any transformations applied.
- Enforce data quality controls
  - Leverage embedded QA signals (e.g., mass-balance checks) and document QA outcomes.
- Manage data lifecycle and access
  - Maintain a clear policy for updating inputs/parameters, with versioned releases and change logs.
- Promote interoperability and discoverability
  - Map variables to common ecological/modeling ontologies and ensure metadata supports cross-model reuse.
- Document usage constraints and activity flags
  - Clearly mark not-active fields, rationale for deprecation, and any caveats for users.