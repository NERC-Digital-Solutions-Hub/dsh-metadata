# Mapping biodiversity: a spatial indicator based on species occurrence data

## Overview
- Provides a spatial indicator of ecological status for biodiversity valuation across the UK, based on species occurrence records.
- Data compiled from multiple sources and organized at 10 km grid squares (hectads) over two time periods: 1970–1990 and 2000–2013.
- Involves 11 taxonomic groups (bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, vascular plants); for vascular plants, non-native species are excluded.
- Birds data for breeding populations sourced from the British Trust for Ornithology (BTO).
- Ecological status is derived by comparing observed species richness to potential richness within environmental zones.

## Data availability
- UK ecological status map version 2 is available from the Environmental Information Data Centre (EIDC).
- Supporting publications: Dyer & Oliver (2016) and related datasets; methodological details available in Dyer et al. (2016) and Hill (2012).

## Data collation and scope
- Data were collated from the Biological Records Centre (BRC) for 11 taxonomic groups.
- Time periods: 1970–1990 and 2000–2013; bird data drawn from two atlas periods (1976 and 2001–2011).
- For each hectad and taxonomic group, a species list was created and species richness computed.
- FRESCALO method (Hill 2012) used to adjust for variation in recorder effort across hectads.

## Methodology for ecological status
- Ecological status per hectad is a relative measure of estimated species richness.
- Each hectad is assigned to an environmental zone defined by land cover type, climate, geology, and topography.
- Zones are determined using the 2007 ITE land classification (45 classes).
- A reference species list is created for each environmental zone; hectad richness is compared to the zone’s potential richness.
- The mean ecological status is calculated across all taxonomic groups for 2000–2013, relative to the 1970–1990 maxima.
- For detailed methodology, see Dyer et al. (2016).

## Dataset structure (key columns)
- gridSquare: Ordnance Survey National Grid 10 km reference.
- Easting: x-coordinate of the southwest corner of the grid square (British National Grid, metres).
- Northing: y-coordinate of the southwest corner of the grid square (British National Grid, metres).
- dominantLandClass: Dominant land class for the 10 km square (2007 version) according to ITE classification.
- ecologicalStatus: Mean ecological status for the hectad.

## Land Classification 2007
- Based on the 2007 ITE land classification (Bunce et al. 2007), comprising 45 land classes used to define environmental zones.
- Zones represent areas with similar abiotic conditions and land-cover characteristics to support the ecological-status assessment.
- Summary names and codes for the land classes provide a structured basis for comparing environmental contexts across hectads.

## References and supporting material
- Bunce, R. G. H., et al. (2007). ITE Land Classification of Great Britain 2007. NERC-EIDC.
- Dyer, R.; Oliver, T. (2016). UK ecological status map version 2. NERC EIDC. DOI: 10.5285/58b248a8-6e34-4ffb-ae32-3744566399a2
- Dyer, R. J., et al. (2016). Developing a biodiversity-based indicator for large-scale environmental assessment. Journal of Applied Ecology. DOI: 10.1111/1365-2664.12784
- Hill, M. O. (2012). Local frequency as a key to interpreting species occurrence data when recording effort is not known. Methods in Ecology and Evolution. DOI: 10.1111/j.2041-210X.2011.00146.x