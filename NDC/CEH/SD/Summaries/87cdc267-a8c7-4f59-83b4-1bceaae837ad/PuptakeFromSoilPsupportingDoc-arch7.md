# Plant tissue 33 P (radio-isotope P) content from a 33 P tracer study to determine the uptake of P by seven different grassland plant species from three different P chemical forms in soil.

## Overview
- Objective: determine uptake of 33P from three P sources by seven grassland species to assess potential niche differentiation in P resource use.
- Location: Arthur Willis Environment Centre, Department of Animal and Plant Sciences, University of Sheffield, UK.
- Timeframe: Experimental work in 2010; plant survey data collected in 2011 at Wardlow Hay Cop, Peak District National Park.
- Responsible party: Gareth K Phoenix, University of Sheffield.
- Completeness: Dataset is complete except for a small number of missing data points due to contamination and removal from analysis.

## Experimental design
- Plant communities: monocultures of seven species or a 7-species mix (Agrostis capillaris, Festuca ovina, Carex flacca, Carex caryophyllea, Lotus corniculatus, Plantago lanceolata, Rumex acetosa).
- Growth conditions: 1 L pots filled with natural limestone grassland soil; plants grown for 30 weeks in a climate-controlled greenhouse (day/night 18°C/15°C).
- P sources: three 33P-labelled forms—orthophosphate, DNA, and calcium phosphate.
- Replication: seven replicates for each P-source by community combination.
- Application: 33P solutions injected at 10 points to a depth of 5 cm with slow withdrawal to ensure distribution throughout the soil profile.
- Post-treatment: aboveground biomass harvested six days after injection; tissue sorted by species for mixed communities.

## Data collection and analysis
- Measurement method: 33P content determined by scintillation counting (Packard Tri-carb 3100TR).
- Sample processing: biomass freeze-dried, ground, acid digested, and prepared for liquid scintillation counting.
- Units: 33P content expressed as KBq per gram of dry weight; uptake metrics include % uptake per pot and per gram dry weight.
- Data handling: live vs dead tissue recorded; seven replicates per pot and per species where applicable.

## Data structure and variables
- Four CSV files:
  - PuptakeFromCalciumphosphate
  - PuptakeFromDNA
  - PuptakeFromOrthophosphate
  - WardlowLimestoneSpeciesCover2011
- PuptakeFrom* files (11 columns each):
  - MixMono: Monoculture or mixed-species sample
  - Species: Species code (ACA, FOF, CFC, CCC, LCL, PL, RAR)
  - PotRep: Pot replicate number (pot identity within mix or monoculture)
  - LiveDead: Tissue status (live or dead; L1, L2, D)
  - DryWtg: Dry weight (g)
  - DPMperPot: Disintegrations per minute (decay-corrected)
  - MBqperPot: MBq activity per pot
  - PotBiomassg: Total biomass in pot (live + dead)
  - TotalMBqPerPot: MBq activity of live + dead tissue per pot
  - %UptakePerPot: Percentage of injected 33P taken up by the species in that pot
  - %UptakePerG: Uptake as a percentage per gram of dry weight
- WardlowLimestoneSpeciesCover2011 file (3 columns):
  - Quadrat: Quadrat ID (30 quadrats total)
  - SpecName: Species code/name
  - PercCov: Percentage cover per quadrat (by eye; potential overlap can exceed 100%)

## Spatial and GIS-relevant details
- Quadrat-based survey data enables spatial mapping of species composition at Wardlow limestone site.
- Provided coordinates for Wardlow Hay Cop location allow spatial context and integration with GIS layers.
- Uptake data by species and pot can be linked to species distribution data to explore spatial patterns in P uptake and potential niche differentiation across the study area.

## Provenance and authorship
- Data origin: Plant tissue 33P uptake study using limestone grassland soil and seven-species mixtures/monocultures.
- Principal investigator: Gareth K Phoenix, University of Sheffield.
- Data completeness note: Generally complete; a few missing data points due to contamination and exclusion from analysis.