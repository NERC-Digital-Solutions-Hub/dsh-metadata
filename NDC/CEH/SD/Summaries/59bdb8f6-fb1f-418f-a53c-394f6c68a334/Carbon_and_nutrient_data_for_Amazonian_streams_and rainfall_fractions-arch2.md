# Sampling Regime

- Purpose and scope
  - Provides standardized data to monitor fluvial carbon (DIC, δ13C-DIC, DOC, POC) and related nutrients in a tropical rainforest catchment.
  - Data intended for environmental health assessment and policy performance over time, with QA/QC and clear documentation of methods.

- Study area and sampling sites
  - Western Amazonian basin, Tambopata National Reserve, Madre de Dios region, Peru (approx. 12°49' S, 69°16' W).
  - Sampling points include two small streams: MT (Main Trail) and NC (New Colpita); and two rivers: LT (La Torre) and TP (Tambopata).
  - Upstream catchment extents: LT ~2000 km2; TP ~14,000 km2. Stream sampling points are 40–80 m wide (LT) and ~200 m wide (TP) at the sampling location.
  - MT is seasonally active; NC flows during the dry season; MT dries up in the dry season, limiting sampling during Sep–Nov 2011.

- Temporal coverage and campaigns
  - Field campaigns: Feb–Apr 2011; Sept–Dec 2011; Mar–May 2012.
  - Rainfall fraction sampling: Apr–May 2012.
  - Note: MT sampling was not possible Sept–Nov 2011 due to drying, affecting MT data for that period.

- Data types collected
  - Aquatic carbon: DIC (mg/L), δ13C-DIC (per mil), DOC (mg/L), POC (mg/L).
  - Nutrients and ions: Ca, Mg, K, Na (mg/L), total dissolved P (totP, μg/L), Si (mg/L).
  - Rainfall fractions: DIC, δ13C-DIC, DOC, POC, Ca, Mg, K, Na for Rain water, Throughfall, Stemflow, and Overland flow.
  - Throughfall and stemflow data collected at designated collectors and trees, plus overland flow measurements near two streams.

- Sampling and analytical methods
  - DIC and δ13C-DIC: pre-acidified exetainers, headspace method, triplicate exetainers per sample; isotopic composition via Gas Bench/Delta V Plus.
  - DOC: filtered water, acidified to pH ~3.9, degassed, measured by combustion (TOC analyzer).
  - POC: loss on ignition of filter papers after drying and combustion; assumed OC = 50%.
  - Ca and Mg: Atomic Absorption Spectrometry (AAS) with nitrous oxide flame at high temp.
  - K and Na: Flame photometry.
  - totP: colorimetric phosphomolybdate method with ascorbic acid reduction (blue color read at 880/700 nm).
  - Si: colorimetric heteropoly blue molybdosilicate method (read at 650 nm).
  - Rainfall fractions and associated nutrients analyzed similarly on subset samples.

- Quality control and data integrity
  - DIC: drift correction standards ~every 10 samples; randomised sample order; replication checks.
  - DOC: calibration drift checks; standards split across batch ends for consistency.
  - Cations (Ca, Mg): mid-range and blank checks; replicate analyses ensured instrumental stability.
  - Si and totP: repeated standard measurements to monitor stability.
  - Missing data are recorded as NA.

- Data structure and contents
  - Two CSV datasets: “Amazon streams C and nutrients” and “Amazon rainfall fractions C and nutrients.”
  - Streams and Rivers dataset: 14 columns; Rainfall fractions dataset: 12 columns.
  - Key columns (streams and rivers): Time (hh:mm:ss), Date (dd/mm/yyyy), Type (stream or river), Site (MT, NC, LT, TP), CollectorID/Tree (TF numbers, SF tree names, OF stream), DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si.
  - Key columns (rainfall fractions): Time, Date, Type (TF, SF, OF, Rainwater), Site/Collector (EI for Rainwater, tree-based IDs for stemflow, etc.), DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si.
  - Data completeness: Some records not analysed (NA). Values are within method detection ranges.

- Sampling details for tree stemflow and overland flow
  - Eight trees sampled for stemflow with diverse species (e.g., Inga sp., Pseudolmedia sp., Virola sp., Oenocarpus sp., Clarisia racemosa, Tachigalia sp., Iriartea deltoidea).
  - Tree diameters ranged across individuals (example diameters provided in Table 3).
  - Overland flow collected via half-cut plastic tubing to capture flow from the stream bank into receiver buckets; not designed to quantify volume, but for compositional analysis.

- References and methodological context
  - Methods and QA referenced to established guidelines (e.g., American Public Health Association, 1999; Waldron et al., 2014).
  - Previous data submissions linked to DOIs for DIC, DOC, and POC data to support traceability and integration.

- Relevance for environmental monitoring and data use
  - The dataset provides standardized, quality-controlled measurements of carbon and nutrient dynamics in tropical freshwater systems, suitable for trend analysis, cross-site comparisons, and integration with other environmental datasets.
  - Clear documentation of sampling regime, analytical approaches, QA measures, and data structure supports reproducibility and data sharing, addressing common monitoring challenges of data value and accessibility.