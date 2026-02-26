# Mapping Quality Assurance Exercise

- Purpose: Assess quality and consistency of digital field mapping for Countryside Survey 2007, aiming to produce high-quality, queryable data in a geodatabase suitable for national-scale analyses, and to enable rapid data checks and improvements via an interactive wiki.

## Overview of approach and data system

- Transition from paper maps to field mapping with Surveyor software in 2007 to reduce interpretation error, enforce mandatory data fields, and support visit status tracking.
- Data uploaded to an interactive wiki for early QA, with on-site QA teams ensuring protocol compliance.
- QA employed multiple analysis methods to compare surveyor data with QA assessments:
  - Direct aggregation comparisons of square-level extents/lengths/points.
  - Raster-level comparisons by converting polygons to 10x10 m rasters per 1 km square.
  - 100-point grid comparisons to gauge the concordance of Broad Habitats (BH) between surveyors and QA.
  - Attribute-level comparisons for areas, lines, and points, using reference ID layers to align datasets.
- Coverage: QA on mapped data across 23 1km squares, with efforts to survey across land classes and locations in GB; some areas refused access but analyses focused on common surveyed areas.

## Key methodological insights

- Data capture and QA integration: Digital collection and wiki-based checks enhanced data quality, introduced visit-status and mandatory fields, and supported post-field verification.
- Analysis breadth: Used multiple scales (square, raster, 100-point grid) and multiple feature types (areas, lines, points) to identify concordance and discrepancy patterns.
- Change recording: Digital change codes (Real change, Error change, No change) enabled refitting past maps with the option to update prior data; required training and clarification during QA.

## Main findings by analysis type

- Direct comparison of aggregate areas (BH proportions per square):
  - In 81% of squares, BH presence agreed between surveyors and QA.
  - Mean differences in BH proportions were typically small (mostly under 1–3.5%), but standard deviations indicated potential issues for a few habitats (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, Fen/Marsh/Swamp).
  - Notable difficulty areas:
    - Blanket Bog vs Dwarf Shrub Heath in uplands; definitions revised for 2007 introduced some mismatches.
    - Urban vs Improved Grassland recording ambiguities.
    - Machair/Sand Dune anomalies in Scotland highlighted by local habitat uniqueness.
- Raster data comparisons:
  - Overall raster agreement across squares varied; many squares showed high concordance (e.g., 364 and 488; 88–98% range), while others were low (e.g., 261, 773).
  - Average agreement across squares generally strong but with specific hotspots of disagreement tied to habitat definition and mosaic mapping.
- 100-point point-based concordance:
  - Majority of squares showed good concordance, with some notable exceptions (e.g., squares 773 and 261 showing substantial mismatches).
  - Broad and Priority Habitats generally well matched; some issues centered on Neutral vs Improved Grassland, Broadleaf vs Coniferous Woodland, upland habitat mosaics, and urban classifications.
  - Concordance for 100-point BH/PH entries typically high, but variability existed depending on habitat type and landscape complexity.
- Polygon species attributes:
  - 1081 QA polygons and 998 CS polygons matched; about 45% of QA polygons had at least one listed species present in the matched CS polygon.
  - Species concordance varied by BH type; highest matching species concordance observed in woodlands and Improved Grassland; more variance in diverse grassland habitats and mosaics.
  - Overall species concordance around 40% for commonly recorded species; dominant species (e.g., Lolium perenne) showed higher agreement; many plant species displayed substantial surveying differences.
- Point features:
  - Generally high consistency in habitat codes assigned to points between QA and CS datasets; some confusion around woodland/forest coding persisted.
- Linear features (land-use themes):
  - Very high consistency in land-use theme assignments between QA and CS for linears; small number of mismatches were expected (e.g., fence vs wall distinctions).
  - Some potential ambiguity between belts of trees (FO) and woody linear features (WNS/WUS).
- Change recording (areas/lines/points):
  - Overall strong alignment between CS and QA on change coding; some habitat-related differences existed, reflecting the difficulty of interpreting change within certain BHs.
  - In many cases, digital field capture helped surveyors tidy and verify change in real-time, though it added complexity to the survey process.

## Implications for data governance and organizational aims

- Data quality improvements through digital workflow:
  - Mandatory fields and immediate QA checks improved data completeness and consistency.
  - Wiki-based data checks facilitated rapid issue resolution and guidance for survey teams.
- Definition and standardization needs:
  - Habitat classification definitions (notably Blanket Bog, Dwarf Shrub Heath, and woodland types) require ongoing refinement to reduce cross-team inconsistencies.
  - Urban vs grassland classifications require clearer, consistently applied criteria.
- Handling mosaics and upland variability:
  - Mapping mosaics and fine-scale heterogeneity in upland habitats introduces matching challenges; methodological alignment and possible disaggregation strategies are needed.
- Data interoperability and discoverability:
  - A geodatabase approach enabled cross-dataset analyses; alignment with national-scale datasets was a priority.
  - Documentation and metadata clarity are essential to support cross-team and cross-network use.
- Training implications:
  - Training is important for complex habitat definitions and for ensuring consistent application of change codes across habitats (especially Blanket Bog and related upland habitats).

## Challenges and recommendations for Data Leaders

- Continue refining habitat definitions to reduce cross-team discrepancies (focus on Blanket Bog, Dwarf Shrub Heath, Neutral vs Improved Grassland, and woodland classifications).
- Improve handling of mosaics and mosaic-to-single-habitat allocation inconsistencies, particularly in upland areas with complex habitat mixes.
- Clarify Urban vs Grassland delineation guidelines to minimize misclassification of urban-adjacent grasslands.
- Maintain and expand the digital QA workflow (mandatory fields, wiki checks) and invest in targeted training for field staff on complex habitat mapping and change-coding.
- Ensure robust metadata, data lineage, and update procedures to support longitudinal analyses and integration with broader data networks.

## Conclusion

- The 2007 Mapping Quality Assurance Exercise demonstrates substantial improvements in data quality and consistency due to digital mapping and integrated QA workflows, while also highlighting persistent challenges around habitat definitions, mosaics, and certain land-cover ambiguities. The study underscores the importance of standardized definitions, continuous training, and robust data governance to achieve reliable, interoperable national-scale data products that Data Leaders can confidently steward and use for strategic data-driven decisions.