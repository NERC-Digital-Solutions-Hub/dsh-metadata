# Broad Habitat area estimates of change for Great Britain, summarized by ITE Land Class 1 Version: 1: 10-12-2014 Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview
- Dataset provides national estimates of Broad Habitat % change between 1990 and 1998 for Great Britain, summarized by ITE Land Classification (2007) groups.
- Source: Countryside Survey data; methodology and classifications described in associated literature (e.g., Barr, 1998; Barr 1991; Bunce et al. series; Scott, 2007).
- File reference: CS90_98_Broad_Habitat_Change_Map.shp (shapefile) containing per-land-class results.

## Data Content and Structure
- LC2007 (number): ITE Land Class (Bunce et al. 1996; 1981; 2007) used for summarizing results.
- LC2007_COD (text): ITE Land Class code.
- SURVEY (text): Years of survey included (to/from).
- Column1 through Column17 (numbers): % increase or decrease in area of each Broad Habitat, mapped as follows:
  - Column1: Broadleaved, Mixed and Yew Woodland
  - Column2: Coniferous Woodland
  - Column3: Boundary and Linear Features
  - Column4: Arable and Horticulture
  - Column5: Improved Grassland
  - Column6: Neutral Grassland
  - Column7: Calcareous Grassland
  - Column8: Acid Grassland
  - Column9: Bracken
  - Column10: Dwarf Shrub Heath
  - Column11: Fen, Marsh, Swamp
  - Column12: Bog
  - Column13: Standing Open Waters and Canals
  - Column14: Rivers and Streams
  - Column15: Montane
  - Column16: Inland Rock
  - Column17: Urban
- All use of Countryside Survey data must be acknowledged (see citation and copyright section).

## Use and Interpretation for GIS
- Combine LC2007 and the 17 habitat change columns to map how each Broad Habitat changed in area across ITE Land Classes.
- Useful for visualizing spatial patterns of habitat gain/loss at a national scale and across land-class typologies.
- Methodology references provide guidance for reproducibility, including the 1 km survey-square basis for national estimates (Scott, 2007).

## Provenance, Methodology, and References
- Data origin: Countryside Survey (CS) datasets, with national estimates derived for 1990–1998 using the 2007 ITE Land Classification.
- Methodological references include:
  - Scott, W.A. (2007) CS Technical Report No. 4/07 (Statistical Report): How national estimates are generated from 1 km survey squares.
  - Bunce, R.G.H. et al. (1996, 2007) ITE Land Classification of Great Britain (Merlewood/Labelling codes).
  - Barr, C.J. (1991, 1998) Countryside Survey Field Handbook and Habitat Mapping Methodology.
  - Jackson, D.L. (2000) Guidance on Biodiversity Classification interpretations.
- Publications and links include the Countryside Survey website and multiple DOIs/URLs for the Land Classification datasets and technical reports.

## Data Rights and Acknowledgement
- Acknowledgement required: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
- All uses of CS data must include the above acknowledgement in copies, publications, and presentations.

## Considerations for GIS Specialists (Challenges and Best Practices)
- Data are distributed across multiple sources and formats; plan for data sourcing and provenance tracking.
- Some datasets may lack consistent data standards; apply harmonization where merging with other layers.
- Large/complex datasets require data packaging into manageable chunks and appropriate filtering for analysis.
- Cleaning and transforming data will be necessary to ensure consistent interpretation of habitat categories across Land Classes.
- Early prototyping and user feedback are valuable to refine map visuals for diverse audiences (policy makers, clients, public).

## Access and References
- Countryside Survey Website: general overview and methodologies (http://www.countrysidesurvey.org.uk/).
- Key references include:
  - Carey et al., 2008. Countryside Survey: UK Results from 2007.
  - Scott, W.A., 2007. CS Technical Report No. 4/07.
  - Bunce et al., 1996/2007. ITE Land Classification of Great Britain.
  - Barr, C.J., 1991/1998. Countryside Survey Handbooks and Habitat Mapping Methodology.
  - Jackson, D.L., 2000. Guidance on Biodiversity Classification interpretations.