# WP1A Dewaterability potential of anaerobic digestate and biomass ash blends using polymer dose approach

- Purpose and scope
  - Investigates dewaterability of anaerobic digestate blended with biomass ash using a polymer-dose approach.
  - Explores the impact of ash on digestate dewaterability and how nutrients (nitrogen, phosphorus) partition between liquor and fibre.
  - Aims to identify optimum polymer doses for four digestate/ash mixtures and to characterize nutrient profiles in the resulting fractions.

- Dataset structure and contents
  - Two associated datasets (WP1A1.csv and WP1A2.csv) covering the polymer-dose tests and the blends’ dewaterability with nutrient fractionation.
  - WP1A1.csv: preliminary polymer-dose test data for four digestate/ash blends; includes variables such as blend id, polymer type, polymer dose (mg/kg DS), supernatant volume, polymer added, and measured total suspended solids (TSS) in the liquor.
  - WP1A2.csv: dewaterability outcomes for blends using the optimum polymer dose from WP1A1 and the nutrient profiles of both liquor and fibre fractions; includes concentrations of Ca, Mg, P, K, TKN, S, and other elements, along with fractions and yields (SupProd, SolidsProd, DS, pH, etc.).

- Materials and sample description
  - Digestates: samples collected from various industrial-scale anaerobic digestion plants across the UK at different project times; feedstocks include source-separated food waste (D1) and mixed inputs such as maize silage, vegetables, sweet corn waste, aerobic-treated food waste, and other biodegradable sludge (D2).
  - Biomass ashes: fly ash and bottom ash derived from thermal biomass processing; samples prepared as composites, ground and sieved to pass 1 mm, stored for analysis.
  - Sample handling: 5–10 kg digestate per sample; 10–20 kg ash per sample; samples stored in cold conditions (<4°C) and analysed promptly.

- Experimental design and methods
  - Preliminary (polymer-dose) testing:
    - Prepare 0.5% polymer solutions and test four dose rates relative to dry solids: 0, 5, 10, 20 g polymer per kg DS.
    - Jar tests: 0.1 L aliquots mixed with 1 L vessels; cycle 2 minutes at 100 rpm, then 15 minutes at 30 rpm.
    - Determine optimum polymer type/dose by minimizing total suspended solids in the liquor after centrifugation (3000 rpm, 15 minutes).
    - Centrifuge and filter to measure TSS in liquor; document results in WP1A1.csv.
  - Dewaterability and nutrient fractionation testing:
    - Use optimum polymer dose for each blend to dewater 50 mL samples via centrifugation (3000 rpm, 10 minutes) to obtain fibre and liquor.
    - Replicate experiments (three repeats), producing multiple samples for each blend (D1, D1A1, D1A2, D2, D2A1, D2A2).
    - Analyze nutrient content and other parameters in both fractions (e.g., Ca, Mg, P, K, TKN, S, and multiple trace elements) following specified methods.

- Key variables and measurements
  - Headline measurements: Total Suspended Solids (TSS) in liquor; volumes of liquor (SupProd) and solids produced (DS/DSProd) for fibre and liquor fractions.
  - Nutrient and elemental concentrations: Ca, Mg, P, K, S, total nitrogen (TKN), nitrate (NO3-N), ammonium (NH4-N), and trace elements (Fe, Mn, Zn, Cu, B, Mo, etc.) in both fractions; expressed on a dry basis unless noted otherwise.
  - Dosing and process parameters: polymer type (DW2145, FO4498SSH, FAM4028), polymer dose per kg DS, and the volume of polymer added.
  - Analytical methods: reference to standard methods for water/wastewater analyses (APHA) and ICP-OES/other methods (ALS Global Ltd) as applicable.

- Data provenance and governance
  - Associated metadata prepared by a team including Dr. Alfonso Lag Brotons, Dr. David Tompkins, Andy Burgess, Dr. Rachel Marshall, and others; includes contact details.
  - Data framed around WP1A1 (polymer-dose testing) and WP1A2 (dewaterability and nutrient fractionation) with explicit mappings of blends to treatment conditions.
  - References to standard methods and laboratory partners; datasets include detailed method notes and data dictionaries (Tables 4–6 referenced in the metadata).

- Notes and references
  - Methods rely on standard APHA procedures (APHA1999) and ALS Global Ltd analytical references (method numbers listed in WP1A2).
  - Background on the context of digestate dewatering and nutrient partitioning in the presence of ash blends.

- Practical implications for data management
  - Data capture aligns with clear file naming (WP1A1.csv, WP1A2.csv) and explicit keys describing blends, polymers, doses, and measured outputs.
  - Metadata documents the experimental workflow, enabling reproducibility, traceability of samples, and assessment of data quality and limitations.