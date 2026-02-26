# October 2018 James Miller and Mike Hutchins, Centre for Ecology and Hydrology Report detailing the monitoring activities that have been undertaken and associated data as part of the NERC Changing Water Cycle funded project POLLCURB - Changes in Urbanisation and its Effect on water quality and quantity from local to regional scale

## Purpose and scope
- Document monitoring activities and data collected for POLLCURB (Oct 2013–Oct 2015) under the NERC Changing Water Cycle program.
- Focus on three data streams: water quality, precipitation, and river flow across urbanizing catchments.
- Describe site selection, methods, data storage, and quality control; provide site-specific flow monitoring details and regimes.

## Monitoring activities (Timeframe and types)
- Period: October 2013 to October 2015, Work Package 4: Data collection and collation.
- Three main monitoring types:
  - Water quality: fortnighly and continuous multi-parameter; three programs as described below.
  - Precipitation: 2-minute to 15-minute tipping-bucket gauge data; rainfall areal estimation.
  - River flow: 5-minute velocity-depth-temperature data; flow derived from velocity and cross-section.

## Study sites and site selection
- Three main locations representing urban catchments and downstream urban influence:
  - Bracknell town and The Cut
  - Swindon town and the River Ray
  - The Thames at London (downstream urban development impacts)
- Additional CEH Thames Basin water quality monitoring sites operated by CEH.
- Aim: capture diversity of land-use types and tributaries, monitoring at low points before major confluences.

## Water quality monitoring
- Intermittent monitoring (Swindon and Bracknell):
  - Fortnightly readings using Eureka Manta2 multiprobe sonde; 1-minute sensor intervals; three spot measurements per site.
  - Quarterly calibration of sensors and pH solution changes per manual guidelines.
- Thames in London (Earthwatch volunteers):
  - Fortnightly monitoring May 2014–Spring 2017; same Manta2 sondes and method; data available on request.
- Continuous monitoring (Environment Agency):
  - Three stations near Bracknell and Swindon flow gauging sites plus a StW site.
  - Additional suspended sediment samples collected fortnightly.
  - Locations chosen to align with flow gauging and capture storm-event responses.

## Precipitation monitoring
- Equipment: tipping-bucket raingauges with 2 mm tipping buckets; data logged every 2 minutes.
- Processing: rainfall totals converted to 15-minute resolution using local Environment Agency gauges.
- Areal rainfall estimation:
  - Thiessen polygon method (area-weighted) and arithmetic mean methods evaluated per standard BS/BSI guidance.
  - Bracknell: arithmetic mean performed best due to gauge distribution.
  - Swindon: Thiessen polygon method performed best due to gauge clustering and coverage.
- Data handling and standards:
  - Processing aligned with BS 7843-2:2012, BS 7843-4:2012, and BS 17898:2014 for precipitation data management.

## Flow monitoring
- Instrumentation:
  - Ultrasonic Doppler flow measurement (UDFM) with velocity-depth sensors mounted on channel beds or in culverts.
  - Two types used: Stingray portable level-velocity meter (smaller/shallower sites) and Unidata 6526H Starflow (rugged, suitable for larger channels).
- Site siting and selection:
  - Based on mapping of drainage pathways (from DEM) and site visits to ensure representative urban, peri-urban, and rural contributions.
  - ISO15769 (Hydrometry) guidance followed for installation and operation.
- Data collection and resolution:
  - Sampling: 5-second sampling period; record every 5 minutes.
  - Monthly data download, site condition checks, battery replacement, and log reset.
- Output:
  - Velocity, depth, and derived flow (cubic metres per second) with GMT time alignment.

## Data processing and quality control (Chapter 2)
- Processing framework based on Blake & Packman (2008) with site-specific adaptations:
  - Identify ultrasonic Doppler flow meter (UDFM) velocity errors.
  - Cleaned data to define depth-velocity relationships.
  - Correct UDFM errors and re-calculate flow.
- Site-specific processing steps (examples include Bracknell and Swindon sites):
  - Data correction to GMT for velocity-depth-flow series.
  - First QC level (QC1) derivation and zero-value filtering.
  - QC2: depth-velocity-flow data analysis and reformatting; use of TSP software; data uploaded to Oracle.
  - QC3: derivation of velocity-index ratings and depth offsets via comparison with spot gauging; updated in SQL and Oracle.
- Documentation of site regimes and physical characteristics (examples of Bracknell and Swindon sites provided, including areas, bed types, and instrument mounting details).

## Site-specific flow monitoring snapshots
- Bracknell (BK_VD1 to BK_VD6) and Swindon (SW_VD1 to SW_VD10) flow sites:
  - BK_VD1–BK_VD6: mix of culverts and small bridges; urban/rural mixtures; sediment buildup; variable flows; presence of wastewater treatment works (WWTW) influences noted; diurnal and flashy responses observed.
  - SW_VD1–SW_VD10: range from large urban culverts to storm drains; some sites show highly flashy responses during storms and baseflows influenced by upstream WWTPs.
  - Regimes generally indicate a strong urban signal with flashy storm responses, variable baseflows, and sediment/ debris influences at several sites.
- Example highlights:
  - Bracknell sites show contributions from urban runoff and upstream WWTW; some sites exhibit substantial diurnal cycles and sediment issues.
  - Swindon sites demonstrate rapid responses to rainfall, with some sites heavily influenced by urban infrastructure and downstream WWTP inputs.

## Data access and metadata
- Water quality data:
  - pH data and other parameters stored in parameter-specific files; full data available on request.
- Earthwatch Thames London data (water quality) available on request.
- Flow and precipitation data:
  - Stored as continuous time series (15-minute flow; 2-minute precipitation; 5-minute flow sampling intervals); organized with site metadata and processing logs.
- Data sharing:
  - Some datasets accessible on request; reports and processing methodologies documented for reproducibility and governance.

## Implications for data leaders and governance
- Demonstrates an integrated, multi-stream data infrastructure for urban hydrology, combining:
  - High-frequency flow data (UDFM) with meteorology and water quality data.
  - Intermittent and continuous sampling regimes across multiple sites and urban contexts.
- Emphasizes data quality and standards:
  - Calibration routines, GMT alignment, QC pipelines, and ISO/BSI-compliant precipitation processing.
- Highlights challenges and opportunities:
  - Fragmented data across sites and formats; some data not publicly open (access on request).
  - Need for robust metadata, documentation, and governance to enable cross-site comparisons and reuse.
- Relevance for data strategy:
  - Aligns with data leaders’ aims to understand data systems end-to-end, verify data suitability, maintain metadata and discoverability, iterate with users, and collaborate across networks to improve urban water data assets.