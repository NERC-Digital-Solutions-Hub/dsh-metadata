# SPEI_IHU_HA

## I. Brief Description of the dataset
- Time series of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Units (IHU) hydrometric areas (IHU HA).
- SPEI is calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months, for each of the 12 calendar months.
- Values are normalised scores from a standard normal distribution (mean = 0, standard deviation = 1), with no units.
- Range limited to -5 to +5; -9999 indicates No Data.
- Accumulation periods longer than 12 months use overlapping data; results may exhibit autocorrelation.
- Dataset period: 1961–2012 (standardisation period 1961–2010).
- Data stored in CSV format.

## II. Motivation
- Derived to be incorporated into a CEH droughts portal, enabling study of drought over specific areas by aggregating SPEI across IHU HAs.
- SPEI accounts for evapotranspiration (CWB: precipitation minus evapotranspiration), offering a drought measure that reflects water balance.
- Provides multi-scale information:
  - 1-month SPEI reflects short-term soil moisture and crop stress.
  - 3-month SPEI indicates short- to medium-term moisture conditions.
  - 6-month SPEI relates to medium-term trends and potential impacts on streamflows and reservoirs.
  - 12-month SPEI captures long-term patterns linked to groundwater.
  - 18 and 24-month SPEIs reveal longer-term patterns.
- Two gridded resolutions (1 km and 5 km) serve different user needs: 1 km for local analysis; 5 km for regional studies and faster processing.
- Supports drought monitoring, trend analysis, and comparison against hydrological and ecological variables.

## III. Data Sources
- IHU hydrometric areas (UK Integrated Hydrological Units).
- CEH-GEAR: gridded estimates of areal rainfall (monthly and daily).
- CHESS PET: potential evapotranspiration dataset.

## IV. Method for deriving the SPEI grids
- SPEI follows Vicente-Serrano et al. (2010a): based on the cumulative probability of climatic water balance (CWB) amounts.
- For each location and duration (1, 3, 6, 12, 18, 24 months) and each month, 72 CWB time series are produced (6 durations × 12 months).
- A statistical distribution is fitted to each time series; chosen distribution is the generalised logistic (log-logistic) distribution.
- Fitting approach (R SCI package): maximum likelihood; if that fails, L-moments; if that fails, method of moments.
- SPEI values are transformed to normal scores (mean 0, SD 1). SPEI values are truncated at ±5.
- The standardisation period used for fitting is 1961–2010; the available data period is 1961–2012 due to data availability.
- Autocorrelation considerations:
  - For accumulation durations > 12 months, overlapping data induce autocorrelation in the underlying CWB series.
  - Monthly SPEI series concatenated from consecutive months are also likely autocorrelated; use appropriately for trend analyses with methods that account for serial correlation.

## V. Format of the [SPEI_IHU_HA] dataset
- Stored as CSV.
- Columns:
  - RID: row identifier
  - POLYGONID: IHU hydrometric area ID (join key to IHU HA shapefile)
  - THEDATETIME: date and time
  - Columns 4–9: SPEI aggregations for the six durations (1, 3, 6, 12, 18, 24 months)
- Output values: normal scores (no units), range -5 to +5; -9999 denotes No Data.

## VI. Acknowledgments
- Funded through the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) under the Natural Environment Research Council (award NE/L010038/1), as part of the Belmont Forum initiative.

## VII. References (selected)
- Vicente-Serrano et al. (2010a): Standardised Precipitation Evapotranspiration Index (SPEI) methodology.
- Stagge et al. (2015): discussions on distributions for climatological drought indices.
- SCI package (Gudmundsson & Stagge, 2014): tool used for SPEI computation.
- CEH-GEAR (Keller et al., 2015) and CHESS PET datasets (Robinson et al., 2015) as data sources.