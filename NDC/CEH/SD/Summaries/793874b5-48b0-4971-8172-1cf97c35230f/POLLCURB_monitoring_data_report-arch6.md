# October 2018 James Miller and Mike Hutchins, Centre for Ecology and Hydrology Report detailing the monitoring activities that have been undertaken and associated data as part of the NERC Changing Water Cycle funded project POLLCURB - Changes in Urbanisation and its Effect on water quality and quantity from local to regional scale

## Overview and aim
- Document monitoring activities and associated data collection for the POLLCURB project (Oct 2013–Oct 2015) under NERC Changing Water Cycle.
- Part of Work Package 4: Data collection and collation.
- Focus on urbanisation effects on water quality and quantity across local to regional scales.
- Provides methods, data storage/quality control, and data processing of flow data; data are stored and managed for later use and sharing.

## Monitoring activities and data collected
- Three main monitoring programs (water quality, precipitation, flow).
- Water quality
  - Intermittent monitoring (Swindon and Bracknell): fortnightly using Eureka Manta2 multi-probe sonde; 1-minute interval readings with 3-minute spot measurements; quarterly sensor calibration.
  - Thames in London (Earthwatch volunteers): fortnightly monitoring May 2014–Spring 2017 with the same Manta2 setup; additional groundwater data from nearby sites.
  - Continuous monitoring (two EA flow gauging locations plus a third site near Swindon STW): high-resolution water quality during storm events; suspended sediment sampling fortnightly at continuous sites.
- Precipitation
  - 15-minute catchment-average rainfall using tipping-bucket raingauges (2 mm bucket); data logged every ~2 minutes and monthly downlink/maintenance.
  - Areal rainfall estimates produced by: Thiessen polygon method and arithmetic mean, depending on catchment and gauge distribution; QA and formatting to 15-minute resolution.
  - Data standardization guided by BS I standards for raingauges and hydrometric data (BSI 7843-2/4; 17898/2014).
- Flow
  - 15-minute flow time series (cumecs) using ultrasonic Doppler flow meters (UDFM): Stingray portable level-velocity meters for smaller sites and Unidata 6526H Starflow for larger channels.
  - Site selection to capture flows from different drainage types; ISO15769 guidance followed for installation and calibration.
  - Sampling: 5-second samples with 5-minute recording frequency; monthly data downloads, site reads, and maintenance.

## Study locations and sites
- Bracknell catchment (Bracknell town and The Cut) and Swindon catchment (Swindon town and River Ray) as primary study areas; Thames at London used for downstream urban impact context.
- Water quality, precipitation, and flow monitoring sites distributed to represent diverse land-use types.
- Bracknell sites (BK_VD1 to BK_VD6) capture various culverts, channels, and outfalls; Swindon sites (SW_VD1 to SW_VD10) cover urban, suburban, and rural-influenced hydrology.
- Key site notes include flow regimes, max flows, and urban/rural influences (e.g., WWTP inputs, sedimentation, debris, diurnal patterns).

## Water quality data details
- Intermittent monitoring parameters (examples): ammonium, dissolved oxygen, pH, specific conductivity, temperature, turbidity (Bracknell/Swindon); chlorophyll and tryptophan added for Thames-London program.
- Data storage: multiple parameter files per location; pH data highlighted in the report with full datasets available on request.
- Methodology emphasizes field calibration, protection of sensors, and consistent sampling technique across sites and programs.

## Precipitation data processing
- Local EA gauge observations used to produce 15-minute areal rainfall estimates.
- Processing guided by BS 7843 series and 17898 standards; Thiessen polygon approach used in some catchments; arithmetic mean in others based on gauge distribution.
- Areal rainfall handling optimized per catchment (Bracknell vs Swindon) to mitigate gauge clustering biases.

## Flow data processing and quality control
- Processing follows Blake & Packman (2008) approach:
  - Identify and correct UDFM velocity errors.
  - Derive depth-velocity relationships; adjust for sensor errors.
  - Apply mass balance checks and donor-site data infill where necessary.
- Data processing steps (QC stages):
  - QC1: Derive flow from corrected velocity-depth data; GMT correction; remove zero values.
  - QC2: Analyze and re-format depth-velocity-flow data; generate new time series.
  - QC3: Derive velocity-index ratings and depth offsets via comparison with upstream/downstream data; upload results to Oracle.
- Site-specific processing summaries (Bracknell and Swindon) include vessel and conduit descriptions, cross-sections, and regime observations (diurnal WWTP influence, flashy urban flows, sediment buildup, debris issues).

## Data management and outputs
- Data storage and management aligned with ISO/BSI standards; all velocity-depth and rainfall data corrected to GMT.
- Data uploaded to Oracle; QA/QC outputs support robust hydrological analysis and mass-balance checks.
- Outputs include datasets and processed time series; some data available on request (e.g., Thames water quality data not fully tabulated in the report).
- The study provides a framework for data sharing, potential dashboards, pivot tables, and self-serve exploration, aligned with POLLCURB objectives.

## Key references and standards
- Hydrometric and precipitation data standards: BS 7843-2/4 (precipitation data acquisition and areal rainfall estimation), BS 17898 (hydrometric data management).
- Hydrometry guidance: ISO15769 for acoustic velocity meters using Doppler/echo correlation.
- Methodological basis for flow processing: Blake & Packman (2008) and Unidata/ISO documentation.

## End note
- The report comprehensively documents monitoring activities, data collection, processing workflows, and site-specific observations necessary to assess the effects of urbanisation on water quality and quantity at local to regional scales, with a clear emphasis on data quality, standardization, and accessibility for end users.