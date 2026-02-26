# DATA STRUCTURE

- The dataset is a shapefile named MANURE-GIS_ManureVolumes_EnW.shp, representing manure volumes by livestock type and land use for England and Wales.
- Each record is encoded as a field with a specific naming convention, linking livestock sector, manure housing type, and destination land use to a unit of measure.

## Fields and coding scheme

- Field prefixes indicate livestock sector and manure/housing type, e.g.:
  - B_ is Beef
  - Bro_ is Broilers
  - D_ is Dairy
  - L_ is Layers
  - P_ is Pigs
  - S_ is Sheep
  - S_FYM, S_Grazing, etc. indicate different manure/housing combinations
- Field suffixes indicate destination land use type, e.g.:
  - Gras = Grass
  - AraW = Arable Winter
  - AraS = Arable Spring
  - (and sometimes AraW or AraS variants)
  - '-' indicates no specific land use destination
- Units specify measurement:
  - kilograms for most Farmyard manure (FYM) and related land uses
  - litres for Slurry (Slu) related fields

## Examples of field mappings

- Beef
  - B_FYM_Gras: Beef, Farmyard manure to Grass; kilograms
  - B_FYM_AraW: Beef, Farmyard manure to Arable Winter; kilograms
  - B_Slu_Gras: Beef, Slurry to Grass; litres
  - B_Grazing: Beef, Direct excreta to unspecified land use (-); kilograms
- Broilers
  - Bro_FYM_Gras: Broilers, Farmyard manure to Grass; kilograms
  - Bro_FYM_AraW: Broilers, Farmyard manure to Arable Winter; kilograms
  - Bro_FYM__1: Broilers, Farmyard manure to Arable Spring (note field naming)
- Dairy
  - D_FYM_Gras: Dairy, Farmyard manure to Grass; kilograms
  - D_FYM_AraW: Dairy, Farmyard manure to Arable Winter; kilograms
  - D_Slu_Gras: Dairy, Slurry to Grass; litres
  - D_Grazing: Dairy, Direct excreta to unspecified land use; kilograms
- Layers
  - L_FYM_Gras: Layers, Farmyard manure to Grass; kilograms
  - L_FYM_AraW: Layers, Farmyard manure to Arable Winter; kilograms
  - L_FYM_AraS: Layers, Farmyard manure to Arable Spring; kilograms
- Pigs
  - P_OutGrazi: Pigs (Outdoor), Direct excreta to unspecified land use; kilograms
  - P_FYM_Gras: Pigs, Farmyard manure to Grass; kilograms
  - P_Slu_Gras: Pigs, Slurry to Grass; litres
  - P_Slu_AraS: Pigs, Slurry to Arable Spring; litres
  - P_Slu_AraW: Pigs, Slurry to Arable Winter; litres
- Sheep
  - S_FYM_Gras: Sheep, Farmyard manure to Grass; kilograms
  - S_FYM_AraW: Sheep, Farmyard manure to Arable Winter; kilograms
  - S_FYM_AraS: Sheep, Farmyard manure to Arable Spring; kilograms
  - S_Grazing: Sheep (Grazing), Direct excreta to managed grass (note on grazing type)

## Special notes and caveats

- S_Grazing field: For Sheep, only the portion of excreta deposited at grazing on managed grass is included; excreta on rough grazing is not included.
- Some fields have Destination Land Use Type as '-' (not specified), indicating no defined land use destination.
- The data cover multiple livestock sectors (Beef, Dairy, Layers, Pigs, Sheep, Broilers) and multiple manure/housing types (Farmyard manure, Slurry, Direct excreta).

## Data format and usability

- The structure is field-based within a single shapefile, suitable for GIS analyses and can be converted to tabular formats for statistical analysis.
- Units are explicitly defined (kilograms or litres), enabling cross-field comparisons and model inputs.
- The data provide a comprehensive mapping of manure volumes by stock type, manure type, and land use destination across England and Wales, facilitating nutrient management, environmental impact assessment, and correlations with land-use outcomes.

## Analyst considerations for use

- Useful for identifying correlations between livestock composition, waste management practices, and land-use allocations.
- Can be integrated into predictive models of nutrient loads or emissions by land-use category and livestock sector.
- Requires attention to field-specific nuances (e.g., certain land uses being unspecified or the grazing caveat for sheep) and potential non-normalized representations across fields.
- Data are best analyzed in conjunction with GIS workflows and may require data normalization to compare across livestock sectors with different manure types.