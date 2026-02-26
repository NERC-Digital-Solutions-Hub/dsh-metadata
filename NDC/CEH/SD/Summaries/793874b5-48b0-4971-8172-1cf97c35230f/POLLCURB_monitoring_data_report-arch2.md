# October 2018 James Miller and Mike Hutchins, Centre for Ecology and Hydrology
Report detailing the monitoring activities that have been undertaken and associated data as part of the NERC Changing Water Cycle funded project POLLCURB - Changes in Urbanisation and its Effect on water quality and quantity from local to regional scale.

## Overview
- Documents monitoring activities (Oct 2013 – Oct 2015) for POLLCURB Work Package 4: Data collection and collation.
- Three main monitoring types across the Thames catchment to assess urbanisation impacts on water quality and quantity:
  - Water quality (fortnightly and continuous, multi-parameter)
  - Precipitation (2-minute tipping-bucket data, processed to 15-minute resolution)
  - River flow (5-minute velocity-depth-temperature using ultrasonic Doppler meters)
- Study sites include Bracknell, Swindon, and the Thames at London, with CEH operating broader Thames Basin water quality monitoring.
- Data handling emphasizes verification, QA, cleaning, standardised processing, storage, and accessibility considerations.

## Chapter 1: Monitoring activities – methods

### 1.1 Water quality monitoring
- Three programmes operating at different temporal/spatial scales:
  - 1) Intermittent monitoring (Swindon and Bracknell)
    - Fortnightly sampling with Eureka Manta2 multi-probe sonde; readings every minute; three spot measurements per site.
    - Periodic calibration every three months (pH recalibration and sensor cleaning).
    - Parameters include ammonium (mg/L-N), dissolved oxygen (% sat), pH, specific conductivity (µS/cm), temperature (°C), turbidity (NTU).
  - 2) Intermittent monitoring (Thames in London)
    - Volunteers (Earthwatch) from May 2014 to Spring 2017; fortnightly sampling using same Manta2 method.
    - Parameters include chlorophyll (µg/L), DO (% Sat), pH, conductivity (µS/cm), temperature (°C), turbidity (NTU), tryptophan (ppb).
    - Data available on request; additional borehole data referenced.
  - 3) Continuous monitoring (Swindon and Bracknell)
    - Environment Agency installed three continuous stations at key flow gauging sites (Bracknell Binfield, Swindon Water Eaton, and Swindon STW vicinity).
    - Additional suspended sediment samples collected fortnightly at continuous sites.
    - Locations chosen to capture storm-event responses and link to concurrent flow data.

### 1.2 Precipitation monitoring
- 15-minute catchment-averaged rainfall data from multiple tipping-bucket raingauges.
- Each raingauge records tips every 2 minutes via a TinyTag Plus logger; monthly maintenance (downloading and cleaning) due to debris risk.
- Precipitation data quality controlled and reformatted to 15-minute resolution using local EA gauges.
- Areal rainfall estimation methods:
  - Thiessen polygon approach (BSI 7843-4) to account for spatial distribution of gauges.
  - Arithmetic mean method as alternative, with caveats about gauge clustering.
  - Findings varied by site:
    - Bracknell: arithmetic mean performed best due to uniform gauge distribution.
    - Swindon: Thiessen method performed best for a larger catchment with clustering considerations.

### 1.3 Flow monitoring
- 15-minute flow time series (cumecs) collected using ultrasonic Doppler flow measurement (UDFM) devices mounted on channel beds or pipe inverts.
- Two main instrument types:
  - Stingray portable level-velocity meter (for smaller sites/very shallow flows)
  - Unidata 6526H Starflow (rugged, suitable for larger channels)
- Site selection aimed at capturing flows from diverse development types and drainage configurations; ISO15769 guidance followed for installation.
- Data capture setup:
  - Sampling every 5 seconds with 5-minute logging intervals.
  - Monthly data downloads, site condition checks, battery changes, and re-starts.
- Processing overview (Chapter 2 references):
  - Velocity-depth data processed to derive depth-velocity relationships and flow estimates.
  - Calibration against spot gauging and mass-balance checks across upstream/downstream sites.

