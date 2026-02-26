# Mapping Quality Assurance Exercise

- Document describes the 2007 Countryside Survey mapping QA exercise, focusing on evaluating the quality and consistency of digital habitat mapping between surveyors and QA teams, and on informing improvements to monitoring frameworks.

## Overview

- Purpose: assess how well mapping data (habitats, features) produced in the field aligns with QA assessments, and identify data quality, metadata, governance and methodological improvements for environmental health monitoring.
- Setting: digital field mapping introduced in 2007 using Surveyor software; data uploaded to a wiki for early QA feedback; extensive QA checks across mapped data.

## Methodology

- Extent and sampling
  - QA covered 23 one-kilometre squares across GB, selected to represent land classes and capture diverse conditions.
  - Effort aimed for comprehensive QA while accommodating landowner access refusals; common surveyed areas between QA and CS data were used for comparisons.
- Data collection and QA processes
  - Field mapping with mandatory fields and prompts to reduce handwriting issues; visit status layers to track feature visitation.
  - QA teams conducted parallel mapping in many squares, using standard CS tablets; data consolidated into a geodatabase.
  - Quality checks included cross-comparisons between CS (surveyors) and QA datasets, with areas, lines, and points analyzed at multiple scales.
- Analysis approaches
  - 4.1 Direct comparison of aggregate areas/lengths/points per square.
  - 4.2 Raster data comparisons: convert polygons to 10x10 m raster cells, compare dominant Broad Habitat per cell, and assess spatial concordance.
  - 4.3 100-point grid: overlay 10x10 point grid to compare presence of Broad Habitats; compute concordance and discrepancies.
  - 4.4 Attribute analysis: compare species attributes within matched polygons using reference IDs.
- Data management and governance
  - Use of geodatabase, standardized metadata practices, and transparent sharing of underlying data where feasible.
  - Documentation of data provenance, change tracking, and QA workflows; analysis of surveyor efficiency and data completeness.

## Key Findings

- Broad Habitat (BH) extents and attribute agreement
  - 81% of squares had BH presence recorded by both CS and QA; mean differences in BH proportions were typically under 1–3.5% across many BHs.
  - Some BHs showed larger variance and potential misallocation between CS and QA (e.g., Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, etc.).
  - Notable issues: Blanket Bog disagreements in upland areas and concerns about revised 2007 field handbook definitions; machair-related anomalies on Scottish dunes.
- Raster data agreement (per square)
  - Overall variation across squares; example percentages ranged from high (e.g., 364: ~98%) to moderate/low (e.g., 261: ~49%, 773: ~23%).
  - Average concordance across squares generally strong but with several outliers; major patterns include strong agreement in many squares but identified problematic cases requiring definition clarification and training.
- 100-point concordance (BH and PH)
  - Generally good concordance across squares, with many showing 70–90% agreement.
  - Some squares showed substantial mis-match (e.g., 773: 19–41% concordance; 261: ~41%).
  - The matrix (Table 6.3b) highlighted recurring issues like overlaps between similar habitats (Neutral vs Improved Grassland; Broadleaf vs Coniferous Woodland) and upland mosaic mapping challenges.
- Change recording
  - Change coding included Real Change, Error Change, No Change; complex process that allowed correction of previous maps.
  - Most broad habitats showed substantial agreement on change coding between CS and QA, though some habitat-specific discrepancies remained, reflecting classification challenges.
  - Linear and point features generally showed higher change-coding agreement than some BH classifications.
- Species attributes and polygons
  - Species were recorded for 2–3 dominant species per polygon; 45% of QA polygons had at least one listed species matching the matched CS polygon.
  - Of polygons with matching species, 77% also matched BH, indicating that species data often aligned with habitat coding but with notable variation.
  -Listed species concordance among commonly recorded taxa varied; Lolium perenne and other focal species showed mixed agreement, with QA often listing more species than CS.
- Linear, point, and terrain features
  - Linear features: high consistency in land-use theme classifications between QA and CS; relatively few cases where QA recorded a feature not observed by CS.
  - Point features: high consistency in habitat coding across matched points; some confusion between woodland/forest codes persisted.
  - Overall performance: digital data capture and parallel QA improved consistency, but habitat definitions and mosaics remained challenging.

## Implications for Monitoring Frameworks

- Data quality and transparency
  - Digital capture with in-field validation markedly improves QA capabilities, metadata completeness, and data governance.
  - Transparent change-tracking and explicit metadata for habitat codes are essential for trustworthy monitoring frameworks.
- Habitat classification and definitions
  - Ambiguities between similar broad habitats (e.g., Neutral vs Improved Grassland; Broadleaf vs Coniferous Woodland) and upland mosaics underscore the need for clear, standardized definitions and ongoing training.
  - Updates to habitat keys (e.g., Blanket Bog) should be integrated consistently across surveys, with explicit guidance on overlapping or transitional habitats.
- Handling mosaics and spatial variability
  - Small-scale mosaics present challenges for exact cross-classifications; consider multi-scale approaches and explicit handling of mosaics in QA designs.
- Data governance and access
  - Barriers to public sharing of underlying datasets can impede transparency; balance openness with data protection and privacy considerations.
  - Harmonization across datasets (historic and current) is critical to enable robust trend analysis and policy evaluation.
- Methodological triangulation
  - Employ multiple QA approaches (area-level, raster, 100-point) to capture different facets of accuracy and to triangulate findings.
  - Include species-level validation to understand how habitat coding interacts with biological composition.

## Challenges and Barriers Highlighted

- Data gaps and access barriers
  - Lack of data or data of insufficient quality; variable metadata quality; some data not readily accessible.
- Organizational silos
  - Silos within and between organizations hinder data sharing and coordination.
- Metadata and format issues
  - Inadequate metadata and data formats that require transformation impede quick verification and reuse.
- Public sharing constraints
  - Requirements to publicly share datasets can deter use of valuable data sources.
- Keeping data current
  - Maintaining up-to-date datasets was cited as a barrier to data sharing and longevity of datasets.

## Recommendations for Monitoring Framework Authors

- Embrace digital field data capture with rigorous QA integration
  - Use field-ready data collection tools with mandatory fields and prompts; implement real-time or near-real-time QA checks (e.g., wiki-based feedback, upload-time validation).
- Standardize and maintain clear habitat definitions
  - Develop and maintain a transparent key with explicit criteria, especially for contentious or transitional habitats; document changes and ensure backward compatibility where possible.
- Implement multi-scale QA approaches
  - Combine area-level comparisons, raster-based checks, and 100-point concordance to comprehensively assess accuracy.
- Track changes with robust metadata
  - Maintain explicit change codes (Real, Error, No Change) with clear guidance and training; enable retroactive corrections where warranted.
- Address mosaics and upland variability
  - Develop guidelines for handling mosaics; consider spatially aware methods that reflect habitat gradients rather than forcing hard boundaries.
- Enhance data governance and access
  - Reduce data silos; establish shared data standards, metadata schemas, and governance processes; balance openness with appropriate safeguards.
- Invest in training and capacity building
  - Provide ongoing training for surveyors and QA staff to reduce misclassification (e.g., Blanket Bog vs Dwarf Shrub Heath) and to improve consistency across squares and teams.
- Integrate ecological details with monitoring indicators
  - Align habitat classifications with policy-relevant indicators; ensure that species data complements habitat codes for richer environmental health assessments.