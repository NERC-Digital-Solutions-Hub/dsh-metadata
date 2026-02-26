# Gathering ground-truth data

- Study area: hedgerow and field margins around a field in Northamptonshire. Ground-truth data collected within eight days of imagery acquisition in March, May, and July for five nectar-rich flowering plant species.
- Purpose: support classification of flowering plant species from high-resolution imagery by providing precise ground-truth locations and unit-level measurements.

- Ground-control and floral unit locations:
  - Individual floral units for field-margin species Centaurea nigra and Silene dioica located relative to known ground-control points using a DeWALT laser (accuracy ±1.5 mm).
  - Floral unit locations used to identify training and validation pixels in imagery.

- Floral unit definitions and measurements:
  - C. nigra: a floral unit defined as one capitulum.
  - S. dioica: a floral unit defined as flowers on the same stalk that a bee would visit in one unit; in practice, flowers within the same pixel cluster treated as a single floral unit.
  - For ground-truth units, recorded orientation (C. nigra) or orientation of flowers within the unit (S. dioica) and the width of each unit.
  - Additional focal hedgerow flowering species: Prunus spinosa, Crataegus monogyna, Rubus fruticosus. These did not flower synchronously at the study site; their floral units formed dense white to nearly white clusters.

- Flowering patterns and identification:
  - Dense white/almost white clusters used to identify flowering plant species of interest within hedgerow sections used for training and validation data.
  - No other species flowered in dense white clusters in the hedgerow sections analyzed.

- Imagery and months:
  - Data collected and analyzed for March, May, and July using corresponding imagery (3 cm resolution for training per month).

- Classification methodology (data preparation and workflow):
  - Semi-automatic classification (SCP) plugin (Congedo, 2016) in QGIS 3.4.15 used for maximum likelihood classifications.
  - Training sets created for March, May, and July using 3 cm imagery; regions of interest (ROIs) created with region growing.
  - Classification categories: each flowering plant species of interest plus an “other” category (for non-target features).
  - Training included both “pure” pixels (the whitest/pinkest pixels per species) and “edge” pixels (on patch edges or center of very small patches with mixed spectral signatures) to capture spectral variability.
  - Edge effects considered because edge pixels may contain non-target features (soil, green vegetation).

- Training and accuracy assessment:
  - A maximum likelihood classifier applied first to the 3 cm imagery for each month.
  - Multiple training variants tested (edge included or excluded) to determine the best performing scheme per month based on overall accuracy.
  - The training variant with the highest overall accuracy for 3 cm imagery per month was then used to classify the corresponding 7 cm imagery for that month.

- May imagery cross-application:
  - A training set generated from May 7 cm data was used to classify the May 7 cm image (May_7cm_class_trained_7cm.tif), illustrating cross-resolution training.

- Data references and tools:
  - Training and accuracy assessment data, Table_flowering_species.csv, Floral_unit_data.csv.
  - May_7cm_class_trained_7cm.tif for May 7 cm classification.
  - Relying on established references for definitions and tools: Carvell et al. (2007) on bumble bee forage, Congedo (2016) on SCP plugin, and QGIS (2020).

- Implications for analysis:
  - Ground-truth locations and unit measurements enable precise mapping of flowering units in remote-sensing imagery.
  - The approach emphasizes handling spectral variability and spatial resolution differences to improve classification accuracy.
  - Documented accuracy metrics (overall, user’s, producer’s) guide interpretation of classification reliability across months and resolutions.