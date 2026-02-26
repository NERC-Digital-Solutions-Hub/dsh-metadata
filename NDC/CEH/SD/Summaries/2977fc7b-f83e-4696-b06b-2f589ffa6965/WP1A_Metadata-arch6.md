# WP1A Dewaterability potential of anaerobic digestate and biomass ash blends using polymer dose approach

## Overview
- Evaluates the dewaterability of blends of anaerobic digestate and biomass ash using polymer dosing to improve solid-liquid separation.
- Two experiments produced two datasets:
  - WP1A1.csv: polymer dose testing to identify optimum doses.
  - WP1A2.csv: dewaterability and nutrient fractionation of blends using the optimum doses.
- Context: understanding how ash addition and polymer dosing influence dewaterability and nutrient distribution between liquor and fibre fractions.

## Datasets Included
- WP1A1.csv: results from preliminary polymer dose tests intended to minimise total suspended solids in the liquid fraction; includes blend identity, polymer type, dose, and measured supernatant solids.
- WP1A2.csv: results from blends dewaterability and nutrient partitioning tests using optimum polymer doses; includes liquor and fibre fractions with measured nutrient and element concentrations, production volumes, and related measurements.
- Both datasets are associated with WP1A and accompanied by metadata describing samples, methods, and units.

## Materials and Sampling
- Digestates: sourced from different industrial-scale anaerobic digestion plants in the UK; two feedstock varieties referenced (D1 and D2) with mixed household/food waste inputs and other biodegradable sludges.
  - Sample handling: 5–10 kg per digestate sample, cooled and transported in suitable containers; analyzed soon after receipt; stored in a cold room (<4°C).
- Biomass ash: ash fractions from biomass combustion, including fly ash (A1) and bottom ash (A2); typical sample size 10–20 kg; prepared by air-drying, milling, and sieving to pass 1 mm.
- Materials characterization: nutritional and elemental analyses conducted by external accredited labs; methods summarized in accompanying tables.

## Experimental Design
- Two-stage experimental workflow:
  1) Preliminary polymer dose (WP1A1) to find the optimum polymer dose for each digestate/ash mix.
     - Polymer solutions (0.5%) prepared and dosed to four digestate/ash mixes at rates equating to 0, 5, 10, 20 g polymer per kg dry solids (DS).
     - Jar testing: 0.1 L aliquots in 1 L jars, mixing as specified, followed by centrifugation (3000 rpm, 15 min) to separate liquor and fibre.
     - Liquor solids (TSS) measured; optimum polymer and dose identified per mix.
  2) Dewaterability and nutrient fractionation (WP1A2) using optimum polymer for blends.
     - Blends tested: D1, D1A1, D1A2, D2, D2A1, D2A2.
     - Each blend tested in triplicate, producing 36 samples for nutrient analysis.
     - Dewatering conducted by centrifugation (3000 rpm, 10 min) to yield liquor and fibre fractions.
- Nutrient/nutrient-related analyses conducted on both liquor and fibre; results include key elements and total nutrient concentrations.

## Polymer Types and Dosing
- Polymers tested (based on market leader guidance and properties):
  - DW2145 (cations, cross-linked)
  - FO4498SSH (cationic, branched)
  - FAM4028 (cationic/anionic, branched)
- Dosing scheme (per WP1A1 and WP1A2 metadata):
  - Preliminary test: 0, 5, 10, 20 g polymer per kg DS.
  - Optimal dosing for each blend determined in WP1A1 and applied in WP1A2:
    - Blend mappings and polymer doses (example mapping): D1 (50 mg/kg DS), D1A1 (40 mg/kg DS), D1A2 (50 mg/kg DS), D2 (40 mg/kg DS), D2A1 (40 mg/kg DS), D2A2 (50 mg/kg DS).

## Data Files and Variables
- WP1A1.csv (Polymer dose test)
  - Key columns: Blend, PolType (polymer type), PolDose (g polymer/kg DS), Supernatant (volume), PolAdded (mL), TSS (mg/L).
- WP1A2.csv (Dewaterability and nutrient fractionation)
  - Key columns: Blend, Fraction (liquor or fibre), for each element (Ca, Mg, P, K, S, N-related metrics such as TKN), plus production volumes (SupProd, SolidsProd), DS, DSProd, pH, and measurement method notes.
  - Nutrients and elements reported include: Ca, Mg, P, K, TKN (total Kjeldahl nitrogen), S, Ni etc. (as listed in the dataset metadata), with units and analytical methods provided in the accompanying tables.

## Data Provenance and Methods
- Analytical references: standard methods for water and wastewater analyses (APHA, 1999) and methods 30–69 from ALS Global Ltd for ICP-OES and related analyses.
- Methods applied: jar testing for polymer dosing, centrifugation for dewatering, drying and weighing for solids, and laboratory analyses for nutrient and elemental composition.

## Access, Authors, and References
- Authors of metadata and supplementary information include Dr. Alfonso Jose Lag Brotons, Dr. David Thompkins, Andy Burgess, Dr. Rachel Marshall, Ben Herbert, Dr. Lois Hurst, and Prof. Kirk T. Semple.
- Primary reference: APHA 1999, Standard Methods for the Examination of Water and Wastewater (20th edition).

## Use Cases for Data Support
- Build self-service dashboards to compare optimum polymer doses across digestate/ash blends and predict dewaterability improvements.
- Create data products showing nutrient partitioning between liquor and fibre for different blends, informing effluent management and nutrient recovery strategies.
- Integrate with broader datasets on anaerobic digestion outputs to support policy or operational decisions in waste management contexts.
- Promote reproducibility by documenting data provenance, methods, and file structures to facilitate reuse and sharing of WP1A datasets.