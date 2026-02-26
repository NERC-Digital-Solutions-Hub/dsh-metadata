# Gathering ground-truth data

## Study area and data collection
- Study area: hedgerow and field margins around a field at a study farm in Northamptonshire.
- Imagery cadence: collected in March, May, and July; ground-truth data gathered within eight days of imagery.
- Target species: five nectar-rich flowering plants (specifics referenced in Table_flowering_species.csv); focal hedgerow species include Prunus spinosa, Crataegus monogyna, and Rubus fruticosus.
- Ground-truth locations:
  - For Centaurea nigra (C. nigra) and Silene dioica (S. dioica), locations of individual floral units relative to ground-control points determined with a DeWALT laser (±1.5 mm precision).
  - Predicted floral unit locations used to identify patches in imagery for training and validation pixels.
- Floral unit definitions:
  - C. nigra: one capitulum per floral unit.
  - S. dioica: floral units defined as flowers within the same pixel space on a main stalk; in this study, flowers within the same pixel cluster could constitute a single floral unit.
- Additional measurements: orientation of C. nigra units and orientation of S. dioica flowers, plus width of each unit (recorded in Floral_unit_data.csv).

## Floral unit data and measurement precision
- Floral units for ground-truthing were annotated with orientation and width data for later use in linking ground-truth points to image patches (referenced in Floral_unit_data.csv).

## Focal species and clustering considerations
- Flowering patterns: Prunus spinosa, Crataegus monogyna, and Rubus fruticosus did not flower synchronously at the study site.
- Floral units manifested as dense white/almost white clusters; in hedgerow sections used for training/validation, no other species formed dense white clusters, allowing clusters to be attributed to target species in each month.

## Classifications and accuracy assessments
- Software and workflow:
  - Semi-automatic classification plugin (SCP) in QGIS 3.4.15 (Congedo 2016) used for maximum likelihood classifications.
  - Training sets created for March, May, and July using 3 cm imagery for each month.
  - Regions of interest (ROIs) created with a region-growing tool.
- Classification categories:
  - Classes included each target flowering plant species and an 'other' category for non-target features.
- Spectral variability handling:
  - Both pure and edge seed pixels used to capture spectral variability; pure pixels are the most representative (whitest/pinkest); edge pixels are on patch edges or within small patches.
- Processing approach:
  - Apply maximum likelihood classification to 3 cm imagery for each month.
  - Test multiple training-set variants (edge included vs excluded) and evaluate accuracy to select the best variant.
  - The best-performing training variant for 3 cm imagery was used to classify the 7 cm imagery for each month.
  - An additional training set was created using 7 cm data for May to classify the May 7 cm image (May_7cm_class_trained_7cm.tif).
- Accuracy and outputs:
  - Accuracy assessments produced for overall, user’s, and producer’s accuracy metrics for each classification.
  - Data products include monthly classification maps at 3 cm (and 7 cm where applicable) and associated training/accuracy metadata.
- Data provenance:
  - Training and accuracy assessment metadata are maintained for each month (March, May, July) and for the 7 cm classifications.

## Data products and outputs
- Classification results:
  - Monthly classifications of flowering plant species and 'other' category (March, May, July) at 3 cm resolution.
  - 7 cm classifications for corresponding months, using the best 3 cm-trained variant (and an additional May 7 cm trained set for May data).
- Metadata and files:
  - Training sets and classification outputs (e.g., May_7cm_class_trained_7cm.tif) documented alongside accuracy metrics.
  - Data references include Table_flowering_species.csv, Floral_unit_data.csv, and May_7cm_class_trained_7cm.tif, plus scripts/metadata describing the training variants and accuracy results.

## Data governance and provenance (Data Stewards perspective)
- Provenance and traceability:
  - Clear linkage from ground-truth measurements (DeWALT laser, ROIs) to image classifications via ground-control points and floral-unit metadata.
  - Explicit documentation of floral-unit definitions and measurement precision.
- Metadata completeness:
  - Metadata files referenced (Table_flowering_species.csv, Floral_unit_data.csv) and month-specific training/accuracy assessment metadata ensure reproducibility.
- Data quality and interoperability:
  - Use of standardized tools (QGIS SCP plugin) and explicit handling of spectral variability (edge vs pure pixels) to improve reproducibility and interoperability.
- Data reuse and sharing:
  - Classification outputs and associated training/accuracy metadata are prepared for cataloguing and sharing; clear definitions and thresholds (e.g., ±1.5 mm measurement precision) support reuse in similar ecological and remote-sensing studies.
- Limitations and references:
  - Flowering asynchrony among focal species noted; dense white cluster appearance used as a proxy for target species; references to Carvell et al. (2007) for floral unit concepts, and to Congedo (2016) and QGIS (2020) for methods and tools.