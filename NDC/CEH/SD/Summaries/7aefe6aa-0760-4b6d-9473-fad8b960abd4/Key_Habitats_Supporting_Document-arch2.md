# Habitat and vegetation data from an ecological survey of terrestrial key habitats in England, 1992-1993

- This dataset describes habitat and vegetation data collected as part of a Key Habitat Survey in England during 1992-1993, supplementing earlier Countryside Survey work (from 1978 onward) to focus on habitats perceived as under threat or of concern.
- Target habitats: Lowland heath, Chalk and limestone calcareous grasslands, Coasts, and Uplands; reporting also incorporated additional river valley/waterside data from Countryside Survey 1990.

## Aim and context for environmental monitoring

- Provides standardized environmental data to assess habitat condition and policy performance over time.
- Data are intended for integration with established monitoring datasets, enabling scrutiny of environmental health across time and space.

## Geographic and temporal coverage

- Geographic coverage: England.
- Time period: 1992-1993.
- Coverage includes four key habitat groups (Calcareous landscapes, Coastal landscapes, Lowland Heath, Upland Heath) across a set of 1km squares; total of 213 squares surveyed.

## Data collected and components

- Vegetation data
  - Detailed plant information: vascular plants, bryophytes, lichens.
  - Plots and sampling within each 1km square:
    - Main (X) plots: 4 m2 or nested 200 m2 plots, located within the square.
    - Targeted (Y) plots: 4 m2, placed in semi-natural habitats not covered by main plots.
    - Streamside (S) and Waterside (W) plots: 10 m x 1 m plots, located near watercourses in upland landscapes.
    - Roadside (R) and Verge (V) plots: 10 m x 1 m plots, in calcareous landscapes.
  - Vegetation plots yield species lists and abundance/cover data.
- Boundary data
  - Nearest boundary description to grid points (within 100 m) using Countryside Survey codes.
  - Boundaries include hedgerows, walls, fences, earth/stone banks, or combinations.
  - Data capture includes boundary length and variability where applicable.
- Land cover data
  - Land cover at grid points within each square, described using Countryside Survey 1990 codes.
  - Each mappable unit is defined by code stability; minimum mappable unit around 400 m2.
- Datasets and data structure
  - Data are organized into multiple CSV tables capturing squares, plots, vegetation species, land cover features, and boundary features, plus their associated metadata.

## Survey design and methods

- Sampling design: stratified sampling across the entire area; not optimised specifically for rarer or more specialised habitats.
- Data collection framework and field procedures draw on Bunce & Shaw’s standardized ecological survey methods (1973) with modifications; field handbooks by Barr and colleagues detail procedures.
- Data management and QA: all data collected by trained surveyors and subjected to verification where possible; managed by the Institute/Centre for Ecology & Hydrology team.

## Datasets and file structure

- Key Habitat Survey of England 1992-93 – Habitat Data & Boundary Data
  - Key_Habitat_Survey_Squares.csv: 1km square identifiers, counties, end dates, habitat type.
  - Key_Habitat_Plot_Headers.csv: vegetation plot headers and locations, plot types, sizes, land-use codes, physical descriptions.
  - Key_Habitat_Plot_Species.csv: plant species lists per plot, coverage, and related details.
  - Key_Habitat_LC_Features.csv: land cover features mapped at each grid point within squares.
  - Key_Habitat_LC_Species.csv: species details tied to land cover features.
  - Key_Habitat_BD_Features.csv: boundary features mapped at each boundary nearest to grid points.
  - Key_Habitat_BD_Species.csv: species details for boundary features.
- Appendices and codes
  - Appendix I: List of square codes and habitat/landscape types.
  - Appendix II: Land Cover Codes (codes and descriptions for land-cover categories).
  - Appendix III: Boundary Codes (codes and boundary feature descriptions).
  - Appendix IV: LUSE Codes (land-use and related codes).
- Related documentation and references
  - Countryside Survey website.
  - Key habitat field handbooks and reports (Barr 1992, Barr 1993, Barr 1997; Bunce & Shaw 1973; ITE/CEH project management and data management credits).

## Data quality, management, and provenance

- Data collected by trained surveyors; data checked and verified to the extent possible.
- Source and management teams include Institute of Terrestrial Ecology and Centre for Ecology & Hydrology, with project coordination and data management by named researchers.
- Field handbooks and published reports provide methodological context and coding schemes.

## How this supports environmental monitoring

- Delivers standardized, repeatable habitat and vegetation data suitable for long-term monitoring and trend analysis.
- Enables integration with Countryside Survey data and other environmental datasets to assess habitat change, habitat condition, and policy effectiveness over time.
- The explicit coding schemes (land cover, boundary features, land use) support cross-walks and interoperability across monitoring efforts.