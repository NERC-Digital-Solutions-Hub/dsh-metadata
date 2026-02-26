# Ebullition dataset (5 files), details as follows:

## Overview
- Dataset documenting methane fluxes in two lowland peatland fens (Strumpshaw and Sutton) for the year 2013.
- Contains four Excel spreadsheets with data related to methane fluxes, plus a related data/documentation package (5 files in total).
- Aimed at enabling analysis of ebullition and chamber fluxes, and the factors controlling them.

## Data files and structure
- Ebullition flux spreadsheet
  - Methane ebullition flux measurements (mg CH4 m-2 h-1)
  - Component parts: methane concentration (ppmv) and bubble volume flux (ml m-2 h-1)
  - Method: calculated ebullition flux using inverted funnels
- Chamber flux spreadsheet
  - Chamber methane fluxes (mg CH4 m-2 h-1) measured with static chambers
  - Measurements span both fens throughout 2013
  - NA indicates missing data
- Controlling factors spreadsheet
  - Mean, standard deviation, and slope of water level (cm) during funnel deployment
  - Mean and standard deviation of net radiation (W m-2)
  - Mean, standard deviation, and slope of air pressure (cm)
  - Vascular Green Area (dimensionless) of adjacent quadrats
- Environmental variables spreadsheet
  - Hourly measurements of soil temperature (°C), air pressure (cm), and water table depth (cm)
- Additional contextual/QA notes
  - Fieldwork instrumentation and QA details, calibration procedures, and references

## Measurement methods and quality assurance
- Field protocols from Defra SP1210 (Lowland Peatland Systems in England and Wales)
- Flux measurements
  - Ebullition: twelve inverted glass funnels per site
  - Chamber fluxes: six tall static chambers per site (capture diffusion, plant-mediated transport, ebullition)
- Site and sampling
  - Area: 0.04 km² per site
  - Vegetation: Phragmites australis-dominated
  - Automatic weather station (MiniMet) and Levelogger pressure transducers in dipwells for water level
  - Manual dips monthly to calibrate pressure data
  - Vascular Green Area monitored non-destructively within chamber collars
- Laboratory analysis
  - Gas chromatography with flame ionization detector (FID) for methane and carbon dioxide
  - Regular instrument calibration with certified gases
  - Precision: ~6% for CO2 and ~7% for CH4 (relative standard deviation)
- Supporting references
  - Wilson et al. 2007 (green area index methodology)
  - Stanley 2015 PhD thesis detailing impacts of nutrient loading on greenhouse gas exchange

## Temporal and spatial scope
- Locations: Strumpshaw and Sutton Fens ( coordinates provided )
- Timeframe: 2013
  - Ebullition flux data: Julian Day 72 to 245
  - Chamber flux data: Julian Day 17 to 313
  - Controlling factors: Julian Day 17 to 213
  - Environmental variables: Julian Day 91 to 243

## Variables and data descriptions
- Ebullition flux (mg CH4 m-2 h-1)
  - Includes methane concentration (ppmv) and bubble volume flux (ml m-2 h-1) for flux computation
- Chamber flux (mg CH4 m-2 h-1)
- Controlling factors
  - Water level metrics, net radiation, soil temperature, air pressure, Vascular Green Area
- Environmental variables
  - Hourly soil temperature (°C), air pressure (cm), water level relative to ground (cm)
- Data quality notes
  - NA values indicate missing measurements
  - Data are designed to support analyses of drivers of methane fluxes and ebullition dynamics

## Access, references, and contact
- Primary contact for dataset queries: Kate Heppell (c.m.heppell@qmul.ac.uk)
- Associated references: Wilson et al. (2007); Stanley (2015 PhD thesis) available at the provided QMUL link