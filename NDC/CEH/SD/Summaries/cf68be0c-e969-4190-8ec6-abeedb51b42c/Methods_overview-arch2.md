# Gathering ground-truth data

- Objective and study area
  - Study area: hedgerow and field margins around a field at a study farm in Northamptonshire
  - Ground-truth data gathered within eight days of imagery acquisition in March, May, and July for five nectar-rich flowering plant species (refer to Table_flowering_species.csv)

- Ground-truth data collection and floral units
  - Floral unit locations determined in relation to known ground-control points using a DeWALT laser (±1.5 mm)
  - Predicted floral unit locations used to locate patches of floral units in imagery for training and validation pixels
  - Floral unit definitions
    - Centaurea nigra: one capitulum per floral unit (per Carvell et al. 2007)
    - Silene dioica: floral unit defined as flowers on a main stalk within the same pixel space; treated as one floral unit in this study
  - For each ground-truth floral unit, recorded orientation and width (Floral_unit_data.csv)

- Focal species and flowering patterns
  - Hedgerow flowering species: Prunus spinosa, Crataegus monogyna, Rubus fruticosus
  - Flowering did not flower synchronously; floral units formed dense white/almost white clusters
  - In hedgerow sections used for training/validation, no other species formed dense white clusters

- Classifications and accuracy assessments
  - Classification method: semi-automatic classification (SCP) plugin in QGIS 3.4.15 using Maximum Likelihood
  - Training sets created for March, May, and July using 3 cm imagery for each month (see training and accuracy assessment metadata)
  - Regions of interest (ROIs) created with region-growing; classes included each target flowering species and an 'other' category
  - Spectral variability handling: used both 'pure' and 'edge' seed pixels
    - Pure: whitest/pinkest pixels per species
    - Edge: edge-of-cluster or center-of-small-patch pixels with mixed spectral signals
  - Process
    - Apply maximum likelihood classification to 3 cm imagery for each month
    - Test multiple training set variants (edge included/excluded)
    - Select the variant with the highest overall accuracy for 3 cm data to classify the 7 cm imagery
  - Additional note: a separate 7 cm May-trained dataset was created and used to classify the May 7 cm image (May_7cm_class_trained_7cm.tif)

- Outputs, data management, and references
  - Outputs include trained classifications and accuracy assessments per month; training/accuracy metadata accompany results
  - Imagery and ground-truth data linked to supporting tables/files (e.g., Table_flowering_species.csv, Floral_unit_data.csv)
  - References:
    - Carvell et al. 2007
    - Congedo 2016
    - QGIS 2020

- Relevance to environmental monitoring objectives
  - Demonstrates a standardized, data-driven workflow to quantify flowering plant presence for environmental health monitoring
  - Verifies and quality-assures ground-truth locations against high-resolution imagery
  - Produces clear outputs (classified imagery and accuracy metrics) suitable for monitoring environmental health and informing policy performance
  - Emphasizes data provenance and storage of training sets and classification results for transparency and reuse