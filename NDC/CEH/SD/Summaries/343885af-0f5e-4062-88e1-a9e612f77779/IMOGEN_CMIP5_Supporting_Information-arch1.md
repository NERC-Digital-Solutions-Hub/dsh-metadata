# IMOGEN dataset: Updated parameters and monthly climatologies used in the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system

- Aim
  - Provide updated energy-balance model (EBM) parameters and monthly climatologies to emulate GCM responses for land areas under climate change.
  - Support testing of new land surface parameterisations before integration into full General Circulation Models (GCMs) and projections for future emission scenarios not yet simulated by GCMs.
  - Use pattern-scaling: local monthly changes scale linearly with global mean temperature increase over land, enabling estimation of land responses from a global warming signal.
  - Link changes in evolving radiative forcing to land warming via an EBM that accounts for oceanic thermal delays.

- Data Description
  - For each GCM in CMIP5 (34 models), IMOGEN calibrates five EBM parameters:
    - λ_land: land climate sensitivity (W m^-2 K^-1)
    - λ_ocean: ocean climate sensitivity (W m^-2 K^-1)
    - ν: constant ratio of mean land and ocean SST warming
    - κ: ocean effective thermal diffusivity (W m^-1 K^-1)
    - f: ocean fraction (unitless), i.e., 1 minus land fraction (including Antarctica)
  - The 5 parameters are provided per GCM/model in Table 1 (34 entries) from CMIP5.
  - IMOGEN is updated from CMIP3-based calibration to CMIP5-based calibration; related work is cited (Comyn-Platt et al. 2018; Zelazowski et al. 2018).

- Data Structure and Access
  - Local monthly patterns are downloadable as ASCII files.
  - For each GCM, a directory named CEN_<Centre>_MOD_<Model> contains monthly files for jan through dec.
  - All GCMs are remapped to a common grid of 2.5° latitude × 3.75° longitude (HadCM3 original grid), yielding 1631 land points.
  - Each monthly file contains:
    - 1) Longitude
    - 2) Latitude
    - 3) Temperature change per degree global warming (K per K)
    - 4) Relative humidity change per degree warming (% change per K)
    - 5) Wind speed change per degree warming (m s^-1 per K)
    - 6) Unused (0.0)
    - 7) Longwave change per degree warming (W m^-2 per K)
    - 8) Shortwave change per degree warming (W m^-2 per K)
    - 9) Unused (0.0)
    - 10) Precipitation change per degree warming (mm day^-1 per K)
    - 11) Unused (0.0)
    - 12) Pressure change per degree warming (hPa per K)
    - 13) Unused (0.0)
  - IMOGEN is routinely coupled to the JULES land surface model (with references to model descriptions).

- Usage and Applications
  - The downloaded local/monthly patterns can be used to:
    - Emulate land-surface responses to different warming scenarios in the context of the IMOGEN framework.
    - Test and compare land surface parameterisations before embedding them in more complex GCMs.
  - The approach enables projection of climate-change impacts on land independent of running full GCMs for each scenario.

- Quality Control and Reproducibility
  - Calibration against CMIP5 models includes full numerical code documentation and traceability on demand.
  - Scripts and workflows rely on open-access software, aligning with ISO standards for numerical model construction.
  - The dataset supports reproducibility and discoverability by providing metadata and structured data products.

- Acknowledgement and References
  - Acknowledges modeling groups, PCMDI, and WGCM for CMIP data; support from the U.S. Department of Energy.
  - Key references include Huntingford et al. (2010), Huntingford and Cox (2000), Best et al. (2011), Clark et al. (2011), and related CMIP3/CMIP5 literature (e.g., Taylor et al. 2012; Meehl et al. 2007; Zelazowski et al. 2018; Comyn-Platt et al. 2018).