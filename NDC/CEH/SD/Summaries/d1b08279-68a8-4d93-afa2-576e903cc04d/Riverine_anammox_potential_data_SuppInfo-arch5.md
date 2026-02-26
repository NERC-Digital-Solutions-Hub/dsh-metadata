# General information: This dataset contains results from slurry incubations with 15N-labelled substrates.

- Scope
  - Results from slurry incubations using 15N-labelled substrates in both anoxic and oxic conditions.
  - Sediment types: clay, sand, and chalk, collected August 2013; measurements in September 2013.
  - Sites span rivers in the Hampshire Avon catchment (Clay, Sand, Chalk categories) with multiple replicates per river.
  - Incubations include reference (no 15N), control (biological activity inhibited), and time-series samples after addition of 15N-labelled substrates.
  - Results are presented as potentials (not absolute in-situ rates) and were conducted in the dark at room temperature.

- Experimental design
  - Anoxic slurries: 3 mL vials (1 mL sediment, 1 mL synthetic river water, N2 headspace).
  - Oxic slurries: 12 mL vials (2.5 mL sediment, 3 mL synthetic river water, air headspace).
  - N-amendments: injections of 14N or 15N-labelled substrates at specific target nitrate or ammonium concentrations (e.g., 100 µM nitrate for clay, 300 µM for sand, 500 µM ammonium for all types).
  - 15N-labelled tracers are 98 atom % 15N.
  - Anoxic slurries pre-incubated overnight before adding 15N tracers to remove ambient 14N nitrate.
  - Time-series sampling: approximately 0.5, 1, 2, 3, and 6 hours post-15N addition; some measurements include earlier/later time points and repeats.
  - Measurements include 15N-N2 production and related metrics via mass spectrometry.

- Data structure and column headers (high-level)
  - Data organized as a table with 42 columns and 46 rows (plus headers); values may be marked as BDL when below detection limits.
  - Key column groups include:
    - Sample metadata: site/river, sediment type, replicate, and precise site coordinates.
    - Time-series measurements: 15NOxT0, T1, T2, T3, T4, T5 representing 15N-labelled NOx concentrations over time in oxic slurries.
    - N2 production metrics: P29-15A, P30-15A, P29-15A14N, P30-15A14N, P29-15N, P30-15N, and total Atotal and ra (anammox contribution) calculations.
    - Proportions in N pools: FN-NH4+, FN-NOx, FN-N2 (fractions of 15N in ammonium, NOx, and N2 pools).
    - Oxic/control series: Oxicp15N-T0…T5 and Oxicp15Nrpt-T0…T5 (repeat measurements for testing nitrification relationships).
    - Ammonium and NOx references: AmmoniumRef and NOxRef (reference concentrations in oxic slurries).
    - Dissolved oxygen: O2Conc-T0, T1, T2, T3 for oxic slurries.
    - 15N labeling details and derived metrics (p15N, 15N-based calculations).
  - Notable: detailed header descriptions are provided for the first column and time-series points; all derived rates and proportions rely on published calculation formulas.

- Measurements, calculations, and interpretation
  - 15N-N2 production tracked via mass spectrometry; P29 and P30 denote 29N2 and 30N2 production, respectively; p15N is 15N-labelled N2 production (P29 + 2 × P30).
  - Headspace N2 and aqueous N2 concentrations are calculated using calibration factors, headspace beam areas, and Bunsen solubility coefficients; results scaled per gram of dry sediment.
  - Rates derived from time-series data using linear trend lines (nmol N2 g-1 dry sediment h-1).
  - Atotal (total denitrification-associated N2 production from 15N-nitrate) and ra (percent contribution of anammox to N2 production) calculated using Thamdrup & Dalsgaard methods; Dtotal derived from P30 and labeling factors.
  - Proportions (FN-NH4+, FN-NOx, FN-N2) calculated when 15N-labelled NOx or NH4+ are above detection limits; used in mixing models.
  - Limits of detection:
    - Headspace 29N2/30N2: ≈0.03 nmol g-1 dry sediment h-1
    - 30N2: ≈0.4 nmol g-1 dry sediment h-1
    - 15N-N2: ≈1.6 nmol g-1 dry sediment h-1
  - Some values are flagged as BDL if below detection.

- Provenance, references, and documentation
  - Calculation and interpretation references include Nielsen (1992), Thamdrup & Dalsgaard (2000, 2002), and related methodological notes.
  - Detailed site descriptions (Clay 1–3, Sand 1–3, Chalk 1–3) with precise GPS coordinates provided.
  - Documentation explains how to interpret “time-series” headers and initial headers for first column.

- Quality and limitations
  - Results represent potential activities rather than absolute in-situ rates.
  - Some data are below detection limits (BDL) and are flagged accordingly.
  - Data include a mix of oxic and anoxic conditions, multiple sites, and replicate measurements; data interpretation requires accounting for mixing models and tracers used.

- Governance and dissemination considerations for Data Stewards
  - Metadata completeness:
    - Ensure site identifiers, sediment type, replicates, coordinates, incubation conditions (oxic/anoxic), volume details, and tracer specifications are captured.
    - Document time-series interpretation rules (T0–T5) and any deviations from the described protocol.
  - Data structure and standards:
    - Preserve 42-column schema with clear definitions for each column; provide a data dictionary mapping abbreviations to full definitions.
    - Maintain units (nmol, µM, h, g dry sediment, etc.) and detection limits; indicate BDL values explicitly.
  - Provenance and reproducibility:
    - Include calculation methods and references in metadata; link to the exact versions of equations (Thamdrup & Dalsgaard; Nielsen).
    - Record instrument specifics (mass spectrometry details) and calibration procedures if available.
  - Access, licensing, and updates:
    - State data access terms; clarify whether datasets are public or shared under restrictions; note any embargo periods or embargoed updates.
    - Plan for versioning and future updates, including re-calibration or re-analysis notes.
  - Quality assurance:
    - Implement QA steps to verify that time-series data align with the described sampling times and that reference/control conditions are properly labeled.
    - Include flags for results that are below detection limits and documentation of how these were treated in analyses.

- Practical guidance for use and dissemination
  - Use the site-level metadata (river, site name, coordinates) to enable proper discovery and cross-dataset linking.
  - When sharing, provide access to both raw measurements (e.g., 15NOxT0–T5) and derived metrics (P29, P30, Atotal, ra, FN-NH4+, FN-NOx, FN-N2).
  - Include methodological context in any reuse, emphasizing that results are potentials and influenced by incubation conditions.
  - Maintain traceability to the three main data streams: oxic slurries (with O2 measurements), anoxic slurries, and the associated 15N-nitrate, 15N-ammonium, and time-series measurements.

- Key takeaway
  - The dataset provides a richly documented, multi-site set of 15N isotope-incubation experiments with explicit methodological references, enabling calculation of nitrogen transformation pathways (denitrification, anammox) and isotope pool contributions across oxic and anoxic sediment conditions; it is well-suited for data stewardship practices focusing on metadata completeness, reproducibility, and clear provenance.