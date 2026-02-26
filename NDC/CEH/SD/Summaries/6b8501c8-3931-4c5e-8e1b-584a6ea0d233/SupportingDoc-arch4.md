# Growing season methane and nitrous oxide static chamber fluxes from Sodankylä region, Northern Finland - Supporting Documentation

## Overview
- Document describes a field study of CH4 and N2O fluxes using static chambers in a sub-arctic boreal environment during the 2012 growing season.
- Study sites include a Scots pine forest with enclosure treatments and a nearby eutrophic fen wetland.
- Data collected include gas fluxes (CH4, N2O), soil temperature, soil moisture, water table depth, soil respiration, and vegetation observations, with additional soil solution proxies via PRS probes.
- Fluxes are derived from chamber measurements using GCFlux v2 with model selection (best-fit) per chamber; N2O fluxes rely on linear model due to detection limits.
- Data are structured with precise timing, location, and environmental context to support cross-site comparison and meta-analysis.

## Site Description
- Location: Arctic Research Centre of Sodankylä, central Lapland, Northern Finland (67°22'N, 26°39'E; 179 m a.s.l.), part of the Pallas-Sodankylä GAW station and an ICOS ecosystem station.
- Ecosystems: Dominant Scots pine forest (UVET type) on sandy podzol and a nearby eutrophic flark fen wetland with Sphagnum and sedge communities.
- Forest details: 12 m vegetation height, ~60–100 year stand age, ~2100 trees ha^-1, lichens dependent on reindeer presence.
- Wetland details: Intermittent water table with birch fen vegetation; mixed shrub and herb communities.

## Experimental Design and Sampling Regime
- Duration: Measurements during growing season 2012; two campaigns: Summer (Jul 12–Aug 2) and Autumn (Sep 22–Oct 14).
- Sampling framework: 60 static chambers total (21 forest, 39 wetland).
  - Forest: 7 chambers in each of three subplots (no enclosure, 12-year enclosure, ~50-year enclosure).
  - Wetland: Chambers spread to capture vegetation and water-table variability.
- Temporal cadence: Flux measurements about every 2 days; Summer yielded 10 measurements across all chambers, Autumn yielded 7 forest and 8 wetland chamber measurements.
- Enclosure purpose: Protect forest plots from grazing; enclosure ages represent differing disturbance histories.

## Collection Methods
- Chambers: 40 cm diameter opaque polypropylene, with 10 cm depth bases; lids sealed to bases for ~45 minutes per flux session.
- Sampling: 4 air samples per chamber during each ~45-minute period, collected in 20 mL glass vials.
- Ancillary measurements: Soil temperature at 10 cm depth, four soil moisture replicates per forest chamber base, 21 dip wells for wetlands to monitor water table, and chamber-adjacent soil respiration measurements.
- Vegetation and root zone data: Visual vegetation assessment inside each chamber; paired cation/anion Plant Root Simulator probes deployed near chamber bases (summer and autumn deployments and recoveries).
- Gas handling: Samples analyzed in labs (Edinburgh) for CH4 and N2O concentrations.

## Fieldwork and Laboratory Instrumentation
- Gas analysis: HP5890 Series II GC with electron capture detector for N2O and flame ionisation detector for CH4 (detection limits <7 μg L^-1 for N2O, <70 μg L^-1 for CH4).
- In-situ measurements: Omega HH370 soil temperature probe; Theta probe HH2 for volumetric soil moisture; PP-Systems SCR-1 IRGA for soil respiration.
- Probes: Plant Root Simulator (PRS) probes from Western Ag Innovations.

## Calibration Steps and Values
- Gas concentrations converted using four-point calibration; standards include CH4 and N2O concentrations at multiple levels (detailed values provided in the table, with progressive increases from standard 1 to 4).
- Calibration standards are run roughly every ~20 samples to ensure accuracy.

## Analytical Methods and Quality Control
- Flux calculation: GCFlux version 2, which evaluates five models and selects the best fit for each chamber set (linear or asymptotic for CH4; linear for N2O due to detection limits).
- N2O fluxes: Reported fluxes derived from the linear model due to higher uncertainty near detection limits.
- Units: Instantaneous fluxes reported as nmol m^-2 s^-1.
- Quality considerations: Emphasis on model-fit suitability and recognition of detection-limit limitations for N2O.

## Data Structure, Nature, and Units
- Date_Time: dd/mm/yyyy hh:mm local time
- Chamber_number: Unique identifier for each chamber
- CH4 Flux: nmol m^-2 s^-1
- N2O Flux: nmol m^-2 s^-1
- Soil Temperature: °C
- WaterTableDepth: cm
- SoilMoisture: %
- Soil Respiration: g m^-2 hr^-1

## Location and Chamber Metadata
- Forest chambers organized by subplot location, with explicit longitudinal and latitudinal coordinates for individual chambers (forest and wetland).
- Wetland chambers labeled 54–60 with corresponding coordinates; comprehensive location data included to support spatial analyses.

## Additional References
- Clough et al. 2015: Chamber Methodology Guidelines
- Levy et al. 2011: Quantification of uncertainty in trace gas fluxes measured by the static chamber method