# Spatial masks for calcareous, coastal, upland and lowland heath habitats [Key Habitats 1992-93] (2017)

## Purpose and scope
- National dataset of spatial masks (1 km squares) for key habitats in England, generated from the Key Habitats surveys conducted in 1992–1993 and supplemented by Countryside Survey 1990 data for reporting.
- Masks define existing or potential areas for calcareous grassland, coastal landscapes, upland and lowland heath, used to identify populations from which 1 km sampling sites were drawn.
- Aims to support ecological surveying, habitat assessment, and related analyses by providing standardized habitat extents and a framework for sampling.

## Geographic coverage and mask extents
- England-wide coverage defined at 1 km grid squares.
- Mask extents and totals:
  - Calcareous mask: 26,555 1 km squares.
  - Coastal mask: final total 7,341 squares (after excluding 787 urban squares >75% built-up and 742 predominantly sea squares).
  - Lowland heath mask: 8,538 1 km squares.
  - Upland mask: 15,616 1 km squares.
- Note: Some masks overlap; coastal heathlands are acknowledged as poorly captured by some approaches and are reported separately.

## Dataset structure and attributes
- Data type: vector dataset comprising 1 km square polygons, each annotated with presence indicators for the four masks.
- Core columns:
  - CALC (type 1 = calcareous mask)
  - COAST (type 1 = coastal mask)
  - LOHEATH (type 1 = lowland heath mask)
  - UPHEATH (type 1 = upland mask)
  - DOMGEOL (describes calcareous mask subtypes: 2 = Oolitic limestone, 7 = Chalk, 8 = Massive limestone, 0 = Other)
  - STRATA (coastal mask category: H = hard coast, S = soft coast, E = estuarine)
- The dataset was prepared to enable GIS-based querying, layering, and integration with other habitat and vegetation datasets (notably Countryside Survey).

## Methodology and mask definitions
- Calcareous mask
  - Built from 1 km squares likely to contain existing/calcareous grassland or potential grassland.
  - GIS approach combining solid geology and drift deposits; steps include identifying limestone-dominated squares, excluding urban-dominated squares (>75%), expanding coverage to escarpments, and validating against other data.
  - Relies on simplified BGS geology and drift data; validated with acceptable fit overall, despite some mismatches with other datasets.
- Coastal mask
  - Defined as land within a 500 m inland belt from the high water mark plus contiguous saltmarsh, dunes, and coastal bare land.
  - HWM data not available; used Land Cover Map 1990 to infer coastline, with Landsat-derived classification for inland/coastal delineation.
  - Inland coastline constrained by a 500 m buffer and grid-based processing; borders with England/Scotland/Wales defined using Bartholomew 1:250,000 maps.
  - Final coastal mask produced 7,341 squares after exclusions.
- Lowland heath mask
  - Based on soils and altitude, using Soil Survey and Land Research Centre soil data to identify squares with potential for heathland (dominant or sub-dominant soils).
  - While soil data indicate potential, differentiation from upland heath is partly subjective; used ITE Land Classification 1990 (land classes 17–24 and 27–32) to distinguish upland from lowland areas.
  - Coastal heathlands were not reliably separable by soil types and are reported separately.
- Upland mask
  - Derived from ITE Land Classification 1990, grouping 1 km squares into predominantly upland vs. lowland classes (excluding urban-dominated squares).
  - Final upland map comprises 15,616 squares (England).

## Data quality, validation, and caveats
- Mask validation: generally acceptable fit when compared with other information, though there are mis-matches between masks and other datasets.
- Coastal heathlands: acknowledged as poorly captured by the soil-based approach; identified as a limitation with separate reporting.
- Data quality is influenced by the spatial resolution (1 km squares) and the availability of ancillary data (geology, soil, aerial imagery) at the time of development.

## Provenance, references, and related materials
- Origin: Institute of Terrestrial Ecology / Centre for Ecology & Hydrology; Key Habitat surveys (1992–93) with supplementary reporting from Countryside Survey 1990.
- Key publications and datasets:
  - Barr, C.J.; Bunce, R.G.H.; Cummins, R.P.; Hallam, C.J.; Hornung, M.; Wood, C.M. (2017). Habitat and vegetation data from an ecological survey of terrestrial key habitats in England, 1992-1993. NERC Environmental Information Data Centre. DOI: 10.5285/7aefe6aa-0760-4b6d-9473-fad8b960abd4
  - Related methodological references: Bunce R.G.H & Shaw M.W. (1973) on standardized ecological survey procedures; ITE Land Classification of Great Britain 1990 (Bunce et al., 1990); Land Cover Map 1990 (Fuller et al., 1993); ITE 1990 land classification products.
- Purpose of linkage: The masks defined used to delineate populations and to select sampling locations for habitat surveys, and can be integrated with habitat and vegetation datasets for England.

## Implications for data strategy and use
- Provides a standardized, GIS-ready basis for habitat-based sampling and analysis across England, aligning with historical survey data.
- Supports planning and prioritization by clarifying where calcareous, coastal, upland, and lowland heath habitats are most likely to occur.
- Highlights data gaps and limitations (e.g., coastal heath detection, reliance on 1 km grid, potential misfits with other datasets), informing data governance, standards, and potential updates or enhancements.
- Facilitates collaboration and cross-referencing with wider data communities (e.g., Countryside Survey) to improve system-wide data coverage and utility.