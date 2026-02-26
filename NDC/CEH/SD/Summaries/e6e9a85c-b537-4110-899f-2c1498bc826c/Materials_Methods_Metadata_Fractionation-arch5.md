# Materials and methods, and metadata for Phosphorus, carbon and nitrogen concentrations in UK soil mineral fractions, 2013-2014

- Scope and purpose
  - Datasets document concentrations of phosphorus (P), carbon (C), and nitrogen (N) in UK soil mineral fractions (across bulk, light fraction LF, heavy fraction HF) for 2013–2014.
  - Derived from the study on distribution of phosphorus between free and mineral-associated soil organic matter using density fractionation (Adams et al. 2018, Plant & Soil).

- Sampling and density fractionation (procedural overview)
  - One fractionation per soil sample.
  - 25 g soil subsamples placed in 400 mL bottles with 250 mL sodium polytungstate (NaPT) at density 1.6 g cm-3.
  - Centrifugation at 5500 rpm for 30 min; separation of floating material (NLF) into 60 μm nylon mesh bags; repeat washing/centrifugation to account for all NLF (up to two repeats).
  - Conductivity checks to confirm removal of excess NaPT: aim for <50 μs cm-1 (calcareous soils <200 μs cm-1 acceptable due to carbonate dissolution).
  - Rinsed samples dried at 40 °C, stored in desiccator until analysis.
  - Light fraction (OLF) extraction by sonication; disruption monitored microscopically until complete aggregate disruption; OLF combined with NLF in mesh bags; LF washed to conductivity targets; dried and weighed.
  - HF processed by repeated centrifugation and washing until waste water conductivity <50 or <200 μs-1; HF dried and weighed.
  - Post-processing: HF ground; carbonate-containing samples (bulk soil pH > 5.5) treated with 0.1 M HCl and re-dried; final sample preparations prepared for analyses.

- Analytical measurements
  - Carbon and nitrogen: total organic carbon (TOC) and total nitrogen (TN) measured in milled sub-samples with a Vario EL elemental analyzer.
  - Phosphorus
    - Total P (TP) by ignition-extraction method (Olsen & Sommers 1982).
    - Inorganic P (IP) by extraction with 0.5 M sulfuric acid, then colorimetric molybdate analysis.
    - Organic P (OP) = TP – IP.
  - Replication: analyses replicated four-fold.
  - Bulk analyses (C, N, IP) reported by Toberman et al. (2016) using the same C/N methods; TP measured with a different method (aqua regia and microwave digestion).

- Dataset structure and metadata (Tables S1–S6)
  - Table S1: Information about soil samples (sample IDs, vegetation type codes, sample numbers, depth descriptors, catchment names, land use, date, database ID, depth). Includes spatial and contextual metadata.
  - Table S2: Recovery of soil mass in density fractionation with fields for collection date, lat/long, MAP, MAT, depth, starting mass, and fractions (bulk, LF, HF).
  - Table S3: OC & TN concentration data (OC bulk, OC LF, OC HF; TN Bulk, TN LF, TN HF) with corresponding units.
  - Table S4: TP, IP, OP concentration data (Bulk, LF, HF) with units and related fraction labels.
  - Table S5: Recoveries of OC & TN (OC/TN in bulk and LF+HF, and recovery percentages).
  - Table S6: Recoveries of TP, IP & OP (mass, recoveries, and related fractions).
  - Metadata conventions
    - Sample IDs encode vegetation type (e.g., b = broadleaf), sample number, and depth (s = shallow, d = deep).
    - Columns include explicit units (e.g., mg g−1, %, cm, g cm−3) and depth-specific notes.
    - Geographic and climatic context (MAP, MAT) and land-use categories are recorded for each site.

- Data provenance and references
  - Primary methods and procedures align with established references (Cerli et al. 2012; Olsen & Sommers 1982; Schrumpf et al. 2013).
  - Related large-scale soil survey data: Toberman et al. 2016 (LTLS) using similar C, N, IP methods; alternate TP method noted.
  - Data are linked to the Adams et al. 2018 study (Plant & Soil) from which the methods and data are derived.

- Data governance and sharing considerations for Data Stewards
  - Ensure consistent unit usage and clear fraction labeling (bulk, LF, HF; OC/TN/IP/TP/OP).
  - Preserve full provenance, including fractionation density (1.6 g cm-3 NaPT), conductivity thresholds, and carbonate removal steps, to support reproducibility.
  - Maintain replication records (four-fold analyses) and document any deviations (e.g., calcareous soils tolerances).
  - Include accompanying metadata tables (S1–S6) to enable dataset discoverability and interoperability; align with standard soil/elemental analysis vocabularies.
  - Note cross-references to Toberman et al. (2016) and Adams et al. (2018) for context and methodological lineage.
  - Prepare the dataset for portal upload with clear data licenses, DOIs where applicable, and links to primary publications and data centre records (e.g., LTLS dataset DOI).