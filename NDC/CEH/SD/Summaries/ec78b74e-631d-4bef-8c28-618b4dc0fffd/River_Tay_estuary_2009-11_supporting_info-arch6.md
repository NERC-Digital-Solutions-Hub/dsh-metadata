# River Tay estuary greenhouse gas and water chemistry data set

## Overview
- A dataset of greenhouse gas (N2O, CH4, CO2) and water chemistry measurements from 10 sampling locations in the River Tay estuary.
- Sampling spans April 2009 to July 2011; previously published Harley et al. (2015) covers April 2009 to August 2010.
- Data were collected to enable spatial and seasonal flux analyses and to support understanding of estuarine biogeochemistry.

## Sampling regime and period
- 10 sampling locations (Site 1 to Site 10) along the estuary, within 100 m of provided UK grid references.
- Axial surveys conducted from a rigid inflatable boat starting at the upstream site at high tide.
- At each site, greenhouse gas and water chemistry samples were collected in triplicate.
- Sampling timeframe extends from April 2009 to July 2011 (publication period covers April 2009–August 2010).

## Measurements and analyses
- In situ physico-chemical measurements at ~10 cm below the water surface using a Hydrolab QuantaProbe:
  - Dissolved oxygen (DO), pH, temperature, conductivity.
- Water sampling and lab analyses:
  - Triplicate samples per site collected with three pre-ashed GF/F filters; analyses include TN, DIN, NO3-, NH4+ using colorimetric methods (SEAL AQ2 discrete analyzer); total suspended solids (TSS) by oven-drying filters.
- Greenhouse gas sampling (headspace method):
  - 40 mL estuary water equilibrated with 20 mL headspace; samples shaken underwater to equilibrate.
  - Headspace gas injected into pre-evacuated 12 mL vials; analyzed by gas chromatography (HP5890 II) with ECD (N2O, CH4) and FID (CO2).
  - Concentrations corrected for water temperature and salinity; gas saturations computed from concentrations and atmospheric equilibrium values.
- Data are reported with two decimal places; missing values are marked with an asterisk.

## Data structure and units
- Data stored in CSV with clear column definitions (as described in Table 1).
- Key columns include:
  - Date, Time (GMT), Site No. (1–10), Site Name, Site Grid Ref
  - N2O-N (µg/L), N2O Sat (%), CH4-C (µg/L), CH4 Sat (%)
  - CO2-C (mg/L), CO2 Sat (%)
  - Temperature (°C), NO3-N (mg/L), NH4-N (mg/L), DIN (mg/L), TN (mg/L)
  - pH, DO (mg/L), DO Sat (%), Conductivity (mS/cm), Salinity (ppt), TSS (mg/L)
- Any missing data values are indicated by an asterisk.

## Data quality, processing, and notes
- Data include replicated measurements (triplicates) for water chemistry and GHG analyses.
- Temperature and salinity corrections are applied to dissolved gas concentrations; saturations are derived from them.
- Salinity is determined via conductivity correlations.
- The dataset provides a transparent basis for data fusion with other estuarine datasets and supports downstream calculations of gas fluxes and biogeochemical relationships.
- While the text outlines measurement techniques and units, it implies standard QA/QA steps (verification, cleaning, formatting) typical for preparing data products and dashboards.

## Usage and integration recommendations
- Suitable for dashboards or pivot-table style exploration of spatial and temporal trends in:
  - Dissolved gas concentrations and saturations
  - Water chemistry parameters (nutrients, pH, DO, conductivity, salinity)
  - Temperature effects on gas solubility and nutrient dynamics
- Can be combined with external datasets (e.g., tidal phase, flow data) to model estuarine gas fluxes and biogeochemical processes.
- Outputs can include summary statistics by site and by sampling period, as well as interactive views of gas saturation vs. temperature, salinity, and DIN/TN relationships.

## References
- Harley, J.F., Carvalho, L., Dudley, B., Heal, K. V., Rees, R.M., Skiba, U., 2015. Spatial and seasonal fluxes of the greenhouse gases N2O, CO2 and CH4 in a UK macrotidal estuary. Estuar. Coast. Shelf Sci. https://doi.org/10.1016/j.ecss.2014.12.004