# Chemical composition of anaerobic digestate and biomass ash blends as a result of storage

## Overview
- A dataset and accompanying description documenting how ash addition affects nutrient stability in anaerobic digestate over time.
- Time-series experiments (spanning several months) focusing on labile agronomic components, especially nitrogen and sulfur.
- Digestates were sourced from UK industrial-scale anaerobic digestion plants; biomass ashes were obtained from thermal biomass processing.
- Comparisons include ash-amended and un-amended digestates, with attention to storage dynamics and potential ammonium loss as ammonia gas.

## Data access and citation
- Data access: https://doi.org/10.5285/e91e8c28-0176-4c5b-9b20-611eb505ab39
- Suggested citation: Lag-Brotons, A.J.; Thompkins, D.; Burguess, A.; Marshall, R.; Herbert, B.; Hurst, L.; Semple, K.T. (2020). Chemical composition of anaerobic digestate and biomass ash blends as a result of storage. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/e91e8c28-01764c5b-9b20-611eb505ab39

## Data content and structure
- Substrates and samples
  - Digestates (D1, D2) sourced from different AD plants; plus ash-containing variants (D1A1, D2A1) and their acidified counterparts (AD1, AD2, AD1A1, AD2A1) to form eight treatment combinations.
  - Ash fractions referenced as A1 (fly ash) and A2 (other ash fractions) as part of composite treatments.
- Treatments and experimental design
  - Eight treatments representing combinations of digestate type (D1 or D2) with ash addition (A1) and acidification status (with or without H2SO4; acidified vs. non-acidified).
  - Treatments include: D1, AD1, D1A1, AD1A1, D2, AD2, D2A1, AD2A1.
  - Each 9 L sample was divided into three replicates per treatment.
  - pH adjustment to target 5.5 using 98% sulfuric acid where applicable.
- Time points and replicates
  - Subsamples collected at days 0, 1, 2, 4, 8, 16, 32, 64, and 128.
  - Three replicates per treatment per time point (designated A, B, C in the dataset).
- Analytical measurements (Table 5 reference)
  - Dry solids (DS, %), pH.
  - Total Kjeldahl Nitrogen (TKNf, mg N/kg fresh; TKNd, mg N/kg dry).
  - Total Sulphur (TSf, mg S/kg fresh; TSd, mg S/kg dry).
  - Additional data points referenced include measurements of nutrients and elements (e.g., nitrate N, ammonium N, phosphorus, potassium, magnesium, copper, zinc, sulfur, calcium, iron, molybdenum, manganese, chloride, boron) as part of broader characterization.
- File structure and metadata
  - Primary data file: WP1B.csv with fields such as Treatment, Material, Acid (whether H2SO4 was added), Days, Replicate, pH, DS, TKNf, TKNd, TSf, TSd, and related nutrient concentrations.
  - Key for WP1B.csv explains the Meaning of each column (treatment description, material, acid addition, time in days, replicate id, and analytical values).

## Sampling, processing, and storage
- Digestate samples
  - Collected from end-of-process lines, 5–10 kg per sample, cooled, transported in ice, and stored in a cold room (<4°C) before analysis.
- Biomass ash samples
  - 10–20 kg per sample, shipped by courier.
  - Sub-sampling included air-drying, grinding/milling, sieving to 1 mm, and storage at room temperature until use.
- Storage and handling
  - Samples kept under controlled conditions prior to analyses; acidification experiments were conducted with careful handling given foaming and mixing challenges (noted as a key procedural consideration).

## Analytical methods and provenance
- Analytical methods referenced include standard methods (e.g., APHA) and specific JAS methods for nutrient and element quantification (datasets indicate multiple method references such as JAS-034, JAS-373, JAS-475, JAS-082, JAS-510, JAS-300, JAS-379, among others).
- The data package indicates collaboration among researchers and institutions (Lancaster University, Aqua Enviro, and associated investigators).
- Data lineages note external laboratories and national research resources (NRM) involved in material characterization.

## Metadata, provenance, and authorship
- Authors and contributors
  - Dr. Alfonso Jose Lag Brotons, Dr. David Thompkins, Andy Burgess, Dr. Rachel Marshall, Ben Herbert, Dr. Lois Hurst, Prof. Kirk T. Semple.
- Contact information provided for corresponding authors.
- Supplementary metadata accompany the dataset, including the detailed explanation of treatments and sampling scheme (Tables 1–6 referenced in the description).

## Reuse considerations and governance
- Reuse goals
  - Enables evaluation of whether high-pH ash amendments promote ammonium loss via ammonia gas during storage and how digestate characteristics evolve over time with ash addition.
  - Facilitates comparisons across digestate and ash combinations, including acidified treatments, to inform management practices for digestate storage and land application.
- Data quality and limitations
  - Comprehensive chemical characterization across multiple time points and treatments enhances usability.
  - Noted practical challenges in acidification (foaming and mixing requirements) may influence interpretation of pH-adjusted experiments and scalability considerations.
- Compliance, citation, and attribution
  - Use the provided DOI and dataset citation when reusing data.
  - Acknowledge all contributing authors and institutions as per the dataset metadata.
- Potential applications for data stewards
  - Integrate this dataset into broader data governance frameworks for digestate management, ensuring metadata captures substrate type, ash type, treatment, pH adjustment, timepoints, and analytical methods.
  - Link chemical composition data with storage and handling policies, disclosure risks, and any embargoes associated with material streams.
  - Support interoperability by aligning units and definitions with standard references (e.g., APHA methods, JAS method catalog).