# Future flows and Groundwater Levels - SC090016

- Purpose and scope
  - Provides datasets and products to assess climate change impacts on river flow and groundwater across Great Britain within a nationally consistent framework.
  - Enables policy scrutiny, monitoring, and informing future decisions through multiple realizations of climate outcomes and their hydrological consequences.

- Key datasets and products
  - Future Flows Climate (FF-HadRM3-PPE): 11-member ensemble of 1-km gridded precipitation and potential evapotranspiration time series (1951–2098) derived from HadRM3-PPE for GB.
  - Future Flows Hydrology (FF-HydMod-CatID): 11-member ensemble of daily river flow time series and monthly groundwater levels for 282 river sites and 24 boreholes.
  - 11-member ensemble of daily catchment-average precipitation and evaporation time series for the same 282 sites and 24 boreholes (derived from Future Flows Climate).
  - National maps of changes in river flow statistics (mean monthly flows, low-flow statistics) for most large GB rivers.
  - Regional maps of changes in groundwater levels and river flow statistics for one region.
  - Briefing notes for decision-makers (interpretation guidance and use recommendations).

- Access, licensing and citation
  - Data hosted via dedicated web pages and CEH/BGS gateways; licensing conditioned on use (non-commercial free; commercial may incur fees).
  - Datasets associated with DOIs and require full citation:
    - FF Climate DOI: 10.5285/bad1514f-119e-44a4-8e1e-442735bb9797
    - FF Hydrology DOI: 10.5285/f3723162-4fed-4d9d-92c6-dd17412fa37b
  - Access points include CEH Gateway, National River Flow Archive (NRFA), and British Geological Survey (BGS) websites.

- Data content and formats
  - Climate time series produced at 1-km resolution (downscaled and bias-corrected from 25-km HadRM3-PPE) and provided as NetCDF files.
  - Available precipitation (APr) time series derived from bias-corrected precipitation inputs; temperature downscaled for internal use (not public).
  - Potential evapotranspiration (PE) time series calculated at 1-km using FAO56 Penman-Montieth method; provided as NetCDF/PE files.
  - Hydrology and groundwater time series (FF-HydMod-CatID) supplied as CSV files (one per ensemble member) for 282 river sites and 24 boreholes.
  - Regional maps (PNG) and gridded groundwater changes (ASCII .asc) available for selected regions.
  - Briefing notes distributed with data packages and on project site.

- Methodology and data quality
  - Downscaling and bias correction align HadRM3-PPE outputs with observed historical patterns to improve hydrological relevance.
  - Snow processes accounted with elevation-dependent snowmelt model; available precipitation (APr) used as hydrological input.
  - Ensemble approach (11 members) designed to capture climate variability under the UKCP09 A1B scenario; not a replica of historical weather sequences.
  - Limitations acknowledged: grid resolution (25-km intermediate; 1-km final), non-physically based bias correction, potential disparities in precipitation partitioning between rain and snow with warming, and inherent uncertainties in downscaling.

- Hydrological modelling approaches
  - Use of lumped (PDM, CERF, BGS) and distributed (CLASSIC and ZOOM) groundwater/hydrology models.
  - Lumped models rely on catchment-averaged inputs (APr and PE); distributed models require model-specific gridded inputs, with climate data extractable as needed.
  - For lumped models, catchment-average time series are provided; for distributed models, climate inputs are available for extraction as required.

- How this supports monitoring frameworks
  - Standardized, nationally coherent dataset suite enables cross-location comparability and consistent policy evaluation.
  - Provides both time series and spatial depiction (maps) of potential climate-driven changes, supporting scenario planning and adaptive management.
  - Facilitates assessment of climate variability and range of possible futures through 11 ensemble realizations, rather than single projections.
  - Includes decision-maker briefing notes to aid interpretation and application of results in policy and management contexts.
  - Emphasizes data governance, open availability where possible, and clear citation to support transparency and reproducibility.

- End-user guidance and considerations
  - Appropriate for assessing impacts on water resources, fisheries, freshwater ecology, and overall water availability under climate change.
  - Useful for identifying data gaps, comparing regional responses, and communicating uncertainties to stakeholders.
  - Users should reference DOIs, adhere to licensing terms, and consult briefing notes for interpretation and recommended usage.

- Summary of end-to-end coverage
  - Background and aims, detailed data sets, methods, access and acknowledgement, ensemble climate time series, catchment and river flow outputs, groundwater maps, regional outputs, briefing notes, and references.