# General information: This dataset contains results from in situ field measurements of riverbed nitrogen transformations in the Hammer Stream (latitude = 51.01085722 N, longitude = 0.801498333 W), a sandy tributary of the River Rother in West Sussex, UK, the results of which have been published in Shelley et al. (2017). Here in the permeable sandy sediments nitrate reduction was measured by 'push-pull' using the techniques described in Lansdown et al. (2014) but here directly in the main piezometer network described in Shelley et al (2017). Briefly, a tracer containing 15N-labelled nitrate (300 micro-M (M), 98 atom % 15N) in a de-oxygenated synthetic river water plus KCl matrix was injected into the riverbed and porewater samples recovered over time (see Lansdown et al. (2014)). A helium headspace is added to the water samples, the 15N-labelled N2 content of which can be determined by mass spectrometry. Measurements were performed in November 2014 and February, April and July 2015.

- This dataset documents in situ riverbed nitrogen transformations using 15N-nitrate push-pull experiments in Hammer Stream, with background porewater measurements prior to tracer injection and seasonal data collection (Nov 2014; Feb, Apr, Jul 2015).
- It provides detailed metadata for each piezometer, including location, depth, proximity to woody debris, hydraulic gradients, and in situ concentrations and isotopic production rates.

## Methods, data collection, and structure

- Push-pull isotope-tracer experiment: injection of 15N-labelled nitrate into the riverbed and sequential porewater sampling to quantify production of 29N2 and 30N2 via mass spectrometry.
- Pre-injection background measurements: NO2, NO3, NH3, PO4, chloride, oxygen (O2), pH, temperature, Fe(II), dissolved organic carbon (orgC), 15N2, CH4, and N2O.
- Sample handling: nutrient samples filtered (0.45 µm) and frozen at -20°C until analysis.
- Piezometer metadata: coordinates (lat/long), piezometer ID, proximity to woody debris (1m LOW coded as y/n), screened-depth (Depth and True depth in cm), vertical hydraulic gradient (head) calculated from inside/outside water levels, and water depth from river surface to the riverbed.
- In situ measurements and calibrations:
  - O2: measured with microelectrode in porewater; calibration and contamination corrections applied (estimated 10 µM possible contamination, subtracted).
  - pH and temp: measured in porewater prior to 15N injection.
  - NO2, NO3, NH3, PO4: automated colorimetry (with inline cadmium reduction for NOx where applicable).
  - Cl: ion-selective electrode analysis.
  - CH4 and N2O: GC-FID and GC-ECD with headspace methods.
  - Fe(II): phenanthroline colorimetric method with filtration to preserve reduced iron.
  - orgC: total organic carbon analyzer.
- Data coding and quality markers:
  - 0 indicates below detection limit.
  - ND indicates no data collected or sample lost.

## Key variables and data structure

- Spatial/time identifiers:
  - month: Nov, Feb, Apr, Jul (2014/2015)
  - lat, long: coordinates of each piezometer
  - peizo: piezometer ID
- Sampling/location metadata:
  - 1m of LOW: whether the piezometer is within 1 m of a large woody debris structure (y/n)
  - Depth, True depth: screened mid-point depth below riverbed (cm)
  - head: vertical hydraulic gradient (m)
  - water depth: vertical depth from river surface to riverbed interface
- Chemical and physical measurements (pre-injection and/or per-sample):
  - O2adj, O2adj%: dissolved oxygen concentration and saturation
  - pH, temp: porewater pH and temperature
  - NO2, NO3, NH3, PO4: nitrite, nitrate, ammonium, soluble reactive phosphorus
  - Chloride: chloride concentration
  - CH4, N2O: methane and nitrous oxide concentrations
  - Fe II: reduced iron
  - orgC: dissolved organic carbon
  - p15N2: in situ rate of 15N2 production (nM N L-1 h-1)
