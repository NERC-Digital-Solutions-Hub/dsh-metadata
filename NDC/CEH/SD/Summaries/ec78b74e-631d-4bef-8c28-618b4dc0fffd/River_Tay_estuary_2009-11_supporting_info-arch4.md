# River Tay estuary greenhouse gas and water chemistry data set

## Overview
- Dataset capturing greenhouse gases (N2O, CH4, CO2) and water chemistry across 10 sampling locations in the River Tay estuary.
- Sampling period spans April 2009–July 2011 (extension beyond Harley et al. 2015, which covered April 2009–August 2010).

## Sampling regime and scope
- 10 sampling locations within ~100 m of UK grid references; site numbers 1 (upstream) to 10 (downstream).
- Axial estuary surveys conducted from a rigid inflatable boat; samples collected at each location, starting at the upstream site at high tide.
- Greenhouse gas and water chemistry samples collected at each site; locations described relative to local landmarks.

## Measurements and analytical methods
- In situ physico-chemical measurements at ~10 cm depth using a Hydrolab QuantaProbe: dissolved oxygen, pH, temperature, conductivity.
- Water sampling in triplicate per site:
  - Filtration through GF/F (0.7 µm), nutrients analyzed colorimetrically (TN, DIN, NH4+, NO3−) with SEAL AQ2.
  - Total suspended solids determined by oven-drying GF/F filters (105 °C, 4 h).
- Greenhouse gases sampled by headspace method:
  - 40 ml estuary water equilibrated with 20 ml headspace in a syringe; headspace analyzed by GC (N2O and CH4 with ECD; CO2 with FID).
  - Corrections applied for temperature and salinity to derive dissolved gas concentrations; gas saturations computed relative to atmospheric equilibrium.

## Data structure, units, and qualifiers
- Data reported to two decimal places; missing values marked with an asterisk.
- Columns include: Date, Time (GMT), Site no. (1–10), Site name, Site Grid Ref; N2O-N (µg/L), N2O Sat (%), CH4-C (µg/L), CH4 Sat (%), CO2-C (mg/L), CO2 Sat (%), Temperature (°C), NO3-N (mg/L), NH4-N (mg/L), DIN (mg/L), TN (mg/L), pH, DO (mg/L), DO Sat (%), Conductivity (mS/cm), Salinity (ppt), TSS (mg/L).

## Provenance and temporal coverage
- Builds on Harley et al. (2015) for spatial and seasonal fluxes of N2O, CO2, and CH4 in a UK macrotidal estuary.
- Data extend the sampling period to July 2011.

## Data quality, notes, and metadata
- Data include a detailed data dictionary (Table 1) with explicit unit details.
- Measurements are linked to standard methods and instrument references; missing data explicitly flagged.
- Clear documentation of site numbering, naming, and grid references to support discoverability and re-use. 

## References
- Harley, J.F., Carvalho, L., Dudley, B., Heal, K. V., Rees, R.M., Skiba, U. (2015). Spatial and seasonal fluxes of the greenhouse gases N2O, CO2 and CH4 in a UK macrotidal estuary. Estuarine, Coastal and Shelf Science. DOI: https://doi.org/10.1016/j.ecss.2014.12.004