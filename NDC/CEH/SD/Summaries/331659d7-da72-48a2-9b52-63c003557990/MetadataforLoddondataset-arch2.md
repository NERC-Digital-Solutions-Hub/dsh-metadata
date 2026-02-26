# High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017- Sept 2018)

## Overview
- A comprehensive dataset from Bow Brook, a headwater tributary to the River Loddon in Hampshire, containing high-resolution water quality and flow data, plus daily and storm water samples, collected Sep 2017–Sept 2018.
- Designed to support consistent environmental monitoring and enable scrutiny of environmental health and policy performance over time.

## Data access and citation
- Data available at: https://doi.org/10.5285/331659d7-da72-48a2-9b52-63c003557990
- Citation: Hawkins, C.E; Kelly, T.J.; Loewenthal, M.; et al. (2019). High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017-Sept 2018). NERC Environmental Information Data Centre. (Dataset).

## Experimental design and sampling regime
- Site: Bow Brook near the confluence with the River Loddon, Sherfield-on-Loddon, in a predominantly agricultural catchment.
- Monitoring setup placed close to the confluence with the River Loddon.
- Sampling schedule:
  - High-resolution water quality and flow: hourly from 00:00 GMT on 08/09/2017 to 00:00 GMT on 09/09/2018.
  - Daily water quality samples: at 09:00 GMT from 08/09/2017 to 08/09/2018.
  - Storm water quality samples: hourly during storm events from 11/09/2017 to 22/01/2018.
- Data gaps: missing data due to equipment breakdown (temperature-related freezing and/or measurement errors).
- Turbidity measurements began on 10 October 2017 due to a delay in turbidity meter arrival.

## Collection, laboratory and analytical methods and instrumentation
- In-field sampling hardware:
  - Peristaltic pump with two flow-through cells.
  - TriOS OPUS UV/VIS Spectral Analyser: full spectral scan 200–800 nm (2.2 nm per pixel).
  - YSI 6600 V2-2 multi-parameter Sonde: turbidity, ammonium, pH, conductivity, temperature, dissolved oxygen.
  - Sontek IQ flow gauge (Doppler): river flow and height at sampling point.
- Equipment maintenance/calibration:
  - Sonde calibrated monthly; UV analyser cleaned weekly (disassembly required for cleaning).
  - Spectral data downloaded biweekly via TriOS G2 interface.
- Sample handling:
  - Daily samples and hourly storm samples collected with two ISCO 6712 autosamplers.
  - Bottle types: 300 mL glass bottles (from Oct 9, 2017 onward) to minimize pesticide sorption; prior use of plastic bottles.
  - Daily sampler: fixed at 09:00; storm sampler activated via telemetry for storm conditions.
  - Samples returned to the lab under refrigeration (4°C) and filtered within 48 hours.
- Laboratory analyses:
  - pH: Mettler Toledo pH meter; calibrated with pH 4 and pH 7 buffers; drift checks every 5 samples.
  - Conductivity: Mettler Toledo EasyFive; calibrated with 1413 μS standard at 25°C; drift checks every 5 samples.
  - Turbidity: Hanna HI-93703; calibrated with 0, 10, 500 FTU standards; measurements taken immediately and after a 5-minute settle.
  - UV-Vis scans: Jenway 7315 Spectrophotometer; scans unfiltered and filtered to 0.7 μm; baseline and drift checks with ultrapure water blanks.
  - Filtering and sample prep: suspended sediments via GF/F filters; NPOC (non-purgeable organic carbon) methodology with acidification and purging to remove inorganic carbon.
  - Pesticide analysis: Affinity Water Ltd. lab using Agilent 6490 LC-MS; 12 pesticides quantified; LOQ around 0.01 μg/L; includes 12 specific pesticides (e.g., 2-4-D, Bentazone, Carbendazim, …, Metazachlor).
- Data are complemented by six CSV files detailing field and laboratory measurements (see data records).

## Data records and structure
- DailyWaterQualityData.csv — 366 samples
  - Variables include: Date, Flow (m3 s-1), Depth (m), 254 nm field absorbance (AU), Turbidity field (NTU), Conductivity field (μS cm-1), pH field, Ammonium field (mg L-1), lab pH, lab Conductivity (μS cm-1), Turbidity 5-min (FTU), Turbidity 0-min (FTU), 254 nm (AU), Total Suspended Solids (g L-1), NPOC (mg L-1), 12 individual pesticides (μg L-1), Total pesticides (μg L-1), Individual EU limits, Total EU limit.
- StormWaterQualityData.csv — 207 samples
  - Similar variables as DailyWaterQualityData, with storm-specific timing (date/time), totals for pesticides and EU limits.
- HighFrequencySensorDataFlowandSonde.csv — 8332 samples
  - Field data from Sontek IQ: FLOWDATE, FLOWTIME, FLOW (m3 s-1), STAGE (m), MEANVELOCITY (m s-1), TOTALVOLUME (L), DEPTH (m), INDEXVELOCITY (m s-1), AREA (m2), TEMP (°C)
  - In-field Sonde data: SONDEDATE, SONDETIME, SONDETEMP (°C), SONDECOND (μS cm-1), SONDEPH, SONDEAMMONIUM (mg L-1), SONDETURBIDITY (NTU), SONDE DOO-pcent (%), SONDE DOO-MGL (mg L-1)
- HighFrequencyDataOpticalScan.csv — 8364 samples
  - TriOS OPUS: DateTime, Date, Time, Absorption from 197.976 to 720.86 nm (AU)
- DailyOpticalScansBlankCorrected.csv — 366 samples
  - Blank-corrected optical scans for daily unfiltered samples; 200–800 nm, every 2 nm; notes on missing dates.
- StormOpticalScansBlankCorrected.csv — 194 samples
  - Blank-corrected optical scans for storm samples; 200–800 nm, every 2 nm; notes on missing data and storm event batching.

## Data quality, limitations and notes
- Data gaps due to equipment failures (temperature-related freezing, measurement errors) and missing storm data in certain events.
- Turbidity measurements in field began later (10 Oct 2017) due to instrument availability.
- Storm optical scan dataset includes intentional batching and some targeted suppression due to time constraints in analysis (e.g., 08/11/17 partial analyses).

## Relevance for Analysts Monitoring the Environment
- Enables longitudinal assessment of hydrology–water quality–pollutant (including pesticides) dynamics at a headwater catchment level.
- Supports integration with other datasets for holistic environmental health and policy performance evaluations.
- Provides standardized, QA-ready data with documented instrumentation, calibration, sample handling, and lab procedures to facilitate replication and comparative monitoring.
- Includes both high-frequency in-situ measurements and lab-validated chemical analyses, suitable for trend analysis, storm-event impact studies, and pesticide exposure assessments.