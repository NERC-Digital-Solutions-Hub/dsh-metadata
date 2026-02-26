# IMOGEN: dataset of energy balance model parameters and pattern changes for CMIP3 GCMs

- Purpose and use
  - Represents parameters used in the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system.
  - Used to test new land surface parameterisation before implementing in a full GCM and to make projections for future emission scenarios beyond existing GCM runs.
  - IMOGEN uses pattern-scaling to emulate GCMs, linking local monthly climate changes linearly to global warming; employs an Energy Balance Model (EBM) to relate radiative forcing to land warming, with oceanic delays.

- Data scope and calibration
  - EBM has five parameters per GCM: climate sensitivity over land (λ_l) and ocean (λ_o), ocean effective thermal diffusivity (κ), a constant SST warming ratio (ν), and ocean fraction (f).
  - Calibrated against 22 GCMs from CMIP3; parameters λ_l, λ_o, κ, ν, f are provided for each GCM.
  - Local and monthly pattern data (changes per degree of global warming) are available for download in ASCII format.

- Data structure and content
  - For each GCM, a directory named pattRelPR_d2_<GCM> exists (22 directories total).
  - Within each directory, monthly ASCII files jan…dec cover patterns re-mapped to a common grid (2.5° x 3.75°, original HadCM3 grid) with 1631 land points.
  - Each file starts with a header, followed by 1631 land-point records containing:
    - Longitude, latitude
    - Temperature change per degree warming (Kelvin per Kelvin)
    - Relative humidity change per degree warming
    - Wind change per degree warming
    - Longwave change per degree warming
    - Shortwave change per degree warming
    - Precipitation change per degree warming
    - Pressure change per degree warming
    - Several unused columns
  - IMOGEN is routinely coupled to the JULES land surface model; examples are documented in supporting literature.

- Quality control and future development
  - Data are part of a beta programme to extend IMOGEN EBM and pattern parameterisation beyond CMIP3.
  - Work is underway to develop a version emulating CMIP5 GCMs, with full traceability and alignment to UK ISO standards.

- Acknowledgement and references
  - Acknowledges CMIP3 data providers (PCMDI, WGCM) and the WCRP; supported by the U.S. Department of Energy.
  - Key references include IMOGEN, JULES, and related pattern scaling and climate modelling literature.