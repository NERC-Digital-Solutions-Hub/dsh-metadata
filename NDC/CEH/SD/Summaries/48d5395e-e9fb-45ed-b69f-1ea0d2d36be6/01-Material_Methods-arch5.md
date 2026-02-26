# Dataset on transfer of radionuclides/elements to foodstuffs in Spain

## Overview
- Describes a published dataset (Deliverable D9.14) on the transfer of radionuclides and stable elements from soils to a wide range of Spanish foodstuffs.
- Part of the CONFIDENCE project; funded by the European Commission (Euratom) and Spanish agencies.
- Methods include ICP-MS for stable elements and gamma spectrometry for radionuclides; transfer parameters are computed following IAEA TRS-472.

## Sampling design and scope
- Two sampling schemes:
  - Main production regions (targeting areas of major food production).
  - Local sampling in a dehesa managed by Extremadura regional government.
- Foodstuff groups sampled:
  - Cereals (wheat, triticale, oats, barley)
  - Grapevine (plant, leaves, grapes, wine)
  - Olive (olives, leaves, branches, olive oil)
  - Lamb, Beef, Pork
  - Dairy products (sheep, goat, cow milk; cheeses; yogurts)
- At each site, accompanying soils (0–10 cm), wild grass, and animal feeds were collected.

## Sample sites and collection details
- Locations mapped across Spain (Extremadura, Castilla-León, Galicia, Andalucía, Málaga, Valladolid, etc.).
- Detailed sampling procedures:
  - Soil: composite samples from the same area (minimum 6 per site).
  - Wild grass: hand-cut, dominant species identified.
  - Cereals: whole plants separated into roots, stems, grain; careful soil minimization.
  - Grapevine/olive: specific plant parts collected; wine/oil obtained from local processing.
  - Animal products: meat, bone, liver, kidney collected at slaughter; livestock fed under defined regimes; diet information provided by producers.
  - Dairy: multiple flocks/herds with varied feeding regimes; feedstuffs sampled.
- GPS coordinates recorded using WGS84.

## Laboratory methods and sample preparation
- ICP-MS preparation (2.1–2.3):
  - Samples dried; soil sieved; plant/feeds dried; olive oil analyzed without prior prep.
  - Microwave-assisted acid digestion using HNO3, HCl, HF or H2O2 for different matrices.
  - Elements measured: Cs, Sr, U, Th, Pb, K, Ca, Na, Mg, P.
  - Internal standards and calibration frameworks ensure accuracy; detection limits and calibration metrics provided.
- Gamma spectrometry (2.4–2.5):
  - Composite soil samples dried, encapsulated; wine and oil prepared as needed.
  - Analysis after ~21 days for secular equilibrium.
  - Radionuclides: 137Cs, 214Pb, 214Bi, 228Ac, 40K (with 226Ra and 228Ra in equilibrium considerations).
  - Calibrations with NPL multi-radionuclide cocktail; ISO/IEC 17025 accredited lab; IAEA reference materials used for QA.
- Physico-chemical soil parameters (2.6):
  - pH (in water), conductivity, texture (clay, sands, silt), organic matter content.

## Transfer parameter calculations
- Based on IAEA TRS-472 (IAEA, 2010):
  - Fv (soil-to-plant transfer factor): plant concentration (Bq/kg dw) divided by soil concentration (Bq/kg dw) for the 0–10 cm layer.
  - Fv for liquid foods (wine, olive oil): liquid concentration (Bq/L or mg/L) divided by soil concentration (Bq/kg dw or mg/kg dw).
  - CR (concentration ratio) for animal-derived foods: concentration in food (fresh weight) divided by concentration in total diet (dry matter). Diet composition used to estimate overall diet concentration when multiple feeds are involved.
  - Milk (liquid): CR defined as concentration in milk (per L) divided by concentration in total diet (dry matter).
- Handling non-detects:
  - If a radionuclide/stable element is not detectable in all diet components, detection limits are used to estimate feed concentration if contributions are <30% of the diet; otherwise, values are reported as “less than” and transfer parameters may not be computed.
- Diet and intake:
  - Daily dry matter intake rates from literature used to estimate wild grass intake and to compute overall diet concentrations.

## Quality assurance, uncertainty, and validation
- Instrument calibration and daily verification procedures described (Be, Ce, Fe, In, Li, Mg, Pb, U standards).
- Oxide and double-charge ion interferences monitored; background levels kept minimal.
- Uncertainty: combined uncertainty (k = 2) calculated from duplicates, certified reference materials (soil, cabbage, surface water), and counting statistics.
- QA framework aligned with ISO/IEC 17025; reference materials (IAEA, NPL) used to verify accuracy; results within expected ranges.

## Data governance, provenance, and documentation
- Dataset provides detailed metadata: sampling locations, sample types, plant parts, animal diets, and processing steps.
- Linkages among soils, feedstuffs, and final food products enable transfer factor calculations and diet-based CR.
- Results include detection limits, calibration details, and uncertainties to support reproducibility and secondary use.
- Data intended for dissemination through relevant data portals and catalogue systems, with accompanying methodological documentation.

## Funding, acknowledgements, and references
- Acknowledges CONFIDENCE project (H2020, Euratom) and supporting Spanish agencies; CICYTEX technical support.
- Key references include IAEA TRS-472, ISO/IEC 17025, and ISO 11929 for measurement limits, plus diet-nutrition sources cited for intake calculations.

## Relevance for data stewardship
- Demonstrates end-to-end data lifecycle: sampling design, field collection, laboratory analysis, data processing, and transfer parameter calculation.
- Highlights the importance of rich metadata, standardized measurement procedures, QA/QC, uncertainty assessment, and transparent data provenance for reuse and governance in large, multi-matrix datasets.
- Provides explicit encoding of units, matrices, and calculation methods critical for discoverability, interoperability, and accurate data reuse by other researchers and data users.