- Isotope and process rates:
  - Denitrification: in situ rate of 15N2 production via denitrification (nM N L-1 h-1)
  - Anammox: in situ rate via anammox (nM N L-1 h-1)
  - DNRA: in situ rate of 15N-NH3 production via DNRA (nM N L-1 h-1)
  - tot 15n: sum of denitrification, anammox, and DNRA
  - qN2: proportion of 15N-labelled N2 in produced N2
  - qN2O: proportion of 15N-labelled N2 in produced N2O
  - %Anammox, %DNRA, %Denitrification: percentage contributions to total 15N production
- Calculations and model outputs:
  - 29N2 and 30N2 production determined from mass-spectrometry data; aN2 calculated from beam areas and calibration factors
  - P29 and P30: production rates derived from linear trend of aN2 over time
  - Detection limits for 29N2 and 30N2 reported
  - Proportions and rates derived from isotope data and standard corrections (Risgaard-Petersen et al., Trimmer et al., etc.)

## Calculations and interpretation

- Isotope pairing technique (IPT) approach:
  - 15N-nitrate injected; production of 29N2 and 30N2 used to quantify denitrification, anammox, and DNRA
  - Rates computed by linear regression of 29N2/30N2 production over time
  - Denitrification, anammox, and DNRA rates expressed as nano-moles N per liter per hour
- Data products:
  - tot15n summarises total microbial N2-production-driven nitrate reduction
  - qN2 and qN2O quantify the fraction of 15N-label in produced N2 and N2O
  - %Anammox, %DNRA, %Denitrification indicate relative contributions of each pathway
- Detection limits and quality:
  - LODs specified (e.g., ~0.003 µM 29N2 L-1 h-1; ~0.009 µM 30N2 L-1 h-1)
  - Background corrections for O2 contamination applied; some data flagged as 0 or ND accordingly

## Data quality, governance, and accessibility notes

- Data are time-stamped across seasonal campaigns; extensive metadata accompanies measurements, enabling reuse and cross-study comparisons.
- Readiness for data sharing is aided by explicit units, instrumentation details, calibration procedures, and referenced methods.
- Potential data challenges highlighted:
  - Occurrence of non-detections (0) and missing data (ND)
  - Complexity of transforming multi-parameter field data into integrated process rates
  - Need for clear documentation of metadata (e.g., depth definitions, head calculations, measurement timing)

## References and methodological context

- Shelley, F., Klaar, M., Krause, S., & Trimmer, M. Enhanced hyporheic exchange flow around woody debris does not increase nitrate reduction in a sandy streambed. Biogeochemistry (2017).
- Lansdown, K. et al. Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed. Environ. Sci. Technol. (2014).
- Sanders, I. et al. Emission of methane from chalk streams has potential implications for agricultural practices. Freshwater Biology (2007).
- Yamamoto, S., Alcauskas, J.B., & Crozier, T.E. Solubility of methane in distilled water and seawater. J. Chem. Eng. Data (1976).
- Weiss, R. & Price, B. Nitrous oxide solubility in water and seawater. Mar. Chem. (1980).
- Risgaard-Petersen et al. (1995, 2003) and Trimmer et al. (2006) methodological references for isotope-based measurements of DNRA, denitrification, and anammox.

## Takeaways for monitoring-framework authors

- Demonstrates a comprehensive, multi-parameter field monitoring design that yields process-level rates (denitrification, anammox, DNRA) from in situ measurements.
- Showcases rigorous metadata capture (spatial, depth, hydrology, proximity to woody debris, in situ conditions) essential for data governance and reuse.
- Highlights data-quality challenges and transparent handling of non-detections, detection limits, and contamination corrections.
- Provides a concrete template for integrating hydrological, chemical, and isotopic data to inform policy-relevant assessments of nitrogen cycling and nitrate attenuation in riverbeds.
- Emphasises the importance of detailed documentation and cross-referencing methodological sources to support reproducibility and comparability across monitoring programs.