# Sampling regime

- Purpose: Documents the River Tay estuary greenhouse gas and water chemistry data collection regime used to derive dissolved gas concentrations and related physico-chemical parameters for map-based geospatial analyses.
- Timeframe: Sampling extends from April 2009 to July 2011 (Harley et al. 2015 describes April 2009–August 2010; data here extend beyond to July 2011).

## Sampling design and locations

- Locations: 10 sampling sites (Site 1–Site 10) along the River Tay estuary.
- Positioning: Sites are within 100 m of the provided UK grid reference location; Site 1 is the furthest upstream, and Site 10 is the furthest downstream (axial surveys of the estuary).
- Spatial relevance: Data are suitable for GIS mapping of spatial patterns across the estuary and for integration with other spatial datasets via site grid references.

## Sampling methods

- In situ measurements:
  - Instrument: Hydrolab QuantaProbe (Hach).
  - Depth: Readings taken ~10 cm below the water surface at each site.
- Water sampling protocol:
  - Triplicate sampling at each site using three plastic buckets.
  - Filtering: Sample filtered through GF/F 0.7 µm filters; portions stored for laboratory analysis.
  - Preservation: Samples kept in a cool box and frozen until laboratory analysis.
- Laboratory analyses:
  - Nitrogen species: TN, DIN, NH4+, NO3- via colorimetric method on a SEAL AQ2 discrete analyser.
  - Particulate/solids: Total suspended solids (TSS) by oven-drying GF/F filters at 105 °C for 4 hours.
- Greenhouse gas sampling:
  - Headspace method: 40 mL of estuary water equilibrated with 20 mL ambient headspace in a Luer-lock syringe with 3-way valve; underwater shaking for equilibration; transfer to pre-evacuated 12 mL vials.
  - Gases analysed: N2O, CH4 (ECD and FID detectors), CO2 (separate GC).
  - Corrections: Gas concentrations corrected for water temperature and salinity.
  - Saturation: Calculated as the ratio of dissolved gas concentration to the atmospheric equilibrium water concentration.
- Data scope: Measurements include dissolved N2O (N2O-N), CH4 (CH4-C), CO2 (CO2-C) and their saturations, plus a suite of water chemistry parameters.

## Data structure and units

- Data recording: Missing values marked with an asterisk (*) in the CSV file.
- Precision: All values reported to two decimal places.
- Key columns and units (as per Table 1):
  - Date, Time: Date of sampling; Time in GMT.
  - Site no.: 1–10 (1 upstream, 10 downstream).
  - Site name: Local landmark-based name.
  - Site Grid Ref: UK grid reference for site location.
  - N2O-N: Dissolved nitrous oxide (µg/L).
  - N2O Sat: Nitrous oxide saturation (%).
  - CH4-C: Dissolved methane (µg/L).
  - CH4 Sat: Methane saturation (%).
  - CO2-C: Dissolved carbon dioxide (mg/L).
  - CO2 Sat: Carbon dioxide saturation (%).
  - Temperature: Water temperature (°C).
  - NO3-N: Nitrate (mg/L).
  - NH4-N: Ammonium (mg/L).
  - DIN: Dissolved inorganic nitrogen (mg/L).
  - TN: Total dissolved nitrogen (mg/L).
  - pH: Water pH.
  - DO: Dissolved oxygen (mg/L).
  - DO Sat: Dissolved oxygen saturation (%).
  - Conductivity: Water conductivity (mS/cm).
  - Salinity: Salinity (ppt).
  - TSS: Total suspended solids (mg/L).

## Data context and reference

- Methodological basis: Harley, J.F.; Carvalho, L.; Dudley, B.; Heal, K. V.; Rees, R.M.; Skiba, U. (2015). Spatial and seasonal fluxes of the greenhouse gases N2O, CO2 and CH4 in a UK macrotidal estuary. Estuarine, Coastal and Shelf Science. DOI provided in the reference.
- Relevance for GIS use: The dataset provides location-based gas and water chemistry measurements with explicit grid references and site ordering, enabling spatial analyses, mapping of gas flux proxies, and integration with other spatial layers for the River Tay estuary.