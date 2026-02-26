# Broad Habitat Area Estimates by Land Class for Great Britain 1990

## Overview
- Countryside Survey 1990 provides national estimates of Broad Habitat stock (Habitats 1–17) for Great Britain, derived from the 2007 ITE Land Classification (Scott 2007; Bunce et al. 2007).
- Outputs include total area by Broad Habitat per Land Class, with lower and upper 95% confidence intervals, expressed in 000s ha.
- Freshwater habitats were modelled separately from other habitats; there was no Montane (BH15) class in 1990.

## Data Files and Columns
- CS1990_Broad_Habitat_Stock.csv
  - Columns: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE
  - MEAN_ESTIMATE may be negative due to the statistical model; treat negative values as zero.
- cs1990_stock.tif
  - 1 km pixel raster; each band corresponds to a Broad Habitat class as described.
  - Specific mapping notes: no Montane class in 1990; Band 15 corresponds to BH16, Band 16 to BH17; cross-walk rules provided for several habitat pairs (e.g., Band 2 maps to Broad Habitat 1 or 2 depending on land class).

## Spatial Information
- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36), Transverse Mercator projection
- Extent: Great Britain

## Data Use, Acknowledgement, and Governance
- All CS data require acknowledgement: Countryside Survey data owned by NERC – Centre for Ecology & Hydrology; © database rights and copyright held by CEH.
- Include appropriate acknowledgment in data uses, publications, and presentations.

## Methodology and Classifications
- Based on the ITE Land Classification (GB), with foundational references including Bunce et al. (1996, 2007), Jackson (2000), and Scott (2007) for statistical linkage from 1 km squares to national estimates.
- Metadata and methodological details are linked to Countryside Survey outputs and technical reports.

## Related Publications and References
- Countryside Survey: UK Results from 2007 (Carey et al. 2008)
- Countryside Survey 1990: main report (Barr et al. 1993)
- ITE Land Classification of Great Britain (Bunce et al. 1996; 2007)
- Guidance on interpretation of Biodiversity Broad Habitat Classification (Jackson 2000)
- Technical and statistical reports (e.g., Scott 2007) detailing estimation procedures

## Relevance for Monitoring Frameworks
- Provides baseline broad habitat areas by Land Class for policy scrutiny and decision-making.
- Includes uncertainty bounds (Lower/Upper Estimates) essential for monitoring confidence.
- Facilitates cross-walk between raster (pixel-level) habitat data and aggregated land-class estimates.
- Useful for trend analysis, scenario assessment, and reporting at national scales.

## Data Gaps and Caveats
- 1990 data reflect the methodologies and classifications of the time; some classes may be absent (e.g., Montane BH15) and model-specific nuances apply.
- Negative MEAN_ESTIMATE values require adjustment to zero; be mindful of rounding and interpretation of confidence intervals.
- Freshwater habitats were modelled with a different approach than terrestrial/flexible classifications; consider this in any cross-habitat comparisons.

## Practical Considerations for Monitoring Frameworks
- Data integration: align 1 km raster bands with current habitat classifications for consistency in ongoing monitoring.
- Metadata: ensure complete metadata for datasets and bands to support data provenance and verification.
- Data sharing: plan for public data sharing while respecting licensing and attribution requirements.
- Data governance: implement standards for data quality, transformation, and versioning; support reproducibility of habitat estimates.

## Endnotes
- Acknowledgement and license text requirements accompany all copies and outputs.
- The dataset and its references provide methodological context for interpreting Broad Habitat stocks and their uncertainty.