# Introduction

- This dataset contains the parameters used in the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system, designed to test new land surface parameterisations and to make projections for future emission scenarios not yet simulated by GCMs.
- IMOGEN uses pattern-scaling to emulate GCMs, relating local monthly changes in meteorology to global land warming, via an Energy Balance Model (EBM) and evolving radiative forcing.
- Details and extended descriptions are to be provided in Zelazowski et al. (In Prep).

## Data Description

- EBM parameters (five per GCM): climate sensitivity over land λl and ocean λo (W m^-2 K^-1), ocean effective thermal diffusivity κ (W m^-1 K^-1), a constant ratio ν of mean land and ocean SST warming, and f (ocean fraction).
- Calibration against CMIP3 GCMs (22 models). Table 1 lists λl, λo, κ, ν, and f for each GCM.
- Local and monthly “patterns” are available for download in ASCII format.
- Patterns are organized into 22 directories named pattRelPR_d2_<GCM>, with monthly files jan…dec.
- All GCM patterns are remapped to a common grid of 2.5° latitude × 3.75° longitude (HadCM3 grid), consisting of 1631 land points.
- Each monthly file contains a header and 1631 data lines describing, in order:
  1. Longitude
  2. Latitude
  3. Temperature change per degree global warming [K × K^-1]
  4. Relative humidity change per degree warming [% × K^-1]
  5. Wind change per degree warming [m s^-1 × K^-1]
  6. Unused
  7. Longwave change per degree warming [W m^-2 × K^-1]
  8. Shortwave change per degree warming [W m^-2 × K^-1]
  9. Unused
  10. Precipitation change per degree warming [mm day^-1 × K^-1]
  11. Unused
  12. Pressure change per degree warming [hPa × K^-1]
  13. Unused
- IMOGEN is routinely coupled to the JULES land surface model; examples of coupling are described in Huntingford et al. (2010). JULES model descriptions appear in Best et al. (2011) and Clark et al. (2011).

## Data Structure

- For each GCM, a directory exists: pattRelPR_d2_<GCM name> (22 directories in total).
- Within each directory there are monthly ASCII files named jan, feb, ..., dec.
- Each GCM has been re-mapped to a common HadCM3 grid (2.5° × 3.75°), containing 1631 land points.
- Each file consists of a header line followed by 1631 lines of data in the described column order.

## Usage and GIS Relevance

- The monthly, gridded pattern data can be loaded into GIS to create map-based visualisations of how climate variables change with global warming, by GCM, and by month.
- The common grid facilitates cross-GCM comparisons and scenario mapping for policy, client, or public-facing analyses.
- The ASCII format supports straightforward integration with GIS workflows and reprojection/regridding as needed.

## Quality Control and Future Developments

- Data are part of a beta program to extend IMOGEN EBM and pattern parameterisation beyond UK GCMs, currently validated against CMIP3.
- A CMIP5-based version is in development, emphasizing full traceability and alignment with UK ISO standards.

## Acknowledgement

- Acknowledges modeling groups, PCMDI, WGCM, and the WCRP for CMIP data; US DOE support is noted.

## References

- Best, M.J. et al. 2011. The Joint UK Land Environment Simulator (JULES), model description - Part 1: Energy and water fluxes.
- Clark, D.B. et al. 2011. The Joint UK Land Environment Simulator (JULES), model description - Part 2: Carbon fluxes and vegetation dynamics.
- Huntingford, C. et al. 2010. IMOGEN: an intermediate complexity model to evaluate terrestrial impacts of a changing climate.
- Huntingford, C. and Cox, P.M. 2000. An analogue model to derive additional climate change scenarios from existing GCM simulations.
- Meehl, G.A. et al. 2007. The WCRP CMIP3 multimodel dataset.
- Zelazowski, P. et al. (2016) Climate pattern scaling set for an ensemble of 22 GCMs (submitted).