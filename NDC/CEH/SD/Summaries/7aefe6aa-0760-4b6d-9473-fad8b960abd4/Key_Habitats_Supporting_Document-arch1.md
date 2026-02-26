# Key Habitat Survey of England 1992-93 - Habitat Data & Boundary Data

- National survey of England’s terrestrial key habitats conducted in 1992–1993 to supplement the Countryside Survey (1990) and address habitats perceived as under threat or of concern to the Department for the Environment.
- Focus habitats: Lowland heath, Chalk and limestone (calcareous) grasslands, Coasts, Uplands; includes additional data for river valleys and waterside landscapes (lowlands).

## Geographic coverage and time period

- Location: England
- Time period: 1992–1993

## Data categories and contents

- Vegetation Data
  - Vascular plants, bryophytes, lichens
  - Detailed plots with multiple plot types:
    - Main (X) plots: 4 m² or nested 200 m² (landscape-dependent)
    - Targeted (Y) plots: 4 m² in semi-natural habitats not covered by main plots
    - Streamside (S) and waterside (W) plots: 10 m × 1 m
    - Roadside (R) and verge (V) plots: 10 m × 1 m (Limestone/Calcareous landscapes)
- Boundary Data
  - Boundaries described at 1 km survey-square points (nearest boundary within 100 m)
  - Boundary types: hedgerows, walls, fences, earth/stone banks; boundary length coded to reflect boundaries
- Habitat Data (Land Cover)
  - Land cover at grid points within each 1 km square
  - Codes based on Countryside Survey 1990; minimum mappable unit 400 m²
  - Boundary and land cover codes described at grid points; data linked to Appendix codes
- Datasets (CSV tables)
  - Key_Habitat_Survey_Squares.csv: survey squares, county, end date, habitat type
  - Key_Habitat_Plot_Headers.csv: vegetation plot headers, location, plot type, size, and plot metadata
  - Key_Habitat_Plot_Species.csv: plant species recorded within each vegetation plot
  - Key_Habitat_LC_Features.csv: land cover data mapped at each grid point within squares
  - Key_Habitat_LC_Species.csv: species details for land cover features
  - Key_Habitat_BD_Features.csv: boundary feature data within survey squares
  - Key_Habitat_BD_Species.csv: boundary feature species details
- Vegetation data details
  - Main X plots: 4 m² (or nested) at multiple grid points per square
  - Y plots: 4 m² in additional semi-natural habitats
  - S/W plots: 10 m × 1 m near water
  - R/V plots: 10 m × 1 m near roadsides (calcareous landscapes)
  - Tables summarize per-habitat square counts and plot counts (e.g., Calcareous, Coastal, Lowland Heath, Upland Heath)

## Survey design and methods

- Stratified sampling across the entire 1 km² grid area
- Methods follow Bunce & Shaw (1973) with handbook references (Barr 1992; Barr 1993)
- Objectives: capture data on key habitats, with supplementation from Countryside Survey 1990 for river valleys and lowland landscapes
- Survey management and data quality
  - All data collected by trained surveyors
  - Data checked and verified where possible
  - Field handbooks provide detailed plotting and coding procedures

## Habitat types and codes

- Appendix I provides a list of square codes and habitat/landscape types
- Appendix II (Land Cover Codes) maps codes to descriptions (e.g., cliff, fen, marsh, heath, grassland, water bodies, agricultural uses)
- Appendix III (Boundary Codes) and Appendix IV (LUSE Codes) provide detailed code dictionaries for boundary features and land-use categories
- The coding system enables standardised reporting across habitats, land cover, and boundary features

## Data structure and key fields

- Square-level data: series numbers, county, end date, habitat type
- Plot-level data: plot type (X, Y, R, V, S, W), grid location, plot size, land-use codes, plant community descriptors
- Species data: species codes, descriptions, cover, age, height, management, and other attributes
- Land cover features: codes for habitat type, land use, canopy, slope, aspect, shade, grazing, substrate, soil depth, and descriptive site notes
- Boundary data: habitat type, land use, boundary features (bracken, hedges, banks, walls), canopy, height, and related descriptors
- Appendices include thousands of code mappings to ensure consistent interpretation of data across datasets

## Data quality, accessibility, and provenance

- Data collected by trained surveyors and subjected to verification processes
- Structured datasets designed to be discoverable and usable, with metadata and clear field definitions
- Datasets are designed to support statistical analysis, correlation studies, and habitat change assessment when linked with other datasets (e.g., Countryside Survey)

## Practical considerations for analysts

- Use the square and habitat codes to stratify analyses by habitat type and geography
- Leverage plot-level vegetation data to assess species composition, abundance, and habitat quality
- Utilize boundary and land-cover data to study edge effects, ecosystem structure, and habitat configuration
- Be mindful of scale: 1 km² squares and grid-point land-cover data may introduce scale-related limitations for local-level analyses
- Refer to Appendix II–IV to decode land-cover, boundary, and land-use codes for accurate interpretation
- Note data completeness: 213 squares with varying plot data; some squares have no plot data; documentation highlights data gaps and code-level nuances

## Summary of usefulness

- Provides a comprehensive, standardized dataset of England’s key habitats (1992–1993) with vegetation, boundary, and land-cover information
- Enables correlations between habitat types, species composition, and landscape features
- Supports predictive analyses and habitat monitoring when combined with other environmental datasets and historical surveys
- Rich metadata and code dictionaries support reproducibility and cross-study comparability for analysts focused on ecology, conservation, and land-use planning