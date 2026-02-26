# A modelled dataset derived from national datasets, describing the distribution of woody linear feature boundaries in Great Britain

## Background
- Hedges and lines of trees (woody linear features) are important boundaries that support habitat connectivity, buffer land-management effects, and boost biodiversity in changing landscapes.
- Field mapping at a national scale is costly; a predictive modelling approach provides national coverage of woody linear features.

## Method
- The dataset results from a model that classifies attributes of linear features within a linear framework, based on a simplified version of OS MasterMap used in Land Cover Map 2007.
- Key steps:
  - Mask areas where woody features are unlikely or undetectable (land >350 m, urban, wooded, coastal tide-washed).
  - Derive boundary height information from a 5 m digital terrain model (NEXTMap 5m); identify woody features using vegetation-height thresholds along each feature, including:
    - Minimum vegetation height: -0.13 m (accounts for adjacent ditches)
    - Maximum vegetation height: 58 m
    - Mean vegetation height: 0.58 m (accounts for gaps)
  - Output features with a high likelihood of being woody linear features.

## Quality control – model evaluation
- Model outputs at national scale are concordant with published statistics and align spatially with Countryside Survey results.
- Evaluation conducted across multiple scales; supporting publication: Scholefield et al. (2016).

## Dataset structure and description
- Data represent linear features with a high likelihood of being woody.
- Geometry: polyline features.
- Attribute: SHAPE_LENGTH (length of feature in metres).

## Data sources and credits
- OS MASTERMAP, OS LAND-FORM PANORAMA (Public Sector Mapping Agreement data).
- NEXTMAP – Digital Elevation Data.
- Countryside Survey 2007 - Mapped estimates of linear feature lengths in Great Britain (Brown et al. 2014; CEH data).
- Related publications:
  - Carey et al. (2008) Countryside Survey UK results, 2007.
  - Morton et al. (2011) Final report for LCM2007 – The New UK Land Cover Map.
  - Scholefield et al. (2016) model evaluation reference.

## Relevance for environmental monitoring
- Provides standardized, model-driven estimates of woody linear features to support monitoring of landscape structure, habitat connectivity, and biodiversity indicators.
- Facilitates integration with other environmental datasets by delivering a coherent, reproducible dataset for national reporting.

## Challenges and opportunities for analysts monitoring the environment
- Increasing the value of datasets by combining woody feature data with other environmental datasets (beyond single-use applications).
- Enabling access to underlying data and methods so others can reuse and validate the outputs.