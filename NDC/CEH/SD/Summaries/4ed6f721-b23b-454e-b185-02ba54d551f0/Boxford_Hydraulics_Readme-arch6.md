# Figure 1 CEH River Lambourn Observatory at Boxford (River and Leat)

## Location
- CEH River Lambourn Observatory coordinates (OSGB 1936): North 172280.373767, South 171747.766452, East 443036.218289, West 442689.348845.

## Weed management
- Weed control drives water level management, with 1–3 cuts per year depending on growth and river flow.
- Weed-cut dates recorded from 01/04/2008 to 30/09/2014 (12 entries across 2008–2014).

## Data collection
A range of hydraulics data were collected for the River and Leat at Boxford. Data collection locations are shown in Figure 1.

- 4.1 River flow gauging using Electro-magnetic Current Meter (ECM)
  - Data period: ~monthly from 08/07/2008 to 25/08/2010.
  - Collected: Stage (mAOD), Discharge (m3 s−1), gauged cross-section (Easting, Northing, mAOD).
  - Velocities measured across vertical profiles; depth-averaged velocity (VD) computed from values at bed to surface; discharges estimated from VD.

- 4.2 Leat flow gauging using ECM
  - Data period: ~monthly; Cross-sections at Inlet (22/05/2012–04/08/2014) and just downstream of wetland weir (22/05/2012–23/04/2014).
  - Collected: Stage (mAOD), Discharge (m3 s−1), cross-sections (Easting, Northing, mAOD).
  - Velocities measured at 0.6D depth; discharges from depth-averaged velocities.

- 4.3 River flow gauging using Acoustic Doppler Current Profiler (ADCP)
  - Data period: ~monthly from 19/05/2009 to 04/08/2014.
  - Collected: Stage (mAOD), Discharge (m3 s−1), gauged cross-section.
  - Measurements conducted from a cableway.

- 4.4 River stage board readings
  - Data period: ~monthly from 10/11/2009 to 04/08/2014.
  - Collected: Stage (mAOD) and stage-board locations.

- 4.5 Leat stage boards readings
  - Data period: ~monthly from 03/05/2012 to 04/08/2014.
  - Collected: Stage (mAOD) and stage-board locations.

- 4.6 River stage at water quality station (WQS) using Druck PDCR 1830
  - Data period: Every 15 minutes between 01/04/2008 and 30/09/2014.
  - Collected: Stage (mAOD) and sensor location; remote GRPS data access.

- 4.7 River stage at four stilling wells using Mini-Diver sensors
  - Data period: 15-minute logged time series with atmospheric correction via Baro-Diver.
  - Stilling wells: 1 (24/07/2012–30/09/2014), 2 (26/06/2012–30/09/2014), 3 (13/04/2012–30/09/2014), 4 (19/10/2011–30/09/2014).
  - Collected: Stage (mAOD) and sensor locations (Easting, Northing).

## Modelled Time Series River and Leat discharges at Boxford (01/04/2008 to 30/09/2014)
- 5.1 River discharge at Shaw (QShaw)
  - Time series obtained from Environment Agency - Thames Region Hydrometric Station 39019 (NGR SU470682).

- 5.2 Bypass discharge (QBypass)
  - Analyzed bypass discharges (supplied by Environment Agency, 23/10/2013 to 01/10/2014) and developed relationships with QShaw (shown in Figure 9).
  - Region-specific equations to estimate QBypass from QShaw.

- 5.3 Total River discharge at Shaw (QTotalShaw)
  - QTotalShaw = QShaw + QBypass.

- 5.4 Time series River discharges at Boxford (QBoxford)
  - QBoxford_t derived from a relationship with QTotalShaw_t+5 (lag of 5 hours) based on monthly Boxford ADCP measurements and Shaw total discharge.

- 5.5 Time series Leat discharges at Boxford (QLeat)
  - QLeat derived from a relationship between Leat inlet measurements (monthly, 22/05/2012–01/10/2014) and Boxford stage at the WQS (HWQS).
  - Piecewise quadratic relationship with HWQS>0.61 m:
    - If HWQS ≤ 0.61 m: QLeat = 0
    - If HWQS > 0.61 m: QLeat = 2.072142×(HWQS−90.134)^2 − 2.519545×(HWQS−90.134) + 0.770414
  - HWQS bed elevation reference: 90.134 m above datum.

## References
- Old et al. (2014) Instream and riparian implications of weed cutting in a chalk river.
- Rameshwaran et al. (2014) Modelling river flow responses to weed management. River Flow 2014.