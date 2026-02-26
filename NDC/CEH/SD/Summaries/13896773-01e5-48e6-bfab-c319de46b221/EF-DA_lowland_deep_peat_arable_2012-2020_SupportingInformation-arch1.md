# Supporting information for: Eddy Covariance measurements of carbon dioxide, energy and water flux at an intensively cultivated lowland deep peat soil, East Anglia, UK, 2012 to 2020.

## Overview of dataset
- Time series of land–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ).
- Fluxes measured with eddy covariance (EC) at an intensively cultivated lowland deep peat site (EF-DA) from 2012-06-22 to 2020-01-01.
- Includes ancillary meteorological and soil-physics observations and turbulence-characterising variables.
- Data provided as gap-filled and partitioned series, with accompanying quality control and processing details.

## Study site and activity
- Location: East Anglian Fens, UK (The Fenland), with US-style lowland peat soils, drained and converted for agriculture post-WWII.
- Site: EF-DA flux site on Rosedene Farm (52°31'N, 0°29'E; ≈0 m amsl).
- Climate: temperate maritime (mean 10.4°C; ~564 mm annual precipitation, 1981–2010 reference).
- Land use: trapezoidal arable fields with hedgerows and ditch systems; crops over the study period included lettuce (2012, 2014, 2016, 2018), leek (2013), celery (2015), sugar beet (2017), potatoes (2019).
- Soil: deeper peat with high bulk density near surface, very low C/N ratio due to drainage and fertiliser history; around 2 m of peat remains.

## Sampling regime
- Automated long-term measurements: flux, meteorological, and soil-physics data from 2012-06-22 to 2020-01-01.
- EC observations above canopy at 1.5 m height; sensors log at 20 Hz and are averaged to 30-minute means.

## Flux data acquisition
- Instruments: LI-7500 open-path IRGA (CO2, H2O) and CSAT3 sonic anemometer; fluxes recorded in south-west wind direction (225°).
- Variables: NEE (μmol CO2 m⁻² s⁻¹), LE (W m⁻²), H (W m⁻²), τ (kg m⁻¹ s⁻²), plus 20 Hz turbulence data and density/CO2/H2O metrics.
- Ancillary flux computations: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability (z/L), and flux footprints.

## Ancillary data acquisition
- Radiometry: net radiation and short/long-wave components (Rnet, Rg) via NRLite2 and CNR4 radiometers (with partial overlaps due to instrument relocations in 2013–2015).
- PAR: photosynthetically active radiation sensor.
- Atmospheric conditions: air temperature (Ta), relative humidity (RH), vapour pressure deficit (VPD), precipitation (ARG100 gauge).
- Soil physics: two arrays of soil instruments measuring soil heat flux (G), soil temperature (Tsoil), and volumetric peat moisture content (VWC) at shallow depths; detailed instrument placements described.
- Data are logged as 30-minute means (or sums for precipitation).

## Data processing
- Flux calculation: EddyPRO v6.1 used for quality-controlled, 30-minute-averaged fluxes; included standard EC corrections (coordinate rotation, spectral corrections, humidity density corrections, and density adjustments for LE and CO2).
- Uncertainty: random uncertainties computed following standard approaches.
- Auxiliary calculations: wind/reframing metrics (u*, TKE, L, z/L), and half-hour flux footprints via Kormann & Meixner model.

## Quality control
- Outlier handling: median absolute deviation criteria; removal of non-stationary turbulence periods.
- Flux range checks: H (-200 to 400 W m⁻²), LE (-200 to 600 W m⁻²), NEE (-40 to 40 μmol CO2 m⁻² s⁻¹).
- Night-time NEE flagged and removed when negative fluxes inconsistent with ecosystem respiration.
- Footprint filter: retain fluxes where ≥70% originates from the target ecosystem (via ART footprint model).
- Semi-manual review: weekly plots of fluxes and ancillary data to catch clearly erroneous values.

## Data gap-filling and flux partitioning
- Gap-filling: Marginal Distribution Sampling (Reichstein et al., 2005).
- Partitioning: NEE divided into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using Ta-driven methods (Reichstein et al., 2005).
- Tools: REddyProc package in R (Reichstein et al., 2016) used for gap-filling and partitioning.

## Details of data structure
- Time series delivered as CSV with ASCII tabular data; missing records denoted by -9999.
- Columns include: NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, and gap-filled/partitioned variants (NEE_filled, NEE_filled_sd, LE_filled, H_filled, etc.), plus meteorological and soil-physics variables (Pa, Ta, RH, VPD, Rnet, Rg, G, Tsoil, VWC, Precipitation, Windspeed, Winddir, FootprintFraction, Ustar, TKE, L, zL, NEE_filled, NEE_filled_sd, GEP, TER, etc.).
- Time reference: DateTime in UTC (yyyy-mm-dd HH:MM:SS).

## Nature and units of recorded values
- Variables described with units and meanings (e.g., NEE in μmol CO2 m⁻² s⁻¹; LE, H in W m⁻²; Pa in kPa/bar; Ta, RH, VPD; G, Tsoil, VWC; FootprintFraction; Ustar; TKE; L; zL; NEE_filled; GEP; TER).

## Acknowledgements
- Site established and funded by NERC Urgency grant NE/K001590/1; ongoing support from NERC studentship NE/L501839 and Defra SP1210 project; SEFLOS and institutional support at University of Leicester.
- Special thanks to landowners J. G. Shropshire & sons and G's Fresh; thanks to Martin Hammond (Rosedene Farm) for access and cooperation.

## References (methods and tools)
- References detailing data processing, QC, and gap-filling methods (e.g., Reichstein et al. 2005, Reichstein et al. 2016; Foken et al. 2004; Papale et al. 2006; Moncrieff et al. 1997, 2004; Mauder et al. 2013; Neftel et al. 2008; Wilczak et al. 2001; Webb et al. 1980; and related EddyPRO and footprint literature).