## Chapter 2: Flow processing

### Flow data processing workflow
- Based on Blake & Packman (2008) methodology with site-specific adaptations.
- Key steps:
  1) Identify and correct velocity measurement errors from UDFM data.
  2) Analyze cleaned data to establish depth-velocity relationships.
  3) Correct velocity-depth data and derive corrected flow estimates.
- Additional site-specific steps include:
  - Data correction to GMT
  - First QC level (QC1): basic flow derivation and outlier removal
  - Data analysis and QC processing of velocity-depth data (QC2) using TSP software; re-formatting and uploading to Oracle
  - Further QC (QC3): deriving velocity-index ratings and depth offsets by comparing with spot gauging; updates uploaded to Oracle

### Bracknell monitoring sites (BK_VD1–BK_VD6)
- BK_VD1a/b Bottle Lane: culvert under arch; multiple upstream/downstream conditions; variable max flows; regime influenced by urban/rural inputs.
- BK_VD2 Osborne Road: brick arch culvert; deep central measurement point; diurnal baseflow with flashy storm response; rural influence upstream of urban outflows.
- BK_VD3 Montessori: large concrete box culvert; significant sediment; baseflow/rate variability with urban influence.
- BK_VD4 Forest Road: wide, low box culvert; urban outfalls maintain base flows; summer flashy response.
- BK_VD5 Binfield Road: rectangular culvert; mixed suburban/urban/agricultural catchment; diurnal pattern with urban outfalls.
- BK_VD6 Triple Bore: three culverts draining Bracknell town centre; highly urban-driven flashy response; no clear attenuation features.

### Swindon monitoring sites (SW_VD1–SW_VD10)
- SW_VD1 Great Western Way: large trapezoidal bridge culvert; sediment buildup; urban-fringe baseflow with rural influence; flashy storm response.
- SW_VD2 The Pry: agricultural catchment; variable bed with debris; rural-urban mixing; diurnal variation with upstream wastewater input.
- SW_VD3 Disused Railway Footbridge: downstream confluence area; debris and variability noted.
- SW_VD4 Rodbourne culvert: urban/suburban catchment; debris impact noted; flashy regimes.
- SW_VD5 Haydon Wick: circular culvert; sediment buildup; urban/suburban drainage; notable 2013–2015 data window; urban outfalls influence.
- SW_VD6 Charmind Way Sewer: large suburban/peri-urban catchment; highly flashy response to storms.
- SW_VD7 Elstree Way Sewer: suburban storm drain; highly flashy storm response; minimal baseflow.
- SW_VD8 Elsham Way Culvert: upper Haydon Wick Brook; flashy response with underlying baseflow; rarely dry.
- SW_VD9 Green Meadow Sewer: suburban runoff; generally flashy with minor baseflow from misconnections/groundwater ingress.
- SW_VD10 Penhill Sewer: suburban, steep catchment; flashy storm response with occasional dry spells; fainter depth pulses observed.

## Data management and accessibility
- Some water quality data available on request; continuous data stored and managed via Oracle (QC’d datasets).
- CEH also conducts weekly Thames Basin water quality sampling to complement site-specific data.
- Overall aim aligns with creating standardized, high-resolution environmental datasets suitable for temporal policy performance assessment and inter-site comparisons.

## Relevance for the Analysts Monitoring the Environment archetype
- Demonstrates a structured, standards-based approach to environmental monitoring across multiple data streams (water quality, precipitation, flow) in urbanizing catchments.
- Uses established protocols (BSI standards, ISO guidance) and transparent QA/QC workflows to ensure data reliability.
- Produces high-resolution time-series outputs (fortnightly to 15-minute intervals) suitable for evaluating urbanization effects on water quality and quantity, enabling cross-site comparisons and trend analysis.
- Documents site-specific regimes and hydrological responses, highlighting the influence of urban outfalls and land-use changes on hydrology.
- Addresses the archetype’s challenges by outlining methods to increase dataset value (e.g., standardisation across sites) and by noting data accessibility considerations (data storage, availability on request).