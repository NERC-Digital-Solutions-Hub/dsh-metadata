# Future flows and Groundwater Levels - SC090016

- Purpose and aim for monitoring frameworks
  - Provide a nationally consistent framework to assess climate change impacts on water availability, informing policy and adaptation decisions.
  - Deliver complementary products to monitor both river flows and groundwater levels across Great Britain over time.

- Datasets and products (key outputs for monitoring)
  - Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded daily climate time series (precipitation and potential evapotranspiration) for Great Britain, derived from HadRM3-PPE under UKCP09 scenarios.
  - Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow and monthly groundwater levels time series for 282 river sites and 24 boreholes, derived from FF Climate using hydrological/groundwater models (HydMod).
  - 11-member ensemble of daily catchment-averaged precipitation and PET time series for the same sites and boreholes (derived from FF Climate).
  - National maps of changes in river flow statistics (mean monthly flows, low-flow statistics) for most large rivers.
  - Regional maps of changes in groundwater level and river flow statistics for one region.
  - Briefing notes for decision-makers on how to use results.

- Access, licensing, and governance
  - All datasets and products are accessible via dedicated web pages under licensing arrangements.
  - Non-commercial use is free; commercial use may incur fees and requires agreement with licensing teams (CEH/BGS).
  - Data are cited with DOIs; usage requires proper reference.
  - Data hosted by CEH Environmental Informatics Data Centre Gateway and related project portals; access terms specified in licensing documents.

- Data processing, methods, and standards (implications for monitoring)
  - Climate data processing
    - HadRM3-PPE outputs at 25-km resolution are bias-corrected and spatially downscaled to 1-km to capture sub-grid heterogeneity and improve hydrological relevance.
    - Snow processes modeled with elevation-dependent snowmelt; available precipitation (APr) is produced as input to hydrological models.
    - Temperature downscaled to provide more realistic inputs; outputs provided as 1-km APr and PE products (NetCDF), designed for hydrological and groundwater modelling.
  - Available precipitation (APr) and PET
    - APr time series derived from bias-corrected, downscaled precipitation; PET computed with FAO56 Penman-Monteith at 5-km, downscaled to 1-km; PET outputs provided as 1-km data.
    - Large volumes of data (multiple files per ensemble member and period) due to ensemble approach.
  - Temporal and spatial scope
    - Climate time series span 1951–2098; climate outputs provided as ensemble realizations to capture variability.
  - Modelling approaches
    - Hydrology and groundwater levels produced using lumped (PDM, CERF, BGS) and (semi-)distributed (CLASSIC, ZOOM) models; input requirements differ by model type.
    - For lumped models, catchment-averaged APr and PE time series are provided to enable independent modelling or uncertainty analyses.
    - For distributed models, climate information is embedded in FF Climate; direct climate datasets may not be provided at the required resolution.
  - Outputs format and accessibility
    - FF Climate data: NetCDF; FF Hydrology data: CSV files per site with 11 ensemble members (and multiple models where applicable).
    - National river flow maps: PNG; regional groundwater maps: PNG (MABSWEC region) and ASCII grid (.asc) files for regional analyses.
    - Briefing notes accompanying datasets to aid interpretation and policy use.

- How the outputs support monitoring and policy evaluation
  - Provides consistent, comparable climate-to-hydrology linkages across Great Britain for policy evaluation and adaptation planning.
  - Enables examination of River Flow and Groundwater changes through 2050s and across six 30-year time slices, supporting long-term resource management.
  - Facilitates uncertainty analysis via 11-member ensemble realizations, improving assessment of risk and resilience planning.
  - Delivers decision-ready materials (maps, time series, briefing notes) to inform water management, ecology, fisheries, and other environmental health considerations.

- Practical considerations, caveats, and data governance
  - Bias-correction and downscaling are statistical (not physical) and may introduce discrepancies with real climate; results should be interpreted with uncertainty in mind.
  - Ensemble design captures climate variability but does not reproduce exact historical weather sequences; results emphasize patterns and ranges rather than precise historical analogues.
  - Large data volumes (e.g., tens of thousands of files and multi-gigabyte datasets) require robust data handling and storage practices.
  - Licensing and data-sharing constraints may affect immediate openness; ensure compliance with licensing terms when using the data for monitoring frameworks and publication.

- Use in future-proofing monitoring frameworks
  - Standardized, transparent methodology supports cross-location comparability and trend assessment over time.
  - Availability of both river flow and groundwater datasets enables integrated hydrology-ecology-water availability monitoring.
  - Briefing notes and documentation aid knowledge transfer to policymakers and non-technical stakeholders, supporting evidence-based decision-making.
  - Clear citation and licensing guidance enhances reproducibility and governance of environmental monitoring initiatives.