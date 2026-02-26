# WP1A Dewaterability potential of anaerobic digestate and biomass ash blends using polymer dose approach

- Purpose and scope
  - Documents two datasets (WP1A1.csv and WP1A2.csv) linked to the study of dewaterability of anaerobic digestate blends with biomass ash using polymer dosing.
  - Explores how ash presence affects digestate dewaterability and how nutrients (notably nitrogen and phosphorus) partition between the liquor and fibre fractions during dewatering.

- Study materials and samples
  - Digestates: sourced from different industrial-scale UK AD plants across the project timeline; feedstocks include source-segregated food waste and other biodegradable streams.
  - Digestate blends: mixes designated as D1, D2, and combinations with ash (D1A1, D1A2, D2A1, D2A2).
  - Biomass ashes: fly ash (A1) and bottom ash (A2), characterized as part of the blend compositions.
  - Sample handling: 5–10 kg per digestate sample; kept cold (<4°C) post-receipt and analyzed promptly.

- Experimental design and workflow
  - Two-stage approach:
    - Stage 1: Preliminary polymer dose test to identify optimum polymer dose for each digestate/ash mix.
    - Stage 2: Dewaterability and nutrient fractionation test using the optimum polymer dose to generate fibre and liquor fractions.
  - Polymer dosing and testing:
    - Polymers tested: DW2145, FO4498SSH, and FAM4028 with varying charge density and molecular structure.
    - Polymers tested as 0.5% solutions added at rates based on dry solids (DS) per kg of digestate/ash mix to achieve different mg/kg DS doses (e.g., 0, 40, 50 mg/kg DS, etc.).
    - Jar-testing procedure: 1 L mixing vessels, two-stage stirring, followed by centrifugation to separate liquor and fibre; solids in liquor quantified as Total Suspended Solids (TSS).
  - Dewaterability and nutrient profiling:
    - After determining optimum polymer for each mix, 50 mL samples of blends and raw digestates were dewatered by centrifugation (3000 rpm, 10 min) to obtain liquor and fibre.
    - Each condition replicated three times (36 samples in total for WP1A2).

- Datasets and key variables
  - WP1A1.csv (Polymer dose test)
    - Variables: Blend (sample identity), PolType (polymer type), PolDose (g polymer per kg DS), Supernatant (volume), PolAdded (volume added), TSS (mg/L in liquor).
    - Purpose: identify optimum polymer type and dose for each digestate/ash mix by minimizing total suspended solids in the liquor.
  - WP1A2.csv (Dewaterability and nutrient fractionation)
    - Fractions and outputs: liquor and fibre fractions; SupProd (volume of liquor produced), SolidsProd (mass of fibre solids), DS (dry solids), DSProd, pH.
    - Measured chemical/elemental contents (in liquor and/or fractions): Ca, Mg, P, K, TKN (Total Kjeldahl Nitrogen), S, and additional elements listed in the dataset key (e.g., Fe, Mn, Zn, Cu, Cl, B) as per Table 2/3 references.
    - Methods and units: ICP-OES for metals (Ca, Mg, K, etc.), 30 Metals in Soil by ICP-OES; TKN by 48 TKN in soil by ISE; APHA methods referenced; results generally reported on a dry basis unless stated otherwise.
  - Data notes: “-NA” denotes non-applicable; DL indicates results below detection limit; results follow the standard methods referenced (APHA1999; ALS Global Ltd analyses).

- Methods, QA, and governance
  - Analytical methods: external accredited laboratories (ALS Global Ltd) performed analyses; methods include JAS-034, JAS-373, JAS-379, JAS-510, JAS-300, JAS-082, APHA 1999 standards.
  - Data management: metadata includes author list with affiliations and contact details; tabled keys and method references are provided to ensure reproducibility and traceability.
  - Data sharing and openness: dataset descriptions note potential barriers to publicly sharing datasets; standard metadata and provenance are documented to support reuse and governance.

- Practical implications for monitoring frameworks
  - Demonstrates a structured approach to evaluating environmental health/process performance metrics (dewaterability, nutrient partitioning) in digestate management.
  - Highlights the importance of:
    - Clear metadata and dataset keys to interpret variables across datasets (e.g., blend IDs, polymer types, dosing, fractions).
    - Adherence to standardized analytical methods to enable cross-study comparability.
    - Data governance considerations (data sharing, provenance, quality assurance) to ensure data usable for policy evaluation and decision-making.
  - Relevance to policy and management: provides quantifiable indicators (TSS reduction, liquor/fibre nutrient content, DS, pH, produced volumes) that can feed into monitoring frameworks assessing efficiency and environmental outcomes of dewatering strategies in anaerobic digestion and digestate handling.