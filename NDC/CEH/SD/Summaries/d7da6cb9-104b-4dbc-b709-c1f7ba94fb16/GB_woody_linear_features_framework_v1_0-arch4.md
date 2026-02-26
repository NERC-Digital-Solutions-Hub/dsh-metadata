# Summary A modelled dataset derived from national datasets, describing the distribution of woody linear feature boundaries in Great Britain

- Objective and significance
  - Provides a national-scale, modelled dataset describing the distribution of woody linear features (hedges and lines of trees) in Great Britain.
  - Addresses data gaps and high costs of field mapping by deriving woody feature extents from existing national datasets to support landscape function, habitat connectivity, and biodiversity analyses.

- Methodology (how the dataset was produced)
  - Based on a simplified version of the Ordnance Survey MasterMap framework (LCM2007).
  - Areas where woody features are unlikely or undetectable were masked (land > 350 m, urban, wooded, coastal tide-washed).
  - Boundaries with woody features identified using vegetation height attributes derived from a 5 m NEXTMap digital terrain model (DTM):
    - Minimum vegetation height: -0.13 m (accounts for adjacent ditches)
    - Maximum vegetation height: 58 m (GB tree height upper bound)
    - Mean vegetation height: 0.58 m (accounts for gaps)
  - The dataset includes linear features with a high likelihood of being woody.

- Data sources and structure
  - OS MASTERMAP and OS LAND-FORM PANORAMA data (Public Sector Mapping Agreement data).
  - NEXTMAP digital elevation data (5 m resolution).
  - Countryside Survey 2007 mapped estimates of linear feature lengths (for validation and context).
  - Dataset format: SHAPE, Type = Geometry; SHAPE_LENGTH (numeric), representing length in metres.

- Quality assurance and validation
  - National-scale outputs are concordant with published statistics and align with Countryside Survey results.
  - Model evaluation referenced against multiple scales and published validation (Carey et al. 2008; Brown et al. 2014; Scholefield et al. 2016).

- Access, licensing, and provenance
  - Data compiled from public sector mapping data (Ordnance Survey) and NEXTMap DEM.
  - Acknowledges Crown Copyright and licensing (OS MasterMap and related datasets); NEXTMap copyright noted.

- Practical use and implications
  - Enables analysis of woody linear features at national scale without exhaustive field mapping.
  - Supports planning and policy work related to habitat connectivity, biodiversity, and landscape function.
  - Provides a basis for identifying data gaps and guiding future data collection or targeted field validation.

- Limitations and caveats
  - Masks out areas where detection is unlikely or data is unavailable (high altitude, urban, coastal).
  - Based on height thresholds and model assumptions; may exclude some woody features or include uncertain cases.
  - Dependent on the quality and coverage of underlying OS and NEXTMap datasets.