# CS2000 Field Handbook (updated 27 November 2013)

- Provides standardized field recording procedures to produce GIS-ready data for monitoring land cover, vegetation, and biodiversity.
- Defines core data products (Field Assessment Books FABs, 1:10,000 maps, and extensive metadata) and the coding/parcel/plot structure used for GIS analyses.
- Integrates multi-source data (plants, bryophytes, mosses, lichens) with planned GIS outputs such as map layers, BAP (Broad Habitat) translations, and change mappings.
- Includes detailed field methods, quality controls, data handling, and annexes to support reproducible GIS workflows.

## Data capture, structure, and GIS outputs

- Core tools and outputs
  - FAB (Field Assessment Booklet): primary data recording form with mapped square-level context.
  - Theme maps and BAP maps: map-based outputs translating field codes to habitat categories.
  - Data recording forms capture CS1990/CS2000 codes, descriptive text, species, and change indicators.
  - Annexed documentation supports GIS alignment (coordinates, plans, photographic evidence).
- Coding and data model
  - Primary vs secondary codes; alpha coding to compress long sequences.
  - Broad Habitat (BAP) framework: mappings between CS1990 and BAP categories; some montane categories require de novo translation.
  - Parcel-based data: each feature linked to parcel numbers with associated CS1990 parcel codes, primary codes, and coverages.
  - Plot-based data: multiple plot types (Areal, X/Wally, Y, U, B, A, H, D, S/W, R/V) with standardized measurement procedures.
- GIS-ready outputs
  - Separate theme maps per square (Physiography, Agriculture/Natural Vegetation, Forestry/Trees, Boundaries, Buildings/Communications, Recreation).
  - BAP maps (mappable vs plottable broad habitats) with changes between time periods.
  - Change mappings for old squares linked to new parcel numbers and BAP codes.
  - Annotations and annexes to support GIS alignment and data traceability.

## Section 10 – SAMPLING

- Types of sampling
  - Soil sampling
  - Calluna sampling
  - Freshwater biota sampling (conducted by IFE staff)
- Background and purpose
  - Establish baseline soil quality for indices of soil biological activity and diversity; national, spatially-referenced soil samples in squares from the 1978 survey framework.
  - Five replicate soil samples per square for chemistry (pH, loss on ignition, heavy metals), soil fauna diversity, and microbiological status; processed at ITE Merlewood.
- Sampling units and procedures
  - Each square includes five centre-plot locations (X-plots) for soil cores.
  - Three cores per X-plot: one long black pipe (soil chemistry), two short white pipes (soil fauna/microbiological status).
  - Detailed steps for placing pipes, extracting soil, sealing samples, packaging, and despatching to Merlewood.
  - Quick processing considerations for short-lived samples; one set posted by First Class mail, the other collected by regional coordinators.
- Calluna sampling
  - Collect foliar nitrogen to assess nitrogen deposition impact on Calluna vulgaris.
  - Within each square, randomly sampled current year growth (CYG) shoots; 30–50 g fresh weight; sealed and despatched to ITE Merlewood.
  - Guidance on drying and packaging to preserve sample integrity.
- Freshwater sampling
  - Coordinated with specially trained IFE staff; sampling occurs concurrently with CS2000 fieldwork.
- Despatch and logistics
  - Detailed instructions for posting, packaging, receipts, and transport of Calluna and soil samples to the ITE Merlewood facility.

## Section 11 – PHOTOGRAPHY

- Photographing protocol
  - One camera per team; film stock managed via Field Training Course guidance.
  - Photograph every vegetation plot to document appearance and context relative to landmarks.
  - Reference features should be obvious, permanent, and uniquely identifiable.
  - Each photo must display square and plot numbers on a visible board placed at the plot edge, ideally near the marker plate.
  - Composition guidelines emphasize plot-focused framing with minimal sky and clear reference features.

## Section 12 – PROCEDURES AFTER SURVEY

- Data quality and integrity
  - Day-end checks to ensure no features are omitted.
  - Re-digitization or map/data transcription only in exceptional cases; avoid if possible.
- Data/Specimen handling
  - FABs and samples should be returned to ITE stations promptly; minimize delays in transport.

## Annex 1 – Collecting GPS data

- GPS readiness and checks
  - Ensure satellite lock, PDOP below ~6 for reliable 3D fixes; monitor battery power and external power options.
- Data recording and file naming
  - Each plot/feature gets its own data file; file names embed square numbers and plot IDs (e.g., 501X4.PSE).
  - For new features (e.g., fences/hedges), include a feature reference in the file name (e.g., 501F1.MOB).
- Logging workflow
  - Steps to record stationary plot positions vs moving boundaries; set logging rate and confirm logging status.
- Post-processing and equipment care
  - Battery charging, almanac updates, PDOP interpretation, handling obstructions, and use of the Magellan keypad for data entry.
- Attribute reference and sheet
  - Quick-access mapping between numeric attribute codes and plot IDs to accelerate field data entry.

## Practical Takeaways for GIS Specialists

- Prepare for a rich, code-driven data model
  - Master CS1990 and CS2000 code sets; understand primary vs secondary codes, alpha coding, and linking FAB entries to map features.
- Expect multi-layer, parcel-based GIS outputs
  - Translate FABs into parcel geometries with attributes for codes, cover percentages, species, and change indicators; maintain lineage from old to new parcels.
- Plan for change-detection workflows
  - CS2000 emphasizes change detection in old squares and de novo mapping in new squares; ensure robust linking between old and new parcel identifiers for GIS analyses.
- Leverage outputs for biodiversity policy and planning
  - Translate field codes into Broad Habitat (BAP) categories and other policy-relevant geodatabases; ensure traceability between field data and GIS-derived habitat classifications.
- Ensure data quality and reproducibility
  - Adhere to standardized field methods, meticulous plotting/recording, and thorough documentation to support reliable GIS analyses and longitudinal studies.