# Gathering ground-truth data

- Study area and imagery timeline
  - Hedge rows and field margins around a field at a study farm in Northamptonshire.
  - Ground-truth data collected within eight days of imagery acquisition in March, May, and July.
  - Ground-truth data cover five nectar-rich flowering plant species (referenced in Table_flowering_species.csv).

- Ground-truth data collection methods
  - Field margin species (Centaurea nigra and Silene dioica): locations of individual floral units determined with a DeWALT laser measurement (±1.5 mm) relative to known ground-control points.
  - Predicted floral unit locations used to locate patches in imagery for training and validation pixel selection.
  - Floral unit definitions:
    - C. nigra: one capitulum per floral unit.
    - S. dioica: one floral unit per group of flowers within the same pixel space; flowers on a main stalk within a pixel count as one unit.
  - For each ground-truth unit, recorded orientation and width (Floral_unit_data.csv).

- Focal hedgerow species and flowering patterns
  - Prunus spinosa, Crataegus monogyna, Rubus fruticosus as hedgerow species of interest.
  - These species did not flower synchronously; flowering units formed dense white to nearly white clusters.
  - Dense white cluster patches in hedgerows were treated as the target flowering species for each data acquisition month.

- Classification and accuracy assessment
  - Classification tool: Semi-Automatic Classification Plugin (SCP) in QGIS 3.4.15 (Congedo, 2016) using maximum likelihood classification.
  - Training data: March, May, and July trained on 3 cm imagery for each month.
  - Regions of interest (ROIs): five target flowering species plus an 'other' category for non-target features.
  - Spectral variability handling: used both 'pure' (unmixed) and 'edge' (potentially mixed) seed pixels to capture variability.
  - Validation approach: multiple training variants tested; the variant with the highest overall accuracy on 3 cm imagery for each month was used to classify the corresponding 7 cm imagery.
  - Additional May processing: created a training set with 7 cm May data to classify the May 7 cm image (May_7cm_class_trained_7cm.tif).

- Data sources and references
  - Carvell et al. (2007) on flowering unit definitions and bee foraging context.
  - Congedo (2016) on the SCP plugin.
  - QGIS (2020) as the GIS platform.

- Implications for monitoring framework authors
  - Emphasizes ground-truthing to calibrate remote-sensing classifications and to define robust floral-unit concepts aligned with target species.
  - Demonstrates use of open-source tools (QGIS SCP) and transparent training/validation workflows to support reproducibility.
  - Shows handling of spectral variability and data resolution trade-offs (3 cm vs 7 cm) to optimize detection accuracy.
  - Highlights the importance of explicit definitions for floral units and careful data collection to enable accurate monitoring outputs.