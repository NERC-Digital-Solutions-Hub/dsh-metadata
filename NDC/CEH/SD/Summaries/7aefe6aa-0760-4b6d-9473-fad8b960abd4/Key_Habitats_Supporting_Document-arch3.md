# Habitat data from an ecological survey of terrestrial key habitats in England, 1992-93

- Summary purpose
  - Part of a national effort to monitor environmental health by collecting data on habitats perceived to be under threat or of concern to policymakers.
  - Supplemented Countryside Survey data from 1990 to provide more targeted information on key habitats.

- Geographic and temporal coverage
  - Location: England
  - Time period: 1992–1993
  - Some reporting data for lowland river valleys/waterside landscapes drawn from Countryside Survey 1990

- Habitats and data focus
  - Target habitats: Lowland heath, Chalk and limestone (calcareous) grasslands, Coasts, Uplands
  - Additional habitat context for river valleys and waterside landscapes
  - Data types include vegetation composition, land-cover at grid points, and boundary/landscape features

- Data content and structure (core datasets)
  - Key_Habitat_Survey_Squares.csv
    - List of 1km survey squares; county; end date; habitat type
  - Key_Habitat_Plot_Headers.csv
    - Vegetation plots and location metadata
    - Fields include HAB_TYPE, SERIES_NUM, REP_ID, QUAD_TYPE, PLOT_SIZE, USE codes, SLOPE, ASPECT, SHADE, GRAZING, SUBSTRATE, site descriptions
  - Key_Habitat_Plot_Species.csv
    - Plant species and cover data per plot; includes SPNO, BRC codes, COMMON_NAME, PRES, COVER
  - Key_Habitat_LC_Features.csv
    - Land cover data mapped at grid points within squares; includes HABT, LUSE, CANOPY, DESCs, WEEDPROP, etc.
  - Key_Habitat_LC_Species.csv
    - Species details for land-cover features; includes SPECIES, SPECIES_DESC, COVER, AGE, HEIGHT, MGT
  - Key_Habitat_BD_Features.csv
    - Boundary feature data near grid points; includes BRACKEN, GAPS, STOCK, CANOPY, HEIGHT, HAB_TYPE, etc.
  - Key_Habitat_BD_Species.csv
    - Species data for boundary features; includes SPECIES, SPECIES_DESC, PROPORTION, AGE, etc.

- Sampling design and field methods
  - Stratified, nationwide sampling across England
  - Each 1km square surveyed with either 16 or 25 points
  - Plots/types within squares
    - Main (X) plots: 4m2 or 200m2 (nested), located at multiple grid points per square
    - Targeted (Y) plots: 4m2 in semi-natural habitats not covered by X plots
    - Streamside (S) and Waterside (W) plots: 10x1m, adjacent to watercourses in upland areas
    - Roadside (R) and Verge (V) plots: 10x1m, adjacent to roads in calcareous landscapes
  - Totals (illustrative)
    - 213–213+ 1km squares across landscape types; total X plots around several hundred to ~675; total Y plots around 620; SW plots around 150; RV plots around 201
  - Vegetation data collection
    - Plots include main and targeted sampling; detailed species lists and cover estimates
  - Field design references
    - Bunce & Shaw standardized survey methods (1973) with modifications
    - Field handbooks and reporting linked to Barr et al. (1992, 1993)

- Data quality, management, and governance
  - All data collected by trained surveyors
  - Data checked and verified “as far as possible”; data management and submission coordinated by Centre for Ecology & Hydrology and Institute of Terrestrial Ecology
  - Data intended for public sharing with appropriate provenance and governance
  - Field handbooks and published reports underpin methods and coding

- Metadata and provenance
  - Originators: Institute of Terrestrial Ecology / Centre for Ecology & Hydrology
  - Related publications and handbooks: Barr (1992, 1993); Countryside Survey materials; field management and data handling led by listed researchers
  - Data lineage includes supplementary Countryside Survey 1990 data for context

- Appendices and codes (data interpretation support)
  - Appendix I: List of square codes and habitats/landscape types
  - Appendix II: Land Cover Codes (extensive code table for land-cover at grid points)
  - Appendix III: Boundary Codes (codes for boundaries and related features)
  - Appendix IV: LUSE Codes (land-use and associated descriptors)
  - The dataset uses standardized codes for habitat types, land cover, boundaries, and land-use, with cross-references to field handbooks

- Limitations and considerations for use
  - The sampling framework is not optimized for rarer or highly specialized habitats
  - Some squares have no plot data (notably in certain lowland heath areas)
  - Data complexity: extensive codebooks and nested plot structures require careful interpretation and alignment with field handbooks
  - Public sharing of underlying datasets may impose governance considerations; requires appropriate data-use controls and citations

- Relevance for monitoring frameworks
  - Provides a structured, multi-layered dataset linking habitat type, vegetation composition, land-cover features, and boundary attributes across England
  - Enables indicators on habitat extent, condition, and landscape context when integrated with other surveys (e.g., Countryside Survey)
  - Offers a documented metadata framework, data management practices, and explicit data governance for environmental monitoring programs
  - Includes detailed appendices of codes and data dictionaries essential for data harmonization and reproducible monitoring analyses