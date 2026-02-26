# Description, Experimental Design and Collection:

- Dataset scope
  - Glucosinolate concentrations in Brassica napus plants within FreeAir Diesel and Ozone Enrichment (FADOE) rings.
  - Data collected in field experiments across two years (2018 and 2019) with multiple environmental and biotic treatments.
  - Seven individual glucosinolates measured, plus aggregated indolic, aliphatic, and total glucosinolate sums.

- Experimental design
  - FADOE rings placed in a field of wheat in 2018 (latitude 51.482853, longitude -0.897749) and moved to an adjacent field in 2019 (latitude 51.482374, longitude -0.895855).
  - Four pollution treatments: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON; natural air). Two rings per treatment, totaling eight rings.
  - Aphid treatments: plants inoculated when five weeks old with 50 aphids, 10 aphids, or none; leaves for glucosinolate analysis taken from three plants per aphid treatment (Aphids_present = Yes for 50 aphids; No for no aphids).
  - Sampling details: leaves from two aphid treatments (50 aphids or none) were analyzed per plant; up to three replicate samples analyzed per ground sample.

- Data structure and variables
  - Sample coding: A = Sample_ug_g-1_dw (concentration units: micrograms per gram of dry weight).
  - Ring identifier: B = Ring.
  - Treatment identifiers: C = Pollutant (D, O3, D+O3, CON).
  - Plant and aphid information: D = Plant_ID; E = Aphids_present (Yes/No).
  - Replication: F = Replicate (1–3).
  - Measured glucosinolates (columns G–M): Progoitrin; Glucoalyssin; Gluconapin; Glucobrassicanapin; Glucobrassicin; 4-methoxyglucobrassicin; Neoglucobrassicin.
  - Totals and groupings: N = Indole_GLS; O = Aliphatic_GLS; P = Total_GLS.
  - Units and measurement method: LC-MS analysis following established protocols; samples were freeze-dried and ground to a fine powder; up to three replicates per ground sample.

- Methods and references
  - Measurement: Liquid Chromatography–Mass Spectrometry (LC-MS) per protocol referenced in the dataset.
  - Methodology references:
    - [1] FADOE configuration and quality control methodology (Ryalls et al. 2022).
    - [2] LC-MS protocol for glucosinolate analysis (Jasper et al. 2020).
  - Quality control and provenance are described in the referenced FADOE documentation.

- Quality assurance and processing
  - Dataset notes that full details of FADOE configuration, including quality control measures, are described in the referenced source.
  - The data are subjected to quality assurance, cleaning, and transformation prior to sharing.
  - Documentation of work performed on datasets is included or available as part of the data record.

- Provenance and hosting
  - Datasets are intended to be uploaded to relevant portals and catalogued as part of data holdings.
  - Data stewards may document processing steps, transformations, and updates to support discoverability and reuse.

- Geographic and temporal metadata
  - Field locations spanned two fields across 2018 and 2019, with explicit latitude and longitude information for ring placements.
  - Ring and treatment assignments were maintained across years, enabling cross-year comparisons of pollutant and biotic stress effects on glucosinolate profiles.

- Relationships to underlying workflows
  - Data collection tied to plant age at aphid inoculation, ring-level treatment assignments, and plant-level sampling decisions.
  - Seven individual glucosinolates plus aggregated totals provide both compound-specific and overall glucosinolate insights.

- Particular considerations for Data Stewards
  - Ensure consistent metadata schemas for: sample_id, ring_id, pollutant_treatment, aphid_treatment, plant_id, replicate, and glucosinolate columns.
  - Maintain clear linkage to methodological references and QA documentation.
  - Preserve provenance by recording processing steps (freeze-drying, grinding, LC-MS protocol, replicates) and update logs.
  - Support data discoverability through portal-ready metadata and catalogue records; track any updates or corrections to measurements or classifications.
  - Be mindful of potential cross-year field relocations and ensure geospatial metadata reflects ring positions in both 2018 and 2019.