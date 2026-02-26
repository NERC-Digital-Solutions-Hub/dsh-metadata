# IMOGEN updated parameters and monthly climatologies

- Purpose and use
  - Represents the updated parameters and monthly climatologies used in the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system.
  - Used to test new land surface parameterisations before implementing in full General Circulation Models (GCMs) and to project future emission scenarios not simulated by the GCMs.
  - Based on pattern-scaling: local monthly changes in meteorology scale linearly with global mean temperature increases to estimate land warming and related climate changes, using an Energy Balance Model (EBM).

- Data scope and lineage
  - Updated dataset based on 34 GCMs from CMIP5 (improved from the CMIP3-based 22 GCMs).
  - Calibrated parameters and monthly climatologies support IMOGEN’s coupling to climate projections and land surface models (JULES).

- EBM calibration parameters (one set per GCM)
  - λ_land: climate sensitivity over land (W m^-2 K^-1)
  - λ_ocean: climate sensitivity over ocean (W m^-2 K^-1)
  - ν: constant ratio of mean land and ocean surface (SST) warming
  - κ: ocean effective thermal diffusivity (W m^-1 K^-1)
  - f: ocean fraction (unitless)

- Data structure and access
  - Local and monthly pattern data are provided as ASCII files.
  - Organization: a directory for each GCM in the form CEN_<Centre>_MOD_<Model>, totaling 34 directories.
  - Within each directory, monthly files named jan, feb, ..., dec.
  - All GCMs are remapped to a common grid: 2.5° latitude by 3.75° longitude (HadCM3 origin), consisting of 1631 land points.
  - Each monthly file contains a header followed by 1631 lines with the following columns:
    1. Longitude
    2. Latitude
    3. Temperature change per degree global warming (K per K)
    4. Relative humidity change per degree global warming (% per K)
    5. Wind change per degree global warming (m s^-1 per K)
    6. Unused (0.0)
    7. Longwave change per degree global warming (W m^-2 per K)
    8. Shortwave change per degree global warming (W m^-2 per K)
    9. Unused (0.0)
    10. Precipitation change per degree global warming (mm d^-1 per K)
    11. Unused (0.0)
    12. Pressure change per degree global warming (hPa per K)
    13. Unused (0.0)

- Grid and data characteristics relevant to GIS
  - Common 2.5° x 3.75° grid facilitates spatial analyses, mapping, and integration with other GIS datasets.
  - 1631 land points per GCM grid cell set enable spatial visualization of climate-pattern responses at local scales.

- Applications and integration
  - IMOGEN is routinely coupled to the JULES land surface model for land-atmosphere interaction studies.
  - Outputs support map-based visualization of pattern-scaled climate responses (temperature, humidity, wind, precipitation, and radiation).

- Quality control and provenance
  - Calibration against CMIP5 models with full numerical documentation and traceability.
  - ISO-standard practices for numerical model development and open-access tooling.
  - Acknowledges CMIP, PCMDI, and WGCM for data and collaboration; support from the U.S. Department of Energy.

- References and further information
  - Foundational papers and data sources related to IMOGEN, pattern-scaling, JULES, and CMIP projects:
    - Huntingford et al. 2010; Huntingford & Cox 2000
    - Best et al. 2011; Clark et al. 2011 (JULES model descriptions)
    - Comyn-Platt et al. 2018; Zelazowski et al. 2016
    - Meehl et al. 2007; Taylor et al. 2012
  - Acknowledgments to CMIP5 data providers and related programs (PCMDI, WGCM, WCRP).