# Files

- 8 raingauges provide hourly rainfall data for Jakarta metropolitan area from 20/01/2007 00:00 to 08/02/2007 23:00
  - Gauges: SRS682 Depok, SRS779 Pondok, BMKG3 Curug, BMKG4 Tg.Priuk, BMKG5 Jakarta_BMKG, BMKG6 Halim, BMKG7 Cengkareng, BMKG9 Dermaga
  - Units: mm/hr
  - Structure: CSV with one column per gauge; header line
  - Quality control: hourly and daily totals checked for inconsistencies and spurious values
  - Purpose: Jakarta_BMKG rainfall used to disaggregate daily rainfall at other locations
  - Location data: includes coordinates (Long, Lat) for each gauge

- 7 location river inflows (hourly modelled data) into the Jakarta metropolitan area from 20/01/2007 00:00 to 08/02/2007 23:00
  - Locations: Cisande, Ciliwung, Kalibekasi1, Kalibekasi2, Kalibekasi3, Kalibekasi4, Kalibekasi5
  - Coordinates: Long, Lat for each site
  - Units: River Flow in m3/s
  - Structure: CSV with a column per discharge point; header line
  - Quality control: produced by calibrated Shetran hydrological model
  - Experimental design: 3 catchments modelled; inflows feed into Jakarta area
  - Calibration: daily discharge for Cisande at Batubela (2003); hourly discharge for Ciliwung at Katulampa (2002–2005, 2007–2008); Kalibekasi uses same parameters as Ciliwung
  - Fieldwork/Instrumentation: model output

- Jakarta-Jan-Feb2007_max_water_depth.tiff
  - Nature and units: Water Depths (meters) from model output
  - Quality control: CityCAT hydrodynamic model output showing maximum depth per grid cell
  - Spatial resolution: 30 m x 30 m grid (grid squares)
  - Data structure: Georeferenced TIFF
  - Experimental design: CityCAT model for Jakarta; uses aw3d30 DEM; OpenStreetMap river network burned into DEM; rainfall and lateral inflows from the other files; no buildings included
  - Calibration/validation: model validated against measured numbers of people displaced and damage caused by the flood
  - Fieldwork/Instrumentation: model output
  - Analytical methods: included as information useful to interpretation of the data