# General information: This dataset contains results from slurry incubations with 15N-labelled substrates.

## Overview
- Dataset from slurry incubations with 15N-labelled substrates, including both anoxic and oxic conditions.
- Incubations conducted in August 2013; mass spectrometry analysis in September 2013.
- Purpose: quantify nitrogen transformations (e.g., anammox, denitrification, nitrification) under controlled conditions and with tracer isotopes.
- Results interpreted as potentials (not rates) due to incubation design and stopping times.

## Experimental design and data collection
- Slurry setup:
  - Anoxic slurries: 3 mL vials with 1 mL wet sediment, 1 mL synthetic river water, N2 headspace.
  - Oxic slurries: 12 mL vials with 2.5 mL wet sediment, 3 mL synthetic river water, air headspace.
- N-amendments:
  - 15N-labelled tracers added as 100 µL injections; target post-injection nitrate/ammonium concentrations vary by sediment type (clay: 100 µM nitrate; sand/chalk: 300 µM nitrate; all: 500 µM ammonium).
  - 15N tracers are 98 atom% 15N.
  - Anoxic slurries pre-incubated overnight to remove ambient 14N nitrate.
- Experimental design:
  - Reference samples (no 15N-substrates), controls (biological activity stopped with zinc chloride before 15N addition), and time-series samples (zinc chloride added at predetermined times after 15N addition).
  - Incubations in the dark at room temperature; results reflect potential activity.
- Time series structure:
  - Time points labeled T0, T1, T2, T3, T4, T5 (measured as hours post 15N addition, e.g., 0, 0.5, 1, 2, 3, 6 h for oxic slurries).
- Data organization:
  - Data table has 42 columns and 46 rows (including headers); missing values marked as BDL (below detection limit).
  - Water samples filtered (0.45 µm), stored frozen until analysis (within 3 months).
- Column headers (described in detail below) include site identifiers, replicate info, isotope-nitrogen measurements, activity rates, and auxiliary measurements.

## Data structure and key variables
- Replication and site:
  - Sites categorized as Clay, Sand, Chalk representing river sub-catchments; multiple specific sites (Clay 1–3, Sand 1–3, Chalk 1–3) with exact coordinates.
  - Replicates: Replicate indicator with 5 replicates per river.
- Core rate measurements:
  - P29-15A, P30-15A: 29N2 and 30N2 production after 15N-labelled ammonium in anoxic slurry (nmol N2 g-1 dry sediment h-1).
  - P29-15A14N, P30-15A14N: production after 15N ammonium with 14N nitrate added (nmol N2 g-1 dry sediment h-1).
  - P29-15N, P30-15N: production after 15N nitrates (nmol N2 g-1 dry sediment h-1); calculated from time-series slopes.
  - Atotal: total anammox activity (nmol N2 g-1 dry sediment h-1) using Thamdrup & Dalsgaard (2002) equations; includes detection limit (~0.08 nmol N2 g-1 h-1).
  - ra: contribution of anammox to N2 production (percent).
- Isotope pool proportions (mixing model inputs):
  - FN-NH4+, FN-NOx, FN-N2: fractions of 15N in ammonium, nitrate/nitrite, and N2 pools, respectively; used in isotope-mixing models with FN-NOx, FN-NH4+, FN-N2.
- Oxic slurry time-series and controls:
  - Oxicp15N-T0 to Oxicp15N-T4: 15N-labelled N2 produced after ammonium addition in oxic slurries (nmol N2 g-1).
  - Oxicp15Nrpt-T0 to T4: repeats for a test of nitrification–N2 production relationship (reference repeats from another collection).
  - Oxicp15NATU-T0 to T5: ammonium + allylthiourea (ATU) treatments to inhibit nitrification and test nitrification–N2 relationship.
- Dissolved oxygen and related measurements:
  - O2Conc-T0, T1, T2, T3: dissolved oxygen (µM) at various incubation times in oxic slurries.
- Reference concentrations:
  - AmmoniumRef: ammonium concentration in oxic reference samples (µM).
  - NOxRef: nitrate + nitrite concentration in oxic reference samples (µM).
- Method-specific notes:
  - 15N-N2 production metrics rely on 29N2 and 30N2 mass-to-charge signals; p15N equals P29 + 2*P30.
  - Headspace N2 calculations use a calibration factor and the ratio of 29/30 to total N2 (AllN2).
  - Aqueous N2 concentration inferred from headspace data via Bunsen solubility and total nmoles in vial.
