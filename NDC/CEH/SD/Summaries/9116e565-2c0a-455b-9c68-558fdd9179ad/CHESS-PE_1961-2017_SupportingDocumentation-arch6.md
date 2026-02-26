# Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2017) [CHESS-PE]

- Overview:
  - CHESS-PE provides two daily potential evapotranspiration (PET) estimates on a 1 km grid across Great Britain for 1961–2017.
  - Derived from the CHESS-met meteorological dataset and CEH-GEAR precipitation data; two variables cover the same time and space: PET and PETI.

- What’s included (PET vs PETI):
  - PET: Penman–Monteith potential evapotranspiration for a well-watered grass surface (mm/day).
  - PETI: PET with interception correction; on rainfall days, interception is added to an interception store that inhibits transpiration, with the store drying during the day.

- Release updates and improvements:
  - This release extends data to 2016–2017 and updates netCDF metadata for all years.
  - PET: humidity deficit (qs - qa) is now constrained to a minimum of zero (affects ~4% of data); mean PET increases by ~0.001 mm/day (~0.1%).
  - PETI: interception correction was previously overestimated and has been corrected (affects ~63% of data); overall PETI decreases by ~0.02 mm/day (~1.5%), with larger differences in winter (~-4%) and smaller in summer (~-1%).
  - Some small numerical differences also arise from upgrades to Python libraries.

- Input data and calculation:
  - PET uses CHESS-met variables: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), and surface air pressure (p*).
  - PETI uses the above plus CEH-GEAR precipitation (scaled as needed).
  - Calculation follows Penman–Monteith for a grass surface; fixed stomatal resistance (rsp) of 70 s m⁻¹; PETI includes a rainfall interception component with an interception store (S0) and a total capacity (Stot), with an exponential dry-down of interception.
  - Full methodological details are documented in Robinson et al. (2017, 2020) and related CHESS publications.

- File format and structure:
  - Data are provided as netCDF files (CF-compliant) following CEH gridded dataset conventions.
  - Monthly files; one file per variable.

- Data availability and access:
  - Hosted by the Environmental Information Data Centre (EIDC).
  - Download location: CEH data catalogue (URL provided in documentation).

- Known issues:
  - ArcGIS reading of CF-compliant files with projected coordinate systems may offset layers by 10–100 m due to a fixed WGS84 datum assumption; adjust layers in ArcGIS to align with the correct datum using standard GIS tools.

- Usage notes and references:
  - PET and PETI are suitable for hydrological and ecological modelling to represent evaporative demand under different interception scenarios.
  - Key references include FAO guidelines (Allen et al., 1998), CEH-GEAR and CHESS methodology papers (Keller et al., 2015; Tanguy et al., 2019; Robinson et al., 2017, 2016, 2020).