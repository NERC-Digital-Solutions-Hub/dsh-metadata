# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Overview
- Countryside Survey 1998 provides national estimates of Broad Habitat stock (Habitats 1–17) for Great Britain, calculated using the 2007 ITE Land Classification.
- Estimates are given as total area (in 000s hectares) per Broad Habitat and Land Class, including lower and upper 95% confidence limits.
- Freshwater habitats were analyzed with a different statistical model than other habitats.
- Field surveys were conducted in 1998 (with a few sites in 1999); the dataset is commonly referenced as Countryside Survey 2000.

## Data Files and Contents
- CS1998_Broad_Habitat_Stock.csv
  - NATIONAL estimates of Broad Habitat stock by Land Class (Habitat 1–17).
  - Columns include: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE.
  - Notes: MEAN_ESTIMATE may be negative due to the statistical model; treat negative values as 0.
- CS1998_stock.tif
  - A 1 km pixel raster where each pixel band represents a Broad Habitat class.
  - Each band provides the mean percentage estimate of habitat within that 1 km square, derived from 1 km survey squares within each Land Class stratum.
  - Band-to-habitat mappings are provided (e.g., relationships between Broad Habitat codes and raster bands); exact band-to-habitat mappings are specified in the dataset documentation.

## Data Format and Spatial Information
- Spatial resolution: 1 km pixel size (1000 m).
- Coordinate system: British National Grid (OSGB36).
- Projection: Transverse Mercator.
- Extent: Great Britain.
- Data use requires acknowledgement to NERC - Centre for Ecology & Hydrology.

## Estimation Methodology
- National estimates are derived from the Countryside Survey using the ITE Land Classification framework (2007 version).
- Land Class areas are used to aggregate Broad Habitat areas (Habitat 1–17) across Great Britain.
- Freshwater habitats used a separate statistical approach from other habitats.
- Data provide both point estimates (MEAN_ESTIMATE) and uncertainty bounds (LOWER_ESTIMATE, UPPER_ESTIMATE).

## Data Quality, Limitations, and Caveats
- MEAN_ESTIMATE values may be negative due to the statistical model; these should be treated as zero in interpretation.
- Freshwater habitat estimates rely on a different model, which may affect comparability with terrestrial habitats.
- Metadata adequacy can vary; users should verify provenance and methods when integrating with other datasets.
- Some data may require transformation for use in different analysis workflows or systems.

## Usage, Attribution, and Access for Monitoring Frameworks
- All uses of Countryside Survey data must be acknowledged using the provided attribution text.
- Data are designed to support environmental health monitoring, policy scrutiny, and informing future decisions by national and regional bodies.
- Potential barriers for monitoring frameworks include the need for robust metadata, data governance, timely data access, and open sharing of underlying data where appropriate.
- The dataset supports cross-walking habitat extent by land class over time and can underpin trend analysis, reporting dashboards, and governance reviews.

## References
- Countryside Survey 1998 data and documentation, including technical reports and linked publications on the ITE Land Classification and habitat accounting methodologies (e.g., Bunce et al., 1996; 2007; Jackson, 2000; Scott, 2007; Carey et al., 2008).
- Related Countryside Survey outputs and supporting materials available through the Countryside Survey project website and data repositories.