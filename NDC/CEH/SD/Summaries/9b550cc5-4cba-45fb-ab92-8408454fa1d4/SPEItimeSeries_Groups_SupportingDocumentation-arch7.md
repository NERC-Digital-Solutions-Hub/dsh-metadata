# Supporting Information

- IHU SPEI time series for Integrated Hydrological Unit groups (IHU groups), covering 1961-2012, computed for accumulation periods of 1, 3, 6, 12, 18, and 24 months, with each accumulation ending in a given month (72 time series per location).
- SPEI values are standardised scores from a generalised logistic distribution, transformed to a normal distribution (mean 0, sd 1), with values truncated to [-5, 5] and no-data coded as -9999.
- Dataset stored in CSV format.

## I. Brief Description of the dataset
- Contains time series of SPEI for IHU groups (Kral et al., 2015).
- SPEI combines precipitation minus evapotranspiration (CWB) over specified accumulation periods.
- Periods: 1, 3, 6, 12, 18, 24 months, for all 12 calendar months.
- Standard fitting period: 1961-2010; data span 1961-2012; CSV format.
- Each location (grid cell) yields 72 SPEI time series (6 durations × 12 months).

## II. Motivation
- Derived to support a CEH droughts portal, enabling aggregation of SPEI over IHU groups to study drought over defined areas.
- SPEI contrasts with SPI by including evapotranspiration, giving a drought rarity measure at chosen time scales.
- Used across drought-related research (variability, reconstruction, atmospheric mechanisms, climate change, ecosystem impacts) and drought monitoring systems.
- Provides multi-scale information: 1-month reflects short-term moisture; 3- to 24-month SPEI capture longer-term patterns.

## III.1 Data Sources
- Integrated Hydrological Units (IHU) groups (UK) as spatial reference units.
- CEH-Gridded Estimates of Areal Rainfall [CEH-GEAR] monthly rainfall grids for SPEI derivation.
- CHESS PET dataset for potential evapotranspiration.

## III.2 Method for deriving the SPEI grids
- SPEI follows Vicente-Serrano et al. (2010a): accumulate CWB, fit a statistical distribution to historic CWB, assign SPEI to the month ending the accumulation.
- Distributions considered: generalised logistic (log-logistic) vs GEV; chose generalised logistic for better global fit and tails, avoiding issues with GEV tails and fixed standardisation period.
- Fitting technique: SCI R package (maximum likelihood; fallback to L-moments or method of moments if needed).
- Transformation: normalize to standard normal distribution (mean 0, sd 1).
- Extreme truncation: SPEI values beyond ±5 are capped.
- Serial autocorrelation: longer accumulations create overlapping data; monthly series may be autocorrelated; use for trend analysis with appropriate correlation considerations.
- Standard fitting period: 1961-2010; dataset covers 1961-2012 (limited by CHESS PET and CEH-GEAR data availability).

## IV. Format of the [SPEI_IHU_groups] dataset
- CSV file with 9 columns:
  - RID: row identifier
  - POLYGONID: IHU group ID (used for joins with IHU shapefile)
  - THEDATETIME: date and time
  - Columns 4-9: six temporal aggregations of SPEI (one per accumulation period × twelve months)
- SPEI values are normal scores (unitsless), range truncated to [-5, 5], with -9999 indicating No Data.

## V. Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research)
- Funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

## References
- Key sources include Vicente-Serrano et al. (2010a, 2010b, 2011, 2012, 2013), Stagge et al. (2015) on distribution choices, Beguería et al. (2014) on SPEI development, and data providers CEH-GEAR, CHESS PET, and IHU.