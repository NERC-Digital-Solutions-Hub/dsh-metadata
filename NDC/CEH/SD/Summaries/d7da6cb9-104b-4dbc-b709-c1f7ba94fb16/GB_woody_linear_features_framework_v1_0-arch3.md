# A modelled dataset derived from national datasets, describing the distribution of woody linear feature boundaries in Great Britain

## Background and purpose
- Hedgerows and lines of trees (woody linear features) are important boundaries that connect/enclose habitats, buffer land-management effects, and enhance biodiversity.
- They are often excluded from landscape-function models due to linear nature and data gaps.
- Field mapping at national scale is expensive/time-consuming, so a predictive modelling approach provides national coverage.
- The dataset aims to identify boundaries with a high likelihood of being woody linear features using existing national datasets.

## Method
- Base data and inputs
  - OS MASTERMAP, OS Land-Form PANORAMA
  - Land Cover Map 2007 (LCM2007) used as part of the framework
  - NEXTMap 5 m digital terrain data (DTM) for height attributes
- Data processing steps
  - Areas unlikely to contain woody features or difficult to detect are masked out (land above 350 m, urban, wooded, or coastal tide-washed areas)
  - Boundary height information is derived from the DEM; woody features are identified along boundaries using vegetation height thresholds by boundary length
  - Height attribute thresholds include minimum vegetation height -0.13 m, maximum 58 m, and mean 0.58 m to accommodate ditch adjacency and partial features
- Output
  - The dataset presents linear features with a high likelihood of being woody linear features

## Quality control and validation
- The model was evaluated by comparing outputs at different scales
- National-scale results are concordant with published statistics and spatially consistent with Countryside Survey (CS) results
- Key references for validation: Carey et al. (2008), Brown et al. (2014), Scholefield et al. (2016)

## Dataset structure and description
- Data type and geometry
  - SHAPE: Geometry
  - SHAPE_LENGTH: Numeric; length of feature in metres
- Data sources and attribution
  - OS MASTERMAP, OS LAND-FORM PANORAMA (Public Sector Mapping Agreement data)
  - NEXTMAP – Digital Elevation Data
  - Countryside Survey 2007 mapped estimates of linear feature lengths in Great Britain
- Licensing and rights
  - © Crown Copyright and database rights 2016; Ordnance Survey Licence number 100017572
  - Data used under Crown copyright, with licensing specifics noted
- Additional references
  - CAREY et al. 2008; MORTON et al. 2011; SCHOLEFIELD et al. (2014/2016) and related CEH/CMS publications

## Implications for monitoring frameworks
- Provides a nationally consistent, model-derived baseline for woody linear feature extent, useful for monitoring habitat connectivity and landscape structure over time.
- Enables policy scrutiny and evaluation of management interventions related to hedgerows and linear features without exhaustive field surveys.
- Can inform dashboards and reports by supplying a standardized spatial indicator derived from multiple national datasets.

## Limitations and data considerations
- Based on predictive modelling with thresholds; may require ground-truthing or updates as data sources change.
- Masking and detection thresholds mean some woody boundaries may be underrepresented in certain landscapes.
- Metadata completeness and data governance considerations are important for reuse and transparency.