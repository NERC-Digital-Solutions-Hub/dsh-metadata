# CEH River Lambourn Observatory

## Purpose and scope
- Documents environmental monitoring activities at the CEH River Lambourn Observatory to scrutinise and inform policy decisions and future management actions.
- Describes location, weed management, comprehensive data collection, data integration, and modeling to produce time-series discharges for the River and Leat at Boxford.
- Demonstrates how multiple data streams are combined to derive policy-relevant indicators (e.g., total river discharge, bypass effects, and Leat flows).

## Location
- CEH River Lambourn Observatory coordinates (OSGB 1936):
  - North: 172280.373767
  - South: 171747.766452
  - East: 443036.218289
  - West: 442689.348845

## Weed management
- River Lambourn weed cutting is used to regulate water levels and flow resistance.
- Cuts occur 1–3 times per year, depending on weed growth and river flow.
- Cut dates (2008–2014) include: 09/07/2008; 20/05/2009; 05/05/2010; 06/07/2010; 18/11/2010; 18/05/2011; 23/05/2012; 13/11/2012; 01/05/2013; 17/07/2013; 21/05/2014; 23/07/2014.

## Data collection (overview)
- A broad suite of hydraulics data were collected for the River and Leat at Boxford, across multiple locations and time periods.
- Data collection methods span traditional gauging, advanced acoustic methods, and fixed-stage sensors, with data varying from monthly to 15-minute intervals.

## Data collection methods

- 4.1 River flow gauging using Electro-magnetic Current Meter (ECM)
  - Data period: roughly monthly 08/07/2008–25/08/2010
  - Collected: Stage (mAOD), Discharge (m3 s-1), cross-section coordinates
  - Velocities measured in vertical profiles; depth-averaged velocity computed to estimate discharge

- 4.2 Leat flow gauging using ECM
  - Data period: roughly monthly 22/05/2012–04/08/2014 (Inlet) and 22/05/2012–23/04/2014 (downstream of wetland Weir)
  - Collected: Stage, Discharge, cross-sections
  - Velocities at 0.6D depth used to compute discharge

- 4.3 River flow gauging using Acoustic Doppler Current Profiler (ADCP)
  - Data period: roughly monthly 19/05/2009–04/08/2014
  - Collected: Stage, Discharge, cross-sections
  - Measurements performed from a cableway

- 4.4 River stage boards readings
  - Data period: roughly monthly 10/11/2009–04/08/2014 (11 locations)
  - Collected: Stage (mAOD) and locations

- 4.5 Leat stage boards readings
  - Data period: roughly monthly 03/05/2012–04/08/2014 (6 locations)
  - Collected: Stage (mAOD) and locations

- 4.6 River stage at water quality station (WQS)
  - Data period: every 15 minutes 01/04/2008–30/09/2014
  - Instrument: Druck PDCR 1830 submersible transducer with CR1000 logger and GPRS
  - Collected: Stage and sensor location

- 4.7 River stage at four stilling wells
  - Data period: 15-minute time series with corrections for atmospheric pressure
  - Instruments: Mini-Diver sensors with Baro-Diver compensation
  - Time spans: Stilling wells range from 2011–2014 for different wells
  - Collected: Stage and sensor location

## Data modeling and time-series construction

- 5. Modeling approach to produce continuous time-series discharges
  - River discharge at Shaw (QShaw) derived from Environment Agency hydrometric station data
  - Bypass discharge (QBypass) modeled as a function of Shaw discharge (region-specific equations)
  - Total Shaw discharge (QTotalShaw) = QShaw + QBypass

- 5.1 River discharge at Shaw (QShaw)
  - Source: Hydrometric Station 39019, SU470682

- 5.2 Bypass discharge relationships
  - Region 1: QBypass = 0.006808 × (QShaw)^2 + 0.0575 × QShaw
  - Region 2: When 4.25 < QShaw ≤ 5.00, QBypass = (QShaw − 4.25) × 0.40978 + 0.367659
  - Region 3: For QShaw > 5.00, bypass relationship uses a different transfer function (nu Passes)

- 5.3 Total River discharge at Shaw
  - QTotalShaw = QShaw + QBypass

- 5.4 Time series of Boxford discharge (QBoxford)
  - Derived from Boxford measurements downstream of WQS and QTotalShaw
  - Relationship includes a 5-hour lag between Shaw/TotalShaw and Boxford measurements

- 5.5 Time series of Leat discharges at Boxford (QLeat)
  - Derived from Leat inlet measurements and Boxford water quality stage (HWQS)
  - Piecewise relation based on HWQS, with bed elevation used in the calculation

## Data sources and integration
- Uses data from multiple sensors and platforms (ECM, ADCP, stage boards, fixed-stage sensors) and from the Environment Agency.
- Integrates hydraulic measurements with hydrological relationships to produce continuous discharge time series for policy-relevant indicators (Boxford and Leat discharges, and total Shaw discharges).

## Implications for monitoring policy and decision making
- Demonstrates a practical workflow for turning heterogeneous, multi-source hydraulic data into policy-relevant indicators (e.g., impacts of weed management on river hydraulics, and the contribution of bypass flows to downstream discharge).
- Enables scenario evaluation (weed-cut timing, bypass influence) and supports decisions on river management, water level targets, and catchment interventions.
- Highlights the value of linking localized measurements with broader gauging networks to extrapolate time series and evaluate hydrological responses.

## Challenges and considerations for monitoring frameworks
- Data gaps and varying data periods across measurement types.
- Dependence on cross-site relationships and calibrations (e.g., Shaw-Boxford, Leat-WQS) which require ongoing validation.
- Managing legacy data and ensuring consistent metadata for reproducibility.
- Need for transparent documentation of data sources, transformations, and uncertainty to support governance and stakeholder scrutiny.

## References
- Old, G.H., et al. (2014) Instream and riparian implications of weed cutting in a chalk river. Ecological Engineering, 71, 290-300.
- Rameshwaran, P., et al. (2014) Modelling river flow responses to weed management. In: River Flow 2014, CRC Press, 467-474.