# Habitat and vegetation data from an ecological survey of terrestrial key habitats in England, 1992-1993

## Purpose and scope
- Provides habitat and vegetation data from a Key Habitat Survey of England (1992-1993), supplementing Countryside Survey data.
- Aims to survey habitats perceived as under threat or of concern: Lowland heath, Chalk and limestone grasslands (calcareous), Coasts, Uplands.
- England-wide regional coverage with integration of Countryside Survey 1990 data for river valleys and waterside landscapes.

## Geographic coverage and time period
- Geographic coverage: England
- Time period: 1992-1993
- Reporting supplemented by Countryside Survey 1990 for lowland river valleys/watersides

## Data categories and content
- Vegetation data: vascular plants, bryophytes, lichens
- Boundary data: descriptions of nearest boundary at 1 km grid points
- Land cover data: mapped at grid points across each 1 km survey square (Countryside Survey 1990 codes)
- Plot types and sampling within squares:
  - Main (X) plots: 4 m² or 200 m² (nested), located within squares
  - Targeted (Y) plots: 4 m² in semi-natural vegetation types/habitats not covered by X plots
  - Streamside (S) & Waterside (W) plots: 10 x 1 m, adjacent to water in upland landscapes
  - Roadside (R) & Verge (V) plots: 10 x 1 m in calcareous landscapes
- Landscape/habitat categories: Calcareous (Chalk/limestone), Coastal, Lowland Heath, Upland Heath
- Data tables (CSV datasets):
  - Key_Habitat_Survey_Squares.csv: survey square metadata (site code, county, end date, habitat type)
  - Key_Habitat_Plot_Headers.csv: vegetation plot header info and locations
  - Key_Habitat_Plot_Species.csv: species recorded within each vegetation plot
  - Key_Habitat_LC_Features.csv: land cover data mapped at grid points
  - Key_Habitat_LC_Species.csv: species details for land cover features
  - Key_Habitat_BD_Features.csv: boundary features mapped at grid points
  - Key_Habitat_BD_Species.csv: species details for boundary features

## Sampling design and methods
- Stratified sampling across entire area; aligned with Bunce & Shaw (1973) methods with modifications
- 1 km squares with either 16 or 25 grid points per square, depending on habitat type
- Land cover unit: minimum mapping unit of 400 m², defined by constancy of codes
- Boundaries recorded within 100 m of grid points; minimum mappable boundary length of 20 m
- Vegetation plots varied by habitat type:
  - X plots: up to 200 m² or nested 4 m² plots
  - Y plots: 4 m² in certain semi-natural habitats
  - S/W plots: 10 x 1 m near water
  - R/V plots: 10 x 1 m near roadsides
- Detailed field methods and codes described in Barr, 1992; Barr, 1993; Bunce & Shaw, 1973 field handbooks
- Data management and QA: data collected by trained surveyors; checked and verified as far as possible

## Appendices and coding schemes (key for GIS integration)
- Appendix I: List of square codes and habitat/landscape types (mapping between square codes and habitat types)
- Appendix II: Land Cover Codes (extensive code descriptions for land cover features)
- Appendix III: Boundary Codes (descriptions for boundary features)
- Appendix IV: LUSE Codes (land use codes for features)
- These codes underpin the CSV datasets and enable consistent GIS classification and querying

## Data quality, provenance, and documentation
- Originators: Institute of Terrestrial Ecology / Centre for Ecology & Hydrology; Countryside Surveys lineage
- Project management and data management teams listed (Barr, Bunce, Cummins, Hallam, etc.)
- All data collected by trained surveyors; extensive documentation and field handbooks referenced
- Some squares have no plot data (noted limitations in lowland heath squares within arable or intensively improved grassland)

## Related resources and references
- Countryside Survey: http://www.countrysidesurvey.org.uk/
- Field handbooks and related Barr publications (1992, 1993)
- Data management and survey origins linked to Countryside Surveys pre-1978 onward

## GIS and data product applications
- Provides map-based data suitable for GIS visualization of habitat types, vegetation composition, and boundary/land-cover features
- Enables spatial analysis across England for key habitats, with compatible 1 km square and plot-level data
- Rich code-based schema allows integration with existing Countryside Survey datasets and standard land-cover classifications
- Useful for policy, client reporting, and public presentations requiring spatially explicit habitat data