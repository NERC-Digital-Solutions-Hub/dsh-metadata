# Broad Habitat area estimates of change for Great Britain, summarized by ITE Land Class 1 Version: 1: 10-12-2014

## Overview
- National estimates of Broad Habitat percentage increase or decrease for 1990–2007, across 17 habitat types, calculated using the 2007 ITE Land Classification.
- Data derived from Countryside Survey (CS) and summarized by ITE Land Class (LC2007).

## Data file and structure
- Shapefile: CS90_07_Broad_Habitat_Change_Map.shp
- Key attributes:
  - LC2007 (number): ITE Land Class (references Bunce et al. 1996; 1981; 2007)
  - LC2007_COD (text): Land Class code
  - SURVEY (text): Years of survey (to/from)
  - Column1 (number): Broadleaved, Mixed and Yew Woodland – % change
  - Column2 (number): Coniferous Woodland – % change
  - Column3 (number): Boundary and Linear Features – % change
  - Column4 (number): Arable and Horticulture – % change
  - Column5 (number): Improved Grassland – % change
  - Column6 (number): Neutral Grassland – % change
  - Column7 (number): Calcareous Grassland – % change
  - Column8 (number): Acid Grassland – % change
  - Column9 (number): Bracken – % change
  - Column10 (number): Dwarf Shrub Heath – % change
  - Column11 (number): Fen, Marsh, Swamp – % change
  - Column12 (number): Bog – % change
  - Column13 (number): Standing Open Waters and Canals – % change
  - Column14 (number): Rivers and Streams – % change
  - Column15 (number): Montane – % change
  - Column16 (number): Inland Rock – % change
  - Column17 (number): Urban – % change

## Geographic scope and time
- Region: Great Britain
- Timeframe: Change from 1990 to 2007

## Methodology
- National estimates derived from 1 km survey squares; results mapped to the ITE Land Classification (2007).
- Mapping methodology described in Maskell et al. 2008; related foundational classifications in Bunce et al. and Barr (historical Land Classification documents).
- See also CS Technical Reports and UK Countryside Survey publications for details on data processing and statistical methods (e.g., Scott 2007 TR4).

## How to use in GIS
- Use LC2007 to classify basemaps by Land Class.
- Use the 17 percentage change columns to create thematic layers showing changes in each Broad Habitat type between 1990 and 2007.
- Join or relate to other CS datasets using LC2007 or SURVEY fields for integrated analyses.
- Ideal for map-based data products to communicate habitat change to policy colleagues, clients, or the public.

## Data quality, standards, and considerations
- Data are national-scale summaries; may involve aggregation across varied input resolutions and sources.
- Data may require cleaning and transformation when integrating with other datasets at different resolutions.
- Consistent acknowledgment is required when using CS data (see copyright notice below).

## Acknowledgement and licensing
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text (to be used on copies, publications, and presentations):
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## Relevant references
- Countryside Survey project overview and methodologies (general context and links)
- Carey et al. (2008) Countryside Survey: UK Results from 2007
- Scott (2007) CS Technical Report No.4/07 – Statistical methods for national estimates from 1 km squares
- Bunce et al. (1996, 2007) ITE Land Classification of Great Britain (and related Merlewood classifications)
- Maskell et al. (2008) CS Technical Report No.1/07 – Field Mapping Handbook
- Barr (1991) Countryside Survey Field Handbook and related habitat mapping methodologies
- Jackson (2000) Guidance on interpretation of Biodiversity Classification (related context for broad habitats)