# WP1A Dewaterability potential of anaerobic digestate and biomass ash blends using polymer dose approach

- Overview
  - Purpose: Investigate how biomass ash addition affects the dewaterability of anaerobic digestate and to understand nutrient partitioning between liquor and fibre during dewatering.
  - Data files: Two datasets associated with WP1A
    - WP1A1.csv: results from the polymer dose screening (preliminary test)
    - WP1A2.csv: results from the blends dewaterability and nutrient fractionation test
  - Context: Digestate from anaerobic digestion is dewatered to separate fibre and liquor; food waste digestate is particularly challenging to dewater and requires more polymer flocculants. The study also examines nutrient distribution (nitrogen and phosphorus) between liquor and fibre fractions.

- Materials and samples
  - Anaerobic digestates
    - Sourced from different industrial-scale UK plants at various project stages.
    - Feedstock variants include source-segregated food waste, maize silage, vegetables/other biodegradable sludges.
    - Samples (5–10 kg per) were cooled and analysed promptly after receipt.
  - Biomass ashes
    - Fly ash (light fraction) and bottom ash (heavy fraction) produced from biomass combustion.
    - Prepared by drying, grinding/milling, and sieving to ≤1 mm before analysis.
  - Nutrient characterization
    - A wide suite of nutrients measured (e.g., total N, nitrate N, ammonium N, total P, K, Ca, Mg, Fe, Zn, Mn, Cu, S, etc.) using specified methods.
    - Data presented as total concentrations per kg or as appropriate units; some measurements use dry basis.

- Experimental design
  - Mixes
    - Four digestate/ash blends created: D1, D2 (digestates) and D1A1, D1A2, D2A1, D2A2 (blends with ash).
    - Final total nitrogen to total phosphorus ratio targeted at 3:1.
  - Polymers tested
    - DW2145 [DW] – cationic, cross-linked
    - FO4498SSH [FO] – cationic, branched
    - FAM4028 [FAM] – cationic/anionic, branched
  - Experimental stages
    - Stage 1: Preliminary polymer dose test to identify optimum dose per blend to minimize total suspended solids (TSS) in the liquor.
    - Stage 2: Dewaterability test using the optimum polymer dose from Stage 1 to generate fibre and liquor, with nutrient profiling.

- Methods (polymer dose screening)
  - Polymer preparation: 0.5% polymer solution made with deionized water.
  - Jar-testing protocol per blend
    - Four 0.1 L aliquots tested per blend in a jar-testing setup.
    - Mixing: 2 minutes at 100 rpm, then 15 minutes at 30 rpm.
    - Polymer dosing: equivalent to 0, 5, 10, 20 g polymer per kg of dry solids (DS) in the blend.
    - Separation: 50 mL subsamples centrifuged at 3000 rpm for 15 min to yield liquor and fibre.
    - Analysis: solids in liquor determined after filtration and drying at 105°C.
  - Outcome: TSS data used to identify optimum polymer type and dose for each blend.
  - Data files: WP1A1.csv contains details of this preliminary polymer dose testing (blend, polymer type, dose, supernatant, TSS, etc).

- Methods (dewaterability and nutrient fractionation)
  - Dewatering test at optimum dose
    - Using 50 mL samples of each blend (D1A1, D1A2, D2A1, D2A2) and raw digestates (D1, D2).
    - Centrifugation: 3000 rpm for 10 minutes to separate fibre and liquor.
    - Replication: three technical replicates, totaling 36 samples for subsequent testing.
  - Measurements in WP1A2
    - Liquor and fibre fractions analyzed for nutrient content and other solids.
    - Nutrients and solids measured include Ca, Mg, P, K, TKN, S, DS, DSProd, SupProd, and other minerals.
  - Data structure
    - Table 5 (Key for WP1A1.csv) explains columns such as Blend, PolType, PolDose, Supernatant, PolAdded, TSS, etc.
    - Table 6 (Key for WP1A2.csv) explains columns for liquor/fibre fractions, nutrient concentrations (Ca, Mg, P, K, TKN, S), product volumes (SupProd), solids produced (SolidsProd), DS, pH, and related measurements.
  - Data provenance
    - Methods referenced include standard techniques (APHA, 1999) and ALS Global Ltd analyses (method numbers 30–69, 2540–4500).

- Data content and structure
  - WP1A1.csv
    - Contains data from preliminary polymer dose tests across blends.
    - Variables include blend identifier, polymer type, polymer dose (mg/kg DS), supernatant volume, amount of polymer added, and measured TSS.
  - WP1A2.csv
    - Contains data from the dewaterability and nutrient fractionation tests.
    - Variables include blend identifiers, liquor and fibre fractions, nutrient concentrations (Ca, Mg, P, K, TKN, S, etc.), total solids produced, DS, DS% (dry solids), and related measurements.
  - Coding and interpretation
    - D1, D2 designate digestates; D1A1, D1A2, D2A1, D2A2 designate digestate-ash blends.
    - DS refers to dry solids; DSProd refers to total mass of solids produced; SupProd to total liquor volume produced.

- Author, references, and notes
  - Authors and affiliations: Dr. Alfonso Jose Lag Brotons; Dr. David Thompkins; Andy Burgess; Dr. Rachel Marshall; Ben Herbert; Dr. Lois Hurst; Prof. Kirk T. Semple.
  - References: APHA (1999) Standard Methods for the Examination of Water and Wastewater.
  - Notes
    - Results are typically on a dry basis unless specified otherwise.
    - Some cells may be marked as DL (detectable limit) or N/A where not measured.
    - Data include detailed method references and are intended to support understanding of dewaterability with ash additions and nutrient partitioning.

- Usage and potential applications
  - Enables analysis of dose-response relationships between polymer dose and dewaterability (TSS reduction) for different digestate/ash blends.
  - Allows comparison of how ash type and proportion affect fibre yield, liquor quality, and nutrient distribution between phases.
  - Supports modelling and optimisation of dewatering processes and nutrient management in anaerobic digestion systems with ash co-processing.