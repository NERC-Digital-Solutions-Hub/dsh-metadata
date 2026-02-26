# Component model iterations for inputs into a multi-scale model describing the effect of host conditions on Hendra virus shedding, eastern Australia, 2008-2019

- Overview
  - Dataset comprises 1,000 iterations of multi-scale model components and associated rasters to predict how host conditions influence the probability of Hendra virus shedding in eastern Australia (2008–2019).
  - Proxies for host conditions include food shortage, rehabilitation admissions, and formation of new roosts; Roost Species Distribution Model (SDM) provides roost suitability predictions.
  - Aims to test whether incorporating host condition information improves space-time predictions of virus shedding.
  - Model objects link to code in the BatOneHealth repository to run analyses and compare eight model structures (three host-condition proxies in various combinations plus a null roost-SDM model).

- Data and formats
  - File formats:
    - Model outputs: .Rdata (FoodShortageModels, NewRoostModels, RehabModels)
    - Roost SDM: .TIF
  - Naming conventions:
    - 1,000 files in FoodShortageModels/ named Iteration_*.Rdata (1–1000)
    - 1,000 files in NewRoostModels/ named Iteration_*.Rdata (1–1000)
    - 1,000 files in RehabModels/ named Iteration_*.Rdata (1–1000)
    - 1,000 folders in RoostSDMIterations/ named Iteration_*/ each containing BatRoostPredictions_YYYY.tif (YYYY = 2007–2020)
  - Data provenance:
    - Input environmental features and training data hosted on figshare
    - Model code and run scripts available at https://github.com/hanlab-ecol/BatOneHealth

- Spatial and temporal scope
  - Spatial resolution: 5 km
  - Spatial coverage: eastern Australia; roost SDMs in 5 km grids with specific bounding coordinates (CRS: GDA2020/SA Lambert; WGS84 bounds provided)
  - Temporal coverage:
    - Food Shortage models trained on monthly data from 1998–2020
    - New Roost models trained on monthly data from 2002–2019
    - Rehab models trained on monthly data from 2005–2020
    - Roost SDM iterations trained on monthly data from 1996–2021
  - Outputs are monthly landscape predictions of prevalence, derived from 1,000 roost-location realizations per month (2008–2019).

- Modelling approach and structure
  - Modelling framework:
    - Four component model families:
      - Roost Distribution Model (RDM) based on roost occupancy data
      - Bat Rehab model (admissions to rehabilitation)
      - New Roosts model (probability of new overwintering roosts)
      - Food Shortage model (probability of acute food shortage)
    - Eight composite structures combining host-condition proxies (P(A), P(R), P(F)) in various pairings or all three together, plus a null model using only roost suitability
  - Host-condition formulations:
    - For all-three-conditions structure:
      C_xt = 1 - (1 - sqrt(P(A_xt) * P(R_xt))) * (1 - P(F_t))
    - Predicted monthly prevalence:
      P_xt = C_xt × MaxP (MaxP = 66.6% from field data)
    - 1,000 roost-location maps per month produced; host condition for each map drawn from bootstrapped models
  - Uncertainty handling:
    - Bootstrapping input data for each model 1,000 times; predictions associated with each bootstrapped realization
    - Zero prevalences from roost absence excluded when averaging maps

- Input data and sources
  - Environmental features (Table 1) sourced from:
    - Australian Gridded Climate Data (AGCD v1)
    - NOAA
    - British Antarctic Survey (BAS)
    - Dynamic Land Cover Dataset (DLCD)
  - Example features include:
    - Temperature (tempMax, tempMin, tempDiff)
    - Precipitation (prec, prec_anom)
    - NDVI, soil moisture, vapor pressure, solar exposure, potential evapotranspiration
    - Oceanic Niño Index (ONI), Southern Annular Mode (SAM)
    - Land cover: forest, urban, crop, pasture
  - Model training data sources (Table 2):
    - Roost Distribution Model: National Flying Fox Monitoring Program (NFFMP), ARS roost data
    - Bat Rehab: WIRES data
    - New overwinter roosts: ARS data
    - Food Shortage: NECT nectar shortage data
  - Data points:
    - Roost Distribution Model: 18,861
    - Bat Rehab: 10,150
    - New overwinter roosts: 195
    - Food Shortage: 267

- Model training details (hyperparameters and tools)
  - Software and packages:
    - R 4.3.2
    - gbm (for most models) and caret
    - XGBoost used for FoodShortageModels
  - Hyperparameter settings (selected via grid search and evaluation statistics):
    - Roost SDMIternations (Roost SDM):
      - eta = 0.01, max depth = 4, min observations in a node = 2, trees = 200,000
    - RehabModels:
      - learning rate = 0.0001, max depth = 2, min observations per node = 10, trees = 150,000
    - NewRoostModels:
      - learning rate = 0.0001, max depth = 2, min observations in a node = 2, trees ≈ 123,533
    - FoodShortageModels:
      - learning rate = 0.001, max depth (interaction) = 4, subsample = 1, colsample_bytree = 0.5, min_child_weight = 1, gamma = 0.5, trees = 15,000

- Output data and how they are used
  - Outputs are not modified post-generation
  - Used to produce multi-scale predictions of Hendra virus shedding
  - Model comparison:
    - Eight structures tested (null roost-SDM plus seven combinations of host-condition proxies)
    - Spatial-temporal stress components combined to yield P_xt
  - Quality control:
    - Model fit evaluated via Area Under the Curve (AUC)

- Accessibility, reproducibility, and governance
  - Data and code are publicly available (figshare for inputs; GitHub for analysis code)
  - Workflow designed to be reproducible through 1,000 bootstrap realizations and explicit parameter settings
  - Metadata and provenance are embedded through data sources, temporal/spatial extents, and dataset descriptions

- Relevance for monitoring framework authors
  - Demonstrates a transparent, reproducible workflow for developing and evaluating environmental-health proxies within an epidemiological model
  - Emphasizes use of multiple data sources, metadata-rich inputs, and clear data lineage
  - Addresses common monitoring challenges through:
    - Incorporation of multiple, complementary proxies of host condition
    - Robust uncertainty quantification via bootstrapping and numerous iterations
    - Open access to data and code to facilitate scrutiny, replication, and policy-informed decision making