- Column header descriptions:
  - Headers include explicit site labels, time-series designations, and derived metrics (AmmoniumRef, NOxRef, 15NOxT0–T5, etc.), with units and calculation notes described for reproducibility.

## Measurements, calculations, and interpretation
- Measurement method:
  - 15N-labelled N2 production quantified by mass spectrometry; 15NOx concentrations determined by cadmium reduction and spectrometry.
- Calculations:
  - P29 and P30 derived from time-series fits (linear trends) of 29N2 and 30N2 against time.
  - p15N = P29 + 2×P30 (production of 15N-labelled N2).
  - Atotal calculated from 15N-nitrate conditions using FN and Thamdrup–Dalsgaard equations; includes a limit of detection (~0.08 nmol N2 g-1 h-1).
  - ra = (Atotal / Dtotal) × 100%, where Dtotal derived from P30 under 15N-nitrate conditions.
  - FN-NH4+, FN-NOx, FN-N2 used in isotope-mixing models to apportion 15N in nitrogen pools.
- Detection limits:
  - 29N2 to AllN2: ~0.03 nmol g-1 h-1; 30N2 to AllN2: ~0.4 nmol g-1 h-1; 15N-N2: ~1.6 nmol g-1 h-1.
- Units:
  - Rates in nmol N2 g-1 dry sediment h-1; concentrations in µM; DO in µM; isotope fractions unitless (0–1).

## Data quality, limitations, and notes
- Data quality considerations:
  - Incubations measure potential activity, not in situ rates.
  - Values below detection are marked BDL; multiple calculated-derived metrics rely on time-series fits.
  - Complete documentation of column headers and calculation methods is provided to enable traceability.
- Limitations:
  - Data represent controlled laboratory potentials and depend on tracer uptake and substrate amendment strategies.
  - Spatial coverage is defined by the listed river sites in Hampshire Avon catchment; replication is per river.
  - Some measurements (e.g., Oxicp15Nrpt repeats) are designed to test specific hypotheses and may not be uniform across all sediments.
- Temporal scope:
  - Collection in August 2013; analyses in September 2013; procedures and calculations reference literature up to 2012–2002.

## Metadata, provenance, and data access
- Provenance:
  - Sediment samples collected from designated sites across Clay, Sand, Chalk categories with precise coordinates.
  - Sample processing and incubations described; nitrogen isotope tracers used with defined atom% 15N.
  - Analytical references cited (Nielsen 1992; Thamdrup & Dalsgaard 2000, 2002; Jensen 2011; Smart & Barko 1985).
- Metadata details included:
  - Site identifiers and coordinates; replicate structure; detailed column header descriptions; measurement methods and detection limits; experimental design notes (reference/control/time-series).
- Data structure readiness for reuse:
  - Table format with 42 columns and 46 rows; explicit descriptions for first column header and time-series applicability to remaining time points.
  - Comprehensive description of how P29, P30, p15N, Atotal, ra, and FN-* variables are calculated and interpreted.

## Implications for data strategy and governance (for Data Leaders)
- Data discoverability and usability:
  - Rich metadata and explicit column manuals enhance discoverability and reusability; ensure inclusion of a machine-readable data dictionary and a README with methodology crosswalk to standard terms.
- Data quality management:
  - Clear LODs, BDL flags, and calibration notes enable reproducible quality checks; maintain versioning for any re-calculation or reprocessing of mass-spectrometry data.
- Data standardization and interoperability:
  - Complex, domain-specific variables (P29, P30, Atotal, ra, FN-*) benefit from standardized naming conventions and consistent units across datasets to support integration with other N-cycle datasets.
- Data governance and stewardship:
  - Timestamped collection and analysis events support provenance tracking; ensure ongoing maintenance if data are updated or extended (e.g., additional sites or time points).
- Practical use cases:
  - Cross-site comparisons of anammox vs. denitrification contributions; investigation of nitrification–N2 coupling under oxic vs. anoxic conditions; isotope-mumap-based partitioning of nitrogen-transforming processes.
- Potential risks and mitigations:
  - Domain-specific interpretation required; provide accessible methodological summaries and code to reproduce calculations (P29, P30, p15N, Atotal, ra).
  - Keep detailed references and assumptions explicit to avoid misinterpretation of poten tial rates as in-situ rates.