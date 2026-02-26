# Spatial masks for calcareous, coastal, upland and lowland heath habitats [Key Habitats 1992-93] (2017)

## Overview
- Historical habitat masking project conducted in England for Key Habitats 1992-93, building spatial masks to identify calcareous landscapes, coastal areas, upland, and lowland heath habitats.
- Part of Countryside Survey lineage (ITE/CEH) to support stratified sampling and habitat status reporting; masks informed site selection for 1 km grid sampling.
- Data published and validated with external datasets; co-authored by Barr, Bunce, and colleagues; linked to Barr et al. 2017 publication in the NERC Environmental Information Data Centre.

## What the dataset contains
- A vector dataset at 1 km square resolution covering England, with four landscape masks (calcareous, coastal, upland, lowland heath) and an STRATA field describing coastal type.
- Masks and coverage:
  - Calcareous mask: 26,555 1 km squares; differentiates limestone types (Oolitic, Chalk, Massive) and “Other.”
  - Coastal mask: 8,870 total 1 km squares identified inland/coastal; after applying exclusions, 7,341 squares used (urban exclusions and sea areas removed).
  - Lowland heath mask: 8,538 1 km squares.
  - Upland mask: 15,616 1 km squares.
- Dataset structure notes:
  - DOMGEOL, COAST, CALC, LOHEATH, UPHEATH columns indicate presence (1) or type/description.
  - STRATA describes coastal classifications (H = hard coast, S = soft coast, E = estuarine).

## How the masks were defined (methodology)
- General approach: use GIS-based, stratified sampling from a 1 km grid to map areas likely to contain each habitat type; masks designed to capture existing and potential habitats to support future sampling and habitat assessments.
- Calcareous mask
  - Based on 1 km squares containing existing/potential calcareous grassland.
  - Derived by combining simplified geology and drift deposits data; steps include identifying limestone-dominated squares, excluding urban-dominated squares (>75% built-up), and expanding to escarpments.
  - Validation: comparisons with other datasets; overall fit deemed acceptable.
- Coastal mask
  - Defined as land within 500 m of the high water mark plus contiguous saltmarsh, dunes, and coastal bare land.
  - HWM data not available from OS; used Land Cover Map 1990 with Landsat-derived coastline delineation.
  - Involves buffer and coastal land-cover processing; final dataset contains 7,341 suitable coastal squares after exclusions.
- Lowland heath mask
  - Based on soils and altitude indicators of potential heath; uses Soil Survey and Land Research Centre soils data to identify squares with high potential for heathland.
  - Distinguishes upland/lowland using ITE Land Classification 1990 to exclude upland areas; coastal heath areas discussed but not fully captured by soils alone.
  - Validation: acceptable fit overall; notes some mis-matches with other datasets.
- Upland mask
  - Derived from ITE Land Classification 1990, grouping 1 km squares into predominantly upland vs lowland classes.
  - Excludes predominantly urban squares (>75% urban); results in 15,616 squares in England.
- Coastal heathlands
  - Acknowledged as part of the project but reported separately due to limitations in soil-based differentiation.
- Data provenance and validation
  - Field surveys (1992–1993) underpin mask development; datasets later published (Barr et al., 2017).
  - Ongoing validation against other information sources; overall fit judged acceptable for project purposes.

## Data provenance and related publications
- Originators and management: Institute of Terrestrial Ecology / Centre for Ecology & Hydrology; data management by Wood, C.M. (ITE/CfEH).
- Key references and data links:
  - Barr, C.J., Bunce, R.G.H., Cummins, R.P., Hallam, C.J., Hornung, M., Wood, C.M. (2017). Habitat and vegetation data from an ecological survey of terrestrial key habitats in England, 1992-1993. NERC Environmental Information Data Centre. DOI: 10.5285/7aefe6aa-0760-4b6d-9473-fad8b960abd4
  - Related method documents and handbooks (e.g., Barr 1993, Barr 1997, Bunce & Shaw 1973) and official ITE land classification documentation.
- Publication and access
  - Data published via NERC Environmental Information Data Centre (EIDC) with associated DOIs and web links.

## Data availability, access, and governance
- Access through NERC Environmental Information Data Centre; dataset described with field definitions and mask applicability.
- Useful for researchers and practitioners conducting habitat status assessments, landscape planning, and stratified ecological surveys.
- Coastal heathlands are included in the project scope but documented separately due to limitations in soil-based delineation for coastal areas.
- Licensing and reuse considerations not explicitly listed in the summary; typical EIDC datasets require citation (Barr et al. 2017) and adherence to data centre terms.

## Data quality, limitations, and caveats
- Validation indicates some mismatches between masks and other datasets; overall fit acceptable for survey design purposes.
- Some methodological limitations:
  - Coastal heathlands difficult to isolate with soil/land-cover data; included in project but not fully represented in the main masks.
  - Temporal gap: masks reflect 1992–1993 conditions; 2017 publication notes use of these masks for historical and methodological purposes.
  - Potential for misclassification where land cover and geology boundaries are ambiguous, especially near escarpments and in urban-adjacent areas.
- The dataset is designed for use in stratified sampling; users should be mindful of the 1 km grid resolution and potential overlaps between masks.

## Implications for Data Stewards
- Metadata completeness: ensure documentation covers data origins, mask definitions, validation results, and limitations; include DOIs and data centre provenance.
- Data formats and interoperability: repository provides vector 1 km squares with clear attribute schema; maintain compatibility with GIS tools and ensure backward/forward compatibility if masks are updated.
- Data governance and stewardship
  - Maintain records of originators, field handbooks, and processing steps; preserve links to related publications (Barr et al. 2017) and earlier methodological documents.
  - Clearly communicate the scope (England, 1992–93) and the scope caveats (coastal heathlands documented separately).
  - Establish update and versioning practices if new mask refinements are created; track lineage from geology/drift data, to Land Cover Map 1990, to ITE Land Classification 1990, to final 1 km square masks.
- Accessibility and reuse
  - Ensure licensing terms are explicit; provide stable access points to the NERC EIDC records and DOIs.
  - Provide clear guidance on reuse contexts (habitat surveying, ecological modeling, planning) and citation requirements.

## Practical takeaways for the Data Steward archetype
- The dataset is a rigorously constructed, GIS-based set of 1 km habitat masks with explicit criteria for each habitat type, suitable for stratified ecological sampling and habitat status assessments in England.
- It emphasizes provenance, methodological transparency, validation notes, and cross-referencing with established land classification and soil data, which supports governance and audit trails.
- Managers should capture and maintain detailed metadata, ensure access via the NERC EIDC, monitor for updates or corrections, and document any known limitations (notably coastal heathland representation and temporal relevance).