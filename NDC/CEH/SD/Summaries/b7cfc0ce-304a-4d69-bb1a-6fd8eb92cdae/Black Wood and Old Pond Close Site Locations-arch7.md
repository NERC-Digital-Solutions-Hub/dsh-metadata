# Black Wood, UK County = Hampshire.

## Overview
- Dataset appears to list plot locations with associated administrative, temporal, and geospatial fields intended for map-based analysis.
- Key sites include Black Wood (Hampshire) and Old Pond Close (Northamptonshire), with references to published studies on interception and atmospheric pollution.

## Dataset structure and fields
- Recorded fields include:
  - UK County
  - Start date (day, month, year)
  - End date (day, month, year)
  - Grid reference
  - Notes
- Many entries are incomplete or contain missing data (represented by dots), indicating partial records alongside fully specified plots.

## Key plots and details
- Black Wood, Hampshire
  - Start date: 23 May 1990
  - End date: 12 Dec 1991
  - Grid reference: SU534428
  - Notes: Details of plot locations given in Neal et al., 2004
- Old Pond Close, Northamptonshire
  - Start date: 20 Mar 1991
  - End date: 6 Apr 1992
  - Grid reference: SP877551
  - Notes: Details of plot locations given in Neal, 2002
- Additional entries contain references to related studies and datasets, but many fields are incomplete or missing.

## Geospatial details
- Contains UK Ordnance Survey grid references (e.g., SU534428, SP877551) suitable for conversion to coordinates.
- No explicit coordinate system or projection stated beyond grid references.

## References and provenance
- Neal, C., Ryland, G.P., Conway, T., Jeffery, H.A., Neal, M., Robson, A.J., Smith, C.J., Walls, J., Bhardwaj, C.L. 1994. Interception of chemicals at a forest edge for a rural low-lying site at Black Wood, Hampshire. Sci. Tot. Environ., 142, 127–141.
- Neal, C. 2002. Interception and attenuation of atmospheric pollution in a lowland ash forested site, Old Pond Close, Northamptonshire, UK. Sci. Tot. Environ., 282/283, 99-109.
- Notes indicate that plot locations are detailed in Neal et al. 2004 for Black Wood.

## Data quality and gaps
- Significant portions of the dataset show missing values (empty fields for many entries).
- Inconsistent field completeness suggests data cleaning and standardization are needed before GIS use.
- While two plots have concrete grid references, many other entries lack usable spatial data.

## GIS implications and potential uses
- When complete, the dataset can support:
  - Mapping plot locations and durations for interception and atmospheric pollution studies.
  - Linking plot data to published literature for GIS-based literature-informed analyses.
  - Temporal analysis of plotting periods in relation to environmental events or interventions.

## Recommended workflow for GIS specialists
- Data cleaning and standardization:
  - Convert all dates to ISO 8601 format; handle missing dates explicitly.
  - Normalize UK county names and resolve any ambiguous entries.
  - Validate and, where possible, fill missing grid references or derive coordinates from available references.
- Data structuring:
  - Create a GIS-ready table with fields: site_name, county, start_date, end_date, grid_reference, notes, literature_refs.
  - Convert valid grid references to point geometries with a clear CRS (e.g., OSGB36 / British National Grid).
- Documentation and provenance:
  - Attach literature references to corresponding plots; document data gaps and assumptions.
- Visualization and analysis:
  - Build map layers for plot locations; create time-slider visualizations to reflect study periods.
  - Integrate with external datasets (e.g., atmospheric pollution records) if available.