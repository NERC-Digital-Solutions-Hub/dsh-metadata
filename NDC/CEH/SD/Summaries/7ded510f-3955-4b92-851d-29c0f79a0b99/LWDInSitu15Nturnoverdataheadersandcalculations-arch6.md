# General information: This dataset contains results from in situ field measurements of riverbed nitrogen transformations in the Hammer Stream (latitude = 51.01085722 N, longitude = 0.801498333 W), a sandy tributary of the River Rother in West Sussex, UK, the results of which have been published in Shelley et al. (2017).

## Overview
- In situ measurements of riverbed nitrogen transformations (denitrification, anammox, DNRA) in the Hammer Stream.
- Methods align with prior work (Lansdown et al. 2014; Shelley et al. 2017) using a push-pull approach with 15N-labelled nitrate.
- Aimed at quantifying in situ rates and the relative contributions of pathways to N2 production.

## Study site and sampling regime
- Location: Hammer Stream, a sandy tributary of the River Rother, West Sussex, UK.
- Sampling periods: November 2014; February, April, and July 2015.
- Sampling setup: main piezometer network in the riverbed; porewater and water-column measurements collected before and after 15N-nitrate injections.
- Pre-injection background water samples collected to measure NO2, NO3, NH3, PO4, Cl-, O2, pH, temperature, Fe(II), organic carbon, 15N2, and CH4/N2O.
- Sample preservation: nutrients filtered (0.45 µm) and frozen at -20°C until analysis.
- Measurement focus: rates of in situ nitrate processing and partitioning of N2 production among denitrification, anammox, and DNRA.

## Measurements and data collection
- Piezometer and hydrology: longitude, latitude, piezometer ID, proximity to large woody debris, screen depth (Depth, True depth), vertical hydraulic head (head), water depth.
- Porewater chemistry (pre-injection): O2 concentration (O2adj, µM), O2 saturation (O2adj%, %), pH, temperature (temp, °C), NO2, NO3, NH3, PO4 (all in µM), chloride (milli-M), CH4 (µM), N2O (nM), Fe(II) (µM), organic carbon (orgC, mg/L).
- p15N2: in situ rate of total 15N2 production (nM N L-1 h-1) from injected 15N-nitrate; used to derive nitrogen transformation rates.
- Instrumental details: methods for pH, O2 measurement, and nutrient analyses described; samples prepared and analyzed with appropriate blanks, calibrations, and quality controls.

## Data columns and header descriptions
- Time/season: month (Nov, Feb, Apr, Jul).
- Spatial/physical: long, lat, peizo, 1m of LOW (y/n), Depth (cm), True depth (cm).
- Hydrology: head (m), water depth (depth from surface to riverbed).
- Chemical measurements: O2adj (µM), O2adj% (% saturation), pH, temp (°C), NO2, NO3, NH3, PO4 (each in µM), Chloride (milli-M), CH4 (µM), N2O (nM), Fe II (µM), orgC (mg/L).
- Isotopic and rate variables: p15N2 (nM N L-1 h-1), Denitrification (nM N L-1 h-1), Anammox (nM N L-1 h-1), DNRA (nM N L-1 h-1), tot 15n (nM N L-1 h-1), qN2, qN2O (15N-labelling fractions).
- Proportions: %Anammox, %DNRA, %Denitrification (percent contributions to total N2 production).
- Data notes: values set to 0 if below detection limit (LOD); ND indicates not collected or sample lost.

## Calculations and derived metrics
- Denitrification, Anammox, DNRA: derived from 15N2 production measurements following injection of 15N-nitrate; rates reported per liter of porewater per hour.
- tot 15n: sum of denitrification, anammox, and DNRA rates.
- qN2, qN2O: fractions of 15N in produced N2 and N2O, determined by mass spectrometry.
- %Anammox, %DNRA, %Denitrification: partitioning of total N2 production among pathways, enabling pathway contribution analysis.
- Mass spectrometry: 29N2 and 30N2 production used to compute in situ rates; calculations rely on calibration factors, sample volumes, and background corrections.
- Detection limits: approximately 0.003 µmol 29N2 L-1 h-1 for 29N2 and 0.009 µmol 30N2 L-1 h-1 for 30N2.

## Data quality and handling notes
- Data quality details provided for measurement methods (e.g., accuracy, limits of detection, calibration procedures).
- Background corrections applied to O2 measurements to account for contamination during sample handling.
- NO3 is calculated as NOx minus nitrite (NO2) using inline cadmium reduction for NOx analysis.
- Some measurements are reported with detection-limitation flags (0 for below detection; ND for not collected or lost samples).

## Outputs and potential applications
- Primary outputs: in situ rates of nitrogen transformation processes and the relative contributions of denitrification, anammox, and DNRA across piezometers and seasons.
- Use cases: integration with hydrological or ecosystem data, development of data products (dashboards, self-serve analyses) for stakeholders, and comparative studies of nitrate processing in permeable sandy streambeds.
- Data provenance and references provided to facilitate replication and cross-study comparisons.

## References
- Shelley, F., Klaar, M., Krause, S., & Trimmer, M. 2017. Enhanced hyporheic exchange flow around woody debris does not increase nitrate reduction in a sandy streambed. Biogeochemistry.
- Lansdown, K. et al. 2014. Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed. Environ. Sci. Technol.
- Sanders, I. et al. 2007. Emission of methane from chalk streams has potential implications for agricultural practices. Freshwater Biology.
- Yamamoto, S. et al. 1976. Solubility of methane in distilled water and seawater. J. Chem. Eng. Data.
- Weiss, R. & Price, B. 1980. Nitrous oxide solubility in water and seawater. Mar. Chem.
- Risgaard-Petersen, N. et al. 1995/2003. Isotope methods for measuring nitrogen transformations; application in sediments with anammox and denitrification.
- Thamdrup, B. & Dalsgaard, T. 2000. Fate of ammonium in anoxic sediments. Geochim. Cosmochim. Acta.
- Trimmer, M. et al. 2006. Direct measurement of anaerobic ammonium oxidation (anammox) and denitrification in intact sediment cores. MEPS.