# Snow water equivalent estimates using cosmic-ray neutron sensors in the United Kingdom (2014-2019)

- Purpose and scope
  - Provides daily Snow Water Equivalent (SWE) estimates derived from cosmic-ray neutron sensors (CRNS) in the COSMOS-UK network.
  - Aims to deliver representative SWE for heterogeneous snowpacks using CRNS footprints (>100 m), complemented by SnowFox sensors, snowmelt-model outputs, depth-based estimates, albedo data, and associated uncertainties.
  - Covers data from 44 COSMOS-UK sites (initially 50, with 4 excluded due to forest cover and 2 lacking snow), up to 2019-08-22, comprising 263 snow events.

- Data content and structure
  - SWE estimates (daily mean) from multiple methods:
    - SWE_CRNS_1, SWE_CRNS_2, SWE_CRNS_3: from CRNS count-rate methods with three approaches to estimate snow-free count rate.
    - SWE_SNOWFOX_1, SWE_SNOWFOX_2, SWE_SNOWFOX_3: from buried SnowFox sensors, normalized by snow-free rate and attenuation curves.
    - SWE_MODEL: daily SWE from PACK snowmelt model using local air temperature and precipitation (with snow/rain classification by temperature threshold).
    - SWE_DEPTH: SWE derived from daily median snow depth (sonic sensor) converted with assumed fresh-snow density (0.1 g cm^-3); not reported when snow depth declines by more than 20% from its maximum.
  - Ancillary inputs and metadata:
    - CTS_CRNS: daily average corrected CRNS count rate; CTS_SNOWFREE_1/2/3: snow-free count rate estimates; N_WAT: CRNS count rate for infinite water depth.
    - DEPTH: median daily snow depth; ALBEDO: mean albedo (10:00–14:00 GMT).
    - UNCERT_CRNS_1/2/3: daily CRNS SWE uncertainty; UNCERT_SNOWFOX_1/2/3: daily SnowFox SWE uncertainty.
  - Data details and quality controls:
    - Albedo-based snow-event detection using thresholds (albedo > 0.5 indicates start; < 0.35 end; two snow-free days required to end a snow event).
    - Figures produced for each snow event (one per site-event), with 24-hour SWE estimates, precipitation, temperature, count rates, and albedo; days around event shaded to indicate reliability windows.
    - Depth-based SWE excluded on days where snow depth declined >20% from maximum during the event.
  - Site coverage and data availability:
    - 44 sites with data available for SWE calculations; site list excludes forest-dominated sites to reduce footprint biases.
    - Data presented as daily means; results aggregated per snow event with corresponding figures.

- Methods and interpretation
  - CRNS-based SWE (SWE_CRNS_1/2/3): uses CTS_CRNS, CTS_SNOWFREE_1/2/3, and N_WAT with three approaches to estimate snow-free count rate, varying in how they handle soil moisture changes.
  - SnowFox SWE (SWE_SNOWFOX_1/2/3): normalizes SnowFox count rate by snow-free rate and applies Howat et al. attenuation curve; typically yields SWE estimates ~1.7 times larger than other methods.
  - Snowmelt model SWE (SWE_MODEL): PACK model inputs (air temp, precipitation) with snow/rain classification; data filtered to remove unreliable precipitation inputs and extreme values.
  - Depth-based SWE (SWE_DEPTH): converts snow depth to SWE using a fixed density for fresh snow; uses robust daily medians to reduce noise and applies quality control.
  - Uncertainty and reliability:
    - Typical one-standard-deviation uncertainties: ~4 mm for CRNS and SnowFox; ~4 mm for depth; ~5 mm for the snowmelt model.
    - Uncertainties reflect soil moisture dependence (CRNS) and method-specific characteristics; used to flag days with more reliable estimates.
  - Data interpretation cautions:
    - SnowFox SWE may be biased high relative to other estimates; no correction applied due to potential biases in other methods.
    - Differences among methods are usually small; Method 3 often marginally more accurate but with greater complexity.

- Data access, licensing, and reuse
  - Licensed under the Open Government Licence.
  - Accessible at the provided DOI: https://doi.org/10.5285/e1fa6897-0f09-4472-adab-5d0d7bbc2548
  - Required citation: Wallbank et al. (2020) Snow water equivalent estimates using cosmic-ray neutron sensors in the United Kingdom (2014-2019). NERC Environmental Information Data Centre. DOI: 10.5285/e1fa6897-0f09-4472-adab-5d0d7bbc2548

- Data governance, provenance, and stewardship considerations
  - Metadata and documentation describe site-level details (SITE_ID, SITE_NAME, coordinates, installation/decommission dates, SNOW_SITE, etc.) and data product definitions (units, methods, inputs, and uncertainty fields).
  - Figures for each snow event assist in assessing reliability and provide a visual audit trail.
  - Data curation choices documented (site exclusions, quality filters for SnowFox and depth data, and precipitation plausibility checks).
  - Publication and data management expectations:
    - Properly cite the dataset when reused.
    - Acknowledge COSMOS-UK and funding sources (NERC Hydro-JULES and ENTRAIN programs); acknowledge data producers and contributors.
  - Considerations for ongoing governance:
    - Ensure consistent metadata standards, clear data provenance, and versioning if updates or corrections are made.
    - Maintain alignment with open data licensing and provide guidance on reuse in downstream analyses and data catalogues.

- Practical implications for data users
  - Choose SWE estimates with awareness of method-specific biases and uncertainties; CRNS-based estimates are robust over large footprints, while SnowFox can reflect fine-scale snowpack heterogeneity but may be biased high.
  - Use uncertainty fields (UNCERT_CRNS_*, UNCERT_SNOWFOX_*) to assess reliability for specific events and sites.
  - Leverage the accompanying figures and albedo-based event delineation to interpret the temporal evolution of SWE during snow events.
  - Document and cite the dataset appropriately in any downstream analyses or publications.