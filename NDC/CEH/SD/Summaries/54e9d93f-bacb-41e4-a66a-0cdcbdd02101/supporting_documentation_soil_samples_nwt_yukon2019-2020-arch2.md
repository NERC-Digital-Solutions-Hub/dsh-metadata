# Environmental context and metadata for permafrost soil samples, NWT & YT, Canada, 2020

- Overview
  - Dataset reports carbon (C) and nitrogen (N) content of permafrost soil samples from the Northwest Territories (NWT) and Yukon Territory (YT), Canada, collected in 2019 and 2020.
  - Samples collected by team led by Julian Murton, Thomas Opel, and Steve Kokelj; CN analysis performed by Nina L. Friggens with support from Joana Zaragoza-Castells.
  - Analytical results generated in 2021; data intended for environmental monitoring and policy-relevant analyses.

- Data structure
  - A single CSV file: Soil_samples_NWT_Yukon2019-2020.csv.
  - Contains 14 columns describing CN data for each soil sample.
  - A separate Word document provides detailed site-level metadata (sampling locations, environment, procedures, etc.).

- Collection and site metadata (sampling context)
  - 14 soil profiles (#1–#14) sampled in three regions: East Channel (EC), Tuktoyaktuk (T), Klondike (K) in August 2019; two additional profiles (HUS and CRB_S) are included from Tuktoyaktuk region in 2019, with broader permafrost context summarized for the Tuk Harbour area.
  - Four permafrost/soil types represented:
    - Non-lake orthels
    - Drained thermokarst-lake sediments
    - Turbels
    - Yedoma deposits
  - Profiles include detailed geomorphic context, vegetation, organic and mineral soil descriptions, active-layer thickness (ALT) measurements, ground ice observations, and sampling methods (soil pits, coring, horizontal drill holes).
  - Representative site descriptions and coordinates provided for each profile, with specifics on ALT, depth ranges, and permafrost features (e.g., ice wedges, cryoturbation, pool ice).

- Analytical methods and quality control
  - Samples were frozen at field stations, shipped frozen to University of Exeter, and stored frozen until processing.
  - CN analysis conducted in June 2021 using a Thermo Scientific Flash 2000 Elemental Analyser.
  - Preparation involved thawing, homogenising, and oven-drying sub-samples (~10 g), followed by CN analysis.
  - Quality control used EDTA standards at the start and as check standards every ten samples:
    - EDTA standard: 9.59% N (±3% accepted) and 41.1% C (±1% accepted).

- Nature and units of recorded values
  - Data fields encoded in the CSV per sample:
    - Sample identifiers: Year (19 for 2019), sample sequence, location code (EC, T, K, HUS, CRB_S), profile number (P1–P6), and specific sample code.
    - Description fields: soil type/formation, active layer or permafrost status (AL, ALc, Pc, Pnc, etc.), coordinates (latitude/longitude in DMS), depth below ground surface (m), date collected, total sample mass (kg), and short description/interpretation.
    - CN results: C content (%) and N content (%) measured by the Exeter lab in 2021.
    - Sampling method and storage during fieldwork (frozen storage indicated).
  - The detailed CN values and their interpretation are tied to the specific soil profiles and depths described in the accompanying site metadata.

- Storage, access, and provenance
  - Field-collected samples were stored frozen, then shipped frozen to the laboratory, and stored frozen until processing.
  - Processed CN data are available in the Soil_samples_NWT_Yukon2019-2020.csv, with the methodology and QA details described above.
  - The dataset is accompanied by a Word document with comprehensive site-level descriptions, sampling procedures, and contextual paleoenvironmental reconstruction for the Tuk Harbour region.