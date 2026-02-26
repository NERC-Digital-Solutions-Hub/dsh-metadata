# Dataset on transfer of radionuclides/elements to foodstuffs in Spain

- Overview
  - This dataset is Deriverable D9.14, “Published dataset on transfer in Mediterranean ecosystems,” of the CONFIDENCE project.
  - Purpose: provide measured transfer of radionuclides and stable elements from soil to foodstuffs in Spain to inform environmental health monitoring and policy decisions.

- Sampling design and scope
  - Two sampling schemes:
    - Main production regions: targeted sampling where the main production of a given food occurs, based on public information from the Spanish Ministry of Agriculture.
    - Local level: dehesa in Extremadura (Mediterranean semi-natural grassland with holm oaks).
  - Foodstuff groups sampled: cereals, grapevine (grapes, leaves, branches, wine), olive (olives, leaves, branches, olive oil), lamb, beef, pork, dairy products (sheep, goat, cow).
  - At each site also collected soils (0–10 cm), wild grass, and animal feeds where relevant.
  - Sampling sites span multiple regions (e.g., Extremadura, Castilla-León, Andalucía, Galicia, Asturias) with specific locations described for each product category.
  - GPS coordinates recorded for sampling locations.

- Field sampling and sample types
  - Soil: composite samples formed from at least six 0–10 cm samples per area.
  - Wild grass: collected by hand, dominated species identified.
  - Cereals: entire plants, separated into roots, stem, and grain.
  - Grapevine: mature grapes, leaves, branches; wine obtained from local cellar or laboratory-made from grapes.
  - Olive: mature olives, leaves, branches; olive oil obtained from mills or cooperatives.
  - Animal products: lamb, beef, pork meat/bone/liver/kidney; dairy products (milk, cheese for sheep, goats, cows).
  - Animal feeds: sampled alongside animal materials; diet information provided by producers.

- Sample handling and processing
  - Soils: GPS-recorded locations; samples air- or oven-dried; composite prepared.
  - Plant and dairy products: prepared as described (e.g., cereals separated into components; wine and olive oil used as is or prepared per product).
  - All handling aimed at preparing samples for chemical analysis while preserving integrity of radionuclide and elemental signals.

- Laboratory methods and quality assurance
  - Elements by ICP-MS:
    - Analytes: Cs, Sr, U, Th, Pb, K, Ca, Na, Mg, P.
    - Sample preparation: soil digested with HNO3/HCl/HF; plant and feed samples digested with HNO3/H2O2; olive oil analyzed without prior digestion.
    - Instrumentation: NexIon 350X ICP-MS with kinetic energy discrimination (helium collision gas); external calibration and internal standards; recovery checks around 106%.
    - Detection limits (LOD) provided for each element.
  - Radionuclides by gamma spectrometry:
    - Analytes: 137Cs, 214Pb, 214Bi (in equilibrium with 226Ra), 228Ac (in equilibrium with 232Th), 40K.
    - Preparation: composite soil samples dried and encapsulated; wine dried; olive oil measured fresh.
    - Equipment: HP(Ge) detectors, 25–45% efficiency; calibration with NPL multi-radionuclide cocktail; use of reference materials (IAEA 385, IAEA Soil6).
    - Secular equilibrium waiting period: ~21 days before measurement.
    - Uncertainty handling per ISO11929.
  - Physico-chemical soil parameters:
    - pH (in water), conductivity, texture, organic matter, clay/sand/silt fractions.
  - Data quality and governance:
    - Accreditation: ISO/IEC 17025 for radiochemical analyses.
    - QA/QC: use of certified reference materials; daily instrument verification with multi-element cocktail; monitoring of oxide and double-charge formation.
    - Uncertainty: combined uncertainty (k = 2) accounting for duplicates, reference materials, and counting uncertainties.

- Calculation of transfer parameters
  - Transfer factors for uptake by plants (Fv):
    - Fv = plant concentration (Bq/kg dry mass or mg/kg dry matter) / soil concentration (0–10 cm, Bq/kg dm or mg/kg dm).
  - Transfer factors to liquids of plant origin (Fv, kg dm/L):
    - Fv = liquid food concentration (Bq/L or mg/L) / soil concentration (0–10 cm, Bq/kg dm or mg/kg dm).
  - Transfer to animal-derived foods (CR - concentration ratio):
    - CR = food product concentration (fresh weight) / total diet concentration (dry matter).
    - If diet includes multiple feeds, diet proportions are used to estimate overall diet concentration.
    - Handling nondetects:
      - If below detection limits and contributing <30% of diet, use detection limit for feed concentration.
      - If >30%, report as less-than value and indicate that transfer parameters may not be determined.
    - For milk (liquid): CR = milk concentration (per L) / total diet concentration (dry matter).
  - Diet and intake modeling:
    - Wild grass intake and other feed proportions estimated using daily dry matter intake rates and provided diet composition.
  - Overall approach follows IAEA TRS-472 (IAEA, 2010) for parameter values and methodology.

- Context, funding, and references
  - Acknowledgements: CONFIDENCE project (EU Euratom H2020; grant 662287) and Spanish Ministerio de Economía, Industria y Competitividad; support from CICYTEX Extremadura; CONCERT project funding.
  - Disclaimers: authors’ views; EC not responsible for use of information.
  - Key references: IAEA TRS 472 (radionuclide transfer parameters), ISO 17025, ISO 11929, and related nutrition and feed literature.

- Relevance to monitoring frameworks
  - Demonstrates end-to-end workflow for environmental health monitoring relevant to policy:
    - Structured sampling design across production regions and illustrative local sites.
    - Comprehensive sample types including soils, plants, animal feeds, and final food products.
    - Transparent, standards-based laboratory analyses with QA/QC and uncertainty assessment.
    - Clear calculation framework for transfer parameters (Fv and CR) aligned with international guidance (IAEA TRS 472).
    - Data provenance, traceability, and comparability across food groups and ecosystems, supporting evidence-based policy decisions on radiological safety and agricultural management.