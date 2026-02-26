# Figure 1 CEH River Lambourn Observatory at Boxford (River and Leat)

- Purpose and scope
  - Documentation of the CEH River Lambourn Observatory at Boxford, including river and leet data collection, sensor deployments, and downstream discharge modeling.
  - Coordinates provided in OSGB 1936: North 172280.37, South 171747.77, East 443036.22, West 442689.35.
  - Data collection spans multiple techniques (ECM, ADCP, stage boards, stilling wells, and submersible pressure transducers) from 2008 to 2014, supporting modeled time-series discharges and system understanding.

- Weed management context
  - River weed cutting is conducted 1–3 times per year to influence water levels; specific cut dates are tabulated (2008–2014).
  - Weed management affects hydraulic conditions and data interpretation for flow measurements.

- Data collection methods and locations
  - River and Leat data collection locations shown in Figure 1 (site map not included here).
  - River flow gauging using Electro-magnetic Current Meter (ECM)
    - Time period: ~monthly 08/07/2008–25/08/2010
    - Measured: Stage (mAOD), Discharge (m3 s-1), cross-sections (Easting, Northing, mAOD)
    - Velocity profiling across verticals; depth-averaged velocity VD calculated from measurements at bed, 0.2D, 0.4D, 0.6D, 0.8D, surface.
  - Leat flow gauging using ECM
    - Time period: ~monthly 22/05/2012–04/08/2014 (Inlet cross-section) and 22/05/2012–23/04/2014 (downstream cross-section near wetland weir)
    - Measured: Stage, Discharge, cross-sections
    - Velocities measured at 0.6D depth; VD = V at 0.6D
  - River flow gauging using Acoustic Doppler Current Profiler (ADCP)
    - Time period: ~monthly 19/05/2009–04/08/2014
    - Measured: Stage, Discharge, cross-sections
    - Data captured from a cableway deployment
  - River stage boards
    - Time period: ~monthly 10/11/2009–04/08/2014
    - Measured: Stage (mAOD) at 11 locations
  - Leat stage boards
    - Time period: ~monthly 03/05/2012–04/08/2014
    - Measured: Stage (mAOD) at 6 locations
  - River stage at Water Quality Station (WQS)
    - Sensor: Druck PDCR 1830 (submersible pressure transducer)
    - Time period: Every 15 minutes 01/04/2008–30/09/2014
    - Data: Stage (mAOD) and sensor location
  - River stage at four stilling wells
    - Sensor: SWS Mini-Diver with internal logger; Baro-Diver for atmospheric correction
    - Time period: Varied per well (2011–2014)
    - Data: Stage (mAOD) and sensor location
    - Data corrected for atmospheric pressure; 15-minute intervals

- Modeling and time-series development
  - River discharge at Shaw (QShaw)
    - Based on Environment Agency hydrometric station data (Station 39019), Shaw, SU470682
  - Bypass discharge (QBypass)
    - Relationship to Shaw discharge under investigation; region-specific piecewise equations (based on observed data 23/10/2013–01/10/2014)
  - Total Shaw discharge (QTotalShaw)
    - QTotalShaw = QShaw + QBypass
  - Boxford discharge (QBoxford)
    - Derived from Boxford measurements downstream of the WQS and total Shaw discharge with a 5-hour lag: QBoxford_t = 0.689332 × (QTotalShaw_t+5) − 0.062936
  - Leat discharge at Boxford (QLeat)
    - Derived from Leat inlet measurements (May 2012–Oct 2014) and Boxford WQS stage (H_WQS)
    - Conditional equation: if H_WQS < 0.61 m, QLeat = 0; if H_WQS > 0.61 m, QLeat = 2.072142×(H_WQS−90.134)^2 − 2.519545×(H_WQS−90.134) + 0.770414
    - Bed elevation at WQS used (90.134 m)
  - Boxford discharge and Leat discharge are linked to the WC Boxford site via observed relationships and staged conditions

- Data integration and outputs
  - Multiple independent measurement techniques are used to derive consistent time-series for river and leet discharges.
  - The modeling framework integrates observed discharges (Shaw, Boxford, Leat) with bypass effects to produce coherent flow time-series for the study area.
  - The dataset supports hydrological interpretation, flow routing, and impact assessment of weed management and infrastructure (weir and bypass).

- Key references
  - Old et al. (2014) on instream and riparian implications of weed cutting in chalk rivers
  - Rameshwaran et al. (2014) on modeling river flow responses to weed management

- Practical implications for data leaders
  - Demonstrates an integrated data system combining field measurements, stage data, and modeled discharge estimates.
  - Highlights the importance of cross-validating data from ECM, ADCP, stage boards, and pressure sensors to produce robust time-series.
  - Illustrates how external factors (weed management, bypass infrastructure) are incorporated into data models with explicit relationships and lag considerations.
  - Emphasizes metadata, data provenance, and the need for clear documentation of measurement methods, periods, sensor deployments, and assumptions for transparency and reuse.