# Dataset on transfer of radionuclides/elements to foodstuffs in Spain

## Overview
- Dataset belonging to Deriverable D9.14: Published dataset on transfer in Mediterranean ecosystems (CONFIDENCE project).
- Authors: J. Guillén, F.M. Gómez-Polo, A. Baeza, M.A. Ontalba (LARUEX, University of Extremadura).
- Scope: Data and methods for radionuclide and stable element transfer from soil to foodstuffs across Spain, enabling map-based analysis and GIS applications.

## Sampling design and sites
- Two sampling schemes:
  - Main production regions: areas where the main production of each food occurs (selected via public info from the Spanish Ministry of Agriculture).
  - Local level: a dehesa managed by the regional government in Extremadura (Mediterranean semi-natural grassland with holm oaks).
- Geolocation:
  - Sites recorded with handheld GPS (latitude/longitude, WGS84).
  - Figure 1 shows approximate sampling-site locations.
- Foodstuff groups sampled:
  - Cereals (e.g., wheat, triticale, oats, barley).
  - Grapevine products (plant, grapes, wine; varieties Pinot noir, Tempranillo).
  - Olives and olive oil.
  - Animal products: lamb, beef, pork; dairy products (sheep, goat, cow milk; cheeses; yogurts; kefir).
- Accompanying matrices:
  - Soils (0–10 cm), wild grasses, and animal feeds collected at each site.

## Sample collection details
- Soil: composite samples (minimum 6 per site) from 0–10 cm, combined for analysis.
- Wild grass: cut to minimize soil contamination; dominant species identified.
- Plants and products: whole cereal plants separated into roots, stem, grain; grape leaves/branches and mature grapes collected; olives and olive leaves/branches collected; wine/olive oil prepared as described.
- Animal products: meat, bone, liver, and kidney collected at slaughterhouses; animal feed information collected from producers.
- Regions and examples:
  - Wheat: Extremadura, Castilla-León, dehesa.
  - Grapevine: Andalusia, Extremadura.
  - Olive: Extremadura, Andalusia.
  - Livestock and dairy: dehesa in Extremadura; various feeding regimes documented.

## Laboratory analyses
- ICP-MS for stable elements (Cs, Sr, U, Th, Pb, K, Ca, Na, Mg, P).
  - Equipment: NexIon 350X ICP-MS; KED mode with helium collision gas to reduce interferences.
  - Calibration and standards: external calibration with internal standardization; detection limits and uncertainties established; recoveries ~106%.
- Gamma spectrometry for radionuclides (after ~21 days for equilibrium):
  - Nuclides: 137Cs, 214Pb, 214Bi (in equilibrium with 226Ra), 228Ac (in equilibrium with 232Th series), 40K.
  - Equipment: HPGe detectors; calibration with NPL multi-radionuclide cocktails; ISO/IEC 17025 accredited.
  - Quality control: IAEA reference materials; uncertainties per ISO11929.
- Physico-chemical soil parameters:
  - pH (in water), conductivity, texture (clay, sand fractions, silt), organic matter; standard soil procedures.

## Transfer parameter calculations
- Transfer from soil to plants (Fv) for radionuclides and stable elements:
  - Fv = Plant concentration (Bq/kg dry mass or mg/kg dry mass) / Soil concentration (Bq/kg dm or mg/kg dm) (0–10 cm).
- Transfer to liquids from plants (Fv,kg dm/L):
  - Fv = Liquid food concentration (Bq/L or mg/L) / Soil concentration (Bq/kg dm or mg/kg dm).
- Transfer to animal-derived foods (CR, concentration ratio):
  - CR = Food concentration (fresh weight) / Diet concentration (dry matter).
  - Diet composition information from producers; includes proportions of feedstuffs and wild grass intake estimated from literature when needed.
  - For milk (liquid), CR = Milk concentration (per L) / Diet concentration (dry matter).
- Special considerations:
  - If a radionuclide/stable element is below detection in all diet components, detection limits used to estimate feed concentration (<30% contribution).
  - If a component contributes >30% of dry matter intake, detection limits used but reported as “less than”; in that case, transfer parameters may not be calculated.
- Data integration:
  - When several feeds contribute to diet, a weighted overall diet concentration is used for CR calculations.

## Data quality and uncertainty
- Instrument verification and calibration performed daily using multi-element standards.
- Use of certified reference materials (IAEA, SPS-SW2; IAEA-359; IAEA-SOIL-7) for accuracy checks.
- Uncertainties calculated following standard protocols (ISO 11929; k=2).
- Carrying out duplicates and internal standards to control measurement variability; high calibration correlation (r > 0.999).

## GIS relevance and data usage
- Spatially explicit transfer parameters across Spain enable map-based visualization of soil-to-food transfer for radionuclides and stable elements.
- Data integrate soils, plant types, animal feeds, and dietary components, supporting:
  - Spatial risk assessment of radionuclide transfer in different land-use contexts (dehesas, vineyards, olive groves, grazing lands).
  - Cross-referencing with land cover, soil properties, and farming practices for policy and public communication.
  - Enhanced GIS datasets for Mediterranean ecosystem transfer studies and comparative analyses within CONFIDENCE/CONCERT frameworks.

## Acknowledgements and funding
- Funded by the CONFIDENCE project (H2020; grant No 662287) and Spanish Ministry of Economy, Industry and Competitiveness (grant PCIN-2017019).
- Euratom research and training programme 2014–2018 support; thanks to CICYTEX for technical support.
- Disclaimer: views are authors’ own; EC not responsible for use.

## References
- IAEA TRS-472 (radionuclide transfer handbook).
- ISO standards: ISO/IEC 17025; ISO 11929 for detection limits.
- Nutritional and dietary references for ruminants (FEDNA and INRA sources cited).