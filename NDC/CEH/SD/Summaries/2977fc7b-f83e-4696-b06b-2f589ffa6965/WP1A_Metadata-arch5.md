# WP1A Dewaterability potential of anaerobic digestate and biomass ash blends using polymer dose approach

- Two-file dataset describing dewaterability experiments for anaerobic digestate and biomass ash blends using polymer dosing
- Aims to explore how ash addition affects digestate dewaterability and how nutrients (N, P, etc.) partition between liquor and fibre
- Digestates were sourced from UK industrial plants; biomass ashes (fly ash and bottom ash) were also used
- Data intended to support understanding of polymer-assisted dewatering performance and nutrient partitioning, with potential implications for waste treatment and resource recovery

## Data files and structure

- WP1A1.csv
  - Polymer dose test results (preliminary optimization)
  - Variables include blend identifiers, polymer type, polymer dose (mg/kg DS), supernatant volume, total suspended solids (TSS) in liquor, and related measurements
- WP1A2.csv
  - Dewaterability and nutrient fractionation results for blends using the optimized polymer dose
  - Variables include blend identifiers, fractions (liquor vs fibre), total nutrient concentrations (e.g., Ca, Mg, P, K, S, N, etc.), and yield indicators for liquor/fibre
- Both files accompany a metadata narrative describing sample origins, preparation, and analysis methods

## Experimental design and methods

- Overall approach
  - Two-stage experimental workflow to determine optimum polymer dose and evaluate dewaterability and nutrient partitioning
- Stage 1: Preliminary polymer dose test
  - Digestate/ash mixes prepared to form four combinations (D1A1, D1A2, D2A1, D2A2)
  - Four polymer doses tested to minimize total suspended solids (TSS) in the separated liquor
  - Procedures
    - Prepare 0.5% polymer solutions and dose 0, 5, 10, 20 g polymer per kg dry solids (DS)
    - Jar tests: mix 2 minutes at 100 rpm, 15 minutes at 30 rpm
    - Centrifuge at 3000 rpm for 15 minutes to separate liquor and fibre
    - Filter liquor, dry solids at 105°C, and measure TSS
  - Outcome: identify optimum polymer type and dose for each mixture (WP1A1)
- Stage 2: Blends dewaterability and nutrient fractionation
  - Use optimum polymer and dose determined in Stage 1
  - Dewater six blends plus raw digestates (D1, D2)
  - Centrifuge 50 mL samples at 3000 rpm for 10 minutes to obtain fibre and liquor
  - Replication: each condition performed three times (total 36 samples across six blends)
  - Nutrient profiling conducted on both liquor and fibre fractions
- Key variables and units
  - Polymer dose expressed as mg/kg DS; other measurements include TSS, nutrient concentrations (various units per element/metallurgy)
  - Data tables provide structured keys for interpreting the measurements (Tables 5 and 6 in the metadata)

## Materials and samples

- Digestates (anaerobic digests)
  - Collected from multiple industrial-scale UK plants over the project lifetime
  - Samples sized 5–10 kg, delivered in jerry cans/barrels, cooled, and stored in ice, then analyzed in a cold room (<4°C)
  - Feedstock compositions referenced include source-separated food waste, maize silage, vegetables, sweetcorn waste, aerobically treated food waste, and other biodegradable sludge
- Biomass ashes
  - Fly ash (light fraction) and bottom ash (heavy fraction) described with source material compositions
  - Sample sizes 10–20 kg, courier-delivered, air-dried, ground/milled to pass 1 mm
- Analytical context
  - Materials characterized using external accredited laboratories (NRM) and ALS Global Ltd for metal/elemental analyses
  - Analytical methods referenced by standard codes (e.g., JAS, APHA methods) and professional laboratory reporting

## Polymers used

- DW2145 (DW): cationic, cross-linked
- FO4498SSH (FO): cationic, branched
- FAM4028 (FAM): cationic/anionic, branched
- Polymer selection based on charge density, molecular weight, functional groups, and branching to evaluate dewatering performance

## Measurements and data columns

- WP1A1.csv (polymer dose test)
  - Blend identifier; Polymer type (PolType); Polymer dose (PolDose, g/kg DS); Supernatant volume; Total Suspended Solids (TSS) in liquor
  - Additional fields include volumes added (PolAdded) and general notes on test execution
- WP1A2.csv (dewaterability and nutrients)
  - Blend identifiers; Fractions (liquor, fibre); Nutrient concentrations (Ca, Mg, P, K, S, N species, etc.); Kjeldahl nitrogen (TKN); Solids production (DS and fibre mass); pH and related fields
  - SupProd and SolidsProd denote liquor and fibre yields, respectively; DS indicates dry solids
- Data interpretation aids
  - Tables 5 and 6 provide keys for WP1A1.csv and WP1A2.csv, respectively
  - Data may include DL (data below detection limit) and blanks indicating non-measured replicates
  - Results are generally expressed on a dry basis unless noted otherwise
- Methods and references
  - Analyses reference standard methods such as APHA (APHA1999) and methods 30/69, 2540/4500, etc., with ALS Global Ltd performing analyses on behalf of the project

## Data provenance, access, and governance

- Authorship and contact
  - Dr. Alfonso Jose Lag Brotons; Dr. David Thompkins; Andy Burgess; Dr. Rachel Marshall; Ben Herbert; Dr. Lois Hurst; Prof. Kirk T. Semple
  - Provided email contacts and ORCID identifiers for principal investigators
- Metadata and standards
  - Dataset described with dedicated parameter tables, units, and method references
  - References to APHA (Standard Methods) and JAS method codes indicate standardized measurement approaches
- Relevance to data stewardship
  - Clear documentation of sampling, handling, and analytical procedures supports data governance, reproducibility, and cross-dataset interoperability
  - The dataset aligns with governance priorities: standardization of formats, provenance, and clarity on data limitations
- Limitations and notes for data stewards
  - Description field includes pending details in the metadata narrative; ensure future curations fill in missing methodological specifics
  - Some measurements are reported as DL or blank, which should be captured in metadata for proper interpretation
  - Methods and conditions vary across stages (preliminary dosing vs. dewaterability tests), requiring careful schema alignment when integrating with broader datasets

## References

- APHA1999. American Waterworks Association (1999) Standard methods for the examination of water and wastewater. 20th edition, USA