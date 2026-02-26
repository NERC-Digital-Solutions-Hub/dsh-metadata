# Environmental conditions at saiga calving and die-off sites in Kazakhstan, 1979 to 2016

- Objective and scope
  - Study of environmental conditions at calving sites of the Betpak-dala saiga population in central Kazakhstan.
  - Purpose: model the probability of mass mortality events (MME) linked to haemorrhagic septicaemia caused by Pasteurella multocida.
  - Key events: MMEs occurred in 1981, 1988, and 2015; most calving progressed normally at many sites.
  - Data comprise environmental predictors, a dataset for 135 sites (out of 214 in the full shapefile), and metadata to merge with site information and mortality outcomes.
  - The dataset and modelling approach are described in Kock et al. (2018).

- Data assets and access
  - Primary data objects:
    - Shapefile with 214 calving/die-off sites and accompanying metadata.
    - Attached dataset for 135 sites containing predictor variables at sufficient resolution, plus site metadata and outcomes (Dieoff: 1 = die-off, 0 = normal calving).
  - Key linkage: combine environmental predictors with site data using a shared variable ID.
  - Access, provenance, and metadata are documented; data and documentation are available via the CEH/EIDC repository link provided in the dataset.
  - Core fields include site ID, year, die-off status, calving dates, onset data, and multiple predictor metric fields.

- Environmental data sources and predictors
  - Climate data: ERA-Interim daily reanalysis from ECMWF (temperature, dew point, soil moisture, snow depth, wind gust, precipitation).
  - Precipitation: GPCC gauge-based products supplement ERA data (available from 1988 onward).
  - Vegetation indices: NDVI from MODIS (7-day filtered/smoothed) for absolute values; NDVI anomaly data from SPOT and PROBA-V (LifeWatch WB) for anomalies.
  - Snow: Snow anomaly data from LifeWatch WB; snow depth and snowmelt timing derived from ERA-Interim snow depth data and MODIS-based anomalies.
  - Periods covered: data span roughly 1998–2016 (NDVI anomaly period; some NDVI data extend earlier via legacy datasets).
  - Focused predictors include humidity, temperature (various summaries), precipitation metrics, vegetation indices (NDVI) and anomalies, snow duration and melt, and related anomalies.

- Data extraction, processing, and metric construction
  - Zero hour defined as calving onset or index case onset; predictors aggregated over 3, 5, and 10 days before onset.
  - Precipitation metrics include totals over windows, number of wet days, and long-term precipitation sums up to onset.
  - Temperature variability metrics computed as:
    - Average and maximum daily temperature variation over 0, 3, 5, 10 days.
    - Overall temperature variation (min-to-max) over 3, 5, 10 days.
    - Maximum daily minimum temperature difference over 3, 5, 10 days.
  - Snow metrics: date of last snow cover (snow melt), length of snow cover, and days between snow melt and calving/onset.
  - NDVI and snow/NDVI anomaly data are interpolated to daily values and used to derive aggregates for multiple pre-onset periods, plus fixed-year windows (e.g., last weeks of March/April/May).
  - Handling missing calving dates:
    - Metrics generated up to fixed dates (May 9 and May 14).
    - Additional metrics created using real dates where available and generalized estimates otherwise (suffix _STGNONSET).
  - Dataset structure and nomenclature:
    - Core metric names listed in Table 1.
    - Variables have four generation suffixes:
      - Core field name only (many missing values)
      - suffix _STGN (metrics up to May 9)
      - suffix _PKGN (metrics up to May 14)
      - suffix _STGNONSET (mixed real and generalized dates for modelling)
  - The dataset includes 135 sites with a rich set of environmental metrics and the Dieoff outcome.

- Metadata, documentation, and modelling context
  - Site metadata fields include:
    - ID, Year, Population (Betpak-dala), Calving and Onset dates (Calving_ST, Calving_PK, Onset), observed deaths (Obs_deaths), last death date, and die-off flag (Dieoff).
    - Additional fields for start and peak calving dates (CALVE_STGN, CALVE_PKGN) and onset-related predictors.
  - Predictors are designed to align environmental data with calving/die-off events and to support multivariate modelling (as described in Kock et al. 2018).

- Modelling purpose and references
  - Predictor variables are intended for multivariate models to explain the probability of MMEs at calving aggregations.
  - Modelling framework and results are detailed in Kock et al. (2018); data sources and processing are documented with citations to ERA-Interim (Dee et al., 2011), GPCC, MODIS, SPOT/PROBA-V LifeWatch WB, and related NDVI/snow anomaly studies.

- Data quality, limitations, and considerations for reuse
  - Uncertainties in event onset dates necessitated dual timing windows (May 9 and May 14) and the use of generalized onset estimates where dates are missing.
  - Precipitation data have known uncertainties; GPCC data are used to mitigate ERA precipitation limitations.
  - Some predictor metrics have missing values (especially when real dates are unavailable), requiring mixtures of real and estimated data for modelling.
  - The dataset emphasizes reproducibility through explicit processing steps, interpolation to daily values, and standardized metric naming conventions.

- Practical notes for data leaders
  - Emphasizes a whole-data-system perspective: data discovery, data quality, metadata richness, discoverability, and traceable data lineage.
  - Clear pathway to link environmental predictors with site-level outcomes across networks (via the shared ID).
  - Includes multiple data sources, documented processing pipelines, and explicit handling of data gaps and date uncertainties, supporting robust governance and reusability.