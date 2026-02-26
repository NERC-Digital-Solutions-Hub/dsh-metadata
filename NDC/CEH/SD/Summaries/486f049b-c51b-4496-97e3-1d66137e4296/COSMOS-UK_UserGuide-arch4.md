# COSMOS-UK User Guide

- Provides near real-time soil moisture data across the UK using cosmic-ray neutron sensing (CRNS), delivering soil moisture information over areas up to about 12 hectares per site.
- Aims to support applied environmental research, improved modelling, flood/earth observation capabilities, and broader data-enabled decision making.

## Data assets and what COSMOS-UK provides

- Primary measurements
  - Cosmic-ray neutron sensor (CRNS) counts used to derive volumetric water content (VWC) via site-specific calibration and processing.
  - Corrected neutron counts accounting for atmospheric pressure, altitude, and humidity.
  - Derived products including VWC (CRNS-based), 86% sensing depth metrics (D86), and related QC data.
- Other monitored data (instruments deployed at sites)
  - Precipitation (rain gauge), air temperature, relative and absolute humidity, atmospheric pressure, wind (speed and direction), shortwave/longwave radiation components, net radiation.
  - Snow depth and snow water equivalent.
  - Soil moisture and temperature from point TDT sensors and a profile soil moisture probe (depths from 2 cm to 50 cm and deeper where available).
  - Soil heat flux, and phenocam imagery for land cover/phenology context.
- Derived data
  - Net radiation, 3D/profile soil moisture estimates, potential evaporation, and other data products derived from the above streams.
- Data update and access
  - Data are available via the CEH Environmental Information Data Centre (EIDC) and are provisional, subject to QC revisions.
  - Live graphical displays and standard retrievals are available on the COSMOS-UK website; data licensing is provided with data releases.

## Network and site coverage

- UK-wide network design to cover diverse conditions (climate, soil, land cover, geology) with clustering to enable cross-site comparisons and regional/national analyses.
- Site selection factors include geographic coverage, environmental variables, presence of high soil moisture variability, existing monitoring, opportunities for model data assimilation, long-term access permissions, accessibility, vandalism risk, and mobile network coverage.
- Detailed site properties and an expanded site list are documented (e.g., start dates, calibration status, location coordinates, soil characteristics, land cover).

## Instrumentation and data streams

- Key instruments
  - Cosmic-Ray Neutron Sensor (CRNS) – main soil moisture proxy; field calibration used to derive VWC.
  - Rain gauge (precipitation data).
  - Point soil moisture sensors (TDT) and a profile soil moisture sensor.
  - Soil heat flux plates, soil temperature sensors.
  - Radiometer, automatic weather station (temperature, humidity, pressure, wind, etc.).
  - 3D and integrated sonic anemometers (wind).
  - Phenocams and snow sensors (snow depth and SWE).
  - Data loggers and microloggers for data capture and transmission.
- Not all instruments are installed at every site; instrumentation can evolve over time.

## Data processing workflow

- Raw to derived data
  - CRNS counts are corrected for atmospheric pressure, altitude, and atmospheric water vapor to produce corrected counts.
  - VWC is derived from corrected counts using one of three methods; COSMOS-UK adopts the site-specific N0 calibration with field calibration and silica soil parameters, plus adjustments for lattice water and soil organic carbon.
  - Additional data streams (e.g., TDT, profile sensors, radiometric, meteorological) provide complementary measurements and enable multi-sensor data fusion.
- Averaging and temporal resolution
  - CRNS data are recorded hourly, but VWC signals are noisy; 6-hour or daily averaging is recommended to extract meaningful signals.
  - A revised method derives daily VWC from daily average counts with allowances for up to two missing hourly values; negative VWC values are set to zero, while values above 100% may remain but should be treated with caution.
