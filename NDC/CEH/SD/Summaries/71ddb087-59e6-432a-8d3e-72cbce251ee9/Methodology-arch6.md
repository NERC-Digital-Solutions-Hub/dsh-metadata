# River Wensum Water Quality Data (2010 - 2016)

- What the dataset covers
  - River water samples collected from 20 sites in the River Wensum catchment (17 tributary outlets and 3 main river sites)
  - Sampling occurred approximately monthly from October 2010 to September 2016
  - Total of 899 water samples

- Sample collection methods
  - Grab samples collected from the centre of the river channel
  - Use of 1 L acid pre-washed polypropylene bottles
  - Samples transported in cool boxes and stored at 4°C within 5 hours to minimise degradation

- Laboratory analysis and QA/QC
  - Analyses performed within five days at the UEA Science Analytical Facilities
  - Analytes: nutrients, carbon, major ions, and total suspended solids (TSS)
  - Quality assurance: certified reference materials for accuracy; instrument precision checked via repeat measurements; reanalysis if tolerances were not met; manual data checks prior to acceptance

- Data structure and metadata (Table 1)
  - Spatial/temporal metadata: latitude/longitude (decimal degrees), date/time (yyyy/mm/dd:hh:mm)
  - Key measured parameters with units and instrument details: pH, electrical conductivity (µS/cm), major ions (Ca, Mg, Na, K, SO4 2-, Cl-), alkalinity (CaCO3), bicarbonate (HCO3-), carbonate (CO3 2-), silica (Si), B, Al, Fe, Mn, NO3-, NO2-, NH4+, total nitrogen (TN), total particulate nitrogen (TPN), total dissolved nitrogen (TDN), dissolved organic nitrogen (DON), total phosphorus (TP), total particulate phosphorus (TPP), total dissolved phosphorus (TDP), total reactive phosphorus (TRP), phosphate (PO4 3-), total carbon (TC), total organic carbon (TOC), total suspended solids (TSS), ion balance error
  - Data quality indicators: long-term precision (±), long-term accuracy (absolute), and detection limits where applicable; some fields marked as N/A or calculated
  - Note: certain fields are calculated (e.g., ion balance, sums) or reported as N/A for some entries

- Data structure and metadata (Table 2)
  - Instruments used by the UEA facilities:
    - Metrohm 855 robotic titro sampler
    - Agilent ICP-OES Vista pro
    - Dionex ICS2000 Ion Chromatography
    - Skalar San ++ Autoanalyser
    - Skalar Formacs CA15 TOC TN analyser

- Data quality and interpretation notes
  - Multiple analyte measurements include detection limits and instrument-specific precision/accuracy
  - Some parameters are reported with calculated values or N/A where appropriate
  - Spatial map reference: Figure 1 shows the 20 sampling sites across the catchment

- Potential uses and data product opportunities (data support perspective)
  - Time-series and spatial analyses of nutrient and carbon dynamics in a network of river sites
  - Data cleaning and harmonisation for integration with other datasets (e.g., land-use or hydrology)
  - Development of dashboards or self-serve reports for end users to explore site- and time-specific water quality trends
  - Assessment of QA/QC implications for downstream analyses (e.g., handling LOD, precision, and accuracy in analyses)
  - Provision of clear provenance and instrument-specific metadata to inform re-analysis or data fusion with comparable datasets