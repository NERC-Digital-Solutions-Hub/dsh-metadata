# Dataset on transfer of radionuclides/elements to foodstuffs in Spain

- Deliverable D9.14: Published dataset on transfer in Mediterranean ecosystems from the CONFIDENCE project
- Objective: quantify transfer of radionuclides and stable elements from soil to foodstuffs in Spain, using representative sampling across main production regions and a dehesa system in Extremadura
- Data uses established transfer definitions and IAEA guidance to enable interpretation and comparison

## Sampling design and sites

- Two sampling schemes:
  - Scheme (i): main production regions, targeting areas of major food production per public agricultural information
  - Scheme (ii): local sampling in a dehesa managed by Extremadura regional government (Mediterranean semi-natural grassland with holm oaks)
- Foodstuff groups sampled:
  - Cereals (wheat, triticale, oats, barley)
  - Grapevine products (plant, grapes, wine)
  - Olive products (olives, olive oil)
  - Animal products: lamb, beef, pork
  - Dairy products: sheep milk/cheese, goat milk/cheese, cow milk/cheese/yogurt/kefir
- Additional materials collected at each site: soil (0–10 cm), wild grass, and animal feeds where relevant
- Geographic reference: sampling locations recorded with GPS (WGS84)

## Sample collection and materials

- Soil: composite samples formed from at least 6 individual 0–10 cm samples per area
- Wild grass: hand-cut, 1 cm above soil to minimize soil contamination; dominant species identified
- Plant and animal products: cereals (roots, stem, grain), grapes (mulpers, leaves, branches), olives (mature olives, leaves, branches), wines and oils prepared as described
- Animal products: lamb, beef, pork and dairy products collected from flocks/herds with defined feeding regimes; animal feeds sampled; slaughterhouse tissues collected for meat and organs as available
- Diet information: for animals fed multiple components, diet composition provided by producers to compute overall diet concentrations

## Sample preparation and analysis

- ICP-MS analysis for stable elements (Cs, Sr, U, Th, Pb, K, Ca, Na, Mg, P)
  - Sample prep: diverse matrices digested by microwave digestion with appropriate acids; internal standards and quality controls used
  - Calibration and detection: external calibration with internal standardization; detection limits provided; combined uncertainty assessed
- Gamma spectrometry for radionuclides
  - Composite soil samples prepared; wine/olive oil samples measured as appropriate
  - Radionuclides analyzed: 137Cs, 214Pb, 214Bi (214Pb/214Bi in equilibrium with 226Ra), 228Ac (in equilibrium with 232Th), 40K
  - Secular equilibrium assumed for related nuclides; quality control via IAEA reference materials; ISO/IEC 17025 accreditation followed
- Physico-chemical soil parameters
  - pH (in water), conductivity, texture (clay, sand fractions), organic matter content (via hydrogen peroxide digestion and sedimentation)

## Calculation of transfer parameters

- Transfer factor for plants (Fv): plant concentration (Bq/kg dry mass or mg/kg dry mass) divided by soil concentration (0–10 cm) (Bq/kg dry mass or mg/kg dry mass)
- Transfer factor for liquid foodstuffs of plant origin (Fv,kg dm/L): liquid food concentration (Bq/L or mg/L) divided by soil concentration (0–10 cm)
- For animal-derived foods: concentration ratio (CR) = food concentration (fresh weight) divided by diet concentration (dry matter)
  - If animal diet includes several feeds, diet proportions provided by producers are used to estimate overall diet concentration
  - Wild grass intake estimated from daily dry matter requirements minus mass diet contributions; if certain feeds are below detection limits and contribute >30% of intake, detection limits used and reported as a ≤ value (leading to possible exclusion from transfer parameter calculation)
- Milk (liquid) CR defined as milk concentration divided by diet dry matter concentration
- Transfer parameters follow IAEA TRS-472 (IAEA, 2010)

## Data quality, uncertainty, and standards

- Quantification limits determined as three times the standard deviation of reagent blanks
- Uncertainty: combined, k = 2, incorporating duplicates, certified reference materials (soil, organic material, surface water), and counting statistics
- Instrument performance verified daily with multi-element standard mix
- Radionuclide measurements validated against IAEA reference materials (IAEA-385, IAEA Soil6) and ISO/IEC 17025-compliant procedures
- Calibration and correction for interferences (kinetic energy discrimination, collision gas) applied in ICP-MS measurements

## Metadata, provenance, and governance

- Dataset produced within the CONFIDENCE project; funded by Euratom H2020 and Spanish agencies
- Contains procedural details necessary for reproducibility: sampling schemes, site descriptions, sample handling, analytical methods, data interpretation rules
- Clear definitions for transfer parameters (Fv and CR) and explicit treatment of undetectable concentrations
- Acknowledgements and references provided to support traceability and context

## Access, impact, and usage

- Provides a structured methodology and results framework for evaluating radionuclide and element transfer in Mediterranean ecosystems
- Enables cross-site comparisons and integration with IAEA guidance (TRS-472) for risk assessment and environmental monitoring
- Beneficial for data leaders aiming to improve data strategy around environmental-to-food transfer datasets, including metadata standards, quality control, and clear transfer metrics