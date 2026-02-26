# Description, Experimental Design and Collection

- This dataset contains glucosinolate concentrations measured in Brassica napus plants within FreeAir Diesel and Ozone Enrichment (FADOE) rings. FADOE configuration and quality control details are described in reference [1].

- Experimental setting and timeline:
  - FADOE rings were distributed within a field of wheat in 2018 (latitude 51.482853, longitude -0.897749) and moved to an adjacent field in 2019 (latitude 51.482374, longitude -0.895855).

- Experimental design:
  - Pollutant treatments: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and a control (CON; natural air).
  - Aphid inoculation: plants inoculated with 50 aphids, 10 aphids, or no aphids.
  - For glucosinolate analysis, leaves were taken from two aphid treatments: 50 aphids (Aphids_present = Yes) or no aphids (Aphids_present = No).
  - Sampling: leaves from three plants per ring were used; samples were labeled with Plant_ID and replicated up to three times per ground sample.

- Sample processing and chemical analysis:
  - Leaves were freeze-dried, ground to a fine powder, and up to three replicate samples were analyzed per ground sample.
  - Glucosinolates measured by LC-MS following protocol by [2].
  - Seven glucosinolates quantified: Progoitrin, Glucoalyssin, Gluconapin, Glucobrassicanapin, Glucobrassicin, 4-methoxyglucobrassicin, Neoglucobrassicin.
  - Derived totals: Indolic glucosinolates (Indole_GLS), Aliphatic glucosinolates (Aliphatic_GLS), and Total glucosinolates (Total_GLS).

- Data structure and outputs:
  - Sample code components include ring, aphid treatment, plant number, and replicate (e.g., 'Sample_ug_g-1_dw' for sample concentration; 'Ring' as Column B, 'Pollutant' as Column C, 'Plant_ID' as Column D, 'Aphids_present' as Column E, 'Replicate' as Column F; glucosinolate measurements in Columns G–M; Indole_GLS in N; Aliphatic_GLS in O; Total_GLS in P).

- Protocols and references:
  - FADOE methodology and quality control: [1] Ryalls et al. 2022 Environmental Pollution, 297, 118847. DOI: 10.1016/j.envpol.2022.118847.
  - Glucosinolate LC-MS protocol: [2] Jasper et al. 2020 Postharvest Biology and Technology, 163, 111157. DOI: 10.1016/j.postharvbio.2020.111157.

- Relevance to environmental monitoring:
  - Provides standardized, QA/QA-structured data on plant chemical defenses under different pollution regimes.
  - Facilitates cross-study comparisons and temporal monitoring; data are suitable for integration with other environmental datasets and policy-relevant analyses.