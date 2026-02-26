# POLLCURB - Changes in Urbanisation and its Effect on water quality and quantity from local to regional scale

## Overview
- Part of the NERC Changing Water Cycle POLLCURB project, focusing on monitoring activities from October 2013 to October 2015 to assess how urbanisation affects water quality and quantity across local to regional scales.
- Study coverage includes Bracknell and Swindon urban catchments and the downstream Thames Basin (London area), with CEH Thames Basin monitoring referenced.
- Aims to detail monitoring activities, data processing, storage, quality control, and data management to support policy scrutiny and future decisions.

## Monitoring activities (Chapter 1: Monitoring activities - methods)

### Water quality monitoring
- Three programmes operating at different scales:
  1) Intermittent monitoring in Swindon and Bracknell
     - Fortnightly measurements using Eureka Manta2 sonde (one-minute sensors; three spot readings per site per visit).
     - Calibration every three months; data stored with site metadata.
  2) Thames in London (Earthwatch volunteers)
     - May 2014–Spring 2017; fortnightly monitoring using the same Manta2 setup at multiple London sites.
     - Data available on request; includes parameters such as chlorophyll, dissolved oxygen, pH, conductivity, temperature, turbidity, and tryptophan.
  3) Continuous monitoring (Environment Agency)
     - Three high-resolution stations at Bracknell, Swindon catchments, and a Sewage Treatment Works site.
     - Focus on storm-event responses; additional suspended sediment samples collected fortnightly.
- Data capture involves multi-parameter water quality readings, with detailed method descriptions and site information. Some datasets are partially publicly available; others require requests.

### Precipitation monitoring
- 15-minute catchment-averaged rainfall data collected with tipping-bucket raingauges.
- Most local data are compiled to 15-minute resolution using local Environment Agency gauges.
- Areal rainfall estimates produced via two methods:
  - Thiessen polygon weighting (BSI 7843-4:2012)
  - Arithmetic mean of active gauges
- Method selection depends on catchment scale and gauge distribution; Bracknell favored arithmetic mean due to gauge uniformity, Swindon benefited from Thiessen due to gauge clustering.
- All precipitation data processed and formatted to 15-minute resolution; data management guided by BSI standards.

### Flow monitoring
- 15-minute flow time series (m3/s) derived from Ultrasonic Doppler flow meters (UDFM) attached to channel beds or pipe inverts.
- Instruments used:
  - Stingray portable level-velocity meter
  - Unidata 6526H Starflow
- ISO15769 guidance followed for siting and data interpretation; sampling 5 seconds with 5-minute recording interval; monthly data downloads and site checks.
- Site selection aims to capture flows from diverse urban drainage configurations and land uses; detailed site visits informed instrument placement and calibration.
- Data storage and processing references:
  - Downstream and upstream cross-checks; mass-balance validation where possible.
  - Data processed and stored with GMT corrections; multiple QC levels applied (see Chapter 2).

## Chapter 2: Flow processing

### Flow data processing workflow
- Based on Blake & Packman (2008) methodology, with site-specific adaptations:
  - Identify and correct ultrasonic velocity meter (UDFM) errors.
  - Develop depth-velocity relationships from cleaned data.
  - Correct velocity-depth data and derive flow.
- Processing steps include:
  - GMT correction for all velocity-depth and rainfall data.
  - QC1: initial flow derivation and filtering of zero values.
  - QC2: depth-velocity-flow analysis using TSP software; generation of new time series.
  - QC3: derivation of velocity-index ratings and depth offsets by comparing with spot gauges; implemented in SQL and uploaded to Oracle.
- Data are subsequently stored and managed in Oracle with site-specific records and regimes.

### Site descriptions and data records

- Bracknell (BK_VD1–BK_VD6)
  - Locations include Bottle Lane, Osbourne Road, Montessori site (Malt Hill), Forest Road, Binfield Road, and Triple Bore.
  - Each site described in terms of culvert type, bed conditions, sediment buildup, and Starflow placement.
  - Regimes range from urban-dominated flashy responses to diurnal patterns influenced by upstream wastewater treatment works (WWTW) and rural upstream inputs.
  - Notable max flows (examples): BK_VD5 ~7.25 cumecs; BK_VD1 ~unknown max in summary; BK_VD3 ~2.52 cumecs; BK_VD6 ~6.29 cumecs.
- Swindon (SW_VD1–SW_VD10)
  - Sites include Great Western Way, The Pry, Rodbourne culvert, Haydon Wick, Charmind Way Sewer, Elstree Way Sewer, and others.
  - Characteristics include large urban-regime influences, debris accumulation, sediment buildup, and significant diurnal variation related to WWTP inputs upstream.
  - Regimes documented as highly flashy during storms, with baseflows controlled by suburban-rural inputs; some sites show blockage or sensor issues during high flows.
  - Notable max flows (examples): SW_VD1 ~15.88 cumecs; SW_VD3 ~11.38 cumecs; SW_VD4 ~2.41 cumecs; SW_VD9 and SW_VD10 show smaller peaks with flashy responses.
- Overall
  - The Bracknell and Swindon networks capture a range of urban to peri-urban drainage configurations, illustrating how urbanisation and WWTPs shape flow dynamics, baseflows, and storm responses.
  - Data reflect sediment issues, debris, and sensor challenges that affect measurement during high-flow events.

## Data governance, openness, and challenges (aligned with monitoring-framework perspective)

- Data management and sharing
  - Data storage includes Oracle-based databases; some datasets are available on request rather than publicly accessible.
  - Metadata completeness and public accessibility of underlying data present barriers to full openness.
- Metadata and standardization
  - QA/QC processes (QC1–QC3) and GMT corrections demonstrate rigorous data governance.
  - Use of ISO and BSI standards (ISO15769; BSI 7843 and 17898) guides instrumentation, data management, and areal rainfall estimation.
- Data gaps and access barriers
  - Large volumes of files; only pH data publicly listed in some sections; other data accessible on request.
  - Potential data silos across organisations (EA, CEH, Earthwatch volunteers, local authorities) can impede rapid data sharing and integration.
- Transformations and interpretation
  - Precipitation areal estimates introduce methodological choices (Thiessen vs arithmetic mean) with context-dependent implications.
  - Flow data require site-specific calibration, force-fitting across diverse urban drainage structures, and mass-balance validation where possible.
- Implications for policy and practice
  - Demonstrates a comprehensive, multi-tier monitoring framework that combines intermittent, continuous, and citizen-science data to inform urban water quality and quantity assessments.
  - Highlights the need for robust metadata, open data sharing, and governance structures to translate monitoring into actionable policy insights.

## Outputs and references
- Document provides detailed methodologies, site-level data descriptions, and references to guidelines and prior work (e.g., ISO15769; BSI standards; Blake & Packman 2008; Dawson et al. 2018).
- Serves as a methodological reference for designing urban hydrology monitoring programs, data processing pipelines, and governance for data-sharing and quality assurance.