# Stable oxygen and hydrogen isotope composition of precipitation, river water and lake water in the Five Lakes of Mikata catchment, 2011-2012 and 2020-2022 - SUPPORTING DOCUMENTATION

## Overview
- Dataset of stable isotope compositions (δ18O, δ2H) and d-excess for waters in the Five Lakes of Mikata catchment.
- Temporal coverage: precipitation, river water, and lake water samples collected March 2011–January 2012 and July 2020–July 2022.
- Includes precipitation totals and average temperatures for subsampling periods.
- Lake Suigetsu water column data and water temperature/salinity variations with depth are provided for six dates during the 2020–2022 interval.
- Aim: assess whether catchment water isotopes reflect East Asian Monsoon variability.

## Collection/Generation Methods
- Hydrological samples: lake and river waters (n = 463) collected weekly (2011–2012) and (2020–2022). Precipitation samples (n = 120) collected event-based.
- Sampling protocol: submerge collection vessel in top ~50 cm; filter if algae present; careful handling to minimize headspace.
- Sampling locations changed between campaigns but remained within the same depth range to represent average surface conditions.
- Weather and environmental context: automated Netatmo station recorded temperature, humidity, precipitation, and wind data alongside isotope samples.
- Lake water column profiling (n = 70): approximately quarterly measurements across six dates; depth-stratified sampling from surface to 34 m with defined depth intervals.
- Analytical methods:
  - δ18O measured with Isoprime 100 IRMS (CO2 equilibration) using VSMOW2 scale; typical standard deviation < 0.05 ‰.
  - δ2H measured with TC-EA-IRMS (liquid autosampler); typical standard deviation < 0.5 ‰.
  - Isotopic data corrected against internal standards CA-HI and CA-LO, and calibrated to VSMOW.
- Derived metric: d-excess calculated from δ18O and δ2H.

## Data Structure and Content
- Two CSV files:
  - mikatagoko_modernisotopes_results.csv: isotope data plus precipitation totals and average temperature for observation periods.
  - lakesuigetsu_tempsalinity_results.csv: lake water temperature and salinity versus depth for six dates.
- Variables in mikatagoko_modernisotopes_results.csv include:
  - Sample Type (Lake/River/Precipitation/Column), Batch, Sample Number/Code, Location, Sampling Position, Sampling Depth (for columns), dates/times for vessel set/seal, Corrected δ18O and δ2H (on VSMOW2), d-excess, Total Precipitation, Average Temperature.
- Variables in lakesuigetsu_tempsalinity_results.csv include:
  - Sampling Date, Sampling Depth, Water Temperature (°C), Water Salinity (%).
- Location codes and coordinates provided to document precise sampling points (Hasu River, Mikata, Suigetsu) with notes on accessibility and campaign specifics.

## Quality Control and Data Processing
- Data corrected using laboratory standards; isotopic values tied to international references (VSMOW2, SLAP2, GISP).
- Acknowledges multiple factors affecting isotope signals:
  - Precipitation variability, catchment transit times, interactions with the Sea of Japan, minor evaporation.
- Metadata and structure:
  - Detailed data dictionary and field descriptions included to support data reuse.
  - Clear documentation of batches, sample codes, and sampling conditions to enable traceability.

## Data Limitations and Considerations for Use
- 2011–2012 precipitation and water-column data are not fully accompanied by corresponding ancillary datasets (e.g., precipitation/water column data limited to that period).
- Sampling locations shifted within campaigns; while within the same depth range, spatial changes may influence representativeness.
- Some dates have higher-resolution geochemical data; others are lower-resolution, affecting comparability across dates.
- Depth-resolved data provide rich context but require careful alignment with surface samples when interpreting monsoon signals.

## Relevance for Monitoring Frameworks
- Demonstrates end-to-end data lifecycle for environmental monitoring:
  - Systematic field collection, depth- and site-specific sampling, and rigorous QA/QC.
  - Comprehensive metadata and a structured data dictionary to support governance and reproducibility.
  - Machine-readable data products with explicit units, sample types, and measurement methods.
- Highlights the importance of:
  - Metadata completeness, provenance tracking, and clear data standards (VSMOW2 scale, boreal-lake contexts).
  - Documentation of sampling design changes and their potential impact on interpretation.
  - Open sharing of data and underlying measurements, with explicit relationships between isotope data and meteorological context.

## Practical Implications for Policy and Monitoring
- Use case supports policy-relevant insights into monsoon-driven hydrological variability in catchments.
- Emphasizes need for consistent metadata, traceable sampling locations, and depth-resolved data to inform water-resource decisions.
- Underlines data governance considerations:
  - Standardized data formats (CSV with explicit fields), reproducible processing (batch-level corrections, standard references).
  - Transparent reporting of limitations, sampling accessibility issues, and dataset coverage across campaigns.