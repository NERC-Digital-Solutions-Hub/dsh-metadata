# Mapping biodiversity: a spatial indicator based on species occurrence data

## Overview
- A spatial indicator of ecological status for biodiversity valuation across the UK, built from species occurrence records across 11 taxonomic groups and two time periods.
- Outputs a per-10 km hectad ecologicalStatus score, representing relative richness across environmental zones.

## Data sources and availability
- Data collated from: Biological Records Centre (BRC) for 11 taxonomic groups (bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, vascular plants); bird data from the British Trust for Ornithology (BTO).
- Time periods: 1970–1990 and 2000–2013.
- Vascular plants: non-native species excluded due to high non-native representation in GB.
- Data availability: UK ecological status map version 2 available from the Environmental Information Data Centre (EIDC) with DOI provided.

## Methodology (how ecological status is estimated)
- For each taxon and time period, construct a species list per hectad and compute species richness.
- Adjust for variable recorder effort using FRESCALO (Hill 2012).
- Ecological status is a relative measure of estimated richness, assigned per hectad to an environmental zone defined by land cover, climate, geology, and topography.
- Land classification: Zones defined using the 2007 ITE land classification (45 classes) to represent abiotic conditions; dominant class per hectad informs zone assignment.
- Reference lists: For each environmental zone, compile a potential species list; compare observed richness to the zone’s potential richness.
- Aggregation: Mean ecological status is computed across all taxonomic groups for 2000–2013, relative to the 1970–1990 maximums.
- For details on the methodology, see Dyer et al. (2016).

## Data structure and key columns
- gridSquare: Ordnance Survey National Grid 10 km grid reference (hectad).
- Easting: X coordinate of the southwest corner in British National Grid (metres).
- Northing: Y coordinate of the southwest corner in British National Grid (metres).
- dominantLandClass: Dominant 2007 ITE land class for the 10 km square (Bunce et al. 2007).
- ecologicalStatus: Mean ecological status across taxa for the hectad.

## Land Classification 2007 (environmental zones)
- Based on the 2007 ITE land classification with 45 classes used to assign environmental zones indicative of similar abiotic conditions.
- Examples of class themes include flood plains, coastal plains, upland valleys, sea cliffs, estuarine/coastal types, and various river valley/plains categories across England, Scotland, and Wales.
- The 45 classes underpin the cross-taxa ecological-status comparison by linking observed richness to comparable abiotic contexts.

## Outputs and interpretation
- A harmonized, nationally comparable ecologicalStatus score per hectad for 2000–2013, enabling mapping of biodiversity status across the UK and identification of spatial patterns relative to abiotic environmental zones.

## References and data lineage
- Key sources include Bunce et al. (2007) on ITE Land Classification; Dyer & Oliver (2016) on UK ecological status map version 2 and methodology; Hill (2012) on interpreting presence data with unknown effort.
- Additional supporting documentation and datasets are linked via the EIDC DOI and the referenced publications.