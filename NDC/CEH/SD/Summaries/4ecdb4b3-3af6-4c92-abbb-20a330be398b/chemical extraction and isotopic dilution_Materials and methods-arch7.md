# Soils

- Four UK soils with contrasting metal contamination histories and metal concentrations were sampled from 0–20 cm depth at Kegworth, Chat Moss, Clough Wood, and a sewage processing farm. Coordinates are provided for each site. Contamination histories include road traffic, 19th-century urban waste from Manchester, Pb/Zn calcareous mine spoil, and digested sewage sludge (Atkinson et al., 2011).
- Samples were air-dried and sieved to <2 mm; soil pH was measured in soil-water suspensions; loss on ignition was used as an estimate of soil organic matter content.

- Soil properties measured
  - pH (soil-water suspensions)
  - Loss on ignition (as a proxy for organic matter)

- Chemical extractions
  - Extractants used: 0.43 M HNO3, 0.43 M CH3COOH, 1 M CaCl2, and 0.05 M Na2H2EDTA (MExt mg/kg)
  - For each soil, three replicate samples were subjected to each extractant
  - Procedure details: suspensions, centrifugation (2200 g, 15 min), filtration to <0.22 µm; CaCl2 extracts acidified to 2% HNO3; samples stored at 4°C prior to analysis
  - Target metals: Ni, Cu, Zn, Cd, Pb
  - Replicates with NA indicate not applicable

- Isotopic dilution assay
  - Enriched stable isotopes used: 62Ni, 65Cu, 70Zn, 108Cd, 204Pb
  - Mixed-isotope spikes created for each soil-extractant combination
  - Protocol: six replicate soil samples (≈1 g) in Ca(NO3)2; three replicates spiked (0.4 mL) and shaken; parallel spiked suspensions for each extractant (CaCl2, CH3COOH, HNO3, Na2H2EDTA)
  - Post-spike handling involved shaking, centrifugation, and filtration prior to analysis

- Multi-element analysis and isotopic abundances by ICP-MS
  - Instrumentation: quadrupole ICP-MS (X-Series II, Thermo Fisher) with collision cell technology and kinetic energy discrimination (CCT-KED)
  - Internal standards: Sc, Ge, Rh, Ir
  - External standards for calibration
  - Isotope ratios measured: 62Ni/60Ni, 65Cu/63Cu, 70Zn/66Zn, 108Cd/111Cd, 204Pb/208Pb, 206Pb/208Pb, 207Pb/208Pb
  - Interference control: CCT-KED; correction for 204Hg interference on 204Pb via 202Hg measurement
  - Detector mode: dilution as needed to operate in pulse-counting mode
  - Mass discrimination (MD) corrections based on calibration standards and NIST SRM-981 for Pb; MD factors applied as drift correction
  - Notes on data integrity: data adjusted for chlorine interferences (e.g., 35Cl-35Cl affecting 70Zn)

- Calculation of E value and E Ext
  - Definitions: isotopically exchangeable metal concentrations in soil (E Value) in 0.01 M Ca(NO3)2 and in each extractant (E Ext)
  - Derivation: using measured isotopic abundances of spike and reference isotopes from three solution types (spike solution, spiked soil-solution, unspiked soil-solution)
  - Variables involved (example names): AM control, AM spike, Cspike, Vspike, MA, IA, and soil mass W
  - Output: E Value and E Ext expressed in mg kg^-1
  - Note: Equation 1 (provided in the text) details the calculation approach, though the printed form is partially garbled

- Data notes and handling
  - NA indicates not applicable for a given replicate
  - Detailed procedural steps cover sampling, extraction, spiking, centrifugation, filtration, storage, and measurement to ensure data quality and comparability

- GIS relevance and potential applications
  - Spatial contextualization: site coordinates enable mapping of metal contamination and extractable pools across landscapes
  - Multi-layer data: combine pH, organic matter proxy (LOI), extractable metal pools (via different extractants), and isotopically exchangeable fractions for risk assessment
  - Data integration: aligns with soil property layers (texture, depth, land use) to support spatial analyses of metal mobility and bioavailability
  - Quality considerations: standardized extraction protocols, QA via replicates, handling of NA values, and instrument corrections support reliable map-based data products

- Limitations and considerations for mapping
  - Four-site scope limits broad spatial generalization; data are depth-specific (0–20 cm)
  - Depth and soil heterogeneity should be considered when aggregating or interpolating for maps
  - Availability of complete datasets (e.g., full table of concentrations by metal and extractant) is necessary to generate detailed thematic maps or exposure models