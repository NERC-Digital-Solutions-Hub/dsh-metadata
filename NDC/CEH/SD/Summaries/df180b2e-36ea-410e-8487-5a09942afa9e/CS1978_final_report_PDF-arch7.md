# Countryside Survey: Measuring Habitat Change over 30 years 1978 Data Rescue - Final Report (CEH Project no.: NEC03689)

## Overview
- Documentation of the digitisation of the 1978 Countryside Survey land-cover maps into a GIS-ready dataset.
- Extends the Countryside Survey time series back to 1978, enabling long-term analysis of Broad Habitat stock and change across Great Britain.
- Integrates 1978 data with later surveys (1984, 1990, 1998, 2007) to support spatial analyses of habitat change and its ecological drivers.

## What was rescued and why it matters for GIS
- 256 annotated land-cover maps from 1978, previously non-digital, digitised in 2009 and stored in CEH Lancaster GIS.
- Enables spatial analyses of Broad Habitats (aligned with BAP Broad Habitats) alongside plant species and soil data.
- Provides a basis to assess 30-year trajectories of habitat stock and change, improving reliability of long-term ecological models.

## Digitization procedure (GIS workflow)
- Maps scanned to .jpg and .pdf formats; original maps archived securely.
- Digitisation conducted by ADAS in 2009 following the CS1978 Data Rescue protocol.
- Resulting vector data stored in a CEH Lancaster GIS; linked to habitat classifications and species/soil data where available.

## Data checking and validation
- Initial QA: checked for omissions, queries, and digitising errors against original field maps.
- Cross-year consistency checks: each 1km square reviewed across 1978, 1984, 1990, 1998, and 2007 to ensure real change, not artefacts.
- Spatial anonymisation: square locations altered to protect scientific integrity while preserving comparability.
- Visual and data-driven review with involvement from researchers who participated in the 1978 survey to confirm whether changes were real.

## Broad Habitat allocations and resolution of ambiguities
- 1978 field codes translated to Broad Habitats (BH) using maps annotated with species and vegetation data.
- Ambiguities (e.g., Mixed Upland Moor allocations, Calcareous vs Herb-rich Pasture) resolved with guidance from field maps and vegetation data.
- Visual checks conducted for every square to ensure correct allocations and to identify potential misclassifications.
- Some upland codes remain inherently difficult to delineate; mosaic approaches or future refinements may be used.

## Notes on the ITE Land Classifications and mapping approach
- 1978 used the original ITE Land Classification across a 15x15 km square grid with 1228 center squares; 6039 squares analyzed overall for land-class proportions.
- National estimates computed as: mean habitat per square in a Land Class × Land Class area, then summed for GB.
- Over time, land classification evolved (All Squares in 1990, Scotland separation in 1998, Wales separation in 2007), affecting comparability across years.
- Appendix materials include a habitat code lookup and a summary of the ITE land classification evolution.

## Results: 1978 national estimates of Broad Habitats
- The report provides GB-wide stock estimates for several Broad Habitats (in thousands of hectares) and their percentage of GB area, noting:
  - Arable and Horticulture: substantial share (~5,100 thousand ha; ~21.9%)
  - Improved Grassland: substantial share (~5,200 thousand ha; ~22.3%)
  - Broadleaved Mixed and Yew Woodland: ~995 thousand ha
  - Coniferous Woodland: ~1,413 thousand ha
  - Bog, Fen, Marsh, and Swamp; Dwarf Shrub Heath; Urban areas; and others also quantified
- Important caveat: 1978 estimates are not directly comparable to 2007 figures due to small sample size (256 squares) and differences in Land Classification and Broad Habitat definitions. Direct change assessments require careful, model-consistent handling.

## Comparisons with previously published data
- Newly digitized 1978 results differ from Bunce & Heal (1984) and Barr et al. (1993) primarily due to:
  - Different Land Classifications used (1978 vs All Squares 1990 and later refinements).
  - Reassignment of polygons to Broad Habitats and edits to improve consistency with later datasets.
  - The new results align more closely with Barr et al. (1993) than with Bunce & Heal (1984).
- Explanations provided for specific habitats where published values fall outside the new dataset limits.

## Habitat-specific notes and cautions
- Boundary and Linear Features: differences may reflect mapping approaches in 1978 vs later years.
- Arable and Horticulture; Grassland categories (Neutral, Improved, Acid, Calcareous): complexities in retrospective allocations.
- Inland Rock and Urban estimates: historical methods and boundary delineations affect comparability.
- Some categories (e.g., Priority Habitats) can be identified but require careful cross-referencing with other data sources.

## Data products and GIS readiness
- Digitised 1978 maps now enable spatial analyses of habitat stock and change across GB for 1978–2007.
- Materials prepared for integration with 1984, 1990, 1998, and 2007 datasets under the Countryside Survey framework.
- Appendices provide the Habitat Code Lookup and summaries of Land Classification evolution to support cross-walks in GIS.

## Endnotes and references
- Provides a scholarly context for the classification framework, sampling strategy, and historical analyses (links to Barr, Bunce, Clark, Furse, Howard, and others; related reports and scoping studies).
- Technical appendix and data descriptors intended to facilitate reproducibility and cross-year GIS analyses.