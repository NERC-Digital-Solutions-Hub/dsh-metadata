# A modelled dataset derived from national datasets, describing the distribution of woody linear feature boundaries in Great Britain

## Background
- Hedgerows and lines of trees (woody linear features) are important for habitats, buffering land management, and biodiversity.
- They are often not included in landscape-function models due to their linear nature and data difficulties.
- National field mapping is costly; a predictive modelling approach provides national coverage based on existing datasets.

## Method
- The dataset is the output of a model that classifies attributes of each linear feature within a linear framework based on a simplified OS MasterMap used in Land Cover Map 2007 (LCM2007).
- Areas are masked where woody features are unlikely or undetectable (land >350 m, urban, wooded, or coastal tide-washed areas) using OS Land-Form Panorama and LCM2007.
- Boundary height information is derived from a 5 m Digital Terrain Model (NEXTMap 5m). Woody features are identified using thresholds for vegetation height over a given boundary length:
  - Minimum vegetation height: -0.13 m (accounts for adjacent ditch)
  - Maximum vegetation height: 58 m (GB tree height limit)
  - Mean vegetation height: 0.58 m (accounts for gaps)
- The dataset includes only linear features with a high likelihood of being woody.

## Quality Control – model evaluation
- Model outputs at national scale are concordant with published statistics and align with Countryside Survey results.
- References for evaluation include Carey et al. (2008), Brown et al. (2014), and Scholefield et al. (2016).

## Dataset structure and description
- Dataset consists of linear features with a high likelihood of being woody.
- SHAPE: Geometry; SHAPE_LENGTH: numeric, length in metres.
- Data sources include:
  - OS MASTERMAP, OS LAND-FORM PANORAMA (Public Sector Mapping Agreement datasets)
  - NEXTMAP – Digital Elevation Data (© Intermap Technologies)
  - Countryside Survey 2007 mapped estimates of linear feature lengths in Great Britain (CEH data)
- Licensing and rights:
  - Cartographic data reproduced by permission; Crown Copyright and database rights; OS Licence details provided.
  - Elevation data and CEH dataset also cited with respective rights.

## Relevant Publications & References
- Carey, P.D. et al. 2008. Countryside Survey UK Results from 2007.
- Morton, D. et al. 2011. Final Report for LCM2007 – The New UK Land Cover Map.
- Scholefield, P.A. et al. (and colleagues) – A Model of the Extent and Distribution of Woody Linear Features in Rural Great Britain (submitted).

## Data use and implications (summary for data support perspective)
- Provides national-scale mapping of woody linear features to support policy, planning, and biodiversity analyses.
- Enables subsequent data products and analyses by supplying a high-likelihood woody feature layer derived from existing datasets.
- Users should be aware of masking and height-threshold criteria that define feature inclusion, which introduce certain spatial biases (areas where features are excluded or uncertain).