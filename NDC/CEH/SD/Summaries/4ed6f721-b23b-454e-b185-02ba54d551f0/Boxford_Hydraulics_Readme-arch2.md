# CEH River Lambourn Observatory at Boxford (River and Leat)

## Overview
- Presents the CEH River Lambourn Observatory data framework at Boxford, covering location, weed management, and extensive hydraulics data collection.
- Establishes modelling of time series discharges for River Lambourn and Leat at Boxford (2008–2014) and relationships with upstream Shaw gauging and bypass flows.
- Aimed at enabling consistent environmental monitoring, data verification, and preparation of outputs (datasets, charts, etc.) for policy and health assessments.

## Location
- Observatory coordinates (OSGB 1936):
  - North: 172,280.373767
  - South: 171,747.766452
  - East: 443,036.218289
  - West: 442,689.348845

## Weed management
- Weed control regulates water levels; cuts are commissioned between 1 and 3 times per year depending on vegetation growth and river flow.
- Cut dates (examples from 2008–2014):
  - 09/07/2008
  - 20/05/2009
  - 05/05/2010
  - 06/07/2010
  - 18/11/2010
  - 18/05/2011
  - 23/05/2012
  - 13/11/2012
  - 01/05/2013
  - 17/07/2013
  - 21/05/2014
  - 23/07/2014

## Data collection
- A range of hydraulics data were collected at Boxford, with locations depicted in Figure 1. Data sources and methods include:
- 4.1 River flow gauging using Electro-magnetic Current Meter (ECM)
  - Data period: ~monthly 08/07/2008–25/08/2010
  - Data: Stage (mAOD), Discharge (m3 s-1), gauged cross-section (Easting/Northing/mAOD)
  - Velocity profiling: six measurements per vertical profile (Bed, 0.8D, 0.6D, 0.4D, 0.2D, surface); depth-averaged velocity calculated as VD = 0.1[Vsurface + 2V0.2 + 2V0.4 + 2V0.6 + 2V0.8 + Vbed]
- 4.2 Leat flow gauging using ECM
  - Data period: ~monthly; Cross-sections 1 (Inlet) 22/05/2012–04/08/2014 and 2 (downstream of wetland Weir) 22/05/2012–23/04/2014
  - Data: Stage, Discharge, gauged cross-sections
  - Velocities: 0.6D depth measurements; Discharge from VD = V0.6
- 4.3 River flow gauging using Acoustic Doppler Current Profiler (ADCP)
  - Data period: ~monthly 19/05/2009–04/08/2014
  - Data: Stage, Discharge, gauged cross-section
  - Measurements: via fully functional cableway
- 4.4 River stage boards readings (11 locations)
  - Data period: ~monthly 10/11/2009–04/08/2014
  - Data: Stage (mAOD) and board locations
- 4.5 Leat stage boards readings (6 locations)
  - Data period: ~monthly 03/05/2012–04/08/2014
  - Data: Stage (mAOD) and board locations
- 4.6 River stage at water quality station (WQS) using Druck PDCR 1830 submersible pressure transducer
  - Data period: every 15 minutes 01/04/2008–30/09/2014
  - Data: Stage (mAOD) and pressure sensor location
- 4.7 River stage at four stilling wells using SWS Mini-Diver non-vented sensors
  - Data period: 15-minute logs; stilling wells 1–4 with varying start/end dates
  - Data: Stage (mAOD) and sensor locations; atmospheric pressure corrections via Baro-Diver
- 5. Modelled Time Series River and Leat discharges at Boxford (01/04/2008–30/09/2014)
  - Discharge time series are modelled by relationships linking monthly measured discharges to Boxford outputs and upstream Shaw data.
- 5.1 River discharge at Shaw (QShaw)
  - Source: Environment Agency Thames Region hydrometric station (No. 39019)
- 5.2 Bypass discharge (QBypass)
  - Regionally calibrated relationships (2013–2014) between QShaw and bypass discharges
  - Region 1: QBypass = 0.006808 × QShaw^2 + 0.05754 × QShaw
  - Region 2: QBypass = (QShaw − 4.25) × 0.40978 + 0.367659 (valid 4.25–5.00)
  - Region 3: QBypass uses a nonlinear relation for QShaw > 5.00
  - Figure reference shows the linking pattern between bypass and weir discharge
- 5.3 Total River discharge at Shaw (QTotalShaw)
  - QTotalShaw = QShaw + QBypass
- 5.4 Time series Boxford discharge (QBoxford)
  - QBoxford at t = 0.689332 × QTotalShaw(t+5) − 0.062936
  - Note: total Shaw discharge lags Boxford by 5 hours (based on observed travel time)
- 5.5 Time series Leat discharges at Boxford (QLeat)
  - QLeat derived from Leat inlet measurements (2012–2014) and Boxford WQS stage (H_WQS)
  - If H_WQS ≤ 0.61 m, QLeat = 0
  - If H_WQS > 0.61 m, QLeat = 2.072142 × (H_WQS − 90.134)^2 − 2.519545 × (H_WQS − 90.134) + 0.770414
  - Note: 90.134 m is the bed elevation at the WQS station
- Figure references illustrate the relationships between measured discharges and the modeled time series
- 6. References
  - Old et al. (2014) Instream and riparian implications of weed cutting in a chalk river
  - Rameshwaran et al. (2014) Modelling river flow responses to weed management