# Countryside Survey: Measuring Habitat Change over 30 years 1978 Data Rescue - Final Report (CEH Project no.: NEC03689)

## Overview
- Describes the digitisation and data rescue of the 1978 Countryside Survey land-cover maps to enable GIS-based analysis and long-term habitat trend assessment alongside 1984, 1990, 1998 and 2007 surveys.
- Establishes a digitised, spatially explicit dataset for Broad Habitats back to 1978, enhancing the GB time-series for stock and change in Broad Habitats.

## Data Rescue and Digitization
- Primary 1978 field maps remained at risk until rescued; digitisation enables daily GIS use and cross-year analyses.
- Maps scanned to .jpg and .pdf; digitisation performed by ADAS in Summer 2009 using a defined protocol; results stored in a CEH Lancaster GIS.
- 1978 line work was digitised independently but later found to be largely consistent with other years’ line work, allowing integration with 1984–2007 datasets.

## Data Structure, Classification, and Mapping
- Field survey used 1km squares (center of 15x15 km grid); 6039 squares classified with ISA-derived land classes; 256 squares surveyed in 1978.
- National habitat stock estimates derived by applying mean habitat per square within each Land Class to the area of that class.
- Land Classification evolved across surveys:
  - 1978: original ITE Land Classification (32 classes via ISA).
  - 1984: refinement; 384 squares; 1978 classification used for estimates.
  - 1990: All Squares classification (expanded to 40 classes); urban/sea corrections added.
  - 1998: 40 classes retained; Scottish reporting separated.
  - 2007: 45 classes; Welsh reporting separated.
- Broad Habitat allocations required translating 1978 codes to BAP Broad Habitats; ambiguous categories resolved using habitat maps, vegetation plots, and expert review.

## Data Checking and Validation
- Initial checks for digitising omissions, queries, and errors against original maps.
- cross-year consistency checks by compiling each survey square per year on separate sheets; visually compared 1978 squares with 1984/1990/1998/2007 data (with anonymised locations).
- Validation ensured 1978 data quality and consistency comparable to other CS datasets, enabling reliable future change detection.

## Broad Habitat Allocations and Challenges
- Most 1978 codes mapped straightforwardly to Broad Habitats (e.g., Conifer Woodland to Coniferous Woodland).
- Key challenges:
  - Upland codes were difficult to delineate; mosaics and patchiness common.
  - Certain codes (e.g., herb-rich pasture) could map to multiple habitats; consulted vegetation plots to resolve.
  - Inland Rock and rock mappings differed between 1978 and later years due to methodology changes.
  - Some allocations required retrospective reclassification (e.g., Neutral/Improved/Calcareous/Acid Grasslands) for consistency.
  - 1978 line work and 1984/1990/1998/2007 line work were aligned to avoid slivers, though 1978 was digitised independently.
- Some areas could be identified as Priority Habitats (Saltmarsh, Blanket Bog, Purple Moor Grass Rush Pasture) where identifiable.

## Note Regarding ITE Land Classifications
- 1978 used the original ITE Land Classification with a 15x15 km grid; ISA produced 32 classes, later expanded to 6,039 squares for proportion-based national estimates.
- Over time, Land Classification evolved (32 → 40 → 45 classes) to enable Scotland/Wales-specific reporting.
- National estimates for 1978 were calculated using the 1990 Land Classification (32 classes) due to sample size limitations; direct comparability with 2007 figures is limited.

## Results: 1978 National Estimates of Broad Habitats
- Provides stock estimates for Great Britain in 1978 across multiple Broad Habitats (in thousands of hectares; percentages of GB area).
- Important caveats:
  - Estimates are not directly comparable to later years due to different classification schemes and sample sizes.
  - When calculating changes with the 2007 framework, inclusion of 1978 slightly affects 2008 results.
  - Some habitats show discrepancies with earlier published figures due to classification changes, coding ambiguities, and methodological shifts (e.g., Urban, Arable, Various Grasslands, Fen/Marsh/Swamp, etc.).
- Examples of 1978 stock figures (illustrative):
  - Arable and Horticulture: ~5105 thousand ha (21.9% of GB)
  - Improved Grassland: ~5188 thousand ha (22.3%)
  - Bog: ~2004 thousand ha (8.6%)
  - Urban: ~1441 thousand ha (6.2%)
  - Dwarf Shrub Heath: ~1677 thousand ha (7.2%)
  - etc. (full table contains detailed means and 95% limits by habitat)

## Comparisons with Previously Published Data
- Differences between newly digitised 1978 results and earlier publications (Bunce & Heal 1984; Barr et al. 1993) are explained by:
  - Non-equivalence of Broad Habitat vs. Reporting Classes across publications.
  - Allocation ambiguities for some 1978 polygons, edited for consistency with later data when possible.
  - Use of different Land Classification frameworks (original 1978 vs. revised All Squares in 1990).
- Some legacy values fall outside the new dataset’s limits due to classification differences; explanations and caveats provided for each habitat category.

## Data Use and GIS Implications
- Enables a rigorous, spatially explicit time series from 1978 onward, allowing analyses of habitat stock and change against later CS surveys.
- Users should be cautious when comparing 1978 with later years due to shifts in land classifications and sampling schemes (e.g., class consolidation, urban corrections, and regional reporting splits).
- Data are suitable for cross-year GIS analyses with careful application of the appropriate Land Classification framework for each year.

## Appendices and References (highlights)
- Appendix II: Habitat Code Lookup Table (1978 descriptions mapped to Broad Habitat allocations).
- Appendix III: Summary of the ITE Land Classification evolution.
- Key references detailing survey methodologies, land classifications, and historical analyses of Countryside Survey data.

## Availability and Access
- Digitised 1978 maps and related field data stored in CEH Lancaster GIS.
- Raw scanned sheets and digitised line work available within CEH infrastructure and referenced team materials (e.g., S: repository paths, workshop notes).