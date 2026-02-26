# Growing season methane and nitrous oxide static chamber fluxes from Sodankylä region, Northern Finland - Supporting Documentation

## Purpose and scope
- Document methods and data structure for measuring methane (CH4) and nitrous oxide (N2O) fluxes using static chambers in forest and wetland environments during the 2012 growing season.
- Supports standardized analysis of GHG fluxes, data quality, and environmental context.

## Site Description
- Arctic Research Centre of Sodankylä (67°22'N 26°39'E; 179 m a.s.l.) in central Lapland, Finland; part of Pallas-Sodankylä GAW and a level 1 ICOS ecosystem station.
- Ecosystem context: sub-arctic/boreal vegetation with Scots pine forests and wetlands.
- Forest: UVET-type Scots pine on sandy podzol; mean vegetation height ~12 m; stand age 60–100 years; density ~2100 ha⁻¹.
- Wetland: Halssiaapa fen with eutrophic conditions; diverse sedges, mosses, and sparse birch vegetation.

## Experimental Design and Sampling Regime
- Two measurement campaigns during growing season 2012: Summer (12 Jul–2 Aug) and Autumn (22 Sep–14 Oct).
- 60 static chambers total: 21 forest, 39 wetland.
  - Forest: 7 chambers per subplot across three subplots (no enclosure, 12-year enclosure, ~50-year enclosure).
  - Wetland: chambers distributed to cover vegetation and water-table variability.
- Sampling cadence: flux measurements approximately every 2 days.
  - Summer: 10 measurements per chamber overall.
  - Autumn: 7 forest and 8 wetland measurements.

## Collection Methods
- Static chambers: 40 cm diameter opaque polypropylene with shallow 10 cm bases; lids sealed during ~45-minute flux measurement period.
- Gas sampling: 4 air samples per chamber during the 45-minute period, stored in 20 mL glass vials, analyzed later.
- Ancillary measurements:
  - Soil temperature at 10 cm depth (four replicate points outside chamber bases).
  - Forest VMC (4 replicates) adjacent to chamber bases.
  - Wetland: 21 dip wells near chambers for water-table assessment.
  - Soil respiration measured adjacent to forest chambers and to 14 wetland chambers.
  - Vegetation recorded in each chamber.
  - Plant Root Simulator (PRS) probes deployed next to each chamber base; deployed on-specific dates and recovered after deployment.
- Sample processing: PRS probes processed by Western Ag Innovations; vials analyzed in Edinburgh, UK.

## Fieldwork and Laboratory Instrumentation
- Gas analysis: HP5890/Agilent GC with electron capture detector for N2O and flame ionisation detector for CH4.
- Detection limits: CH4 < 70 μg L⁻¹; N2O < 7 μg L⁻¹.
- In-situ measurements: soil temperature (Omega HH370), soil moisture (Theta probe HH2), soil respiration (PP-Systems SCR-1 IRGA setup).
- PRS probes provided by Western Ag Innovations.

## Calibration, Standards, and Quality Control
- GC calibration: four-point calibration with standards for CH4 and N2O, run roughly every 20 samples.
- Standards:
  - CH4: 1.26, 1.83, 5.16, 101.1 ppmv
  - N2O: 0.1995, 0.285, 0.490, 0.975 ppmv
- Flux calculation: GCFlux v2; selects best-fit model per chamber (linear or asymptotic) for CH4; N2O fluxes derived from the linear model due to higher uncertainty near detection limits.
- Units: instantaneous fluxes reported as nmol m⁻² s⁻¹.

## Data Structure, Values, and Units
- Date_Time: dd/mm/yyyy hh:mm (local time)
- Chamber_number: unique identifier for each chamber
- CH4 Flux: nmol m⁻² s⁻¹
- N2O Flux: nmol m⁻² s⁻¹
- Soil Temperature: °C
- WaterTableDepth: cm
- SoilMoisture: %
- Soil Respiration: g m⁻² h⁻¹

## Location Details (Table 2)
- Forest chambers: multiple coordinates in longitude/latitude (examples provided for chambers 1–21)
- Wetland chambers: coordinates provided for chambers 54–60 and 1–53, with associated longitudes/latitudes
- Data include precise chamber geolocations to capture spatial variability in fluxes

## References
- Clough, T. J. et al. Chamber Design. In: Nitrous Oxide Chamber Methodology Guidelines, 2015.
- Levy, P.E. et al. Quantification of uncertainty in trace gas fluxes measured by the static chamber method, Eur. J. Soil Sci., 2011.

## Notes for Analysts
- CH4 fluxes use the best-fit model per chamber; N2O fluxes rely on the linear model due to detection-limit uncertainties.
- Data are structured for integration with standard monitoring workflows and portal uploads where applicable.