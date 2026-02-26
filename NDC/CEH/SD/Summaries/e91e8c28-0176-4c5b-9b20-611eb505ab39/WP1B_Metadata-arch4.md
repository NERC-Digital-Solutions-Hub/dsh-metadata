# Chemical composition of anaerobic digestate and biomass ash blends as a result of storage

## Overview
- Investigates how adding biomass ash to anaerobic digestate affects nutrient stability, especially ammonium loss as ammonia gas, and how digestate characteristics change over time.
- Time-series study focusing on labile agronomic components (nitrogen and sulfur) across several months.

## Data access and citation
- Data available at: https://doi.org/10.5285/e91e8c28-0176-4c5b-9b20-611eb505ab39
- Suggested citation: Lag-Brotons et al. (2020). Chemical composition of anaerobic digestate and biomass ash blends as a result of storage. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/e91e8c28-01764c5b-9b20-611eb505ab39
- Dataset description and key file: WP1B.csv; metadata and methods provided for data reuse and verification.

## Study design and materials
- Sample sources:
  - Anaerobic digestates from UK industrial-scale plants, representing diverse feedstocks (e.g., source-segregated household food waste, maize silage, vegetables waste, sweet-corn waste, biodegraded sludges).
- Sample sizes and handling:
  - Digestates: 5–10 kg per sample, collected at end-of-process, cooled, transported in ice, stored in a cold room (<4°C) until analysis.
  - Biomass ashes: 10–20 kg per sample, fly ash and bottom ash fractions; samples air-dried, ground, and stored at room temperature.
- Material characterization:
  - Comprehensive elemental and nutrient analyses (e.g., total nitrogen, nitrate, ammonium, phosphorus, potassium, sulfur, calcium, magnesium, trace metals, chloride, boron, etc.) using multiple established methods (e.g., JAS, APHA, and other external labs).

## Experimental treatments and procedures
- Substrates and treatments:
  - Four base substrates: D1, D2, D1A1 (D1 + ash), D2A1 (D2 + ash); eight treatment combinations, including acidified variants.
  - Acidification to target pH 5.5 using concentrated sulfuric acid (98% H2SO4); some treatments received acid, others did not (as per Table 4 in the dataset).
- Experimental setup:
  - 9 litres per treatment, divided into three replicates.
  - Storage conditions: ambient temperature (~20°C).
  - Time-course sampling: days 0, 1, 2, 4, 8, 16, 32, 64, 128.
- Analytical suite (per TABLE 5 in the document):
  - Parameters include dry solids (DS), pH, Total Kjeldahl Nitrogen (TKN) on fresh and dry basis, Total Sulfur (TS) on fresh and dry basis, and an array of other nutrients/elements (e.g., nitrate N, ammonium N, P, K, Mg, Ca, Fe, Mn, Zn, Cu, Mo, Cl, B, etc.).
  - Standard methods referenced (e.g., DS by 2540 B3, pH by 4500-H+ B, TKN by 48, etc.).

## Data structure and metadata
- Data file: WP1B.csv
  - Columns include: Treatment, Material, Acid (whether H2SO4 was added), Days, Replicate, pH, DS, TKNf (total Kjeldahl N, fresh basis), TKNd (total Kjeldahl N, dry basis), TSf (total S, fresh), TSd (total S, dry), plus other elemental measurements (N-NO3, N-NH4, P, K, Mg, Ca, Fe, Mn, Zn, Cu, Mo, Cl, B, etc.).
  - A key (Table 6) explains each field, units, and descriptions to facilitate data reuse.
- Documentation and references:
  - Data collection methods, affiliations of contributing authors, and contact details provided to support data provenance and reuse.
  - References to standard methods (APHA, JAS) and related research on acidification of animal slurry and digestate handling.

## Practical implications for data leadership and practice
- Data discoverability and reuse:
  - The dataset is clearly cited with a DOI and accompanied by a detailed data key, enabling cross-institutional sharing and validation.
- Metadata and standardization:
  - Rich metadata (treatment descriptions, sampling schedule, analytical methods) supports integration with other data systems, but the diversity of substrates highlights the need for harmonized data standards when comparing across projects.
- Data quality and governance:
  - Multisite sampling, varied feedstocks, and multiple analytical methods introduce heterogeneity; robust metadata and method documentation are essential for comparability and reproducibility.
- Data-driven insights and collaboration:
  - The dataset enables evaluation of nutrient stability under ash amendments, informing digestate management and fertilizer valorization strategies; coordination with industry partners and data communities can enhance system-wide understanding of digestate-a sh interactions.
- Operational considerations:
  - Preliminary observations note foaming during acidification requiring vigorous mixing, raising considerations for scaling, process design, and data interpretation of pH-adjusted treatments in practice.

## Key challenges and considerations
- Practical feasibility:
  - Acidification induced significant foaming that persisted, necessitating energetic mixing; scalability and industrial applicability require further development.
- Data scope and gaps:
  - While the dataset provides extensive chemical profiles over a time course, explicit final conclusions on ammonium retention/loss are not detailed in the summary and would require access to the full dataset and results.
- Sector coordination:
  - The study exemplifies multi-partner collaboration, underscoring the value of shared data practices and common metadata standards to support wider data ecosystems.