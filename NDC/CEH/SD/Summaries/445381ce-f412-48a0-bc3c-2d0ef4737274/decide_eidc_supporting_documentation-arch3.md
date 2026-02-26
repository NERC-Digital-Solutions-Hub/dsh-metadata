# Species data

- Purpose and scope
  - Uses to inform environmental health monitoring and decision-making for policy scrutiny and future planning.
  - Focused on presence-only data for butterflies and moths across Great Britain, integrated into a DECIDE-style recording priority framework.

- Data sources
  - Presence-only occurrence data from Butterfly Conservation:
    - Butterflies: 66 species, 7,471,102 records.
    - Day-flying moths: 43 species, 94,113 records.
    - Night-flying moths: 716 species, 11,044,769 records.
  - Species list includes a wide range of named species (e.g., Cinnabar, Five-Spot Burnet, Burnet moths, hawk-moths, etc.), with day- vs night-flying distinctions established via expert consultation.
  - Data quality considerations include metadata gaps and public sharing requirements.

- Environmental data and processing
  - Climate: HadUKGrid monthly min/max temperature and total rainfall (2010–2019); used to derive WorldClim bioclimatic variables.
  - Habitats: UKCEH 2015 Landcover map (GB, 25 m resolution).
  - Topography: Copernicus DEM (Europe, 25 m resolution).
  - All environmental layers were converted to a 100 m resolution and used consistently across species distribution models (SDMs).

- Modelling approach
  - Data preparation: removed spatial-temporal duplicates; retained a single observation per species per 100 m grid cell.
  - Pseudoabsences: target-group background approach generating 10,000 pseudoabsences per species (or equal numbers if presences were limited).
  - Modelling techniques: four models per species — GLM, GAM, Random Forest, MaxEnt.
  - Model weighting and balancing: presences and pseudoabsences weighted to equalize numbers; MaxEnt required equal presences and pseudoabsences.
  - Model evaluation: 10-fold cross-validation; AUC scores averaged across folds; ensemble inclusion threshold set at AUC ≥ 0.75. If all models underperform (<0.75), all models retained but flagged as poorly performing.
  - Predictions: produced probability of presence per species across GB for each model type; generated mean and standard deviation maps across models; ensemble probabilities weighted by mean AUC.
  - Ensemble construction: mean probability and mean standard deviation across model types; variability used to inform downstream priority metrics.

- Outputs and interpretation
  - Nature and units: outputs on 100 x 100 m grid cells in Great Britain (OS National Grid).
  - Species richness: stacked richness by summing predicted probabilities across species within a taxonomic group (e.g., two species with 0.5 probability yield a richness of 1.0 in that cell).
  - Model variability: summed standard deviation across the 10 models for each grid cell and species group; higher values indicate greater uncertainty in predictions.
  - DECIDE recording priority: scaling of model variability by 1 / (months since last record) with spatial smoothing to down-weight neighboring cells that had recent records. If a record occurred recently, priority approaches zero; areas with no records have priority driven by model variability.
  - Outputs include separate layers for butterflies, day-flying moths, and night-flying moths:
    - butterfly_decide_priority.tif
    - butterfly_model_variability.tif
    - butterfly_species_richness.tif
    - day_flying_moth_decide_priority.tif
    - day_flying_moth_model_variability.tif
    - day_flying_moth_species_richness.tif
    - night_flying_moth_decide_priority.tif
    - night_flying_moth_model_variability.tif
    - night_flying_moth_species_richness.tif

- Data structure and access
  - Flat file structure; GeoTIFF (.tif) format stored in /data/.
  - Filenames reflect taxonomic group and information layer, e.g.:
    - butterfly_decide_priority.tif
    - butterfly_model_variability.tif
    - butterfly_species_richness.tif
    - day_flying_moth_decide_priority.tif
    - day_flying_moth_model_variability.tif
    - day_flying_moth_species_richness.tif
    - night_flying_moth_decide_priority.tif
    - night_flying_moth_model_variability.tif
    - night_flying_moth_species_richness.tif
  - Example read-in: R terra package (terra::rast("butterfly_decide.tif")), with metadata such as resolution (100 m), extent, and CRS provided.

- Quality control and governance
  - Project team reviewed model outputs through a data end-user interface to identify anomalies.
  - DECIDE Recorder tool provides interactive access within a local 5 km radius and supports user feedback; used by a substantial user base (~5,000 users) to flag issues.

- Computing resources
  - Analyses and models run on the JASMIN high-performance computing facility.