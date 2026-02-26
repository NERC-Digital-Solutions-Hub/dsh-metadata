# Methodology

- Purpose and scope
  - Long-term river water chemistry dataset from the River Frome at East Stoke flow gauging station.
  - Samples filtered on return to the lab within one hour and analysed rapidly (usually within a few days, always within one week) to minimise sample stability errors.
  - Data omissions occur when analysis could not be completed in time due to instrument failure, QC issues, or staffing limits.
  - Methodologies for determinands changed over time; old and new methods run in parallel for 3–6 months during transitions to ensure comparability.

- Sampling and data handling
  - Sampling point: main flow at East Stoke flow gauging station.
  - Sample handling: immediate filtration on return to laboratory; analyses conducted promptly with time constraints.
  - Longitudinal data: 44-year duration with method-change overlaps to maintain continuity; changes documented under each determinand.

- Nitrogen analysis (NO3-N / TON)
  - 1965–1986: diphenyl sulphonic acid colorimetric method (APHA 1965).
  - 1986–2004: NO3-N and NO2-N (TON) measured by Flow Injection Analysis after cadmium reduction; colorimetric detection.
  - 2006 onward: nitrate-N measured by ion chromatography (Dionex DX500).
  - TON approximately equates to NO3-N in most rivers; cadmium reduction method yields slightly higher results (0.08–0.12 mg/L) than the later method.
  - Nitrite alone generally < 0.05 mg/L.
  - Note: data labeled as NO3-N or nitrate; comparability maintained via parallel runs during transitions.

- Phosphorus analysis
  - Soluble reactive phosphorus (SRP) via molybdenum blue colorimetry.
  - 1965–1986: manual reagent addition and spectrophotometric analysis; automation in 1986 via FIAStar 5012.
  - 1965–2004: SRP analysed within 6 hours of sampling (minimising instability).
  - 2004–2006: LOCAR program; SRP analysis conducted by Thames Water laboratories.
  - 2007–2009: CEH Wallingford, SRP analysed within 24 hours using a Seal AA3.
  - Total phosphorus (TP) and total dissolved phosphorus (TDP) determined by persulfate digestion and spectrophotometric detection; during LOCAR (2004–2006) TP analyzed by ICP-OES.
  - Noted inconsistencies between pre-2004 CEH data, LOCAR TP data, and later data; a two-year portion (River Frome at East Stoke in 2004–2006, analysed by CEH) was omitted due to significant deviation.

- Dissolved reactive silicon analysis
  - Determined on filtered samples (0.45 μm) by molybdate colorimetry, forming silicomolybdenum blues measured at 810 nm.
  - 1986 automation via FIAStar 5012; 2006 onward via Seal Auto Analyser 2.
  - Reduction reagent updated from metol-sulphite to tin(II) chloride (1998).

- Major cations and anions
  - Na, K, Mg, Ca: measured by atomic absorption spectroscopy (1965–1996); 1997–2009 by ion chromatography.
  - Sulfate and chloride: measured by ion chromatography from 1997 onward.

- pH
  - Measured on unfiltered samples within 6 hours of sampling.
  - 1965–1995 and 2006–2009: pH probe with standard buffers.
  - 1996–2004: Metrohm 702 Autotitrator with Aquatrode electrode; 2-minute equilibration prior to measurement.

- Conductivity
  - Measured on unfiltered samples within 6 hours using a handheld conductivity meter; 2-minute equilibration prior to measurement.

- Alkalinity
  - Titration with hydrochloric acid; 1996–2004: Metrohm 702 Autotitrator; alkalinity calculated with a Gran titration plot.

- Suspended solids
  - Filter known mass of river water (~1 kg) through pre-dried GF/C filters; dry to constant weight at 70°C for 24 h.

- Data quality, standards, and metadata implications for GIS
  - Quality control includes rapid analysis, parallel method testing during transitions, and documentation of methodological changes.
  - Data comparability across time depends on documenting method changes, parallel runs, and any known biases (e.g., NO3-N vs TON differences, TP method discrepancies).
  - Data availability may be uneven due to lab changes, handling times, and historical laboratory practices; some portions may require metadata notes or caution when visualising long-term trends.

- Practical GIS considerations
  - When mapping time-series trends, annotate periods with methodological changes or data omissions.
  - Use consistent units and clearly label determinands (e.g., NO3-N, SRP, TP) and their measurement method per time window.
  - Include metadata on sample stability windows, analysis delays, and any identified biases between methods to support accurate interpretation of map-based visuals.