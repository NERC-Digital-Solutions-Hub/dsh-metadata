# Summary A modelled dataset derived from national datasets, describing the distribution of woody linear feature boundaries in Great Britain

## Overview
- A modelled national dataset describing the distribution of woody linear features (hedges and lines of trees) across Great Britain.
- Aims to support understanding of landscape function and biodiversity by including linear features that are often omitted from models due to data challenges.

## Data sources and provenance
- Based on a simplified version of OS MasterMap used in Land Cover Map 2007 (LCM2007).
- Additional data inputs: OS Land-Form Panorama and NEXTMap 5m digital elevation data.
- Public data sources with licensing:
  - OS MasterMap / OS Land-Form Panorama (Public Sector Mapping Agreement data) © Crown Copyright, licence 100017572.
  - NEXTMap digital elevation data © Intermap Technologies Inc.
  - Countryside Survey 2007 mapped estimates of linear feature lengths in Great Britain (Brown et al. 2014), DOI provided.

## Methodology and data processing
- Area masking: exclude regions where woody linear features are unlikely or undetectable (e.g., land > 350 m, urban/wooded/ coastal tide-washed areas).
- Boundary height reasoning: derive boundary height from a digital terrain model; apply vegetation height thresholds along boundaries to identify woody features (min -0.13 m to max 58 m; mean 0.58 m) to account for ditches and gaps.
- Output: dataset consists of linear features with a high likelihood of being woody as identified by the model.

## Quality control and evaluation
- Model evaluated at multiple scales and shown to be concordant with national statistics and spatially consistent with Countryside Survey results.
- References for evaluation and methodology include Scholefield et al. (2016) and related CEH publications.

## Dataset structure and description
- Feature type: SHAPE, Type = Geometry (polyline).
- Attribute: SHAPE_LENGTH, Type = Numeric (length of feature in metres).
- Indicates a focus on polyline representations of woody features with length measurements.

## Licensing and access
- OS master data and related cartographic content licensed under Crown Copyright; OS licence number 100017572.
- NEXTMap data used under its own license terms.
- Countryside Survey data cited with DOI; data usage governed by these licensing arrangements.

## Related publications and references
- Carey et al., 2008. Countryside Survey UK results from 2007.
- Morton et al., 2011. Final report for LCM2007 – The New UK Land Cover Map.
- Scholefield et al., 2016. Model of the extent and distribution of woody linear features in rural Great Britain.
- Brown et al., 2014. Countryside Survey 2007 mapped estimates of linear feature lengths in Great Britain.

## Limitations and considerations for use
- Includes only features with a high likelihood of being woody; potential omissions in areas where masking excludes relevant features.
- Dependency on existing national datasets and the modeling thresholds applied to vegetation height attributes.
- Some areas may require caution due to data origin, licensing constraints, or resolution limits of input datasets.

## Use and update considerations for Data Stewards
- Document provenance and licensing clearly to ensure ongoing compliance with data rights.
- Maintain versioning to reflect updates or recalibrations of the model, ensuring transparency about changes in feature detection thresholds or input sources.
- Provide guidance on appropriate use given the model’s scope (high-likelihood woody features) and known limitations.