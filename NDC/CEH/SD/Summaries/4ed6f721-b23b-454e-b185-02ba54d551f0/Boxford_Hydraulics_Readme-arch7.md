# CEH River Lambourn Observatory at Boxford (River and Leat)

- A GIS-focused report detailing spatially-referenced hydraulic data collection and time-series modelling for the River Lambourn and Leat at Boxford, including multiple sensing technologies, data fusion approaches, and discharge relationships.

## Spatial Reference and Location

- Observatory located in OSGB 1936 coordinates.
  - North: 172,280.373767
  - South: 171,747.766452
  - East: 443,036.218289
  - West: 442,689.348845
- Data are tied to specific Easting/Northing locations and metres AOD (mAOD) for stage and cross-sections.
- Figure 1 (not included here) shows data collection locations around Boxford.

## Weed Management and Hydrology Context

- River water levels are influenced by aquatic vegetation management with 1–3 cuts per year depending on growth and river flow.
- Weed-cutting dates listed (2008–2014) indicating potential impacts on hydraulic conditions.

## Data Collection Overview

- A range of hydraulics data were collected at Boxford with locations shown in Figure 1.
- Data collection spans varied periods and sampling frequencies across multiple instruments and methods.

### 4.1 River flow gauging (ECM)
- Data period: ~monthly, 08/07/2008–25/08/2010
- Measured: Stage (mAOD), Discharge (m3 s-1), gauged cross-section (E,N,mAOD)
- Approach: depth-averaged velocity from profiles across the channel (six measurements per profile; D = water depth)

### 4.2 Leat flow gauging (ECM)
- Data period: ~monthly; Cross-sections 1 (Inlet) and 2 (downstream of wetland weir)
- Measured: Stage, Discharge, cross-sections (E,N,mAOD)
- Approach: velocities at 0.6D depth; discharge from depth-averaged velocity (VD = VD)

### 4.3 River flow gauging (ADCP)
- Data period: ~monthly, 19/05/2009–04/08/2014
- Measured: Stage, Discharge, cross-section (E,N,mAOD)
- Method: measurements from a fully functional cableway

### 4.4 River stage boards
- Data period: ~monthly, 10/11/2009–04/08/2014
- Measured: Stage (mAOD) and locations (E,N)

### 4.5 Leat stage boards
- Data period: ~monthly, 03/05/2012–04/08/2014
- Measured: Stage (mAOD) and locations (E,N)

### 4.6 River stage at Water Quality Station (WQS)
- Data period: every 15 minutes, 01/04/2008–30/09/2014
- Sensor: Druck PDCR 1830 submersible, connected to CR1000 logger with remote access
- Measured: Stage (mAOD) and sensor location (E,N)

### 4.7 River stage at stilling wells
- Four stilling wells using Mini-Diver non-vented level sensors with internal dataloggers
- Atmospheric pressure correction via Baro-Diver
- Data record: 15-minute intervals, various start/end dates (2011–2014)
- Measured: Stage (mAOD) and sensor locations (E,N)

## Modelling Time Series Discharges (Boxford area, 2008–2014)

- Purpose: derive continuous time-series discharges from discrete field measurements using site relationships with upstream gauges.
- 5.1 Shaw Discharge (QShaw)
  - Based on Environment Agency hydrometric station at Shaw (EA Station 39019, NGR SU470682)
- 5.2 Bypass Discharge (QBypass)
  - EA-supplied bypass discharges; relationships to QShaw developed (three regions with formulae)
- 5.3 Total Shaw Discharge (QTotalShaw)
  - QTotalShaw = QShaw + QBypass
- 5.4 Boxford Discharge (QBoxford)
  - Boxford discharge derived from QTotalShaw with a 5-hour lag: QBoxford_t = 0.689332 × QTotalShaw_(t+5) − 0.062936
  - Based on ADCP measurements downstream of WQS and Shaw total discharge
- 5.5 Leat Discharge (QLeat)
  - Derived from Leat inlet measurements and Boxford H_WQS stage (above Ordnance Datum)
  - Piecewise relationship with threshold: if H_WQS ≤ 0.61 m, QLeat = 0; if H_WQS > 0.61 m, QLeat = 2.072142×(H_WQS−90.134)^2 − 2.519545×(H_WQS−90.134) + 0.770414
  - 90.134 m is bed elevation at WQS

## Data Uses and GIS Implications

- Use of OSGB 1936 and precise Easting/Northing coordinates enables map-based visualization of stages, cross-sections, and discharge relationships.
- Time-series discharges enable hydrological modelling and scenario analysis in map formats (e.g., flow paths, flood extents, peat/weed-management impacts on hydraulics).
- Relationships between sites (Shaw, Boxford, WQS, and the Leat) provide spatial-temporal linkage for integrated river-leat systems.
- High-frequency (15-minute) data at the WQS and multi-source cross-sectional data support dynamic map-based dashboards and decision-support tools.
- The combination of direct measurements (ECM, ADCP, stage boards) with derived discharges supports data fusion, quality assurance, and resolution-matching across datasets.

## References

- Old, G.H. et al. (2014) Instream and riparian implications of weed cutting in a chalk river. Ecological Engineering, 71, 290-300.
- Rameshwaran, P. et al. (2014) Modelling river flow responses to weed management. In River Flow 2014, CRC Press, 467-474.