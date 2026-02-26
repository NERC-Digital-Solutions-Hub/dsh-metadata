# ReadMe file for SoilCharacteristics.csv

- The dataset describes soil characteristics from two seasonal field trials (2017-2018) conducted to monitor greenhouse gas fluxes from sheep urine applied to unimproved pasture.
- Study area: common grazing land in the Carneddau range, Snowdonia National Park, North Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Sampling design: control plots from each seasonal study (n = 4 soil samples per season) collected at 0-10 cm depth (summer and autumn plots).

## Location, sampling and seasonality

- Seasons: summer sampling on 18/07/17; autumn sampling on 17/10/17.
- Soils by season:
  - Summer plots: Dystric Histosol
  - Autumn plots: Humic Gleysol
- Bulk density measured at 0-5 cm using undisturbed metal rings; corrected for stones.
- Gravimetric soil moisture and organic matter (loss-on-ignition) determined via oven-drying and standard procedures.
- pH and electrical conductivity (EC) measured on 1:2.5 soil-to-water suspensions; calibration against certified standards.

## Measurements and laboratory methods

- Total soil carbon (TotC) and nitrogen (TotN) and carbon-to-nitrogen ratio (CN) determined with a TruSpec analyzer.
- N mineralisation rate (Nmin) measured following Waring and Bremner (1964) using NH4+ quantified before and after 7-day anaerobic incubation.
- N forms and related metrics:
  - Extractable NH4+ and NO3- (via 0.5 M K2SO4 extractions; analyses per Mulvaney 1996 and Miranda et al. 2001).
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN) with CHCl3-fumigation-extraction; microbial biomass C and N estimated using KEC and KEN corrections (Voroney et al. 2008).
  - Phosphate (PO4^3-) and exchangeable cations (Na, K, Ca) measured after 1.0 M CH3COOH extraction; PO4^3- via Murphy and Riley (1962); cations by flame photometry.
- Quality assurance:
  - All solutions analysed against matrix-matched certified reference standards.
  - Procedural blanks checked for contamination.
  - Data visually inspected for quality assurance.

## Data headers, units and structure

- Variables (examples):
  - BulkDensity_Summer; BulkDensity_Autumn — g cm-3 (0-5 cm, dry weight basis)
  - GravMoist_Summer; GravMoist_Autumn — % (gravimetric soil moisture)
  - OrgMatter_Summer; OrgMatter_Autumn — % (organic matter, dry weight)
  - pH_Summer; pH_Autumn — pH
  - EC_Summer; EC_Autumn — µS cm-1
  - TotC_Summer; TotC_Autumn — % (total soil carbon, dry weight)
  - TotN_Summer; TotN_Autumn — % (total soil nitrogen, dry weight)
  - CN_Summer; CN_Autumn — unitless (C:N ratio)
  - Nmin_Summer; Nmin_Autumn — mg N kg-1 d-1
  - DOC_Summer; DOC_Autumn — mg C kg-1 soil dry weight
  - TN_Summer; TN_Autumn — mg N kg-1 soil dry weight
  - MicC_Summer; MicC_Autumn — g C kg-1 soil dry weight
  - MicN_Summer; MicN_Autumn — mg N kg-1 soil dry weight
  - Nitrate_Summer; Nitrate_Autumn — mg NO3--N kg-1 soil dry weight
  - Ammonium_Summer; Ammonium_Autumn — mg NH4+-N kg-1 soil dry weight
  - Phos_Summer; Phos_Autumn — mg P kg-1 soil dry weight
  - Na_Summer; Na_Autumn — mg Na kg-1 soil dry weight
  - K_Summer; K_Autumn — mg K kg-1 soil dry weight
  - Ca_Summer; Ca_Autumn — mg Ca kg-1 soil dry weight
- All data are tied to control plots and seasonal sampling within unimproved pasture.

## Usage notes and limitations

- Data-use note: Authors must be acknowledged if the data are reused or reproduced.
- Scale and scope: N = 4 per season; focused on control plots within a specific upland pasture in Snowdonia, which may limit extrapolation to broader regions.
- The dataset integrates multiple laboratory methods and references multiple established procedures; careful attention to method-specific units and contexts is required when combining with other datasets.

## References for methods

- Ball, D.F. (1964). Loss-on-ignition as an estimate of organic matter and organic carbon in noncalcareous soil.
- Miranda, K.M., Epsey, M.G. and Wink, D.A. (2001). A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite.
- Mulvaney, R.L. (1996). Nitrogen - inorganic forms. In Sparks, D.L. (Ed.), Methods of Soil Analysis. Part 3.
- Voroney, R.P., Brookes, P.C., and Beyaert, R.P. (2008). Soil microbial biomass C, N, P and S. In Carter & Gregorich, Soil sampling and methods of analysis, 2nd edn.
- Waring, S.A., and Bremner, J.M. (1964). Ammonium production in soil under waterlogged conditions as an index of nitrogen availability. Nature.