- Footprint and depth considerations
  - Sensor footprint and effective depth (D86) are distance- and moisture-dependent; prior assumptions of a fixed depth were revised to reflect distance-based D86 values near calibration distances (1, 5, 25, 75 m) and footprint radii up to 150–200 m in wet/dry UK soils.
  - A 75 m D86 value is used as a representative indicator of the footprint depth variation.
- Calibration and correction factors
  - A correction factor Fi is applied to account for cosmic ray fluctuations; historically unity scaling (ɣ = 1) was used, with 2018 introducing site-specific gamma (ɣ) values to remove spurious trends.
- Processing revisions and harmonization
  - When processing method changes occur, the new approach is applied to the entire dataset for consistency; some legacy calculations may continue in the background.
- Comparison with other measurements
  - CRNS signals are noisy; co-located TDT sensors typically provide more stable VWC estimates and help cross-validate CRNS results; discrepancies can arise due to sampling volumes and temporal/spatial scales.

## Quality control and data gaps

- Quality control
  - Two-stage QC process: automated tests on raw (level1) data; and daily visual inspection of plots.
  - Level1 data passing automated QC are moved to Level2; both levels may be retained with labels in references.
  - QC tests cover zero data, too few samples, low power, sensor faults, diagnostic flags, out-of-range values, secondary variable dependencies, spikes, and error codes.
- Gap handling
  - As of the guide, there is no automatic gap-filling; gaps may be filled via manual site visits or data recovery where possible.
- Data reliability notes
  - Daily VWC values for peat soils can be less reliable; mineral soils yield more robust daily values.
  - Negative VWC values are now set to zero; values >100% are left in the dataset with caution advised.
- Documentation and provenance
  - Comprehensive appendices document site data, data availability, phenocams, standard graphical retrievals, embedding plots, and quality control tests.

## Accessing and using COSMOS-UK data

- Data access
  - Primary access through the CEH EIDC at http://eidc.ceh.ac.uk/; data are uploaded in annual tranches and can lag behind real-time by up to 1–2 years.
  - Data requests outside the EIDC are considered on a reasonable-effort basis; data are provisional and licenced.
  - Contact cosmosuk@ceh.ac.uk for data requests and collaboration opportunities.
- Visualization and retrieval
  - Graphs of precipitation, air temperature, and CRNS-derived soil moisture are available on the COSMOS-UK website; standard graphical retrievals are provided (see Appendix D for examples).
  - A web API-like embedding option allows users to generate graphs on their own websites via simple URLs (examples provided in Appendix E).
- Data freshness and latency
  - Typical latency from site to graph is under two hours, but can vary depending on processing status; refreshing graphs is manual.
- Data licensing and usage
  - Data are provided with a license specifying usage terms; provisional status means users should account for ongoing QC and potential revisions.

## Practical takeaways for data leaders

- Strategic value
  - COSMOS-UK delivers a scalable, non-invasive, near real-time soil moisture dataset across diverse UK environments, enabling model validation, data assimilation, drought/flood risk assessment, and agricultural productivity analytics.
- Data governance and stewardship
  - Clear QC regimes, metadata, and processing revisions are essential for trust and reproducibility; plan for versioning and documentation when data processing methods change.
- interoperability and collaboration
  - Integration with other data streams (TDT, weather, phenology) supports robust data products and cross-domain use; opportunities exist for partnership with national monitoring and modelling initiatives.
- Risks and limitations
  - Data gaps, peat soils, and spatial-temporal variability require careful handling and site-aware interpretation; users should leverage multiple sensors for cross-validation.
- Future directions
  - Anticipated expansion of data products, broader data accessibility, and ongoing methodological refinements to improve reliability and interpretability of CRNS-derived soil moisture.

## Contact and references

- Primary contact for COSMOS-UK data: cosmosuk@ceh.ac.uk
- CEH and partner institutions provide ongoing data governance, updates, and collaboration opportunities.
-References cited within the guide cover methodology for CRNS processing, calibration, footprint analysis, and data quality practices.