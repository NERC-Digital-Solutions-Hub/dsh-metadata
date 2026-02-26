# Simulated Monthly Biological Indicators for England and Wales 1964-2012

## Context and Aim
- Part of the Historic Droughts project (2014–2018, £1.5m) aiming to understand past UK droughts to improve future management.
- Involves eight UK institutions and focuses on drought surveillance and interdisciplinary understanding of drought impacts.
- This dataset specifically investigates how three biological indicators respond to discharge: ASPT (Average Score Per Taxon), LIFE at the Family level (LIFE_F), and LIFE at the Species level (LIFE_S).

## Data sources and motivation
- Biological indicators sourced from the Environment Agency’s BIOSYS dataset (England), circa 2011–2012.
- Indicators provide a snapshot of invertebrate community health at sampling sites, serving as proxies for river ecological health.
- Discharge is characterized by the Standardised Streamflow Index (SSI), tailored for drought studies (SSI6).

## Methods and modelling approach
- Data: Twice-yearly bio-indicator values from 86 sites matched to 76 EA gauging stations (approx. 1950 data-points; 1964–2012 period), part of drought surveillance network.
- Pre-processing: Seasonal and annual trends removed via detrending and deseasonalising using site-specific linear models.
- Predictor suite: SSI6 for the sampling month plus six lagged SSI6 values (6, 12, 18, 24, 30, 36 months prior).
- Modelling: Three distinct multilevel models (one per bio-indicator) with two levels (data and site).
- Inference: Multi-Model Inference (MMI) selects sets of good models and averages them to form the final model, rather than relying on a single best model.
- Output generation: Final dataset consists of simulated, de-trended, and de-seasonalised indicators for 1964–2012.

## Data format and contents
- Outputs provided as CSV files:
  - HD_Bio_Indicators_Site_Location: site location and site-station mapping
  - HD_Input_ASPT_ENG_WLS_1985-2011: observed and detrended ASPT
  - HD_Output_ASPT_ENG_WLS_1964-2012: modeled DTDS ASPT
  - HD_Input_LIFE_FAMILY_ENG_WLS_1985-2011: observed and detrended LIFE (Family)
  - HD_Output_LIFE_FAMILY_ENG_WLS_1964-2012: modeled DTDS LIFE_F
  - HD_Input_LIFE_SPECIES_ENG_WLS_1985-2011: observed and detrended LIFE (Species)
  - HD_Output_LIFE_SPECIES_ENG_WLS_1964-2012: modeled DTDS LIFE_S
- Key headers describe site coordinates, station IDs, sample dates, seasons, observed indicators, detrended variables, SSI and lag predictors, and modeled outputs.

## Relevance to monitoring framework design
- Demonstrates linking hydrological drivers (SSI and lags) to ecological responses (bio-indicators) across multiple sites.
- Applies rigorous data preparation (detrending/deseasonalising) to ensure comparable temporal signals for policy evaluation.
- Uses hierarchical modelling and model averaging to enhance robustness of environmental health inferences.
- Provides transparent data provenance, with explicit metadata and data lineage, supporting data governance and reuse in monitoring frameworks.

## Data governance and accessibility considerations
- Data provenance tied to the Historic Droughts project; acknowledgments and references supplied.
- Metadata included in output headers; data sharing and documentation are explicitly addressed (paper in preparation describing methods in more detail).