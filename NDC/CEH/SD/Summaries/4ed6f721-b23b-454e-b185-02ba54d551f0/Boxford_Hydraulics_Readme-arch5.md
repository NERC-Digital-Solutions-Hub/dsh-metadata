# Figure 1 CEH River Lambourn Observatory at Boxford (River and Leat)

- Purpose and scope
  - Documentation of hydrological data collection at the CEH River Lambourn Observatory (Boxford) for River and Leat systems.
  - Multi-sensor, multi-method dataset (ECM, ADCP, stage boards, stilling wells, water quality station) spanning 2008–2014 with various temporal resolutions.

- Spatial and coordinate context
  - Location described in OSGB 1936 coordinates for the study area and cross-sections (River and Leat).
  - Specific measurement locations and cross-sections illustrated in accompanying figures.

- Data collection methods and datasets
  - 4.1 River flow gauging (ECM)
    - Data: Stage (mAOD), Discharge (m3 s-1), cross-section coordinates (Easting, Northing, mAOD).
    - Frequency: ~monthly (08/07/2008–25/08/2010).
    - Method: depth-averaged velocity from six vertical profiles; VD = 0.1[VS + 2V0.2 + 2V0.4 + 2V0.6 + 2V0.8 + Vbed].
  - 4.2 Leat flow gauging (ECM)
    - Data: Stage, Discharge, cross-sections.
    - Frequency: ~monthly (2012–2014); two cross-sections.
  - 4.3 River flow gauging (ADCP)
    - Data: Stage, Discharge, cross-sections.
    - Frequency: ~monthly (19/05/2009–04/08/2014); cableway measurements.
  - 4.4 River stage boards
    - Data: Stage (mAOD) at 11 locations; coordinates.
    - Frequency: ~monthly (2009–2014).
  - 4.5 Leat stage boards
    - Data: Stage (mAOD) at 6 locations; coordinates.
    - Frequency: ~monthly (2012–2014).
  - 4.6 River stage at water quality station (WQS)
    - Data: Stage (mAOD); sensor location.
    - Frequency: every 15 minutes (01/04/2008–30/09/2014); Druck PDCR 1830 sensor, CR1000 logger with GRPS.
  - 4.7 River stage at four stilling wells
    - Data: Stage (mAOD) and sensor location; atmospheric pressure correction via Baro-Diver.
    - Frequency: every 15 minutes; intervals vary by well (2011–2014 in different spans).

- Data modelling and derived time series
  - 5.1 River discharge at Shaw (QShaw)
    - Based on Environment Agency discharge data (Station 39019, Shaw).
  - 5.2 Bypass discharge (QBypass)
    - Relationships with QShaw (23/10/2013–01/10/2014) using a piecewise function across three regions.
  - 5.3 Total River discharge at Shaw (QTotalShaw)
    - QTotalShaw = QShaw + QBypass.
  - 5.4 Boxford discharges (QBoxford)
    - Boxford discharge derived from QTotalShaw with a 5-hour lag: QBoxford_t = 0.689332 × QTotalShaw_(t+5) − 0.062936.
  - 5.5 Leat discharges (QLeat)
    - Leat discharge derived from Leat inlet measurements (2012–2014) and Boxford water quality station height (HWQS) via a piecewise relationship:
      - HWQS ≤ 0.61 m: QLeat = 0
      - HWQS > 0.61 m: QLeat = 2.072142×(HWQS−90.134)^2 − 2.519545×(HWQS−90.134) + 0.770414
    - Uses Boxford HWQS as a predictor; bed elevation offset included.

- Data provenance, sources, and references
  - Primary data sources include in situ sensors (ECM, ADCP, stage boards, stilling wells, Druck sensor) and external data (Environment Agency Shaw discharge data, bypass analyses).
  - Key references: Old et al. (2014) on weed cutting and river responses; Rameshwaran et al. (2014) on river flow modeling.

- Data governance considerations for Data Stewards
  - Metadata and provenance
    - Capture instrument type, measurement period, locations, units (mAOD, m3 s-1), sampling frequency, and cross-section identifiers.
    - Document modelling equations, lags (e.g., Boxford 5-hour lag), and region-specific bypass formulas.
  - Data quality and transformations
    - Clearly record calculation methods (depth-averaged velocities, stage-to-discharge relationships, and derived time series).
    - Note calibration, data gaps, and any corrections (e.g., barometric corrections for stilling wells).
  - Data interoperability and formats
    - Harmonize data from multiple sensors/formats; maintain consistent coordinate reference (OSGB 1936) and units across datasets.
  - Update and maintenance
    - Define update cadence for observed vs. modelled data; manage ongoing data collection (e.g., bypass status under EA investigation) and integration of new measurements.
  - Access and sharing considerations
    - Distinguish between public observational data and data subject to agency oversight or embargo (e.g., bypass discharge status and EA data).
  - Documentation and reuse
    - Provide clear documentation of data processing steps, modeling relationships, and validation context to support discovery and reuse by data users. 

- End notes
  - The document outlines a comprehensive, multi-method data collection and modelling framework for river and leet discharges at Boxford, with explicit relationships between observed measurements and derived time series, emphasizing provenance, methodological transparency, and governance needs relevant to data stewardship.