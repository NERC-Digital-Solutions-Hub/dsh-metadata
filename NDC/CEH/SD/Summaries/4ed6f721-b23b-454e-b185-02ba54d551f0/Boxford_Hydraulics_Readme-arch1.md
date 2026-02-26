# CEH River Lambourn Observatory at Boxford (River and Leat)

- Purpose: Document hydraulic data collection and modeling to understand river-leat dynamics and the impact of weed management on water levels, enabling data-driven predictions of discharges at Boxford and Shaw.

## Location
- CEH River Lambourn Observatory located at Boxford in OSGB 1936 coordinates:
  - North: 172280.373767
  - South: 171747.766452
  - East: 443036.218289
  - West: 442689.348845

## Weed management
- Weed cutting drives water level control in the River Lambourn at Boxford.
- Between one and three cuts per year, depending on weed growth and river flow.
- Cut dates (2008–2014): 09/07/2008; 20/05/2009; 05/05/2010; 06/07/2010; 18/11/2010; 18/05/2011; 23/05/2012; 13/11/2012; 01/05/2013; 17/07/2013; 21/05/2014; 23/07/2014.

## Data collection
- A range of hydraulics data were collected at Boxford (various locations and instruments). Data collection locations are shown in accompanying figures.

### 4.1 River flow gauging (ECM)
- Period: ~monthly, 08/07/2008–25/08/2010.
- Data: Stage (mAOD), Discharge (m3/s), cross-section (Easting, Northing, mAOD).
- Velocities: primary velocities measured at vertical profiles across the channel; six measurements per profile (Bed, 0.8D, 0.6D, 0.4D, 0.2D, Surface).
- Discharge: depth-averaged velocity VD = 0.1*(Vsurface + 2V0.2 + 2V0.4 + 2V0.6 + 2V0.8 + Vbed).

### 4.2 Leat flow gauging (ECM)
- Period: ~monthly; Cross-section 1 (Inlet): 22/05/2012–04/08/2014; Cross-section 2 (downstream of wetland weir): 22/05/2012–23/04/2014.
- Data: Stage, Discharge, cross-sections.
- Velocities: 0.6D depth for verticals; discharge from 0.6D velocity.

### 4.3 River flow gauging (ADCP)
- Period: ~monthly; 19/05/2009–04/08/2014.
- Data: Stage, Discharge, cross-section (Easting, Northing, mAOD).
- Method: Measurements from a fully functional cableway.

### 4.4 River stage boards
- Period: ~monthly; 10/11/2009–04/08/2014.
- Data: Stage (mAOD) at 11 locations (Easting, Northing).

### 4.5 Leat stage boards
- Period: ~monthly; 03/05/2012–04/08/2014.
- Data: Stage (mAOD) at 6 locations (Easting, Northing).

### 4.6 River stage at water quality station (WQS)
- Period: every 15 minutes, 01/04/2008–30/09/2014.
- Instrument: Druck PDCR 1830 submersible transducer connected to Campbell Scientific CR1000 with GRPS.
- Data: Stage (mAOD) and sensor location.

### 4.7 River stage at stilling wells
- Four stilling wells using SWS Mini-Diver sensors with internal dataloggers; barometric correction via Baro-Diver.
- Periods varied by well; time series logged every 15 minutes.
- Data: Stage (mAOD) and sensor locations.

## Modelled time series: river and leet discharges at Boxford (01/04/2008–30/09/2014)
- River discharges at Boxford are derived from relationships between Boxford ADCP measurements (monthly, 19/05/2009–01/10/2014) and total Shaw discharges.

### 5.1 River discharge at Shaw (QShaw)
- Shaw discharge time series (QShaw) sourced from Environment Agency Thames Region Hydrometric Station 39019 (NGR SU470682).

### 5.2 Bypass discharge (QBypass)
- An EA-maintained drainage ditch bypassing Shaw weir; CEH developed relationships to QShaw (23/10/2013–01/10/2014).
- Piecewise relationships:
  - Region 1 (QShaw < 4.25 m3/s): QBypass = 0.006808 × (QShaw)^2 + 0.05754 × QShaw
  - Region 2 (4.25 ≤ QShaw ≤ 5.00 m3/s): QBypass = (QShaw − 4.25) × 0.40978 + 0.36759
  - Region 3 (QShaw > 5.00 m3/s): QBypass = νPasses (the equation appears truncated/unclear in the text)
- Figure 9 (not reproduced here) shows the relationships between QBypass and QShaw.

### 5.3 Total River discharge at Shaw (QTotalShaw)
- QTotalShaw = QShaw + QBypass

### 5.4 Time series Boxford discharges (QBoxford)
- QBoxford(t) = 0.689332 × QTotalShaw(t+5) − 0.062936
- Explanation: QBoxford is derived from a linear relationship with QTotalShaw, with a 5-hour lag (observed travel time of flow/sediment peaks between Shaw and Boxford).

### 5.5 Time series Leat discharges at Boxford (QLeat)
- QLeat is derived from Leat inlet measurements (22/05/2012–01/10/2014) and Boxford stage above Ordnance Datum at WQS (HWQS).
- If HWQS ≤ 0.61 m: QLeat = 0
- If HWQS > 0.61 m: 
  QLeat = 2.072142 × (HWQS − 90.134)^2 − 2.519545 × (HWQS − 90.134) + 0.770414
- Note: 90.134 m is the bed elevation above Ordnance Datum at the WQS.

## References
- Old, G.H. et al. (2014). Instream and riparian implications of weed cutting in a chalk river. Ecological Engineering, 71, 290-300.
- Rameshwaran, P. et al. (2014). Modelling river flow responses to weed management. In River Flow 2014, CRC Press, 467-474.