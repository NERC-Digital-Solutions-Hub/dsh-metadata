# POLLCURB - Changes in Urbanisation and its Effect on water quality and quantity from local to regional scale

- Aims and scope
  - Analyzes monitoring data from the POLLCURB project (Oct 2013–Oct 2015) to assess how urbanisation affects water quality and quantity from local to regional scales.
  - Combines water quality, precipitation, and river flow data to identify patterns, correlations, and potential impacts of urban development on hydrology.
  - Documents monitoring activities, data processing, storage, and quality control procedures.

## Monitoring activities (Chapter 1) and data types

- Three main types of monitoring
  - Water quality: Fortnightly and continuous multi-parameter measurements
  - Precipitation: 2-minute tipping-bucket rainfall data converted to 15-minute areal rainfall estimates
  - River flow: 5-minute velocity-depth-temperature measurements for flow derivation
- Study sites and scale
  - Bracknell town and The Cut, Swindon town and River Ray, and the Thames at London (downstream urban impact)
  - CEH conducts weekly Thames Basin water quality sampling; sites shown in accompanying figures
  - Aims to capture diverse land-use types across urban and downstream contexts
- Water quality monitoring details
  - Intermittent monitoring (Swindon and Bracknell): Fortnightly water samples with Eureka Manta2 multi-parameter sonde (one-minute sensors, three-minute spot readings, calibrated quarterly)
  - Thames in London (Earthwatch volunteers): Fortnightly sampling May 2014–Spring 2017 using Manta2; parameters include chlorophyll, DO, pH, conductivity, temperature, turbidity, tryptophan
  - Continuous monitoring (Environment Agency): Three high-resolution stations near Bracknell and Swindon flow gauging points plus a Sewage Treatment Works site; includes fortnightly suspended sediment sampling
- Precipitation monitoring and processing
  - Rainfall measured with tipping-bucket raingauges across study catchments; data logged every ~2 minutes and quality-checked
  - Areal rainfall estimates derived at 15-minute resolution using: 
    - Thiessen polygon weighting (Bracknell and Swindon contexts)
    - Arithmetic mean (alternative in some cases)
  - Processing follows BS standards for precipitation and hydrometric data management; areal rainfall methods chosen to reduce biases in clustering gauges
- Flow monitoring
  - Continuous flow data at 15-minute resolution (m^3/s)
  - Ultrasonic Doppler flow monitoring (UDFM) using:
    - Stingray portable level-velocity meters (smaller sites, shallow flows)
    - 6526H Starflow (larger channels, rugged usage)
  - Site selection aims to capture flows from different drainage areas and urban configurations
  - ISO15769 guidance followed for setup; sampling every 5 seconds with 5-minute data records; monthly data downloads and field updates

## Data storage, quality control, and workflow (Chapter 1)

- Data handling framework
  - Data stored and managed with clear metadata; datasets uploaded to Oracle-based systems
  - Weekly sampling by CEH complemented by partner organizations; data quality controlled and reformatted to standardized resolutions
- Precipitation data handling
  - Quality controlled and reformatted to 15-minute resolution
  - Areal rainfall estimation uses local gauges plus weighting methods depending on catchment characteristics
- Flow data processing framework (Chapter 2)
  - Based on Blake & Packman (2008) methodology for ultrasonic flow measurements
  - Key stages:
    - Identify and correct UDFM velocity errors
    - Analyze cleaned data to define depth-velocity relationships
    - Correct velocity-depth data and derive calibrated flow
  - Site-specific processing with cross-site validation (mass balance checks) and donor-site infill where data are missing
- Data processing outputs
  - GMT-corrected velocity-depth and rainfall data
  - Creation of QC1, QC2, and QC3 data series
  - Data uploaded to Oracle with associated quality control and validation notes

## Site-specific flow monitoring (Bracknell and Swindon) and regime characteristics

- Bracknell (BK_VD1–BK_VD6)
  - BK_VD1 Bottle Lane: Bracknell STW outflow, sediment buildup; urban-impervious influence; baseflow diurnal plus storm response
  - BK_VD2 Osborne Road: Brick arch culvert; focal on deep central velocity readings; urban/suburban to rural mix
  - BK_VD3 Montessori School: Large concrete box culvert; sediment buildup; low flows under dry conditions
  - BK_VD4 Forest Road: Wide box culvert; urban outfalls influence; summer flashy response
  - BK_VD5 Binfield Road: Highly variable bed depth; urban/ suburban/ agricultural mix; flashy responses with diurnal signals
  - BK_VD6 Triple Bore: Three culverts draining Bracknell town; highly urban-dominated regime; no clear attenuation features
  - Overall Bracknell regime: Flashy urban responses with significant influence from WWTW outfalls; baseflows variable; debris and sediment issues noted
- Swindon (SW_VD1–SW_VD10)
  - SW_VD1 Great Western Way: Large trapezoidal culvert; sediment buildup; urban near Swindon STW; steady baseflow with flashy storm response
  - SW_VD2 The Pry: Agricultural catchment; rural-influenced flows; responsive when catchment saturated
  - SW_VD3 Disused Railway Footbridge: Rectangular brick culvert; debris concerns; partial blockage possible
  - SW_VD4 Rodbourne culvert: Suburban/urban mix; debris present; flashy regime with winter rise
  - SW_VD5 Haydon Wick Footbridge culvert: Suburban housing estates; sediment buildup; urban flood protection works implemented
  - SW_VD6 Charmind Way Sewer; SW_VD7 Elstree Way Sewer; SW_VD8 Elsham Way Culvert; SW_VD9 Green Meadow Sewer; SW_VD10 Penhill Sewer: Series of suburban to urban storm drains with highly flashy responses to storm events; some sites show ongoing baseflow from natural or groundwater inputs
  - Overall Swindon regime: Dominated by urban drainage with flashy storm responses, variable baseflows, and in some cases diurnal patterns linked to upstream wastewater outfalls or groundwater contributions

## Data accessibility and references

- Datasets and methodology are documented to support reproducibility and reuse; some Earthwatch time-series data and site-specific details are available on request
- Methods and standards cited include ISO15769 (hydrometry), BSI standards for precipitation and hydrometric data management, and related literature on flow and sediment measurement