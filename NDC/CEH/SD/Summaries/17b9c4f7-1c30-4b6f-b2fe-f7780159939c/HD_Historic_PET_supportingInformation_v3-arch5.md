# Historic Gridded Potential Evapotranspiration (PET) based on temperature-based equation McGuinness-Bordne calibrated for the UK (1891-2015)

## Overview
- 5 km gridded PET dataset for the UK covering 1891–2015.
- Based on the McGuinness-Bordne temperature-based equation calibrated for the UK (calibration period: 1961–1990).
- Daily PET grids (mm/day) and monthly PET grids (mm/month); accompanied by quality metrics grids.
- Data stored in NetCDF4 format on the British National Grid; includes four metric files.

## Context and Projects
- Produced as part of two NERC Drought and Water Scarcity Programme projects: Historic Droughts and IMPETUS.
- IMPETUS (2014–2018) aimed to improve drought forecasting and decision-making; evaluated PET input and modelling methods within drought forecasts.
- Historic Droughts (2014–2018) sought to develop interdisciplinary understanding of past UK droughts to inform management; included the Historic Droughts Inventory for cross-sector understanding and planning.

## Motivation and Need
- PET is a key input for hydrological models to reconstruct past streamflows and forecast future flows (e.g., ESP-based forecasts).
- A long-term PET dataset was needed because Penman-Monteith requires data not readily available for long historical periods; a temperature-based approach was adopted for data availability reasons.

## Data Sources
- Met Office 5 km monthly mean temperature grids:
  - 1910–2011 (UKCP09-based)
  - 2012–2015 (unpublished updates)
  - 1891–1909 (rescued data)
  - Daily temperature series generated from these using piecewise cubic Hermite interpolation (pchip)
- CHESS temperature data (Robinson et al., 2016a) used for calibration and as the best available gridded temperature dataset.
- CHESS PET data (Robinson et al., 2016b; 2017) used as reference (Penman-Monteith-based) for calibration and evaluation.

## Method
- Evaluated multiple PET formulations; selected McGuinness-Bordne (Oudin et al., 2005) with UK-specific calibration (1961–1990) as best for the UK.
- Daily PET grids derived from daily temperatures; monthly PET grids derived by summing daily PET.
- Calibration and validation against CHESS PET (Penman-Monteith) over 1991–2012:
  - Metrics: Nash-Sutcliffe Efficiency (NSE), Mean Absolute Percentage Error (MAPE), correlation, bias ratio, variability ratio (VR), Kling-Gupta Efficiency (KGE).
  - MAPE provided as mean monthly values to indicate uncertainty.
- Data are provided with accompanying performance metric grids to help users assess confidence by location.

## Quality Metrics and Confidence
- Quality assessment metrics accompany both daily and monthly PET grids:
  - NSE, MAPE, correlation, bias ratio, VR, KGE (validated against CHESS-PET).
- Metrics enable users to gauge dataset reliability by region and timescale; MAPE serves as an uncertainty indicator.

## Dataset Format and Structure
- Format: NetCDF4, following CEH gridded dataset conventions.
- Spatial reference: British National Grid.
- Daily grids: 365 or 366 time slices per year; 5 km resolution across the UK.
- Monthly grids: 12 monthly grids per year.
- Accompanying files: four metric NetCDF files (two daily, two monthly) detailing the quality metrics.
- Documentation: derived from Tanguy et al. (2018) and related methodological references.

## Data Governance, Provenance, and Reuse
- Provenance established through calibration against CHESS datasets and explicit calibration period (1961–1990).
- Dataset designed to support reproducibility: detailed methodological description, calibration, and evaluation metrics.
- Joint product from Historic Droughts and IMPETUS projects; data sharing aligned with project outputs and UK hydrological research needs.

## Access, Usage, and Limitations
- Data are stored as NetCDF4 on the UK grid; suitable for hydrological modelling and drought analysis.
- Limitations:
  - PET is derived from a temperature-based method (less data-intensive) and calibrated to UK conditions; accuracy varies by region.
  - Original calibration based on 1961–1990; extrapolation beyond that period relies on temperature inputs and model assumptions.
- Users can use the provided metrics to assess location-specific confidence and uncertainty.

## Acknowledgements and References
- Acknowledges Historic Droughts (NERC grant NE/L01016X/1) and IMPETUS (NERC grant NE/L010267/1).
- References include foundational work on PET methods, calibration datasets (CHESS), and drought forecasting methodology (e.g., Harrigan et al., Kling et al., Monteith, Oudin et al., Perry & Hollis, Robinson et al., Tanguy et al.).