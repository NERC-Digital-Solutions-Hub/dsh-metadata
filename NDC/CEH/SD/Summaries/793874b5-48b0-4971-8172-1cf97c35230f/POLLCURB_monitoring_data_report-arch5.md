# October 2018 James Miller and Mike Hutchins, Centre for Ecology and Hydrology Report detailing the monitoring activities that have been undertaken and associated data as part of the NERC Changing Water Cycle funded project POLLCURB - Changes in Urbanisation and its Effect on water quality and quantity from local to regional scale

## Overview and aim
- Document monitoring activities and data produced as part of the POLLCURB project (Changing Water Cycle, NERC theme).
- Covers activities from October 2013 to October 2015 as part of POLLCURB Work Package 4: Data collection and collation.
- Three main monitoring types described: water quality, precipitation, and river flow.
- Sites chosen to represent urbanisation impacts across Bracknell (The Cut), Swindon (River Ray), and the River Thames at London, with CEH also conducting weekly Thames Basin water quality sampling.

## Monitoring activities and study sites
- Study locations:
  - Bracknell town and The Cut
  - Swindon town and the River Ray
  - Thames at London (downstream urban influence)
- CEH conducts weekly water quality sampling across the Thames Basin (locations shown in accompanying figures).

## Water quality monitoring
- Intermittent monitoring (Swindon and Bracknell):
  - Fortnightly readings using a Eureka Manta2 multi-parameter sonde with sensors taking readings at 1-minute intervals.
  - Spot measurements taken over a 3-minute period, with sensors calibrated every three months per manufacturer procedures.
- Thames in London (Earthwatch volunteers):
  - Fortnightly monitoring from May 2014 to Spring 2017 by volunteers using the same Manta2 setup.
  - Parameters include Chlorophyll, Dissolved Oxygen, pH, Specific Conductivity, Temperature, Turbidity, and Tryptophan; data available on request.
- Continuous water quality monitoring:
  - Environment Agency (EA) installed three continuous stations at Swindon and Bracknell flow gauging sites and at Swindon STW to capture storm-event dynamics.
  - Additional suspended sediment measurements taken fortnightly at continuous sites.
  - Station locations include Binfield (Bracknell), Water Eaton (Swindon), and a site upstream of Swindon STW.

## Precipitation monitoring
- Measurement:
  - 2 mm tipping bucket gauges provide 15-minute catchment-average rainfall (mm).
  - Data logged at 2-minute intervals by TinyTag Plus data loggers; monthly site visits for download and maintenance.
- Data processing and areal rainfall estimation:
  - Precipitation data quality-controlled and reformatted to 15-minute resolution using local Environment Agency gauges.
  - Areal rainfall estimated using:
    - Thiessen polygon method (area-weighted)
    - Arithmetic mean of active gauges
  - Methods aligned with BSI standards (BSI 7843-2, 7843-4, 17898:2014).
  - Bracknell: arithmetic mean performed best; Swindon: Thiessen polygons performed best due to gauge distribution and density.

## Flow monitoring
- Data type: 15-minute flow in cubic metres per second (cumecs) at multiple sites.
- Sensing technology:
  - Ultrasonic Doppler flow monitoring (UDFM) using bed-mounted instruments.
  - Two instrument types:
    - Stingray portable level-velocity meter (for smaller/shallow sites)
    - Unidata 6526H Starflow (rugged, suitable for larger channels)
- Site selection and installation:
  - Sites chosen to capture flows from different drainage types and urbanisation levels.
  - ISO15769 Hydrometry guidelines followed for siting and installation.
- Data collection:
  - Sampling period set to 5 seconds; recording every 5 minutes.
  - Monthly data downloads, site measurements, battery changes, and re-starts of logs.
- Processing and quality control:
  - Based on Blake & Packman (2008) workflow:
    - Identify UDFM velocity errors
    - Develop depth-velocity relationships from cleaned data
    - Correct UDFM errors
  - Site-specific processing steps and cross-site validation (mass balance) with donor sites for data gaps.
  - Data adjustments:
    - Corrected to GMT for velocity-depth and rainfall data.
    - Multi-stage QC (QC1, QC2, QC3) with reformatting and uploading to Oracle.
- Site details and regimes (examples):
  - Bracknell (BK_VD1 to BK_VD6 sites) across multiple culverts and channels; regimes range from diurnal baseflows influenced by upstream treatment works to flashy urban responses with sediment/build-up effects.
  - Swindon (SW_VD1 to SW_VD10 sites) including major culverts and sewers; regimes show flashy responses to storms, strong urban influence, and varying baseflows from rural upstream areas.
  - Data include site-specific maximum flows and qualitative descriptions of regime behavior (e.g., urban outfalls, debris effects, and diurnal variations).

## Data storage, accessibility and metadata
- Data files:
  - Water quality data available in grouped files by location/parameter (pH data explicitly noted; other parameters available on request).
  - Earthwatch Thames data and some London-area data available on request.
- Data processing outputs:
  - Flow data processed and uploaded to Oracle after QC stages.
- Data sharing:
  - Some datasets available on request; other datasets stored in project data repositories and Oracle system for QC-enabled sharing.
- Documentation:
  - Methods and site descriptions rely on standards and references (ISO15769, BSI standards) and project manuals (Blake & Packman, 2008).

## Relevance for data governance and stewardship
- Clear documentation of data collection methods, instrument types, measurement intervals, and site metadata.
- Alignment with international and national standards for precipitation and hydrometric data management.
- Structured, multi-stage quality control and data processing workflow (QC1–QC3) with provenance preserved and data uploaded to a central repository (Oracle).
- Explicit notes on data availability and access controls (data on request; some continuous data publicly accessible through project channels as defined).
- Comprehensive site-level detail supports auditability, reproducibility, and potential re-use by others studying urban hydrology and water quality.

## Challenges and considerations for Data Stewards
- Fragmented data across multiple datasets and formats (water quality, precipitation, flow) from different monitoring programs and volunteer contributors.
- Ensuring metadata completeness for diverse sites and sensor types.
- Maintaining consistent data quality across intermittent, continuous, and volunteer-sourced data streams.
- Managing large, high-resolution datasets (e.g., 15-minute flow, minute-interval water quality measurements) and ensuring timely data processing and updates.
- Balancing data accessibility with quality-controlled archival (e.g., data available on request vs. openly shared).