# Spatial masks for calcareous, coastal, upland and lowland heath habitats [Key Habitats 1992-93] (2017)

## Overview
- Provides spatial mask datasets for four Key Habitats in England to identify populations and locations for habitat surveys.
- Masks were used to define the population from which 1 km sampling sites were selected during the 1992–1993 surveys and were published in 2017 (Barr et al., NERC EIDC).

## Data provenance and coverage
- Origin: National surveys since 1978 by the Institute of Terrestrial Ecology/Centre for Ecology & Hydrology; Key Habitat survey conducted in the early 1990s to target habitats under threat or of concern.
- Supplement: For reporting, additional data from Countryside Survey 1990 (river valleys/waterside landscapes) were used to support reporting for lowland areas.
- Geography: England; masks cover 1992–1993 data with validation against other information; coastal heathlands noted as separately reported due to identification challenges.
- Publication and access: Barr et al. (2017) Habitat and vegetation data from ecological survey; data available via the NERC Environmental Information Data Centre (DOI provided in documentation).

## Mask definitions and methodology
- Calcareous mask
  - Based on 1 km squares containing existing or potential calcareous grassland.
  - Built from GIS using solid geology, drift deposits, slope, and exclusion of urban-dominated squares (>75% urban).
  - Coverage: 26,555 squares; used to define population for 1 km sampling.
  - Validation: Compared with other data; overall fit judged acceptable.
- Coastal mask
  - Defined as land within 500 m inland of the high water mark plus contiguous coastal features (saltmarsh, dunes, coastal bare land).
  - HWM derived from Land Cover Map 1990; coastline defined using Landsat imagery and refined with GIS editing.
  - Coverage: 8,870 km2; after exclusions, 7,341 squares included (excluding highly urban or inland-sea dominated areas).
- Lowland Heath mask
  - Derived from soils and altitude data to identify 1 km squares with potential for heathland at landscape scale.
  - Soils typologies from Soil Survey and Land Research Centre used; peat soils included; distinctions among upland/lowland defined to avoid misclassification.
  - Coverage: 8,538 squares in lowland England.
  - Validation: Acceptable fit with other datasets, with noted mismatches.
- Upland mask
  - Uses ITE Land Classification 1990 to classify 1 km squares as predominantly upland vs lowland.
  - Excludes predominantly urban squares; final coverage: 15,616 squares.
- General notes
  - Masks are provided as a vector dataset at 1 km resolution; each square has indicators for applicable masks (Calcareous, Coastal, Lowland Heath, Upland).
  - Mask layers include sub-designations (e.g., calcareous mask types and coastal subtypes).

## Dataset structure and access
- Format: Vector dataset; 1 km squares across England.
- Key fields:
  - DOMGEOL (calcareous mask types: e.g., 2 = Oolitic limestone, 7 = Chalk, 8 = Massive limestone, 0 = Other)
  - COAST (coastal mask presence)
  - CALC (calcareous mask presence)
  - LOHEATH (lowland heath mask presence)
  - UPHEATH (upland mask presence)
  - STRATA (coastal type: H = hard coast, S = soft coast, E = estuarine)
- Purpose: To identify and stratify sampling frames for habitat surveys and monitoring activities.

## Quality assurance and limitations
- Overall validation indicated acceptable fit for monitoring purposes.
- Limitations include some mismatches with other datasets and incomplete coverage for coastal heathlands due to methodological challenges in soils-based separation.
- Data are historical (1992–1993 survey basis; published 2017) and reflect the state of knowledge and mapping practices of that period.

## Use in monitoring frameworks and governance implications
- Demonstrates how to construct habitat-specific population masks integrating geology, soils, land classification, and remote sensing.
- Supports stratified random sampling and robust monitoring design for environmental health measures.
- Highlights governance considerations:
  - Data management and metadata needs for complex, multi-source GIS datasets.
  - Open data access considerations; the dataset is available via EIDC with specific DOIs.
  - Documentation and validation procedures required to ensure datasets meet monitoring standards.
  - Acknowledges gaps (e.g., coastal heath coverage) and the need for ongoing updates to keep masks current.

## Related documents and access
- Barr, C.J.; Bunce, R.G.H.; Cummins, R.P.; Hallam, C.J.; Hornung, M.; Wood, C.M. (2017). Habitat and vegetation data from an ecological survey of terrestrial key habitats in England, 1992-1993. NERC Environmental Information Data Centre. https://doi.org/10.5285/7aefe6aa-0760-4b6d-9473-fad8b960abd4
- Supporting handbooks and reports on methodology (e.g., Barr 1993; Barr 1997; Bunce & Shaw 1973) and ITE land classification (1990) referenced within dataset documentation.
- Data management and access notes: dataset hosted and published through the NERC Environmental Information Data Centre.