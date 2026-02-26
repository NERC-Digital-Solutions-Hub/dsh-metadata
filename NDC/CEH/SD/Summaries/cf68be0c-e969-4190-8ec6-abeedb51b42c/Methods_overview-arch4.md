# Gathering ground-truth data

- Study area and timing
  - Field margin hedgerows and surrounding margins in Northamptonshire; imagery acquired in March, May, and July.
  - Ground-truth data collected within eight days of each imagery capture for five nectar-rich flowering plant species.

- Ground-truth methodology
  - Floral unit locations for field-margin species (Centaurea nigra and Silene dioica) measured relative to ground-control points using a DeWALT laser (±1.5 mm).
  - Floral unit locations used to identify patches in imagery for training and validation pixel selection.
  - Floral unit definitions
    - C. nigra: one capitulum constitutes a floral unit.
    - S. dioica: floral unit defined as a group of flowers on one stem; in this study, flowers within the same pixel space on the main stalk were treated as one floral unit.
  - Additional data recorded
    - For C. nigra and S. dioica: orientation of the floral unit (or flowers within) and width of each unit.

- Species focus and clustering
  - Focal hedgerow flowers: Prunus spinosa, Crataegus monogyna, Rubus fruticosus.
  - Flowering did not occur synchronously; floral units appeared in dense white/almost white clusters.
  - Dense white clusters in hedgerow sections were interpreted as the target species for each month (per Table_flowering_species.csv).

- Data pipeline and analysis workflow
  - Classification approach: semi-automatic classification (SCP) plugin in QGIS 3.4.15 using maximum likelihood classification.
  - Training data
    - Monthly training sets created for March, May, and July using corresponding 3 cm imagery.
    - Regions of interest (ROIs) generated with a region-growing tool.
    - Classes: each target flowering species plus an “other” category.
  - Spectral variability handling
    - Both ‘pure’ (unmixed, high-purity) and ‘edge’ (mixed or boundary) seed pixels used to capture spectral variability.
  - Edges and mixed pixels
    - Edge pixels may contain other features; inclusion of edge and pure pixels aimed to robustly represent spectral signatures.
  - Multi-resolution workflow
    - Initial classification conducted on 3 cm imagery for each month; multiple training variants tested (edge included/excluded).
    - The training variant yielding the highest overall accuracy on 3 cm imagery was selected to classify the 7 cm imagery for the corresponding month.
    - A separate May 7 cm training set was created and used to classify the May 7 cm image.

- Accuracy assessment and data quality
  - For each month, accuracy assessments computed: overall accuracy, user’s accuracy, and producer’s accuracy.
  - The best-performing training variant (in terms of overall accuracy) was retained for final classification at the 7 cm resolution.

- References and tools
  - Carvell et al. (2007) for floral unit definitions in pollinator studies.
  - Congedo (2016) Semi-Automatic Classification Plugin (SCP) methodology.
  - QGIS (2020) software reference (version 3.4.15-Madeira).