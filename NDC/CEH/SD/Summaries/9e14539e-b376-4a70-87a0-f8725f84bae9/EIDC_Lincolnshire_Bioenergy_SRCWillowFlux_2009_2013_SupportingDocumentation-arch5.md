# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a short rotation coppice willow ( Salix viminalis ) plantation, Lincolnshire, UK, 20092013

## Overview of dataset
- Time series of surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured at a short rotation coppice willow plantation in Lincolnshire, UK.
- Turbulent fluxes obtained with open-path eddy covariance (EC) over 2009-10-14 to 2013-10-01.
- Dataset includes ancillary weather and soil physics observations, plus variables describing atmospheric turbulence and quality of turbulent flux observations.
- Provided as a single CSV with gap-filled and partitioned flux data; includes both raw (pre-gap-filling) and processed metrics, uncertainties, and metadata.

## Study site
- Location: SRC willow flux site, mature 9.4 ha commercial bioenergy plantation, ~10 km north of Lincoln, UK (coordinates given in document).
- Climate: temperate maritime; mean annual air temperature ~9.8°C and precipitation ~614 mm (1981-2010 baseline).
- Soils: Beccles 1 association; seasonally waterlogged fine loams over Charnmouth Mudstone; bulk density ~1.4 g cm-3; pH ~5.8.
- Land-use history: established on former arable land in 2000; coppiced in 2001; biomass harvests in 2011 and 2013; minimal management otherwise; rainfed (no irrigation).

## Data collection and sampling regime
- Automated measurements of flux, meteorology, and soil physics from 2009-10-14 to 2013-10-01.
- Flux data: EC system on a central mast; measurement height adjusted to ~2x canopy height.
- Instruments: open-path EC system with Mk4 Hydra sonic anemometer-thermometer and LI-7500 CO2 analyzer; data at 20 Hz, logged with a Hydra Mk4 Datalogger.
- Ancillary data: net radiation (Rnet), short/longwave components, below-canopy PPFD, soil heat flux (G), soil volumetric water content (VWC), soil temperature, precipitation, air temperature (Ta), relative humidity (RH).
- Data are logged as 30-minute means; missing data flagged as -9999.

## Flux calculation and ancillary data
- Fluxes computed from raw EC data using EddyPRO v6.1, with:
  - QC of 20 Hz data and various instrument-specific corrections (angle of attack, tilt, high/low-frequency attenuation, density corrections, etc.).
  - 30-minute averaging, and calculations of wind metrics, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), and stability parameter (z/L).
- Ancillary data compiled to accompany flux data for interpretation and analysis.

## Data processing and quality control
- Processing workflow includes:
  - Quality control of raw data, removal of statistical outliers (median absolute deviation) and flux observations flagged with EddyPRO quality flag > 1.
  - Physically plausible ranges for fluxes (H, LE, NEE) applied to filter outliers.
  - Footprint analysis to ensure representativeness within the target ecosystem (retain fluxes with >75% footprint within site).
  - Weekly visual checks of flux and ancillary data; manual removal of clearly erroneous values.
- QC ensures data are suitable for gap-filling and partitioning analyses.

## Gap-filling and flux partitioning
- Gaps in EC data (NEE, LE, H) filled using Marginal Distribution Sampling (MDS) approach.
- NEE partitioned into Gross Ecosystem Production (GEP) and Total Ecosystem Respiration (TER) using partitioning methods following Reichstein et al. (2005).
- Partitioning driven by air temperature (Ta) and implemented with REddyProc in R (v2016).
- Outputs include gap-filled fluxes and partitioned components (NEE_filled, LE_filled, H_filled, NEE_filled_sd, LE_filled_sd, H_filled_sd, TER, GEP, etc.).

## Data structure and variables
- Time series delivered in a single CSV file with columns described in Table 1; time stamps are end of 30-minute periods (UTC).
- Recorded variables (pre-gap-filling) include:
  - NEE, LE, H, Tau and their uncertainties.
  - CO2 storage term, pressure (Pa), air temperature (Ta), relative humidity (RH), VPD.
  - Radiation terms (SW in/out, LW in/out, net radiation), below-canopy PPFD, G (soil heat flux) at two locations.
  - Soil metrics: soil temperature (Tsoil), volumetric water content (VWC) at two locations.
  - Precipitation, windspeed and winddir, footprint fraction, and friction velocity (Ustar).
  - Turbulent metrics: TKE, Temperature scaling (Tstar), Obukhov length (L) and stability parameter (zL).
- Gap-filled and partitioned outputs are provided alongside uncertainties:
  - NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.
- Missing data denoted by -9999.

## Nature and units of recorded values
- DateTime: dd/mm/yyyy HH:MM (GMT/UTC).
- NEE: μmol CO2 m-2 s-1; NEE_unc: μmol CO2 m-2 s-1.
- LE: W m-2; LE_unc: W m-2.
- H: W m-2; H_unc: W m-2.
- Tau: kg m-1 s-2; Tau_unc: kg m-1 s-2.
- CO2 storage term: μmol CO2 m-2 s-1.
- Ta: °C; RH: %; VPD: hPa.
- Radiation: SW in/out, LW in/out, R net in two variants (1,2).
- PPFD: μmol photons m-2 s-1 (below canopy variants).
- G: W m-2; Tsoil: °C; VWC: %; and other meteorological and turbulence metrics (winds, footprints, u*, TKE, L, zL).

## Data availability and usage notes
- Data cover 2009-10-14 to 2013-10-01 with gap-filled and partitioned products provided for analysis.
- Key methodological references and software tools used are documented (EddyPRO, REddyProc, and referenced literature).
- Data include quality flags and uncertainty metrics to support reproducibility and uncertainty assessment.

## Acknowledgments
- Funding and project context described (CarboBiocrop, CEH Integrating Fund).
- Acknowledgment of landowners’ permission for site access.

## References
- Methodologies and related studies referenced for data processing, QC, gap-filling, and partitioning (e.g., Reichstein et al., Moncrieff et al., Mauder et al., Papale et al., etc.).

## Data stewardship considerations (for Data Stewards)
- Metadata completeness: clear documentation of variables, units, time stamps, QC criteria, and processing steps to ensure reproducibility.
- Data provenance: explicit trail from raw 20 Hz data to 30-minute aggregates, QC decisions, gap-filling, and flux partitioning outputs.
- Format and accessibility: single CSV with both raw and processed fields; use of -9999 for missing data; availability of gap-filled products for ready analysis.
- Standards alignment: usage of established software (EddyPRO, REddyProc) and adherence to community-accepted EC processing methods and footprint analyses.
- Update and versioning: note ongoing data revisions or reprocessing should be versioned with clear change logs and references to methods.
- Data licensing and citation: ensure proper citation for data usage and provide references to underlying methodological papers for reproducibility.