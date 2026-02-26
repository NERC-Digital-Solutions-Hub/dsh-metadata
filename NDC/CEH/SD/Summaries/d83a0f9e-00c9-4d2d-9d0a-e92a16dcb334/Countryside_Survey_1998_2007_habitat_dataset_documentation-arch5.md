# Dataset Documentation for 'Countryside Survey mapped estimates of Broad Habitat area change in Great Britain between 1998 and 2007'

## Overview
- National estimates of Broad Habitat percentage change between 1998 and 2007
- Based on the 2007 ITE Land Classification; summarized by Land Class 1
- File: CS98_07_Broad_Habitat_Change_Map.shp (vector GIS)
- Document provides dataset citation, licensing, field descriptions, and references

## Data Content and Structure
- Primary dataset: percentage increase or decrease in Broad Habitat area for each Habitat category (1-17)
- Key fields:
  - LC2007: ITE Land Class (text/number descriptor)
  - LC2007_COD: ITE Land Class code (text)
  - SURVEY: Years of survey (text)
  - Column1 to Column17: Broad Habitat categories with corresponding % change
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
- Estimations cover Great Britain for 1998–2007

## Provenance and Methodology
- Mapping methodology described in Maskell et al. (2008)
- National estimates derived from Countryside Survey framework
- Background references include Barr (1998), Bunce et al. (1996, 2007), and Scott (2007)
- Related technical reports and field mapping handbooks cited for context and reproducibility

## Licensing and Reuse
- Open Government Licence (OGL) terms for data reuse
- Required citation:
  - Barr et al. (2015). Countryside Survey mapped estimates of Broad Habitat area change in Great Britain between 1998 and 2007. NERC Environmental Information Data Centre. DOI provided
- Acknowledgement and copyright notice:
  - Acknowledgement: Countryside Survey data owned by NERC Centre for Ecology & Hydrology; Countryside Survey © CEH
- Full reuse details available via the dataset DOI
- Publication and presentations should include the acknowledgement and copyright notice as specified

## Availability and Access
- Dataset available from the NERC Environmental Information Data Centre
- DOI: https://doi.org/10.5285/d83a0f9e-00c9-4d2d-9d0a-e92a16dcb334
- Supporting documentation linked for broader Countryside Survey materials

## Supporting Documentation and References
- Supporting documentation: "Supporting documentation for Countryside Survey mapped estimates of Broad Habitat area change in Great Britain between 1998 and 2007" (DOI provided)
- Related publications and resources:
  - Barr et al. (1998) Countryside Survey 2000 Field Handbook
  - Countryside Survey Habitat Mapping Methodology 1998/2007
  - Bunce et al. (1981, 1996, 2007) on ITE Land Classification
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Countryside Survey website and technical reports (CS Technical Reports No. 1/07, 4/07)
  - Additional methodological guidance: D.L. Jackson (Guidance on Biodiversity Classification) and BAP Broad Habitats references

## Governance and Stewardship Considerations
- Data Stewards should ensure alignment with data governance: metadata clarity, standard field definitions, and consistent coding (LC2007, LC2007_COD)
- Format considerations: dataset is a shapefile; plan for interoperability with other GIS platforms and potential format conversions
- Data quality and provenance: maintain citations to methodology sources and updater references; track versioning if updates occur
- Availability and updates: while the document describes historical 1998–2007 estimates, establish processes for any future updates or re-mapping and ensure ongoing accessibility through the NERC EH data centre
- Access controls: current licensing is open (OGL); ensure attribution is provided in all downstream uses

## How to Cite and Use
- Citation guidance provided in licensing section
- Use for national-scale habitat-change analyses, reporting, and comparative studies, ensuring metadata fields (LC2007, LC2007_COD, SURVEY, and Column1–Column17) are properly interpreted and mapped to habitat categories
- Reference the primary methodological sources for reproducibility when re-creating estimates or mapping procedures