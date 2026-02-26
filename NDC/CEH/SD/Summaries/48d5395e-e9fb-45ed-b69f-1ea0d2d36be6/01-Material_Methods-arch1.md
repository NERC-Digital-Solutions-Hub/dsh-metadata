# Dataset on transfer of radionuclides/elements to foodstuffs in Spain

## Overview
- Public dataset constituting Deliverable D9.14 of the CONFIDENCE project related to published transfer data in Mediterranean ecosystems.
- Aimed at quantifying transfer of radionuclides and stable elements from soil to foodstuffs in Spain to support risk assessment and modeling.
- Transfer parameters calculated following IAEA TRS-472 guidelines; data support both plant-based and animal-derived food products.

## Sampling sites and foodstuffs
- Two sampling schemes:
  - Main production regions, selecting areas with high production of specific foods using public information.
  - Local level sampling in dehesa landscapes managed by Extremadura regional government.
- Food product groups sampled:
  - Cereals: wheat, triticale, oats, barley.
  - Grapevine: leaves, grapes, wine (two regions; Pinot noir and Tempranillo varieties).
  - Olive: olives, leaves, branches, olive oil.
  - Animal-derived: lamb, beef, pork (Iberian pig), dairy products (sheep, goat, cow milk; sheep/goat/cow cheeses, yogurts, kefir).
- Additional samples: soil (0–10 cm), wild grass, and various animal feeds collected at each site.
- Regions covered include Extremadura, Castilla-León, Andalusia, Galicia, and others; approximate site locations illustrated in accompanying figure.

## Sample collection
- Site coordinates recorded with handheld GPS (WGS84).
- Soil: composite 0–10 cm samples formed by combining at least six subsamples from the same area.
- Wild grass: hand-cut; dominant species identified.
- Cereals: whole plants separated into roots, stem, grain; careful handling to minimize soil contamination.
- Grapevine, olive, and animal products: detailed collection of plant parts, wine, olive oil, and dairy/meat products; various varieties and feeding regimes documented.
- Animal feed and diet information collected from producers; animal data (where possible) linked to individual animals or flocks.

## Sample preparation and analysis
- ICP-MS analyses for stable elements (Cs, Sr, U, Th, Pb, K, Ca, Na, Mg, P):
  - Soil and solid samples digested via microwave with HNO3, HCl, HF; plant/food digested with HNO3 and H2O2.
  - External calibration with internal standardization; kinetic energy discrimination used to reduce interferences.
  - Detection limits prepared for each element (e.g., Cs 0.0005 µg/L, U 0.0004 µg/L, Ca 30 µg/L, etc.).
  - Daily instrument verification using a multi-element standard; recoveries ~106%.
- Gamma spectrometry for radionuclides:
  - Composite soils analyzed after drying and scintillation; wine and olive oil prepared per matrix needs.
  - Radionuclides targeted: 137Cs, 214Pb, 214Bi (in equilibrium with 226Ra), 228Ac (in equilibrium with 232Th), and 40K.
  - Secular equilibrium waited (~21 days) before measurement; calibration with NPL cocktail; quality control with IAEA reference materials (IAEA 385, IAEA Soil6) and ISO-compliant uncertainty calculation.
- Physico-chemical soil parameters:
  - pH (in water), electrical conductivity, texture (clay, sand fractions), organic matter content; standard procedures described (H2O2 digestion for organic matter, sieving, etc.).

## Transfer parameters and calculations
- Transfer parameters defined per IAEA TRS-472:
  - For plants (Fv): Fv = (plant concentration, Bq/kg dry matter) / (soil 0–10 cm concentration, Bq/kg dry matter).
  - For liquids derived from plants (wine, olive oil): Fv (kg dm/L) = (liquid food concentration, Bq/L or mg/L) / (soil 0–10 cm concentration, Bq/kg dm).
  - For animal-derived foods: CR (concentration ratio) = (concentration in food product, fresh weight) / (concentration in the total diet (dry matter)).
- Diet and feeding data:
  - When animals consume multiple feeds, proportions provided by producers used to estimate overall diet concentration.
  - Wild grass intake estimated by subtracting the known mass of other feeds from the required daily dry matter intake (per literature).
  - Handling of nondetects:
    - If a radionuclide/stable element not detectable in all feeds contributing <30% to the diet, detection limits used to estimate feed concentrations.
    - If >30% contribution, detection limits used but results reported as “less than” values; transfer parameters not determined in that case.
- Milk as a liquid food:
  - CR defined analogously as concentration in milk (per L) relative to the diet’s dry matter concentration.
  
## Data quality, uncertainty, and validation
- QA/QC:
  - Use of certified reference materials (IAEA and others) to verify accuracy.
  - ISO/IEC 17025 accreditation for radiometric methods; ISO 11929-based uncertainty calculations.
  - Regular instrument checks with standard mixtures; monitoring oxide/double-charge interferences.
- Uncertainty:
  - Combined uncertainty reported with k = 2 (approximately 95% confidence).
  - Recovery checks and duplicate analyses contribute to uncertainty estimates.

## Funding and disclosures
- Study conducted within the CONFIDENCE project; funded by the European Atomic Energy Community (H2020) and the Spanish government under grant references provided.
- Acknowledgments to regional technical support centers.

## Practical takeaways for data-driven analysis
- The dataset provides comprehensive multi-tier measurements (soil, wild grass, feeds, plant parts, animal products) across Spain, enabling:
  - Calculation of soil-to-plant transfer factors (Fv) for multiple elements and radionuclides.
  - Calculation of diet-based transfer (CR) to animal-derived foods, incorporating detailed diet compositions.
  - Cross-comparison of transfer behavior across food types (cereals, grapes, olives, meat, dairy) and feeding regimes.
  - Assessment of uncertainties and QA/QC provenance to support robust statistical modeling and risk assessment.