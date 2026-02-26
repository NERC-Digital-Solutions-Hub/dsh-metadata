# LAC Project Datasets – Description and Methods

- The document describes a multi-site paleoenvironmental data package from the LAC project, detailing seven CSV datasets (Ruppert 1cm, Ruppert 2cm, WBP, NOR1, NOR3, AT2 1cm, AT2 2cm) and their authorship, sampling design, analytical methods, data formats, and quality controls.
- It reflects large-scale collaboration across UK, Norway, Greenland, and Canada, with many contributing institutions and researchers.

## Data scope and provenance

- Datasets involved
  - LAC_Ruppert_1cm_dataset.csv
  - LAC_Ruppert_2cm_dataset.csv
  - LAC_WBP_dataset.csv
  - LAC_Nor1_dataset.csv
  - LAC_Nor3_dataset.csv
  - LAC_AT2_1cm_dataset.csv
  - LAC_AT2_2cm_dataset.csv
- Core geography: sediment sequences from lakes/ponds in Alaska, Norway, Greenland, etc., with cores collected from the deepest part of each study lake.
- Core sampling and subsampling: continuous 1 cm and 2 cm sections; subsampling performed in the UK; overlapping sections correlated into running depth profiles.
- Core analysis spans multiple proxies (see Proxies section) and uses standardized lab protocols with documented metadata.

## Sampling design and regime

- One sediment sequence per study lake; cores collected with specified methods (Livingstone corer, Russian corer, etc.).
- Core dates range around 2013–2014 for the different sites, with water depths reported per site.
- Core processing:
  - Surface cleaned and split longitudinally; sections obtained at 1 cm and 2 cm intervals.
  - Overlapping sections correlated to produce running depth profiles.
- Some sequences have combined 1 cm and 2 cm analyses in data spreadsheets (NOR1, NOR3) while Ruppert and AT2 datasets are split into 1 cm and 2 cm CSVs.

## Methods and laboratory instrumentation

- LOI (Loss on Ignition)
  - 1 cm resolution; dry weight and organic matter content estimated; carbonate content inferred from high-temperature combustion.
- Diatoms
  - Fossil diatoms prepared from 1 cm samples; counting and identification to species where possible; counts converted to % abundance; concentrations computed per g dry mass using microsphere methodology.
- Biogenic Silica (BSi)
  - Wet alkaline digestion with ICP-MS to determine dissolved silica; BSi calculated from time-course data using calibration with SCP standards; reproducibility indicated by low variability in SCP references.
- Isotopes
  - δ13C and δ15N measured using EA-IRMS with reference standards; C and N percentages reported as % dry weight.
- XRF scanning
  - Elemental scanning (Ca, Fe, Ti, Zr, Fe:Mn, etc.) with normalization by total counts; 200 μm (Ruppert) or 400 μm resolution (other cores).
- Macrofossils
  - Sieved plant and animal macrofossils analyzed with standardized digestion/sieving; taxa identified from published resources and reference collections; counts converted to per-volume metrics.
- Chironomids
  - Invertebrate remains extracted from >40 μm fraction; standardized chemical treatments; head capsules identified to taxa; counts converted to abundance and concentrations.
- Cladocera
  - Volumetric subsamples processed similarly to chironomids; counts adjusted using Lycopodium marker for concentration calculations.
- Pigments
  - HPLC pigment analysis (Chl a, Chl b, carotenoids, diadinoxanthin, diatoxanthin, etc.) for algal community characterization; 1 cm contiguous samples.
- Pollen
  - 1 cm3 subsamples processed with standard pollen prep and counted; taxa identified to genus/species where possible; percent abundances produced.
- Data integration and normalization
  - 1 cm and 2 cm data aligned for certain datasets; XRF data normalized to total counts; Ca, Fe, Ti, Zr values and related ratios prepared for cross-proxy comparisons.

## Data format and structure

- Storage format: comma-separated values (CSV) for all primary datasets.
- Key columns and units (examples)
  - Running_top_cm, Running_bot_cm: depth extents in cm (final sequence running depth)
  - SubID: unique sample barcode
  - LOI: percent dry weight; LOI550%DW (organic matter); LOI_CO3% (carbonate)
  - WetDensity_gcc, DryDensity_gcc, BulkDensity_gcc: density metrics
  - Biogenic silica (wt% SiO2)
  - Isotopes: δ13C‰, δ15N‰, C%, N%
  - XRF: element counts per second (cps) normalized to total cps; Ca_kcps, Fe_kcps, Ti_kcps, Zr_kcps, FeMn ratios, etc.
  - Diatoms: species abundances and taxa lists; Diatom_conc (valves/g dw x 10^8)
  - Macrofossils, Chironomidae, Cladocera: taxon counts or abundance scores; sample volumes and marker-based concentrations
  - Pigments: nmol/g organic mass for each pigment (e.g., Chl_a, Fucoxanthin, Zeaxanthin)
  - Pollen: % abundances by taxa; marker columns for pollen datasets
- Taxonomic references and standard abbreviations are provided to ensure consistent naming across datasets.

## Data quality control and metadata

- Quality checks
  - Detection limits and data-entry validation; cross-checks against previous cores and site metadata.
  - Pigment retention verification with reference standards; diatom identifications cross-validated with established literature and experts.
  - XRF data quality checks include cross-core comparison where possible and alignment with bulk density signals.
  - Taxonomic identifications cross-checked with literature and peers; uncertain IDs flagged in metadata (cf naming conventions).
- Metadata and documentation
  - Extensive column headings and units documented in the accompanying data dictionaries (e.g., Table 2 of column headings and units).
  - Abbreviations and units table included to support interpretation of complex datasets.
- Format and storage
  - Data organized by core/dataset with clear sample top/bottom depths; running depth alignment provided for integrated interpretation.

## Implications for data stewardship and usage (Data Leaders perspective)

- Data integration and harmonization
  - Rich multi-proxy matrix (geochemical, biological, isotopic, and physical proxies) enables holistic reconstructions but requires careful cross-proxy alignment and consistent depth sampling.
  - Some sequences combine 1 cm and 2 cm data; ensure consistent depth scales when integrating across cores.
- Data discoverability and governance
  - Datasets are CSV-based with explicit column definitions, aiding discoverability but requiring stable metadata schemas for long-term reuse.
  - Extensive provenance (authorship, sampling details, instrumentation) supports traceability and accountability.
- Data quality and standards
  - Strong QA/QC philosophy evident; however, the multi-proxy nature across sites highlights the need for standardization of taxonomic nomenclature and data normalization when comparing across cores.
- Operational considerations for leaders
  - The dataset package demonstrates effective cross-institution collaboration, coordinated sampling, and shared data management practices.
  - Opportunities exist to adopt or adapt the documented data management plan for broader organizational data systems, particularly for coordinating multi-proxy datasets and ensuring metadata richness.

## Endnotes and references

- The document includes an extensive References section detailing foundational methods, instrumentation, and identification guides used across proxies (diatoms, chironomids, cladocera, pollen, pigments, isotopes, LOI, etc.).