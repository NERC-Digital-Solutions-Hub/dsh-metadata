# SPEI_IHU_groups

## Overview
- Dataset contains time series of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Units (IHU) groups.
- SPEI computed for accumulation periods: 1, 3, 6, 12, 18, 24 months, each for all 12 calendar months.
- Time span: 1961–2012 (standard distribution fitting period: 1961–2010).
- Data storage: CSV format; values are normal scores (mean 0, standard deviation 1), unitless, typically within -2 to 2 (extremes truncated at ±5).
- For each location, 72 time series are derived (6 durations × 12 months); data period limited by availability of CHESS PET and CEH-GEAR inputs.

## Purpose and intended use
- Created to support incorporation into a CEH droughts portal and enable drought analysis over specific IHU-based areas.
- Provides a drought index that accounts for evapotranspiration (CWB) across multiple time scales, aiding short-, medium-, and long-term drought assessment.

## Data provenance and sources
- IHU groups (Integrated Hydrological Units of the UK) as spatial units.
- CEH-GEAR: gridded areal rainfall estimates (monthly and daily).
- CHESS PET: potential evapotranspiration dataset.

## Methods and processing
- SPEI calculation: based on cumulative Climatic Water Balance (CWB) across accumulation periods; end-month assignment (e.g., 6-month SPEI ending July 1998 corresponds to CWB Jan–Jul 1998).
- Distribution fitting: generalized logistic (log-logistic) distribution fitted to historic CWB accumulations; alternative GEV considered but not adopted due to tail behavior and fitting stability concerns.
- Parameter estimation: SCI R package (fitSCI) using maximum likelihood; fallback to L-moments or method of moments if needed.
- Transformation: CWB data transformed to normal scores (mean 0, sd 1).
- Data limitations handling: extreme SPEI values truncated at ±5; ~95% of SPEIs fall within -2 to 2; 68% within -1 to 1.
- Autocorrelation considerations: overlapping data for >12-month periods cause autocorrelation in annual CWB series; concatenated monthly SPEI series are also likely autocorrelated; caution advised for trend analyses and independence assumptions.

## Dataset format and structure
- File format: CSV.
- Columns: 9 total.
  - RID: row identifier.
  - POLYGONID: IHU group ID (use for joins with IHU shapefile).
  - THEDATETIME: date and time.
  - Columns 4–9: SPEI values for different temporal aggregations (the six durations across the 12 calendar months, yielding 72 time series per location; stored as unitless normal scores).
- Data values: SPEI normal scores in range [-5, 5]; -9999 denotes No Data.

## Data governance, sharing, and updates
- Standard period used for distribution fitting is 1961–2010; dataset covers 1961–2012 due to data availability.
- Clear documentation of methods and limitations facilitates proper data use and reproducibility.
- Join capability with spatial data via POLYGONID or RID supports discovery and reuse across portals and catalogues.
- Updates and versioning considerations: maintain records of standardisation period, input datasets (CEH-GEAR, CHESS PET), and any methodological changes to ensure compatible updates.

## Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of Belmont Forum initiative.

## References
- Key methodological and data source references listed in the document, including Vicente-Serrano et al. on SPEI methodology, Stagge et al. on distribution choices, and details for CEH-GEAR and CHESS PET datasets.