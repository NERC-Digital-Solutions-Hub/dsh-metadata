# Chemical composition of anaerobic digestate and biomass ash blends as a result of storage

## Overview
- Purpose: Evaluate whether adding high-pH biomass ash to digestate affects nutrient stability, particularly ammonium retention, and how treated digestates change over time.
- Scope: Time-series experiments on ash-amended and un-amended digestates over several months, focusing on labile agronomic components (nitrogen and sulphur).
- Relevance: Supports environmental monitoring and policy by understanding nutrient dynamics and potential volatilization (NH3) from digestate with ash amendments.

## Data and Materials
- Digestates
  - Sourced from UK industrial anaerobic digestion plants at different project phases.
  - Samples labeled D1 and D2 (different feedstocks); D1A1 and D2A1 refer to digestates amended with biomass ash.
  - Sample sizes: 5–10 kg per digestate sample; chilled after receipt and analysed promptly.
- Biomass ashes
  - Waste from biomass combustion; includes fly ash (light fraction) and bottom ash (heavy fraction).
  - Example composition described for fly ash (A1) with specific base materials (e.g., Sitka spruce, Larch).
  - Ash samples processed to sub-samples, air-dried, milled to pass 1 mm, stored at room temperature.
- Data structure elements
  - Detailed material characteristics (e.g., oven dry solids, total nitrogen, nitrate, ammonium, phosphorus, potassium, sulphur, calcium, magnesium, copper, zinc, iron, manganese, chlorine, boron, molybdenum).
  - Analytical methods referenced (primarily JAS standards; external labs involved).
- Accessibility
  - Data accessible via DOI: https://doi.org/10.5285/e91e8c28-0176-4c5b-9b20-611eb505ab39
  - Dataset citation provided in the document.

## Experimental design and methods
- Treatments (8 total)
  - D1, D2: unamended digestates
  - AD1, AD2: digestates acidified with 98% sulfuric acid to target pH 5.5
  - D1A1, D2A1: digestates amended with ash
  - AD1A1, AD2A1: digestates amended with ash and acidified
- Procedure
  - 9 litres of each substrate per treatment, divided into three replicates (to yield three containers per treatment).
  - Acidification performed with concentrated sulfuric acid as needed to reach pH 5.5 (with noted foaming challenges).
  - Samples stored indoors at ~20°C.
  - Sub-sampling schedule: days 0, 1, 2, 4, 8, 16, 32, 64, and 128.
- Analytical suite
  - General parameters: dry solids (DS) and pH.
  - Nutrients: Total Kjeldahl Nitrogen (Total-N), Total Sulphur (Total-S).
  - Additional data (for both digestates and ashes): comprehensive elemental analyses (e.g., N, N-NO3, N-NH4, P, K, Mg, Ca, Cu, Zn, Fe, Mn, Mo, Cl, B, S) with various standard methods (JAS series) and external laboratories.
- Observations during testing
  - Acidification caused significant foaming; required vigorous agitation to reach and maintain target pH.
  - Foaming persisted for hours, creating practical barriers for mixing and commercial-scale implementation.
  - Implications noted: further work needed to manage foaming for scalable digestate acidification.

## Data structure and metadata
- Key dataset fields (WP1B.csv)
  - Treatment: describes material and whether acid was added; ties to Table 4 for descriptions.
  - Material: digestate and ash combination.
  - Acid: whether 98% H2SO4 was added.
  - Days: time since start (in days).
  - Replicate: replicate identifier (e.g., a, b, c).
  - DS: dry solids (%).
  - TKNf/TKNd: total Kjeldahl nitrogen (fresh and dry basis).
  - TSf/TSd: total sulphur (fresh and dry basis).
  - Other fields reflect detailed nutrient and elemental concentrations for digestates and ashes.
- Data quality and provenance
  - Measurements performed following standard methods; external laboratories involved for certain analyses.
  - Dataset compiled to support monitoring of environmental nutrient dynamics and the impact of waste amendments on digestate quality.

## Key findings and implications
- Ash amendment and nutrient stability
  - The study investigates whether biomass ash amendments influence ammonium retention in digestate and how the composition evolves during storage.
- Acidification challenges
  - Acidifying digestates (and ash-containing mixes) to pH 5.5 produced strong foaming, requiring intense mixing; this presents a practicable obstacle for field or commercial-scale implementation.
- Data utility for monitoring
  - The dataset provides a time-resolved view of nutrient dynamics (N, S, and other elements) in digestates with and without ash, both with and without acidification, enabling assessment of environmental risk and nutrient management strategies.

## Access, attribution, and contact
- Access: Data available via the provided DOI link; dataset and accompanying metadata published for reuse.
- Citation: Lag-Brotons, A.J.; Thompkins, D.; Burguess, A.; Marshall, R.; Herbert, B.; Hurst, L.; Semple, K.T. (2020). Chemical composition of anaerobic digestate and biomass ash blends as a result of storage. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/e91e8c28-01764c5b-9b20-611eb505ab39
- Authors and affiliations: Includes researchers from Lancaster University, Aqua Enviro, Stopford Energy, and collaborators.
- References: APHA (1999) Standard methods; Fangueiro et al. (2015) on acidification of animal slurry.