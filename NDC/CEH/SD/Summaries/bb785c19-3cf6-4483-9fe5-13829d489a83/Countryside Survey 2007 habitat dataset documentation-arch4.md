# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- National estimates of Broad Habitat stock for 2007, calculated using the 2007 ITE Land Classification.
- Data cover Habitats 1–17 with total area in 000s ha per Land Class; includes 95% confidence intervals.
- Freshwater habitats were modeled separately from terrestrial/freshwater habitats.
- Data are published by the Countryside Survey (CEH) and are copyright/restriction governed; all uses require acknowledgement.

## Data Products
- CS007_Broad_Habitat_Stock.csv
  - Contents: Year, Land Class, Broad Habitat code, Broad Habitat name, Land Class Area (000s ha), Mean Estimate (000s ha), Lower/Upper 95% CI (000s ha).
  - Notes: Mean estimates may be negative due to the statistical model; treat negatives as zero.
- CS2007_Stock.tif
  - A 1 km pixel raster; each pixel band represents a mean percentage estimate of a Broad Habitat within that land class stratum.
  - Band-to-habitat mapping described for Broad Habitat 1–17 across bands (e.g., coniferous woodland, arable, grasslands, wetland types, water bodies, urban, etc.).

## Data Schema and Content
- CSV fields (per row): YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE.
- Raster details: 1 km pixel size; British National Grid (OSGB36); projection is Transverse Mercator Great Britain; 1000 m pixel size.

## Spatial and Technical Details
- Spatial reference: British National Grid (OSGB1936).
- Extent and units: Area values in 000s hectares; pixel-level data at 1 km resolution.
- Freshwater habitats use a different statistical model than other habitats.

## Data Use, Quality, and Limitations
- Data support national-scale habitat stock assessment and land-class-specific breakdowns.
- Gaps: data reflects 2007 survey wave; may not capture recent changes without updated surveys.
- Quality notes: CI intervals provided; negative mean estimates should be treated as zero.
- Metadata and documentation are essential for correct interpretation and alignment with ITE Land Classification.

## Access, Attribution, and References
- Acknowledgement required: Countryside Survey data owned by NERC - CEH; data are © CEH.
- Publications and references provide methodological context (CS UK Results 2007, Statistical Reports, Land Classification descriptions, and related JB/JNCC guides).

## References
- Countryside Survey: UK Results from 2007 (Carey et al., 2008)
- Countryside Survey: Technical Reports and Statistical Methods (Scott, 2007)
- ITE Merlewood Land Classification (Bunce et al., 1996; Bunce et al., 1981)
- Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000)
- Countryside Survey Field Mapping Handbook (CS Technical Report No.1/07)

## Practical Considerations for Data Leaders
- Data system perspective: integrate CSV stock estimates with raster-based habitat extents to support cross-cutting analyses (e.g., trend assessment, policy alignment, accessibility, and discoverability).
- Data governance: ensure proper attribution, license compliance, and metadata richness to support reuse across networks and partners.
- User needs and uptake: facilitate co-ownership by policy colleagues and other stakeholders through clear documentation of data lineage, classification schemes, and uncertainty (confidence intervals).
- Data quality and standards: watch for changes in land classification taxonomy over time; harmonize datasets when combining with other habitat datasets; address gaps in granularity or region-specific data.
- Collaboration: leverage wider data communities to validate classifications, improve metadata, and align with standard spatial data practices.