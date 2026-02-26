# Growing season methane and nitrous oxide static chamber fluxes from Sodankylä region, Northern Finland - Supporting Documentation

## Overview
- Study of methane (CH4) and nitrous oxide (N2O) fluxes during the growing season 2012 using static chambers at the Sodankylä Arctic Research Centre, Northern Finland.
- Data suitable for GIS-based visualization of spatial and temporal patterns of greenhouse gas fluxes across forest and wetland ecosystems.
- Two campaigns: Summer (12 Jul – 2 Aug 2012) and Autumn (22 Sep – 14 Oct 2012), with measurements approximately every 2 days.

## Study area and geospatial context
- Location: Arctic Research Centre of Sodankylä (67°22'N, 26°39'E; ~179 m a.s.l.), central Lapland, ~100 km north of the Arctic Circle.
- Ecosystems: UVET Scots pine forest on sandy podzol and Halssiaapa eutrophic flark fen wetland.
- Measurement sites: 60 static chambers total (21 forest, 39 wetland) distributed to capture variability in vegetation and hydrology.

## Experimental design and sampling framework
- Forest: Chambers distributed across three subplots (no enclosure, ~12-year enclosure, ~50-year enclosure) to assess grazing exclusion effects.
- Wetland: Chambers positioned to span vegetation communities and water table depths; included dip wells to characterize hydrology.
- Sampling cadence: Approximately every 2 days during each campaign, yielding about 10 summer measurements (across all chambers) and 7 (forest) to 8 (wetland) in autumn.
- Associated measurements: soil temperature, soil moisture, and soil respiration; vegetation recorded per chamber; PRS probes deployed adjacent to each chamber base.

## Measurements, methods, and instruments (data collection)
- Static chamber construction: 40 cm diameter opaque polypropylene chamber bases (10 cm depth) with 25 cm lid and pressure compensation. Gas samples collected at ~45 minutes, 4 draws per chamber.
- Gas analysis: CH4 and N2O concentrations measured with GCFlux (GC with ECD for CH4 and FID for N2O).
- Ancillary sensors: in-situ soil temperature (10 cm depth), soil moisture (Theta probe), soil respiration (PP-Systems chamber with IRGA), and PRS probes for soil nutrient status.
- Calibration: 4-point calibration for CH4 and N2O standards; standards run ~every 20 samples.
- Data products: fluxes reported as instantaneous rates in nmol m^-2 s^-1; concentrations linked to time-stamped, geolocated measurements.

## Data structure and variables (GIS-ready attributes)
- Time and location:
  - Date_Time: dd/mm/yyyy hh:mm local time
  - Chamber_number: unique chamber identifier
  - Location type: Forest or Wetland; forest subplots (enclosure types) noted
  - Coordinates: longitude and latitude provided per chamber (decimal degrees)
- Key variables (per chamber per sampling event):
  - CH4 Flux: nmol m^-2 s^-1
  - N2O Flux: nmol m^-2 s^-1
  - Soil Temperature: °C
  - WaterTableDepth: cm
  - SoilMoisture: %
  - Soil Respiration: g m^-2 h^-1
- Data provenance: measurements linked to specific campaign (Summer or Autumn) and chamber location; PRS probe deployment dates included.

## Data processing, quality control, and analytical methods
- Flux calculation: GCFlux version 2; selects best-fit model per chamber (linear or asymptotic) for CH4; N2O fluxes derived from linear model due to detection limits.
- Uncertainty and QC: standard calibrations; N2O fluxes emphasized from linear model because concentrations near detection limits increase uncertainty.
- Units and reporting: fluxes as nmol m^-2 s^-1; ancillary measurements in standard SI units.

## Spatial and temporal characteristics relevant to GIS
- Spatial: 60 measurement points (forest and wetland) with explicit coordinates for georeferencing; forest chambers spread across three subplots; wetland chambers cover hydrological gradients.
- Temporal: two discrete campaigns in 2012 with repeated measurements; enables analysis of seasonal dynamics and enclosure effects (forest) or vegetation/hydrology interactions (wetland).

## Potential GIS-derived products and applications
- Spatial maps of CH4 and N2O flux distributions across forest and wetland microhabitats.
- Joint maps and analyses of fluxes with soil temperature, moisture, and water table depth to identify drivers.
- Temporal comparisons between summer and autumn fluxes; assessment of enclosure treatment effects in forest plots.
- Linking chamber locations to vegetation and hydrology layers for landscape-scale GHG modelling.

## References and methodological context
- Chamber design and methodology references: Clough et al. 2015; Levy et al. 2011 (uncertainty in static chamber flux measurements).
- Data interpretation context: standard GCFlux approaches and quality-control considerations for trace-gas flux measurements.