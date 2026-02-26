# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment colloidal carbohydrate concentration in saltmarsh and mudflat habitats

## Purpose and scope
- Dataset measures concentration of colloidal carbohydrates in surface sediments, expressed as glucose equivalents in micrograms per gram of sediment (µg g⁻¹).
- Observations are from CBESS field campaign conducted in winter and summer 2013.
- Two habitat types (saltmarsh and mudflat) across multiple sites; five replicates per 1 m quadrat.

## Location and sampling design
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Site locations chosen to represent contrasting habitats and sediment types; Essex saltmarsh with clay soils vs. Morecambe Bay saltmarsh with sandy soils; differing inundation, creek structure, and vegetation.
- Mudflat sites reflect cohesive clays, mud, and silt (Essex) vs. coarse, mobile sediments (Morecambe Bay).
- Twenty-two 1 x 1 m quadrats randomly allocated per mudflat and saltmarsh site.

## Methods and measurements
- Core sampling: collection of contact cores; sample cores frozen with liquid nitrogen, stored below -80°C; weighed for water content.
- Laboratory analysis: freeze-drying, Dubois Phenol-Sulphuric assay for colloidal carbohydrate concentration; sample processing includes sub-sampling (50–500 mg), water addition, vortexing, centrifugation, and color development with phenol-sulfuric reagents.
- Measurement readout: absorbance at 486.5 nm using a spectrophotometer; concentrations calculated from standard regression; reported as µg g⁻¹.
- Data quality: calibration with known glucose standards; notes on detection limits (zero values indicate below detectable levels).

## Variables and data structure
- Primary variable: Colloidal Carbohydrate concentration (µg g⁻¹), with standard deviation (StDev) per measurement.
- Metadata fields: Season (Winter or Summer), Location (Essex or Morecambe), Site (AH, FW, TM, CS, WS, WP), Habitat (Mudflat or Saltmarsh), Quadrat Number (1–22), Scale (A–D representing spatial arrangement), StDev.
- Data file format: Comma separated values (.csv).
- Data quality notes: some missing data indicated as NA due to inaccessibility of a quadrat.

## Temporal coverage and sampling design
- Seasons: Winter (W) and Summer (S) 2013 sampling.
- Spatial scales: four levels (A: 1 quadrat; B: 3 quadrats 1–10 m apart; C: 6 quadrats 10–100 m apart; D: 12 quadrats 100 m to site maximum).

## Data provenance and governance
- Dataset steward: Jack Maunder.
- Core procedures and lab methods are described to support reproducibility and quality assurance.
- Data collection aligned with CBESS field campaign practices; data management includes recording wet/dry weights, measurement readings, and ensuring traceability to original quadrats and sites.

## Relevance for monitoring frameworks
- Provides a concrete, standardized measure of sediment biogeochemistry linked to coastal biodiversity and ecosystem service sustainability.
- Demonstrates a replicable sampling design across contrasting habitats and sediment types, with explicit spatial scales and seasonal coverage.
- Highlights data management considerations (metadata completeness, reproducibility, data formats) pertinent to governance and data sharing in monitoring programs.