# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a commercial Miscanthus x. giganteus plantation, Lincolnshire, UK, 2008 to 2013 Ross Morrison, Emily Clark, Milo Brooks, Jonathan G. Evans, Jon Finch, Colin Lloyd, Rebecca Rowe, Helen C. Ward & Niall P. McNamara

- Purpose and scope
  - Time series of surface-atmosphere exchanges for net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured at a commercial Miscanthus plantation in Lincolnshire, UK.
  - Turbulent fluxes derived with eddy covariance (EC) technique from 2008-05-01 00:30 to 2013-02-18 00:00.
  - Includes ancillary weather and soil physics observations and turbulence characteristics.

- Study site and environment
  - Location: 11.5 ha Miscanthus x. giganteus plantation, ~10 km north of Lincoln, UK (53°19'10.07"N, 0°35'18.65"W).
  - Climate: temperate maritime; mean annual air temperature ~9.8°C and precipitation ~614 mm (1981–2010 baseline).
  - Soils: Beccles 1 association; fine loams, seasonally waterlogged; detailed soil properties (bulk density, texture, soil organic carbon and nitrogen, pH).
  - Management history: established spring 2006 on former arable land; planting density ~10,000 rhizomes ha⁻¹; partial replants in 2007; no fertilizer until 2010 (Fibrefoss 660 kg ha⁻¹); annual spring harvests from 2008 onward.

- Data collection and instrumentation
  - Flux measurements: open-path EC system on a retractable mast; fluxes measured at ≈2× canopy height; 20 Hz sampling; 30-minute block averages.
  - Instruments: LI-7500 CO2 analyser; Mk4 Hydra sonic anemometer-thermometer.
  - Ancillary meteorology and soil observations: air temperature (Ta), relative humidity (RH), net radiation (Rnet) and components (SWin/SWout, LWin/LWout), total incoming shortwave (SWin_total) and diffuse components, below-canopy PPFD (PPFDbc), soil heat flux (G), volumetric water content (VWC), soil temperature (Tsoil), logged with CR10 dataloggers.
  - Data processing: EddyPRO v6.1; QC and correction steps applied to raw 20 Hz data to produce 30-min flux estimates.

- Quality control and data processing
  - QC procedures: removal of statistical outliers (median absolute deviation), EddyPRO quality flags, and flux ranges (-200 to 400 W m⁻² for H, -100 to 500 W m⁻² for LE, -70 to 35 μmol CO₂ m⁻² s⁻¹ for NEE).
  - Footprint assessment: fluxes retained if >75% originated from the target ecosystem (using ART Footprint Tool).
  - Additional checks: weekly visual review of flux and ancillary data; manual removal of clear errors.
  - Flux corrections: include angle-of-attack correction, 2D coordinate rotation, spectral attenuation corrections, humidity-related corrections, and density effect corrections (Webb et al. 1980); random uncertainties computed per Finkelstein & Sims (2001).

- Gap-filling and flux partitioning
  - Gap-filling: Marginal Distribution Sampling (Reichstein et al. 2005) for NEE, LE, and H.
  - NEE partitioning: partitioned into gross primary production (GEP) and total ecosystem respiration (TER) using Reichstein et al. 2005 framework driven by Ta.
  - Tools: REddyProc package in R (2016) for gap-filling and partitioning.

- Data structure and content
  - Output: a single CSV file with time-aligned 30-minute observations from 2008-05-01 00:30 to 2013-02-18 00:00; missing data marked as -9999.
  - Variables and format: Table-based description with two-part series (raw and gap-filled/partitioned) for key metrics:
    - NEE, NEE_unc, NEE_filled, NEE_filled_sd
    - LE, LE_unc, LE_filled, LE_filled_sd
    - H, H_unc, H_filled, H_filled_sd
    - Tau, Tau_unc
    - CO2_strg, Pa, Ta, RH, VPD
    - SWin, SWout, LWin, LWout, Rnet, SWin_total, SWin_diffuse
    - PPFDbc1/2/3, G1/2, Tsoil1/2, VWC1/2, Windspeed1/2, Winddir1/2
    - FootprintFraction1/2, Ustar1/2, TKE1/2, L1/2, zL1/2
  - Time reference: timestamps are in GMT (UTC); end of each 30-minute averaging period.
  - Data coverage notes: includes gap-filled and partitioned flux estimates alongside original observations and uncertainties.

- Data provenance and references
  - Data collection funded by NERC CarboBiocrop and CEH Integrating Fund; authors acknowledge landowners.
  - Key methodological references for EC processing, QC, gap-filling, and partitioning cited (e.g., Mauder et al., Reichstein et al., Moncrieff et al., Webb et al., Foken et al., etc.).

- Practical notes for analysts
  - When using the dataset, distinguish raw flux values (NEE, LE, H) from gap-filled products (NEE_filled, LE_filled, H_filled) and partitioned components (GEP, TER).
  - Respect the QC flags, flux ranges, and footprint criteria to ensure data representativeness.
  - Integrate ancillary variables (Ta, RH, radiation components, soil moisture/temperature) for contextual analyses and model inputs.
  - Consider the site-specific management and climatic context (fertilization in 2010, annual harvests) when interpreting carbon and energy flux dynamics.