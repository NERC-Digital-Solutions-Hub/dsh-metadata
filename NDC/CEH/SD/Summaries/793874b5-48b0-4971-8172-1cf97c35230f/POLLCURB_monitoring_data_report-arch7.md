# POLLCURB - Changes in Urbanisation and its Effect on water quality and quantity from local to regional scale

- Overview
  - A 2018 report detailing monitoring activities and data gathered as part of the NERC Changing Water Cycle funded POLLCURB project.
  - Timeframe for the monitoring activities covered: October 2013 to October 2015 (Work Package 4: Data collection and collation).
  - Three main monitoring types were implemented across urban catchments and the Thames Basin:
    - Water quality (fortnightly intermittent and continuous multi-parameter measurements)
    - Precipitation (2-minute tipping-bucket data aggregated to 15-minute resolution)
    - River flow (5-minute velocity-depth-temperature measurements)
  - Study locations focus on Bracknell and Swindon urban catchments and the Thames at London to capture upstream urban influences and downstream urban impacts.

- Monitoring activities: Water quality
  - Intermittent monitoring – Swindon & Bracknell
    - Fortnightly sampling using Eureka Manta2 multi-probe sondes ( readings every minute; three-minute burst measurements at each site)
    - Periodic calibration every three months; sensors and reference pH solutions maintained per Manta2 manual
    - Parameters (example table shows ammonium, dissolved oxygen, pH, specific conductivity, temperature, turbidity)
  - Thames in London – Earthwatch volunteers
    - Fortnightly sampling (May 2014–Spring 2017) using the same Manta2 sondes
    - Parameters include chlorophyll, dissolved oxygen, pH, conductivity, temperature, turbidity, tryptophan
    - Locations mapped; data available on request; additional borehole data nearby
  - Continuous monitoring – Swindon & Bracknell
    - Environment Agency installed three high-resolution stations to capture storm-event responses
    - Two primary stations at Bracknell (Binfield gauging station) and Swindon (Water Eaton) plus a station at Swindon STW
    - Continuous water quality with fortnightly suspended sediment sampling
    - Instrument housings, inlets, and installation details provided for repeatability

- Monitoring activities: Precipitation
  - 15-minute catchment-averaged rainfall (mm) using tipping-bucket raingauges
  - 2-minute tipping-bucket data logged by TinyTag Plus loggers; monthly site visits for download/cleaning
  - Data quality-controlled and reformatted to 15-minute resolution using locally observed Environmental Agency gauges
  - Areal rainfall estimates generated via two methods:
    - Thiessen polygon approach (area-weighted)
    - Arithmetic mean of active gauges
  - Bracknell: Thiessen method accounted for clustering and gauge distribution; Swindon: Thiessen method better captured clustering and sparse gauges
  - Standards referenced for data management: BS 7843-2, BS 7843-4, BS 17898:2014

- Monitoring activities: Flow
  - Flow data provided as 15-minute cumecs time series
  - Measurement method: ultrasonic Doppler flow meters (UDFM) mounted on channel bed or in culverts
  - Two main instrument types:
    - Stingray portable level-velocity meter (smaller/shallower sites)
    - Unidata 6526H Starflow (rugged, suitable for larger channels)
  - Site selection focused on capturing flows from varied drainage types and urban configurations
  - ISO15769 Hydrometry guidelines followed for siting and operation
  - Sampling: 5-second samples with 5-minute recording frequency; monthly data downloads and site condition checks
  - Data processing and storage planned to a consistent workflow (see Chapter 2 for processing steps)

- Chapter 2: Flow processing (data QC and processing)
  - Core steps for data quality and consistency:
    - Identify and correct ultrasonic velocity meter (UDFM) velocity errors
    - Analyze cleaned data to establish depth-velocity relationships
    - Correct velocity-depth data and derive flow values
  - Site-specific processing and data repair using donor sites for infill where needed; validation against upstream/downstream data (mass balance checks)
  - Processing workflow includes:
    - GMT corrections for velocity-depth and rainfall data
    - First QC level (QC1) to derive initial flow; removal of zero values
    - Data analysis and QC processing of velocity-depth (QC2) using TSP software; reformatting and uploading to Oracle
    - Final QC processing (QC3) to derive velocity-index ratings and depth offsets; application via SQL and Oracle upload

- Site inventories and site characteristics (Bracknell and Swindon)
  - Bracknell monitoring locations (BK_VD1 to BK_VD6) along The Cut and Bracknell STW upstream/outflow
    - Examples: BK_VD1 Bottle Lane; BK_VD2 Osborne Road; BK_VD3 Montessori School; BK_VD4 Forest Road; BK_VD5 Binfield Road; BK_VD6 Triple Bore
    - Each site includes description (culverts/arch bridges), cross-sectional area, and qualitative regime notes (e.g., urban flashy responses, baseflow, diurnal variation)
  - Swindon monitoring locations (SW_VD1 to SW_VD10) along River Ray and urban/suburban drainage
    - Examples: SW_VD1 Great Western Way; SW_VD2 The Pry; SW_VD3 Disused Railway Footbridge; SW_VD4 Rodbourne culvert; SW_VD5 Haydon Wick; SW_VD6 Charmind Way Sewer; SW_VD7 Elstree Way Sewer; SW_VD8 Elstree Way Culvert; SW_VD9 Green Meadow Sewer; SW_VD10 Penhill Sewer
    - Each site includes drainage area (km2), structural description, and regime notes (e.g., highly flashy responses to storms, urban/rural mix, seasonality, and potential issues such as blockages or variability in bed depth)
  - This inventory supports GIS mapping of instrument locations, catchment connections, and hydrological response interpretation across urbanized landscapes

- Data products and accessibility
  - Water quality, precipitation, and flow data collected at multiple spatial scales across urban catchments
  - Data are stored as time series (15-minute resolution for most data) and linked to site locations for GIS integration
  - Some data (e.g., full water quality parameter sets outside pH) are available on request; CI/QA workflows ensure traceability and reproducibility
  - The documented methods emphasize standardization, quality assurance, and traceable processing to enable reliable map-based analyses and visualizations for policy, consultancy, and public audiences

- Relevance for GIS specialists
  - Provides a robust, geo-referenced dataset across urban and downstream catchments suitable for map-based data products
  - Clear workflow for data quality control, cross-site calibration, and time-series integration with spatial units (catchments, channels, culverts)
  - Site-level metadata (structure type, drainage area, flow regime) supports spatial analyses of urban hydrology, flood risk, and water quality pathways
  - Framework and standards (BS standards, ISO guidance) facilitate data governance and interoperability with other hydrological datasets