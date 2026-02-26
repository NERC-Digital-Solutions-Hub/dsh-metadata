# River Tay estuary greenhouse gas and water chemistry data set

- Sampling locations: 10 sites (Site 1 furthest upstream to Site 10 furthest downstream) on the River Tay estuary; sites within 100 m of the provided UK grid reference. Sampling conducted axially by rigid inflatable boat, starting at high tide.
- Timeframe: Data extend from April 2009 to July 2011 (Harley et al. 2015 covers April 2009–August 2010; the dataset here extends to July 2011).

## Sampling regime and locations

- Location details include Site number, Site name, and Site Grid Ref (UK grid reference format).
- Field sampling focused on both greenhouse gas measurements and water chemistry at each site.

## Measurements and field procedures

- In situ measurements: dissolved oxygen (DO), pH, water temperature, and conductivity measured about 10 cm below the surface using a Hydrolab QuantaProbe (Hach).
- Water sampling: triplicate samples collected at each site using three plastic buckets; samples filtered through GF/F 0.7 µm filters, then stored frozen for laboratory analysis.
- Units and data organization: data recorded with specific column definitions (Date, Time, Site No., Site Name, Site Grid Ref, etc.) and reported to two decimal places.

## Gas sampling and analysis

- Greenhouse gases sampled using the headspace method: at each site, 40 mL of estuary water equilibrated with 20 mL of ambient headspace in a luer-lock syringe, shaken underwater for 1 minute, then transferred to pre-evacuated 12 mL vials for GC analysis.
- Analytes and instruments:
  - Nitrous oxide (N2O) and methane (CH4) analyzed on an HP5890 Series II GC with electron capture detector (ECD) and flame ionisation detector (FID).
  - Carbon dioxide (CO2) measured on a separate HP5890 Series II GC.
- Calculations: dissolved gas concentrations corrected for water temperature and salinity; gas saturations calculated as the ratio of dissolved concentration to atmospheric equilibrium concentration.

## Laboratory analyses and chemical measurements

- Nitrogen species: TN, DIN, NH4-N, and NO3-N measured by a SEAL AQ2 discrete analyzer (colorimetric method).
- Particulate and dissolved components: total suspended solids (TSS) determined by oven-drying GF/F filters at 105°C for 4 hours.
- Additional notes: Data include two decimal place reporting; missing values are marked with an asterisk in the CSV dataset.

## Data structure, units, and quality notes

- Data are organized in a CSV with columns described in Table 1, including:
  - Date (Date), Time (GMT), Site No. (1–10), Site Name, Site Grid Ref, gas concentrations (N2O-N, CH4-C, CO2-C) and their saturations, Temperature (°C), NO3-N (mg/L), NH4-N (mg/L), DIN (mg/L), TN (mg/L), pH, DO (mg/L), DO Sat (%), Conductivity (mS/cm), Salinity (ppt), TSS (mg/L).
- Units per column: as specified (e.g., N2O-N in µg/L; CH4-C in µg/L; CO2-C in mg/L; NO3-N, NH4-N, DIN, TN in mg/L; temperatures in °C; conductivities in mS/cm; salinity in ppt; TSS in mg/L; pH unitless; DO in mg/L and DO Sat %).
- Data provenance: referenced to Harley, J.F. et al. (2015) “Spatial and seasonal fluxes of the greenhouse gases N2O, CO2 and CH4 in a UK macrotidal estuary.” Estuarine, Coastal and Shelf Science; dataset details align with section 2.2–2.3 of Harley et al. (2015).

## Reference

- Harley, J.F., Carvalho, L., Dudley, B., Heal, K. V., Rees, R.M., Skiba, U. (2015). Spatial and seasonal fluxes of the greenhouse gases N2O, CO2 and CH4 in a UK macrotidal estuary. Estuarine, Coastal and Shelf Science. DOI: 10.1016/j.ecss.2014.12.004