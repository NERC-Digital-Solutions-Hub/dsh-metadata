# Topsoil carbon concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Addresses soil carbon concentration in the top 0–15 cm as a key indicator of soil health and ecosystem services.
- Provides modelled, 1 km² resolution estimates of topsoil carbon concentration for Great Britain in 2007 using Countryside Survey data.
- Advances previous approaches by incorporating climate, atmospheric deposition, habitat, soil, and spatial variables within a Generalized Additive Mixed Model (GAMM).

## Data inputs and sampling
- Data come from 2,446 sample locations across Great Britain (1 km² survey squares nested in sampling design).
- Soil carbon measured via a core sampling method (15 cm long, 5 cm diameter); Loss-on-ignition (LOI) used to estimate carbon concentration.
- Carbon concentration estimated as LOI × 0.55 (CEH Lancaster UKAS accredited method SOP3102); standardized protocols followed (Emmett et al. 2008, 2010).
- Prior work used broader habitat/parent material predictors; this study uses a more detailed, data-rich modelling approach.

## Modelling approach
- Generalized Additive Mixed Model (GAMM) fitted with a Tweedie distribution (variance power = 1.99) using R package mgcv (gamm).
- Includes a random effect to account for nesting of samples within 1 km² survey squares.
- Non-linear smooths applied to climate and atmospheric deposition variables.
- Two-dimensional tensor product smooths applied to spatial coordinates (latitude/longitude) to capture large-scale spatial variation.
- Model details and approach described in Thomas et al. (2020).

## Variables and model terms (Table 1)
- Climate and deposition predictors (smoothed terms and tensor products):
  - s(5-year mean summer temperature) — 5 km spatial resolution; 2003–2007; Met Office.
  - s(5-year mean summer precipitation) — 5 km; 2003–2007; Met Office.
  - te(Easting, Northing) — 1 km resolution; spatial positioning.
  - s(5-year mean spring temperature) — 5 km; 2003–2007; Met Office.
  - s(3-year mean SO₄ deposition) — 5 km; 2005; CBED.
  - s(5-year mean winter temperature) — 5 km; 2003–2007; Met Office.
  - s(3-year mean NH₄ deposition) — 5 km; 2005; CBED.
  - s(3-year mean NO₃ deposition) — 5 km; 2005; CBED.
- Broad habitat, soil-related and other categorical/derived predictors:
  - Broad Habitat, CACO3 Rank, Soil Group and Soil Parent Material Model (with respective 1 km references or categorical classes).

## Output, data attributes, and tooling
- Data product: CS_topsoil_carbon_gam.nc
- Key variable: Soil_OrgC_Conc — mean topsoil carbon concentration (g kg⁻¹) for 2007 as modelled by GAM.
- VAR — standard error of the estimate divided by the predicted mean (ratio).
- Spatial coordinates: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (EPSG:27700); transverse_mercator mapping defined.
- Purpose of dataset: provide geographically explicit estimates of topsoil carbon to inform soil health assessments and related ecosystem service analyses.

## Sampling, calibration, and quality control
- Method and calibration detailed in Reynolds et al. (2013) and Emmett et al. (2008, 2010) soil manuals.
- LOI-based carbon estimation with a conversion factor of 0.55; laboratory analyses conducted following CEH SOP3102 and UKAS accreditation.
- Quality control aligned with Defra/NERC Joint Codes of Practice.

## Supporting documents and references
- Thomas, A., Cosby, B.J., Henrys, P., Emmett, B. (2020). Patterns and trends of topsoil carbon in the UK: Complex interactions of land use change, climate and pollution. Science of the Total Environment (methodological details for GAMM approach).
- Dore et al. (2015); Emmett et al. (2008, 2010); Henrys et al. (2012); Morton et al. (2014); Reynolds et al. (2013).