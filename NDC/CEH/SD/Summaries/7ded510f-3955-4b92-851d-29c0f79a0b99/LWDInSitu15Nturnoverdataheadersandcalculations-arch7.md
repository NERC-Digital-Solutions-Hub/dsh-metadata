# General information: This dataset contains results from in situ field measurements of riverbed nitrogen transformations in the Hammer Stream (latitude = 51.01085722 N, longitude = 0.801498333 W), a sandy tributary of the River Rother in West Sussex, UK, the results of which have been published in Shelley et al. (2017)

## Overview and purpose
- In situ measurements of riverbed nitrogen transformations in a permeable sandy streambed.
- Focus on nitrate reduction pathways using 15N-labelled nitrate push-pull experiments.
- Data published in Shelley et al. (2017); methods also referenced to Lansdown et al. (2014) and related techniques.

## Spatial and temporal coverage
- Location: Hammer Stream, a tributary of the River Rother, West Sussex, UK.
- Coordinates provided for piezometers in the riverbed.
- Sampling seasons: November 2014; February 2015; April 2015; July 2015.

## Methods and data collection
- Tracer experiment: injection of 15N-labelled nitrate (300 µM, 98% 15N) in de-oxygenated synthetic river water + KCl; samples collected over time.
- Gas measurements: helium headspace; 15N-nitrogen in N2 measured by mass spectrometry.
- Pre-injection sampling: background porewater nutrients (NO2, NO3, NH3, PO4), chloride, O2, pH, temperature, Fe(II), organic carbon, 15N2, N2O.
- Sample handling: filtered porewater (0.45 µm) and frozen at -20°C until analysis.
- Data marking: values below detection limit labeled 0; missing or not collected labeled ND.

## Key variables and data structure
- Spatial identifiers: long, lat; piezometer ID (peizo); 1m LOW (near large woody debris: y/n).
- Depth metrics: Depth (screened mid-point depth in cm); True depth (true mid-point depth in cm); head (vertical hydraulic gradient) in meters.
- Hydrology: water depth (depth of river water to riverbed).
- Oxygen and chemistry (pre-injection porewater): O2adj (µM) and O2adj% (saturation); pH; temp (°C); NO2, NO3, NH3, PO4 (all in µM); Chloride (milli-M); CH4 and N2O (µM or nM depending on method); FeII (µM); orgC (mg/L).
- Isotopic/nitrate processing: p15N2 (in situ rate of total 15N2 production; nM N L^-1 h^-1); Denitrification, Anammox, DNRA (nM N L^-1 h^-1); tot 15n (sum of denitrification + anammox + DNRA); qN2 and qN2O (proportion of 15N labelling in produced N2/N2O).
- Proportions/percentages: %Anammox, %DNRA, %Denitrification.
- Data quality notes: 0 indicates below detection limit; ND indicates not collected or missing for that sample.

## GIS-focused implications
- Spatial analysis: piezometer locations enable mapping of nitrogen-processing hot spots across the riverbed.
- Attribute-rich points: include depth, proximity to woody debris, hydraulic gradient, and a full suite of chemical and isotopic measurements.
- Temporal analysis: four seasonal snapshots allow trend assessment and comparison across seasons.
- Derived metrics: potential to map rates of denitrification, anammox, and DNRA, and their relative contributions (percentages) across space.
- Data integration: aligns with GIS workflows by providing coordinates, categorical (1m LOW), and continuous attributes suitable for layering with hydrology and land-use data.

## Considerations for GIS workers
- Data completeness: some fields may be ND; others are 0 for below detection limits—plan for handling censored data.
- Units and scale: multiple measurement units across parameters; ensure consistent unit conversion when integrating with other datasets.
- Data provenance: method descriptions reference established literature (Lansdown 2014; Shelley 2017) for reproducibility and cross-study comparability.
- Data standardization: expect variability across in situ datasets; this dataset provides explicit column definitions and measurement contexts to aid harmonisation.

## References
- Shelley, F., Klaar, M., Krause, S., & Trimmer, M. (2017). Enhanced hyporheic exchange flow around woody debris does not increase nitrate reduction in a sandy streambed. Biogeochemistry.
- Lansdown, K. et al. (2014). Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed. Environ. Sci. Technol.
- Sanders, I. et al. (2007). Emission of methane from chalk streams... Freshwater Biology.
- Yamamoto, S., Alcauskas, J.B., & Crozier, T.E. (1976). Solubility of methane... J. Chem. Eng. Data.
- Weiss, R. & Price, B. (1980). Nitrous oxide solubility... Mar. Chem.
- Risgaard-Petersen et al. (1995, 2003); Thamdrup & Dalsgaard (2000); Trimmer et al. (2006). Methodological references for isotope labelling and measurements.