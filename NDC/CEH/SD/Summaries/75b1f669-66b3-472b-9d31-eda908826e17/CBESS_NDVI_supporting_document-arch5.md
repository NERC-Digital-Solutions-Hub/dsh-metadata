# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Normalised Difference Vegetation Index (NDVI) in saltmarsh and mudflat habitats

- Overview
  - NDVI dataset detailing surface reflectance as NDVI for saltmarsh and mudflat habitats, part of the CBESS project.
  - Primary staff: Timothy Hill.

- Study Area and Sampling Design
  - Locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands).
  - Habitat types: Saltmarsh and Mudflat with contrasting soil types (Essex: clay soils; Morecambe Bay: sandy soils) and differing inundation, creek structure, and vegetation.
  - Sampling framework: 22 randomly allocated 1 x 1 m quadrats per site, spanning four spatial scales (A: 1 quadrat, B: 1–10 m, C: 10–100 m, D: 100 m to site limit). Quadrats common to all CBESS quadrat datasets.

- Data Collection and Processing
  - Timeframe: CBESS field campaign conducted in winter and summer 2013; no planned repeats.
  - Instrumentation: OceanOptics USB2000 spectrometer with 1.5 m fibre; data logged with OOIBase32 (v2.0.1.3).
  - Measurement protocol: NDVI measured at 1.5 m height; steps include spectrometer integration tuning (~75% of max for white reference), spectral averaging for short integrations, dark and white reference measurements, and NDVI calculation; measurements repeated if ambient light conditions changed; measurements under variable light discarded.
  - Data handling: Each quadrat linked to a corresponding OOBase file; notes recorded include cloud and water cover, and any relevant contextual information.
  - Processing: NDVI calculated in Matlab using the Field Spectroscopy Facility Post Processing Toolbox (FSFPostProcessing1.3.8).

- Dataset Content and Metadata
  - Primary variable: NDVI (Normalised Difference Vegetation Index) values.
  - Dataset fields (described columns): Row Number (sorting), Season (Winter W or Summer S), Location (Morecambe M or Essex E), Site (Morecambe: Cartmel Sands CS, Warton Sands WS; Essex: Abbotts Hall AH, Fingringhoe Wick FW, Tillingham Marshes TM), Habitat (Mudflat MF or Saltmarsh SM), Quadrat Number (1–22), Scale (A, B, C, D with corresponding metre ranges), NDVI (numeric value).
  - Data format: CSV; missing data represented as NA.

- Quality Assurance, Provenance, and Documentation
  - Measurement quality controls: Re-measurements under changing light conditions; discarding data collected in variable light.
  - Provenance notes: Random quadrat placement via R; explicit documentation of sampling scales and quadrat counts; alignment of NDVI data with quadrat and site metadata.
  - Processing provenance: NDVI computed in Matlab with FSFPostProcessing toolbox; logging of file references and environmental context (e.g., cloud/water cover).

- Temporal and Spatial Coverage
  - Temporal: Winter and Summer 2013 field campaigns.
  - Spatial: Essex (AH, FW, TM) and Morecambe Bay (CS, WS) sites; two habitat types (saltmarsh and mudflat) across contrasting soil types and inundation conditions.