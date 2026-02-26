# Key Habitat Survey of England 1992-93 - Habitat Data & Boundary Data

- Purpose and context
  - Part of a series of national environmental surveys (Countryside Surveys) conducted since 1978 by the Institute of Terrestrial Ecology/Centre for Ecology & Hydrology.
  - This Key Habitat survey was commissioned in the early 1990s to investigate habitats perceived as under threat or of concern to the Department for the Environment.
  - Supplements data from Countryside Survey 1990 for reporting river valleys and waterside lowland landscapes.
  - England-wide coverage for 1992-1993; sampling not optimised for rarer or specialised habitats.

- Datasets and data products included
  - Habitat and boundary data for Key Habitat Survey of England 1992-93
  - Datasets (CSV tables) describing survey squares, vegetation plots, land cover, and boundary features
    - Key_Habitat_Survey_Squares.csv: survey square identifiers, county, end date, habitat type
    - Key_Habitat_Plot_Headers.csv: vegetation plot headers and locations
    - Key_Habitat_Plot_Species.csv: plant species recorded in vegetation plots
    - Key_Habitat_LC_Features.csv: land cover data per grid point
    - Key_Habitat_LC_Species.csv: species details for land cover features
    - Key_Habitat_BD_Features.csv: boundary feature data per grid point
    - Key_Habitat_BD_Species.csv: species details for boundary features
  - Appendix I–IV provide codes for squares, habitats, land cover (LC) codes, boundary (BD) codes, and land use (LUSE) codes

- Geographic scope and timeframe
  - Geographic coverage: England
  - Time period: 1992–1993

- Type and structure of data collected
  - Habitat and boundary data
    - Land cover data at grid points within 1 km survey squares
    - Nearest boundary descriptions (within 100 m) for each grid point
    - Boundary types include hedgerows, walls, fences, earth/stone banks
  - Vegetation data
    - Detailed plant species information collected from multiple plot types
    - Plot types:
      - Main (X) plots: 4 m2 or 200 m2 (nested), located within each square
      - Targeted (Y) plots: 4 m2 in semi-natural types not covered by main plots
      - Stream side (S) and waterside (W) plots: 10 x 1 m
      - Roadside (R) and verge (V) plots: 10 x 1 m in calcareous landscapes
    - Data per habitat type and per plot include species, covers, and plot descriptions
  - Land cover data
    - Land cover at grid points described using Countryside Survey 1990 codes
    - Minimum mappable unit: 400 m2
  - Data management and provenance
    - All data collected by trained surveyors
    - Data checked and verified as far as possible
    - Field handbooks and standard procedures referenced (Barr 1992, Barr 1993; Bunce & Shaw 1973)

- Sampling design and reporting structure
  - Stratified sampling across the full study area
  - 1 km survey squares with varying numbers of sample points (16 or 25 per square)
  - Habitat-focused sampling for key habitats: Calcareous (Chalk/Limestone), Coastal, Lowland Heath, Upland Heath
  - Supplementary data for lowland river valleys and waterside landscapes
  - Tables summarize site counts and plots by habitat type (e.g., Table 1 and Table 2 totals by habitat)
  - 35 squares have no plot data (mostly lowland heath in arable/intensively improved grassland)

- Data standards, codes, and documentation
  - Extensive code sets for:
    - Land cover (Appendix II)
    - Boundary features (Appendix III)
    - Habitat types and square codes (Appendix I)
    - Land Use codes (Appendix IV)
  - Relationships among tables are established via series/square identifiers (e.g., SERIES_NUM) and plot identifiers
  - Documentation includes field assessment handbooks and referenced publications

- Data quality, limitations, and caveats
  - Sampling framework not optimised for rarer or highly specific habitats
  - Some squares missing plot data (35) due to location in arable or intensively improved land
  - Potential ambiguities in codes and cross-referencing between land cover, boundary, and habitat descriptors due to legacy coding
  - Data originate from early 1990s methods; may require careful historical context when integrating with modern datasets

- How this data can support data strategy and decision-making (for Data Leaders)
  - Provides historical baselines for England’s habitat distribution and boundary features across major habitat types
  - Facilitates cross-dataset integration with Countryside Survey data (1990 and other years) for trend analysis and system-wide data governance
  - Rich metadata and multiple linked tables enable end-to-end data provenance, discoverability, and reusability
  - Useful for planning data collection efforts, especially around ensuring data standards, metadata completeness, and cross-community data sharing
  - Highlights importance of standardized field methods, documented data management, and clear coding schemes to enable collaboration across partners and disciplines

- Related documents and provenance
  - Countryside Survey website and field handbooks
  - Key habitat survey reports and management/authorship credits (Barr, Bunce, Cummins, Hallam, etc.)
  - Data management roles and contributors (Institute of Terrestrial Ecology, Centre for Ecology & Hydrology)

- Practical notes for use and integration
  - Expect complex joins across multiple CSV tables to assemble complete habitat, vegetation, and boundary datasets
  - Use Appendix I–IV codes to interpret habitat types, land cover, boundaries, and land use
  - Consider cross-referencing with Countryside Survey 1990 data for enhanced temporal studies
  - Be mindful of data gaps and square-specific limitations when conducting analyses at fine spatial scales