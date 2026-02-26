# Supporting Information

## I. Brief Description of the dataset
- Time series of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Units (IHU) hydrometric areas (IHU HA).
- SPEI is a drought index based on the Climatic Water Balance (CWB = precipitation minus evapotranspiration) for various accumulation periods.
- SPEI calculated for accumulation periods: 1, 3, 6, 12, 18, and 24 months, each for the 12 calendar months.
- Standard fitting period for the distribution: 1961–2010.
- Dataset covers 1961–2012 and is stored in CSV format.

## II. Motivation
- Derived for incorporation into a CEH droughts portal to study drought over specific IHUs.
- SPEI accounts for evapotranspiration, offering advantages over SPI for drought analysis.
- Multi-scale information:
  - 1-month SPEI: short-term moisture, soil/crop stress.
  - 3-month SPEI: short- to medium-term moisture, seasonal CWB.
  - 6-month SPEI: medium-term trends, potential links to streamflow and reservoirs.
  - 12-month SPEI: long-term CWB, linked to streamflow/reservoirs.
  - 18–24-month SPEIs: very long-term CWB, related to groundwater.
- Two gridded datasets with different spatial resolutions (1 km and 5 km) to meet diverse user needs: local detail vs. quicker, regional analysis.

## III.1 Data Sources
- IHU hydrometric areas (UK) as the spatial framework.
- CEH-GEAR: gridded areal rainfall estimates for UK hydrological use.
- CHESS PET: potential evapotranspiration dataset.

## III.2 Method for deriving the SPEI grids
- SPEI defined as the cumulative probability of CWB amounts using the generalised logistic (log-logistic) distribution.
- For each location, SPEI is calculated for 6 durations and 12 months (72 time series per location).
- Distribution parameters estimated with the SCI R package (maximum likelihood; fallback to L-moments or method of moments as needed).
- SPEI values are transformed to normal scores (mean 0, sd 1) and are unitless; values are truncated at ±5.
- About 95% of SPEIs fall within [-2, 2], and ~68% within [-1, 1].
- For durations >12 months, overlapping data cause autocorrelation in the underlying CWB series.
- Monthly SPEI series may also be autocorrelated when concatenating successive months; this should be accounted for in trend analyses.
- Standard period to fit the distribution: 1961–2010; dataset period: 1961–2012 (aligned with CHESS PET and CEH-GEAR data).

## IV. Format of the [SPEI_IHU_HA] dataset
- File format: CSV.
- Columns: RID, POLYGONID, THEDATETIME, and six SPEI aggregations (columns 4–9).
- SPEI values are normal scores (unitsless), range limited to [-5, 5].
- No Data value coded as -9999.

## V. Acknowledgments
- Outcome of the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

## References
- The dataset builds on SPEI methodology and related drought index literature, including sources on the generalised logistic distribution, SC I tools, and drought applications across hydrology, ecology, and climate studies.