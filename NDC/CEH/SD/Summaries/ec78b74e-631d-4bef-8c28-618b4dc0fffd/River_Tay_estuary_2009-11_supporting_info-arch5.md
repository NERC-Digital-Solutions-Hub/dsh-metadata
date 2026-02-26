# Sampling regime

## Overview
- Describes the River Tay estuary greenhouse gas and water chemistry data set sampling framework, including locations, timing, methods, and data units.
- Notes that Harley et al. (2015) covers April 2009 to August 2010; the data here extend from April 2009 to July 2011.

## Sampling locations and design
- 10 sampling locations along the River Tay estuary (Locations 1–10) shown in Figure 1 of Harley et al. (2015).
- Samples collected within 100 m of the provided UK grid reference for each site.
- Sampling sequence starts at the upstream site at high tide; axial surveys conducted using a rigid inflatable boat.
- Temporal scope: original publication period (April 2009–August 2010); current data extend to July 2011.

## Methods and analyses (field and lab)
- In situ physico-chemical measurements: dissolved oxygen (DO), pH, temperature, and conductivity measured ~10 cm below the water surface using a Hydrolab QuantaProbe (Hach).
- Water sampling: triplicate samples at each site using three plastic buckets; filtered through pre-ashed GF/F 0.7 µm filters; samples stored in tubes and kept frozen until laboratory analysis.
- Nutrients: total nitrogen (TN), dissolved inorganic nitrogen (DIN), ammonium (NH4+), nitrate (NO3−) analyzed colorimetrically with SEAL AQ2 discrete analyser.
- Particulates: total suspended solids (TSS) determined by oven-drying GF/F filters at 105 °C for four hours.
- Greenhouse gas sampling: headspace approach with 40 ml estuary water equilibrated with 20 ml ambient headspace in a luer-lock syringe; post-equilibration, headspace injected into pre-evacuated 12 ml vials for GC analysis.
- Gas analyses: N2O and CH4 measured by GC (HP5890 Series II) with ECD and FID detectors; CO2 measured on a separate GC.
- Data corrections and calculations: dissolved gas concentrations corrected for water temperature and salinity; gas saturation values calculated from dissolved concentration to atmospheric equilibrium values.
- See Harley et al. (2015) section 2.2 and 2.3 for further analytical details.

## Data structure and units
- Data values are reported to two decimal places.
- Missing data values are marked with an asterisk (*).
- Column types and units (as per Table 1):
  - Date/Time: sampling date and GMT time.
  - Site No./Site Name/Site Grid Ref: site identifiers.
  - N2O-N: µg/L; N2O Sat: %.
  - CH4-C: µg/L; CH4 Sat: %.
  - CO2-C: mg/L; CO2 Sat: %.
  - Temperature: °C.
  - NO3-N, NH4-N, DIN, TN: mg/L.
  - pH: (unitless).
  - DO: mg/L; DO Sat: %.
  - Conductivity: mS/cm.
  - Salinity: ppt.
  - TSS: mg/L.

## Data governance and provenance (implications for data stewards)
- Provenance tied to a published methodological framework ( Harley et al., 2015 ), enabling traceability of sampling and analysis workflows.
- Clear labeling of site identifiers, coordinates (Site Grid Ref), and measurement depths supports interoperability and repeatability.
- Standardized units and explicit missing data markers facilitate data integration across systems and datasets.
- Temporal coverage and versioning: note the extension beyond the Harley et al. 2015 publication period.

## Reference
- Harley, J.F., Carvalho, L., Dudley, B., Heal, K. V., Rees, R.M., Skiba, U. (2015). Spatial and seasonal fluxes of the greenhouse gases N2O, CO2 and CH4 in a UK macrotidal estuary. Estuarine, Coastal and Shelf Science. DOI: https://doi.org/10.1016/j.ecss.2014.12.004