# Data access and citation

- Data can be accessed at: https://doi.org/10.5285/e91e8c28-0176-4c5b-9b20-611eb505ab39
- Suggested citation: Lag-Brotons, A.J.; Thompkins, D.; Burguess, A.; Marshall, R.; Herbert, B.; Hurst, L.; Semple, K.T. (2020). Chemical composition of anaerobic digestate and biomass ash blends as a result of storage. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/e91e8c28-01764c5b-9b20-611eb505ab39

## Purpose and scope

- Investigates the impact of adding high-pH biomass ash on nutrient stability in anaerobic digestate, focusing on ammonium (NH4+) retention and changes to digestate characteristics over time.
- Emphasizes labile agronomic components, particularly nitrogen and sulfur, across several months.

## Materials and samples

- Anaerobic digestates (digestate) collected from UK industrial-scale AD plants at different project stages.
- Digestate samples include different feedstock compositions (e.g., D1, D2; plus combinations with ash such as D1A1, D2A1).
- Biomass ashes: fly ash and bottom ash from thermal biomass processing (e.g., fly ash ABaF/A1; feedstock primarily virgin wood).
- Sample handling: digestates (5–10 kg per sample) collected at process end, cooled, and stored; ashes (10–20 kg per sample) courier-delivered; ash composites air-dried, ground/milled to pass 1 mm, stored at room temperature until use.
- Comprehensive material characterization (composition and solids) performed by external labs (NRM).

## Characterization and methods

- Analytical suite includes measurements such as:
  - Oven-dried solids (DS)
  - Total nitrogen (Total-N), nitrate-N (N-NO3), ammonium-N (N-NH4)
  - Total phosphorus (P), potassium (K), magnesium (Mg)
  - total metals (Cu, Zn, Fe, Mn, etc.), sulfur (S), calcium (Ca)
  - measurements performed with multiple standard methods (e.g., JAS-034, JAS-373/JAS-475, 2540 B3, 4500-H+ B, etc.)
- Data tables provide both fresh and dry basis values (e.g., TKNf/TKNd, TSf/TSd).

## Experimental design: digestate–ash acidification study

- Substrates and treatments:
  - Four primary substrate types: D1, D2, D1A1 (D1 + A1 ash), D2A1 (D2 + A1 ash)
  - Corresponding acidified treatments with H2SO4 to reach target pH of 5.5 (AD1, AD1A1, AD2, AD2A1)
  - Eight treatment configurations described in the study (presence/absence of acid and ash combinations)
- Volume and replication:
  - Each treatment started with 9 liters of substrate (digestate alone or digestate + ash)
  - Divided into three replicates per treatment
- Storage and sampling:
  - Containers stored at ambient ~20°C
  - Subsamples collected at days 0, 1, 2, 4, 8, 16, 32, 64, and 128
- pH adjustment:
  - Acidification used concentrated sulfuric acid (98% H2SO4)
  - Target pH of 5.5; volumes recorded per liter of mixture (e.g., 13.9 ml/L for AD1, 17.3 ml/L for AD1A1, 4.0 ml/L for AD2A1)
- Observations:
  - Acidification caused significant foaming; vigorous agitation required to reach target pH
  - Foaming remained extensive and could hinder commercial-scale implementation

## Data and metadata

- Data file: WP1B.csv
  - Columns describe: treatment (material, ash presence), acid addition (yes/no), volume of acid added, days, replicate, pH, dry solids (DS), total Kjeldahl nitrogen (TKNf, TKNd), total sulfur (TSf, TSd), among others
  - Describes mapping of treatments to materials and conditions (see Table 4 in the study for definitions)

## Practical implications and considerations

- Ash addition may influence ammonium stability in digestate; time-series data help assess NH3 loss risk and changes to nutrient profiles.
- The acidification experiments reveal practical challenges (foaming and mixing energy) that could limit industrial adoption without process adjustments.
- The dataset provides a foundation for correlating ash type, substrate, storage duration, and nutrient dynamics, informing nutrient management and agronomic use of treated digestates.

## Authors and references

- Authors: Alfonso Jose Lag Brotons; David Thompkins; Andy Burgess; Rachel Marshall; Ben Herbert; Lois Hurst; Kirk T. Semple
- References:
  - APHA (1999). Standard methods for the examination of water and wastewater. 20th ed.
  - Fangueiro, D.; Hjorth, M.; Gioelli, F. (2015). Acidification of animal slurry - a review. J Environ Manag.