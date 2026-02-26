# WP1A Dewaterability potential of anaerobic digestate and biomass ash blends using polymer dose approach

## Overview
- Evaluates the impact of biomass ash on the dewaterability of anaerobic digestate blends using polymer dosing.
- Two experiments were conducted to explore dewaterability and nutrient partitioning between liquor and fibre fractions.
- Samples come from anaerobic digestion plants across the UK; ash fractions (fly ash and bottom ash) are included.
- Produces two datasets: WP1A1.csv (polymer dose test) and WP1A2.csv (blends dewaterability and nutrient fractions).
- Methods involve jar-testing, centrifugation, and analysis of total suspended solids (TSS) and nutrient content.

## Data Components
- WP1A1.csv: Preliminary polymer-dose test results for four digestate/ash blends (D1A1, D1A2, D2A1, D2A2); records optimum polymer type and dose per blend.
- WP1A2.csv: Dewaterability and nutrient-fractionation results using optimum polymer dose; includes blends plus raw digestates (D1, D2) and measured components (e.g., Ca, Mg, P, K, N, S, DS, TKN, pH, solids produced).
- Tables and metadata reference: detailed keys for data columns (e.g., Blend, PolType, PolDose, TSS, DS, SupProd, SolidsProd, fractions for liquor and fibre).

## Experimental Setup
- Digestates: samples from different UK AD plants; 5–10 kg per sample; stored cold and analyzed promptly.
- Ash: biomass fly ash and bottom ash; 10–20 kg per sample; processed to pass 1 mm and stored for analysis.
- Blends: four combinations (D1, D2) with ash fractions to form D1A1, D1A2, D2A1, D2A2; designed with final total nitrogen to total phosphorus ratios of 3:1.
- Polymer dosing: four levels at 0, 5, 10, and 20 g polymer per kg of dry solids (DS) in the blends.

## Procedures
- Preliminary polymer-dose testing (WP1A1):
  - Prepare 0.5% polymer solutions; dose blends in jar-test vessels.
  - Mix: 2 min at 100 rpm, then 15 min at 30 rpm.
  - Centrifuge at 3000 rpm for 15 min to separate liquor and fibre.
  - Filter, dry solids to constant weight, and determine TSS in liquor.
- Dewaterability and nutrient fractionation testing (WP1A2):
  - Use optimum polymer type and dose from WP1A1.
  - Centrifuge 50 mL samples at 3000 rpm for 10 min to obtain liquor and fibre.
  - Replication: three runs per blend (36 samples total for WP1A2).
  - Measure nutrient and elemental concentrations in liquor and fibre fractions.

## Measurements and Methods
- Parameters measured (per WP1A2): Ca, Mg, P, K, S, TKN, DS, pH, and various other elements (Fe, Mn, Zn, Cu, Mo, Cl, B), expressed on a dry basis where applicable.
- Fraction data: liquor vs fibre; total solids produced (SolidsProd); liquor volume (SupProd); dry solids (DS); pH.
- Analytical methods: referenced to standard methods (ALS Global Ltd) and APHA 1999 for various elements and parameters; multiple method codes (e.g., JAS-034, JAS-373, 30 Metals in Soil by ICP-OES; 2540-4500).
- Data notes: results may include non-detects (DL<); blank replicates indicate unmeasured samples; methods are largely dry-basis unless specified.

## Data Quality and Standards
- All measurements follow standard laboratory practices with clearly defined method references.
- Results are reported on a dry basis unless stated otherwise.
- Documentation includes detailed metadata (tables 1–6) describing blends, polymers, dosing, and measurement keys.

## GIS and Data Product Opportunities
- Spatial mapping of dewaterability performance across UK AD plants:
  - Link blend compositions (D1, D2, ash fractions) and optimum polymer doses to plant location.
  - Create map layers showing expected TSS reduction in liquor at given DS and polymer dose.
  - Visualize nutrient partitioning (N, P, K) between liquor and fibre by site and feedstock mix.
- Data-driven decision support:
  - Identify best-performing polymer types and doses for different blend compositions.
  - Assess regional data gaps where dewaterability or nutrient data are lacking at suitable resolution.
- Potential data products:
  - Interactive maps of optimum polymer dose vs. blend type.
  - Spatial dashboards showing dewaterability efficacy and nutrient separation profiles.

## Authors and Access
- Dr. Alfonso Jose Lag Brotons; a.lagbrotons@lancaster.ac.uk
- Dr. David Thompkins; david.tompkins@suez.com
- Andy Burgess; AndyBurgess@aquaenviro.co.uk
- Dr. Rachel Marshall; r.marshall2@lancaster.ac.uk
- Ben Herbert; ben.herbert@stopford.co.uk
- Dr. Lois Hurst; loishurst@outlook.com
- Prof. Kirk T. Semple; k.semple@lancaster.ac.uk

## References
- APHA1999. American Waterworks Association. Standard methods for the examination of water and wastewater, 20th edition.