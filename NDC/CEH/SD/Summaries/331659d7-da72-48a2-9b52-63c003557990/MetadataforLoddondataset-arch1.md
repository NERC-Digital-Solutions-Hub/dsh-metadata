# Supporting information for 'High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017- Sept 2018)'

- Provides experimental details and data descriptors to accompany high-resolution water quality and flow data collected from Bow Brook (headwater of the River Loddon) in Hampshire, Sept 2017–Sept 2018.
- Data are available via a DOI with a formal citation required for reuse.

## Study site and sampling regime

- Location: Bow Brook near its confluence with the River Loddon at Sherfield-on-Loddon, in an agriculturally influenced catchment.
- Monitoring location: Close to the confluence with the Loddon.
- Temporal coverage:
  - High-resolution (hourly) water quality and flow data: 08/09/2017 to 09/09/2018.
  - Daily water quality samples: 09:00 each day from 08/09/2017 to 08/09/2018.
  - Storm water quality samples: hourly during storm events from 11/09/2017 to 22/01/2018.
- Data gaps: Some samples missing due to equipment breakdown or measurement errors; turbidity measurements began 10 October 2017 due to a delay in the meter arrival.

## Data collection, instrumentation and sampling methods

- In-field equipment:
  - Peristaltic pump system with two flow-through cells.
  - TriOS OPUS UV/VIS Spectral Analyser for full spectral scans (200–800 nm, 2.2 nm per pixel).
  - YSI 6600 V2-2 multi-parameter Sonde (turbidity, ammonium, pH, conductivity, temperature, dissolved oxygen).
  - Sontek IQ flow gauge for river flow and height at the sampling point.
- Maintenance and calibration:
  - Sonde calibrated monthly.
  - UV/Vis analyser cleaned weekly; cleaning involves removing sensor from flow cell and using cotton buds, ultra-pure water, kitchen roll.
  - UV-Vis baselines drift-checked with blanks.
- Sampling protocol:
  - Daily samples collected with two ISCO 6712 autosamplers; 300 mL of sample in 350 mL glass bottles to reduce pesticide sorption to plastics.
  - Daily sampler set to 9:00 a.m.; storm sampler activated to take hourly samples for 24 hours during storm conditions.
  - Samples kept cold (4°C) on return to the lab and filtered within 48 hours.
- Analytical workflow (lab analyses):
  - pH, conductivity, turbidity, and UV-Vis spectral scans (unfiltered and filtered 0.7 µm) using laboratory instruments.
  - Suspended solids (TSS) by gravimetric filtration (GF/F filter) and calculating concentration from filtered mass and sample volume.
  - NPOC (non-purgeable organic carbon) by purging inorganic carbon prior to TOC measurement; filtered samples prepared and analyzed with dilution considerations.
  - Pesticides: 12 pesticides quantified by LC-MS/MS (Agilent 6490) through Affinity Water Ltd., with LOQ around 0.01 µg/L.
- Quality controls in the lab:
  - pH and conductivity meters calibrated with standard buffers and solutions.
  - Turbidity meter calibrated with FTU standards; measurements taken after a settle period to match Sonde readings.
  - Blank corrections and drift checks performed for UV-Vis and optical scans.

## Nature and units of recorded data and data structure

- Six CSV data files:
  - DailyWaterQualityData.csv – 366 daily samples
    - Variables include date, flow (m3 s-1), depth (m), 254 nm field absorbance (AU), turbidity (NTU), conductivity (µS cm-1), pH (field), ammonium (mg L-1), lab pH and conductivity, lab turbidity (5 min and 0 min), 254 nm lab absorbance, TSS (g L-1), NPOC (mg L-1), 12 pesticides (µg L-1), total pesticides (µg L-1), and EU limits.
  - StormWaterQualityData.csv – 207 samples
    - Similar fields as daily data, with per-storm structure including 254 nm, turbidity (5 min and 0 min), pH, conductivity, ammonium, TSS, NPOC, 12 pesticides, total pesticides, and EU limits; also includes per-storm event assignments.
  - HighFrequencySensorDataFlowandSonde.csv – 8332 samples
    - In-field Sontek flow data: FLOW (m3 s-1), stage (m), mean velocity (m s-1), total volume (L), area (m2), depth (m), index velocity (m s-1), temperature (°C).
    - In-field Sonde data: DO, conductivity (µS cm-1), pH, ammonium (mg L-1), turbidity (NTU), DO percentage, and related measurements.
  - HighFrequencyDataOpticalScan.csv – 8364 samples
    - Raw optical spectra from TriOS OPUS: DateTime, and absorption across 197.976–720.86 nm (AU).
  - DailyOpticalScansBlankCorrected.csv – 366 samples
    - Blank-corrected daily UV-Vis scans (200–800 nm) in AU; notes about missing dates (18/01/18, 08/02/18, 12/02/18, 18–30/07/18).
  - StormOpticalScansBlankCorrected.csv – 194 samples
    - Blank-corrected storm scans (200–800 nm) in AU; includes notes on large storm event timing and missing data for certain dates; storm sample naming based on sampler trigger times.
- Data accessibility and citation:
  - Data accessible at the provided DOI; users should cite Hawkins et al. (2019) in NERC Environmental Information Data Centre when using the dataset.

## Data quality, completeness and caveats

- Data gaps due to equipment temperature-related failures and measurement errors.
- Turbidity measurements began later (10 Oct 2017) due to a delayed instrument arrival.
- Storm data includes periods or events with incomplete sampling; storm sample naming corresponds to sampler activation times rather than exact calendar dates.
- Optical scans require drift correction for absolute interpretation; blank-corrected scans are provided to mitigate drift.

## How this data can support analysis

- Enables correlations between hydrology (flow, depth, velocity) and water quality/optical properties (pH, conductivity, turbidity, ammonium, DOC/NPOC, pesticides, UV-Vis features).
- Allows assessment of storm-driven pulses in pesticides, turbidity, TSS, and DOC.
- Facilitates spectral analyses to relate UV-Vis features to dissolved/particulate organic matter and potential pesticide indicators.
- Supports comparisons against regulatory limits for individual and total pesticides post-treatment.
- Provides a robust metadata framework for data provenance, reproducibility and data sharing in environmental data portals.