# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a pasture, Yorkshire, UK, 2021-2023

- 30-minute observations of land-atmosphere exchange of net ecosystem CO2 exchange (NEE) and sensible (H) and latent heat (LE) over 1.5 years at an agriculturally managed pasture in Yorkshire, UK.
- Measurements collected using micrometeorological eddy covariance (EC) method from 01/09/2021 to 01/01/2023.
- Dataset includes weather and soil physics measurements alongside flux data.

## Study site

- Location: field at the University of Leeds Research Farm (coordinates provided in the document).
- Management: grazed by sheep since 2012; occasional silage cutting; rainfed with no fertiliser applied; July 2022 silage cut and periodic grazing during measurement period.
- Climate: temperate oceanic; mean annual air temperature 9.5 ± 1 °C; precipitation 885 ± 231 mm (1992-2022).
- Soil: loamy, calcareous brown earth, pH 6.8, bulk density 1.1 g cm-3; total soil C and N at 0-30 cm 27.7 g kg-1 and 2.3 g kg-1 respectively.
- Soil and site characteristics support flux and meteorological measurements under field conditions.

## Collection methods and fieldwork instrumentation

- Flux instrumentation: EC system, sensors 2 m above canopy; LI-7200RS CO2/H2O analyzer; Gill Windmaster 3D anemometer; data at 10 Hz, summarized to 30-minute means; data logged by CR1000X and Smartflux 2.
- Ancillary measurements: energy fluxes (Rnet, SWin, SWout, LWin, LWout); air temperature (Tair), relative humidity (RH); soil temperature (Tsoil) and soil moisture (VWC) at 5 cm depth; all logged as 30-minute means.
- Automated measurements conducted between 01/09/2021 and 01/01/2023.

## Data processing

- Processing workflow follows Morrison et al. (2019).
- 30-minute fluxes for H, LE, and NEE computed from raw EC data using EddyPro 7; includes data conditioning, angle of attack correction for the sonic anemometer, cross-correlation for time lags, and correction for high- and low-frequency co-spectral attenuation.
- Random uncertainty estimated following Finkelstein and Sims (2001).

## Quality control

- Performed in R to ensure high-quality flux data.
- Data removal criteria include: statistical outliers (Papale et al., 2006); LI-COR signal strength > baseline by >10%; nonrepresentative data according to footprint model (>20% outside site boundaries); unrealistic flux values (H < 200 or > 450 W m-2; LE < -50 or > 400 W m-2; NEE < -60 or > 30 μmol CO2 m-2 s-1); friction velocity (u*) < 0.14 m s-1.

## Gap-filling

- Gap filling and NEE partitioning performed with REddyProc (Reichstein et al., 2016) in R (v4.1.3).
- Missing periods filled using marginal distribution sampling; uncertainty represented by the standard deviation of observations used for filling (Reichstein et al., 2005; Reichstein et al., 2016).
- Flux partitioning outputs include NEE_f (gap-filled NEE), NEE_f_sd (uncertainty), Reco (ecosystem respiration), and GPP (gross primary productivity).

## Details of data structure

- File: Yorkshire_Pasture_2021_2023.csv
- Structure: multiple columns with 30-minute time-stamped observations (Date, Time in GMT).
- Key variables:
  - NEE (μmol m-2 s-1) and NEE_unc
  - LE (W m-2) and LE_unc
  - H (W m-2) and H_unc
  - Tau (kg m-2 s-1) and Tau_unc
  - CO2_strg, LE_strg, H_strg (storage terms)
  - Pa (kPa)
  - Tair (°C)
  - RH, VPD
  - SWin, SWout, LWin, LWout, Rnet
  - PAR, G
  - Tsoil (°C) and Tsoil variants
  - VWC (soil moisture)
  - windspeed, winddir
  - Ustar (m s-1)
  - TKE, Tstar
  - L, (z-d)/L (stability)
  - NEE_f (gap-filled NEE) and NEE_f_sd
  - Reco and GPP (partitioned components)
- Note: NA indicates missing data.

## Acknowledgements

- Data collection funded by the Leeds-York-Hull Natural Environmental Research Council (NERC) Doctoral Training Partnership (DTP) Panorama (grant NE/S007458/1).
- Acknowledgement of the University of Leeds Research Farm and Rob Yardley for farm management information.

## References

- Cited instruments, methodologies, and processing tools include SN-500, CR100X, The Soils Guide, various eddy covariance processing standards (Mauder et al., Moncrieff et al., Papale et al.), EddyPro 7, REddyProc, and foundational meteorological datasets and software (R, Vaisala probes, LI-COR instruments, Gill Instruments, Met Office MIDAS data).