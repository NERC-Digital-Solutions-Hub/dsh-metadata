# Supporting information for 'High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017- Sept 2018)'

## Overview
- Dataset from Bow Brook, a headwater tributary to the River Loddon in Hampshire, monitored near its confluence with the Loddon.
- Timeframe: hourly high-resolution data from 08/09/2017 to 09/09/2018; daily water quality samples from 08/09/2017 to 08/09/2018; storm samples from 11/09/2017 to 21/01/2018 with intermittent events.
- Data types include: high-frequency sensor data, daily and storm water quality data, full UV–Vis spectral scans, and pesticide analyses.
- Data volumes: six CSV files with 366 daily samples, 207 storm samples, 8,332 high-frequency sensor records, 8,364 high-frequency optical scans, 366 daily optical scans, and 194 storm optical scans.

## Data Access and Citation
- Access via DOI: https://doi.org/10.5285/331659d7-da72-48a2-9b52-63c003557990
- Recommended citation:
  Hawkins, C.E; Kelly, T.J.; Loewenthal, M.; Smith, R.; Dudley, A.; Leggatt, A.; Dowman, S.; Oliver, R.G.; Collins, C.D.; Clark, J.M. (2019). High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017-Sept 2018) . NERC Environmental Information Data Centre. (Dataset).

## Experimental Design and Sampling Regime
- Location: monitoring equipment near the confluence of Bow Brook and the River Loddon, Sherfield-on-Loddon, Hampshire, in an agricultural catchment.
- Sampling cadence:
  - High-frequency water quality and flow: hourly from 00:00 GMT on 08/09/2017 to 00:00 GMT on 09/09/2018.
  - Daily water quality samples: collected at 09:00 GMT from 08/09/2017 to 08/09/2018.
  - Storm water quality samples: hourly during storm events, from 11:00 GMT on 11/09/2017 to 08:00 GMT on 22/01/2018.
- Data gaps: missing samples due to equipment breakdown from temperature-related freezes and/or measurement errors; turbidity measurements began on 10 October 2017 due to a delay in turbidity meter arrival.

## Collection, Laboratory and Analytical Methods and Instrumentation
- In-field data collection:
  - Water sampling: hourly extraction with a peristaltic pump through two flow-through cells.
  - Instruments: TriOS OPUS UV/VIS Spectral Analyser (full spectral scan 200–800 nm, 2.2 nm per pixel) and YSI 6600 V2-2 multi-parameter sonde (turbidity, ammonium, pH, conductivity, temperature, dissolved oxygen).
  - Flow measurement: Sontek IQ Doppler flow gauge at the sampling point.
  - Maintenance: sonde calibrated monthly; UV-Vis analyser cleaned weekly (sensor removed from flow cell for cleaning).
  - Data transfer: UV spectral data downloaded biweekly via TriOS G2 interface.
- Sample collection:
  - Daily and storm samples: two ISCO 6712 autosamplers; 300 mL samples in 350 mL glass bottles to minimize pesticide sorption to plastic.
  - Storm sampling: hourly samples for 24 hours when storm conditions were met; triggered by precipitation and shifts in conductivity/turbidity indicators.
- Laboratory analyses:
  - pH: Mettler Toledo pH meter; calibration with pH 4 and pH 7; drift checks every 5 samples.
  - Conductivity: Mettler Toledo EasyFive; calibration with 1413 µS standard at 25°C; drift checks every 5 samples.
  - Turbidity: Hanna HI-93703; calibrated with 0, 10, and 500 FTU standards; immediate reading and a second reading after 5 minutes; blanks every 10 measurements.
  - UV–Vis scans: Jenway 7315 spectrophotometer; both unfiltered and filtered (0.7 µm) samples; baseline and drift checks with ultra-pure water blanks.
  - Filtering: suspended sediments via GF/F filters; gravimetric calculation for TSS.
  - NPOC (non-purgeable organic carbon): processed after acidification and filtration; purging to remove inorganic carbon; analysis with Shimadzu TOC-L; dilution factor applied.
  - Pesticide analysis: daily and storm samples analyzed by Affinity Water Ltd. using Agilent 6490 LC–MS/MS; quantification for 12 pesticides with detection limits ~0.01 µg/L.
    - Pesticides included: 2-4-D, Bentazone, Carbendazim, Carbetamide, Chlorotoluron, Clopyralid, MCPA, Mecoprop, Metaldehyde, Propyzamide, Quinmerac, Metazachlor.
- Sample handling and storage:
  - Samples stored at 4°C on return to the laboratory.
  - Filtration and analyses conducted within 48 hours of collection.

## Data Structure and Recorded Values
- Data files:
  - DailyWaterQualityData.csv (366 samples)
  - StormWaterQualityData.csv (207 samples)
  - HighFrequencySensorDataFlowandSonde.csv (8,332 samples)
  - HighFrequencyDataOpticalScan.csv (8,364 samples)
  - DailyOpticalScansBlankCorrected.csv (366 samples)
  - StormOpticalScansBlankCorrected.csv (194 samples)
- Key fields and units (highlights):
  - In-field flow (m3 s-1), depth (m), mean velocity (m s-1), area (m2), total volume (liters)
  - In-field optical 254 nm (absorbance units, AU); field turbidity (NTU); conductivity (µS cm-1); pH; ammonium (mg L-1); temperature (°C)
  - Laboratory measurements: pH, conductivity (lab), turbidity (FTU), TSS (g L-1), NPOC (mg L-1)
  - UV–Vis data: full spectral scans (unfiltered and filtered to 0.7 µm) in AU
  - Pesticide data: concentrations of 12 pesticides and totals (µg L-1)
- Notes on data quality and completeness:
  - Missing data due to equipment temperature-related failures and measurement errors.
  - Turbidity measurements began later (10 Oct 2017) due to equipment availability.
  - Storm optical scans: some dates missing or partially analyzed; some storm events represented with non-sequential sample naming to reflect sampling times.

## Data Quality, Gaps and Metadata
- Calibrations and drift checks documented for pH, conductivity, and other in-field instrumentation.
- Cleaning and maintenance routines described for UV–Vis and sensors to ensure data integrity.
- Metadata embedded in the file headers and method sections provide context for units, dates, times, and sample handling.
- Caution advised when combining datasets due to missing periods and event-driven sampling (daily vs. storm vs. high-frequency records).

## Potential Uses and Reuse Guidance
- Suitable for hydrology–water quality time series analyses, event-based (storm) loading assessments, and multivariate investigations (e.g., UV–Vis spectral features correlated with turbidity, organic carbon, and pesticide occurrences).
- Useful for method comparison studies and data integration with other catchment datasets, provided adherence to the documented sampling regimes, units, and calibration notes.
- Proper attribution required via the provided data citation when using the dataset.