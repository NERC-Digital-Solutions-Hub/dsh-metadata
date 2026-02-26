# Habitat data from an ecological survey of terrestrial key habitats in England, 1992-1993

- Overview and purpose
  - National survey project to investigate habitats perceived as under threat or of concern to the Department for the Environment.
  - Supplemented Countryside Survey data (1990) with targeted survey components for key habitats: Lowland heath, Chalk and limestone grasslands, Coasts, Uplands; additional lowland river valleys/waterside data included.
  - England-focused dataset compiled in the early 1990s to improve understanding and reporting of key habitats.

- Data scope and components
  - Geographic coverage: England.
  - Time period: 1992–1993 (with supplementary 1990 Countryside Survey data for reporting on certain river/waterside areas).
  - Data categories:
    - Vegetation data: vascular plants, bryophytes, lichens.
    - Boundary data: boundary descriptions at grid points.
    - Land cover data: land cover at grid points within 1 km squares.
    - Habitat data: land cover features and boundary features mapped within squares.
    - Plot-level data: vegetation plots of various types (Main/X, Targeted/Y, Streamside/S, Waterside/W, Roadside/R, Verge/V).
  - Data products (datasets):
    - Key_Habitat_Survey_Squares.csv
    - Key_Habitat_Plot_Headers.csv
    - Key_Habitat_Plot_Species.csv
    - Key_Habitat_LC_Features.csv
    - Key_Habitat_LC_Species.csv
    - Key_Habitat_BD_Features.csv
    - Key_Habitat_BD_Species.csv

- Sampling design and field methods
  - Stratified sampling across the study area, using 1 km survey squares.
  - At each square, 16 or 25 points recorded land cover and the nearest boundary, using Countryside Survey 1990 land cover codes.
  - Boundary data collected for the nearest boundary within 100 m of each grid point; minimum mappable length of 20 m.
  - Plot types and sizes (per field handbooks):
    - Main (X) plots: 4 m2 or 200 m2 (nested), located at grid points within squares.
    - Targeted (Y) plots: 4 m2 in semi-natural habitats not covered by main plots.
    - Streamside (S) and Waterside (W) plots: 10 x 1 m plots near watercourses (upland).
    - Roadside (R) and Verge (V) plots: 10 x 1 m plots near roads (calcareous landscapes).
  - Vegetation data collection: detailed species lists and cover per plot (see plot species datasets).
  - 213 squares surveyed; 35 squares have no plot data (mostly lowland heath in arable or intensively improved grassland).
  - Data collection and management led by a team of named researchers; trained surveyors collected data and performed quality checks.

- Data structure and metadata
  - Datasets provide structured metadata for governance and discovery, including:
    - Dataset name, background & description, geographic coverage, time period, data categories.
    - Survey design & methods, related datasets, key documents & publications.
    - Originator details, field surveyors, quality control measures.
  - Detailed field and code documentation included:
    - Appendix I: List of square codes and habitat/landscape types.
    - Appendix II: Land Cover Codes.
    - Appendix III: Boundary Codes.
    - Appendix IV: Land Use (LUSE) Codes.
  - Key data tables describe:
    - Square-level site information (site code, county, end date, habitat type).
    - Plot headers (habitat type, series, plot type, plot size, land-use codes, physical attributes).
    - Plot species (species codes, names, abundance/cover, age, management, height).
    - Land cover features (location, codes, descriptions, canopy, soil, slope, shading, etc.).
    - Boundaries and boundary-associated species (boundary habitat types, boundary features, usage codes).

- Data quality, provenance, and governance
  - All data collected by trained surveyors; data checked and verified to the extent possible.
  - Provenance clearly documented: originators (Barr, Bunce, Cummins, Hallam, etc.), project management, and data management (Centre for Ecology & Hydrology staff).
  - Metadata emphasizes reproducibility and traceability to field methods, field handbooks, and the Countryside Survey framework.
  - Data quality caveats noted: incomplete data for some squares; reliance on Countryside Survey land-cover coding for consistency; some codes allow unique, square-specific codes.

- Usage, accessibility, and related sources
  - Linked to Countryside Survey framework and field handbooks for methodology and code interpretation.
  - Datasets are suitable for establishing habitat extent, change analysis, and habitat-condition assessments, with careful attention to the coding schemes and square-level metadata.
  - Related publications and documents cited (Barr et al. field handbooks and status reports) provide context and methodological grounding.

- Practical considerations for Data Stewards (supporting governance and discoverability)
  - Ensure complete, consistent metadata across all dataset components, including origin, methods, and data categories.
  - Maintain cross-references to Appendices I–IV for coding schemes to enable interoperable data interpretation.
  - Preserve the linkage to Countryside Survey 1990 data to support comparative analyses.
  - Manage access and update workflows to handle potential updates or corrections to plot data and boundary features.
  - Document any squares with missing plot data and rationale to aid data users in parsing completeness.
  - Provide guidance on translating legacy codes to modern equivalents where applicable to facilitate reuse in current data ecosystems.

- Notes for users
  - This dataset provides a comprehensive, code-dense snapshot of England’s terrestrial key habitats from 1992–1993, with rich plot- and point-level data, boundary and land-cover information, and extensive metadata to support governance, discovery, and reuse.