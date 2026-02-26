# Description, Experimental Design and Collection: Glucosinolate concentrations from Brassica napus within FreeAir Diesel and Ozone Enrichment (FADOE) rings

- Overview
  - Datasets measure glucosinolate concentrations in Brassica napus planted in FreeAir Diesel and Ozone Enrichment (FADOE) rings.
  - Seven individual glucosinolates were quantified, plus aggregated totals for indolic, aliphatic, and all glucosinolates.
  - Measurements were obtained via LC-MS following established protocols; full methodological details are described in referenced sources.

- Experimental Design
  - Field setup: FADOE rings located in 2018 and relocated to an adjacent field in 2019 (field coordinates provided for each site).
  - Treatments:
    - Pollutants: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON; natural air).
  - Biotic treatment: aphid inoculation with either 50 aphids, 10 aphids, or no aphids; leaves sampled from plants under two aphid treatments (50 aphids vs. none).
  - Ring assignment: each ring assigned to one of the four pollutant treatments; aphid treatments applied to plants within rings.
  - Sampling design: leaves collected from three plants per sampled unit; up to three replicate samples per ground sample.
  - Plant and sample labeling: samples coded by ring, aphid treatment, plant number, and replicate per plant (Sample_ug_g-1_dw); Plant_ID and Aphids_present indicate specific plant and aphid status.

- Data Collected and Variables
  - Seven glucosinolates measured: Progoitrin, Glucoalyssin, Gluconapin, Glucobrassicanapin, Glucobrassicin, 4-methoxyglucobrassicin, Neoglucobrassicin.
  - Derived totals:
    - Indole_GLS (indolic glucosinolates)
    - Aliphatic_GLS (aliphatic glucosinolates)
    - Total_GLS (all glucosinolates)
  - Columns and identifiers (as named in the dataset): Sample_ug_g-1_dw, Ring, Pollutant, Plant_ID, Aphids_present, Replicate, G-M (the seven individual glucosinolate columns), N (Indole_GLS), O (Aliphatic_GLS), P (Total_GLS).

- Data Provenance and Protocols
  - FADOE configuration and quality control details described in reference [1].
  - LC-MS glucosinolate analysis protocol described in reference [2].
  - References:
    - [1] Ryalls et al. 2022. Anthropogenic air pollutants reduce insect-mediated pollination services. Environmental Pollution.
    - [2] Jasper et al. 2020. Growth temperature influences postharvest glucosinolate concentrations... Postharvest Biology and Technology.

- Data Structure and Metadata
  - Field layout includes field-to-field movement (2018 in one field, 2019 in an adjacent field) with precise latitude/longitude provided.
  - Sample coding encodes ring, aphid treatment, plant, and replicate, enabling traceability of measurements to experimental conditions.
  - Metadata scope relies on the two primary methodological references for quality control and LC-MS procedures; explicit metadata quality, sharing permissions, and data governance are not detailed in this description.

- Relevance for Monitoring Frameworks
  - Provides a structured set of biochemical biomarkers (glucosinolates) in response to air pollutants and biotic stress (aphids), enabling assessment of environmental impact pathways on crop biochemistry.
  - The factorial design (pollutants × aphid treatment) supports analysis of interaction effects relevant to policy scenarios on pollutant exposure and pest dynamics.
  - Data can inform monitoring of plant biochemical responses as part of environmental health indicators and decision-making for agricultural resilience under air pollution.

- Key Considerations for Use
  - Quality control and comparability depend on the referenced FADOE methodology and LC-MS protocol; users should consult [1] and [2] for detailed procedures.
  - Metadata completeness and data governance aspects (sharing, versioning, updates) should be reviewed in the context of data management practices typical for monitoring datasets.