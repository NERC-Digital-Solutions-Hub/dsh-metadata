# Growing season methane and nitrous oxide static chamber fluxes from Sodankylä region, Northern Finland - Supporting Documentation

## Overview
- Purpose: quantify growing season CH4 and N2O fluxes using static chambers in forest and wetland ecosystems near Sodankylä, Northern Finland.
- Campaigns: two measurement periods in 2012 (Summer: July 12–Aug 2; Autumn: Sept 22–Oct 14).
- Setup: 60 static chambers (21 forest, 39 wetland) across plots to capture variability due to enclosure treatment and vegetation/water table differences.
- Output focus: fluxes (CH4 and N2O), coupled with environmental variables and substrate indicators.

## Site Description
- Location: Arctic Research Centre of Sodankylä (67°22'N, 26°39'E), ~100 km north of the Arctic Circle; sub-arctic/boreal vegetation zone.
- Ecosystems: Scots pine forest (UVET type) on sandy podzol, versus a eutrophic flark fen wetland with Sphagnum, sedges, and Betula spp.
- Environments sampled: three forest plots with varying grazing enclosure histories; a wetland with diverse vegetation and water table depths.
- Measurements aimed to capture spatial variability in emissions due to substrate and hydrology.

## Experimental Design
- Chamber allocation: 60 total chambers (forest: 21; wetland: 39).
  - Forest: distributed across three subplots representing no enclosure, 12-year enclosure (established 2000), and ~50-year enclosure.
  - Wetland: positioned to cover the range of vegetation communities and water table depths.
- Sampling frequency: approximately every 2 days.
  - Summer campaign: 10 measurements per chamber overall.
  - Autumn campaign: forest and wetland measurements distributed to reflect seasonal conditions.
- Enclosures: purpose-built to exclude grazing animals and create variation in vegetation/lichen cover impacts.

## Methods

### Chamber Design and Deployment
- Chambers: 40 cm diameter opaque polypropylene pipes; shallow bases (10 cm) installed the day before first sampling and left in place.
- Lids: 25 cm PP sections with metal top and pressure compensation plug, sealed during 45-minute flux measurements.
- Gas sampling: air drawn 4 times during the 45-minute period; collected in 20 mL glass vials, then analyzed later in the lab.
- Ancillary measurements: soil temperature (10 cm depth) at four replicate forest points; forest soil moisture via four VMC measurements near chamber bases; wetland water table via 21 dip wells near/between chamber bases.
- Other measurements: soil respiration near forest chambers and a subset of wetland chambers; vegetation recorded upon visual inspection.
- Substrate probes: paired cation/anion Plant Root Simulator (PRS) probes deployed adjacent to each chamber during both campaigns; deployment and recovery dates recorded.

### Field Equipment
- Gas analysis: HP5890 Series II GC with electron capture detector (CH4) and flame ionisation detector (N2O).
  - CH4 detection limit: <70 μg L-1; N2O detection limit: <7 μg L-1.
- In-situ measurements: Omega HH370 soil temperature probe; Theta probe HH2 for soil moisture; PP-Systems SCR-1 IRGA for soil respiration.
- PRS probes: provided by Western Ag Innovations Inc., Canada.

## Calibration, Validation, and Quality Control
- GC calibration: 4-point calibration with standards run approximately every 20 samples.
  - CH4 standards: 1.26, 1.83, 5.16, 101.1 ppmv.
  - N2O standards: 0.1995, 0.285, 0.490, 0.975 ppmv.
- Flux estimation and QC: fluxes calculated with GCFlux version 2, which selects the best-fit model among multiple options for each chamber set; CH4 fluxes use best-fit model (linear or asymptotic). N2O fluxes rely on the linear model due to higher uncertainty near detection limits.
- Reported units: instantaneous fluxes as nanomoles per square meter per second (nmol m^-2 s^-1).
- Data corrections: PRS-derived data corrected for deployment length; standard analytical processing followed for gas concentrations.

## Data Structure, Values, and Units
- Date_Time: dd/mm/yyyy hh:mm local time
- Chamber_number: unique chamber identifier
- CH4 Flux: nmol m^-2 s^-1
- N2O Flux: nmol m^-2 s^-1
- Soil Temperature: °C
- WaterTableDepth: cm
- SoilMoisture: %
- Soil Respiration: g m^-2 h^-1

## Location Details for Chambers
- Forest chambers: distributed across multiple coordinates (latitude ~67.36–67.37, longitude ~26.63–26.64), numbered 1–21 with specific positions catalogued.
- Wetland chambers: distributed across coordinates around latitude ~67.37, longitude ~26.64–26.65, numbered 54–60 in the dataset, covering 54–60 and related entries for wetland locations.
- The dataset includes detailed coordinates for each chamber to capture spatial variability in flux measurements.

## References
- Clough, T. J. et al. (2015). Chamber Design. In Nitrous Oxide Chamber Methodology Guidelines.
- Levy, P. E. et al. (2011). Quantification of uncertainty in trace gas fluxes measured by the static chamber method. European Journal of Soil Science.