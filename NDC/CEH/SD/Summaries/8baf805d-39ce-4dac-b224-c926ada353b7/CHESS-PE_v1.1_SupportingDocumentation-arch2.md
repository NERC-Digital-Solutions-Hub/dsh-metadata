# Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2015) [CHESS-PE]

## Overview
- Provides two daily potential evapotranspiration (PET) estimates on a 1 km grid over Great Britain for 1961–2015.
- Derived from CHESS-met meteorological variables and CEH-GEAR precipitation; identical time and spatial extent for both PET variables.

## PET and PETI definitions
- PET: Penman–Monteith potential evapotranspiration for a well-watered grass surface (mm/day).
- PETI: PET with interception correction; on days with rainfall, canopy interception is added to evaporation, with transpiration and interception modeled together using a dry-down process.

## Calculation and assumptions
- PET is calculated using the Penman–Monteith equation with inputs Ta, qa, downward longwave and shortwave radiation, and surface pressure.
- PETI uses the same calculation for potential transpiration, plus interception components; interception store capacity and initial store govern the interception term, assuming exponential dry-down.
- Assumptions include a well-watered grass surface and a fixed stomatal resistance (70 s m⁻¹) for PET, with interception effects altering daily evaporation in PETI.

## Input data sources
- CHESS-met: climate/met data for Great Britain (1961–2015).
- CEH-GEAR: daily areal precipitation estimates for the UK, used to scale precipitation for PETI.

## File format and structure
- Format: netCDF, CF-compliant, following CEH gridded dataset conventions.
- Temporal resolution: daily values stored in monthly files.
- Variables: PET and PETI (two separate monthly files, one per variable).

## Relevance for environmental monitoring
- PET represents atmospheric evaporative demand; PETI provides a more hydrologically nuanced estimate by including interception, useful for rainfall-influenced hydrological modelling.
- Standardized, high-resolution dataset supports consistent monitoring of evaporative demand and its role in environmental health and water balance analyses.

## Practical use and data management
- Designed for clear outputs (maps, charts, reports) and integration into data portals; suitable for benchmarking environmental health and policy performance over time.
- Encourages reuse by providing underlying meteorological and precipitation inputs from established, quality-assured sources.

## References and provenance
- Key sources include FAO guidelines (Allen et al., 1998), CHESS-met (Robinson et al., 2015), CEH-GEAR (Keller et al., 2015; Tanguy et al., 2016), Monteith (1965), and related methodological details (Robinson et al., in review).