# Materials, methods and metadata for Denitrification and greenhouse gas emissions in natural and semi-natural terrestrial ecosystems [LTLS]

## Overview
- Metadata and methodological overview for a study within LTLS (Limbang Macronutrient Cycles Programme) investigating N, C, and P fluxes between soil, water, and air under climate change and perturbed C cycles.
- Two UK catchments: Conwy (N. Wales) and Ribble-Wyre (NW England) with predominantly natural/semi-natural land uses.
- Aimed at quantifying in situ denitrification-derived N2 and N2O fluxes and overall greenhouse gas emissions across land-use types.

## Study sites
- Catchments: Conwy (345 km2) and Ribble-Wyre (1145 km2).
- Study sites by land use:
  - Conwy: C-PB (peat bog), C-UG (unimproved grassland), C-IG (improved grassland), C-MW (mixed woodland).
  - Ribble-Wyre: R-UG (unimproved grassland), R-IG (improved grassland), R-HL (heathland), R-DW (deciduous woodland).
- Soils range from organic-rich or stagnopodzols to brown podzolic and gleys; altitudes ~260–440 m; rainfall typical of upland sites.
- Sampling sites included multiple replicate locations per land-use type (coded as C-ML, C-RG, C-WL, C-IG, R-ML, R-WL, R-RG, R-IG with grid references provided).

## Gas flux measurement protocol
- Frequency: Monthly measurements from April 2013 to October 2014 (17 months total); no sampling in November 2013 and January 2014.
- Method: Static chamber technique with five plots per study site (total 40 plots per campaign).
- Chamber setup: PVC collars inserted ~10 cm soil depth (15 cm for R-HL and C-PB) with a 25 mm groove to fit an acrylic chamber; covered with reflective foil to minimize headspace temperature rise.
- Gas sampling: 20 mL samples collected at T=1 h and T=2 h after chamber closure; a T=0 h sample collected prior to sealing.
- Tracer: Labeled N-15 nitrate solution (98 at. %) applied in ten injections per plot at rates between 0.03 and 0.50 kg N ha-1 depending on land-use type compared to natural deposition and fertilization practices.
- Sample storage: Pre-evacuated Exetainer vials used; analyzed within 8 weeks.

## 15N tracer application
- Purpose: Quantify in situ N2 and N2O fluxes specifically from denitrification.
- Application strategy: Rate adjustments to mimic natural deposition vs. fertilizer-derived inputs; tracer distribution across grid injections designed to minimize soil nitrate enrichment beyond normal conditions.

## Gas analysis and flux calculation
- Analyses performed on two sample sets:
  - CFIRMS: 15N-N2 and 15N-N2O measured for denitrification-derived fluxes using non-equilibrium isotope ratio calculations.
  - GC-based methods: Total N2O (labeled and unlabeled), CH4, and CO2 measured for overall GHG fluxes.
- Detection limits and quality control:
  - Minimum detectable concentration differences (MDCD) calculated for N2O, CH4, and CO2 to ensure reliable flux estimation.
  - Only samples above/below MDCD used for flux calculations; otherwise treated as zero flux.
  - Instrument precision < 1% RSD for all gases.
- Flux calculation: Based on linear regression of gas concentrations in chamber headspace (corrected for T and P) over 0–2 hours, scaled by chamber volume and area and incubation time.
- Data handling: Annual fluxes estimated by interpolating monthly data; fluxes expressed as N2, N2O, CH4, and CO2 fluxes with units specified in data files.

## Denitrification-derived N2O estimation
- DN2O/TN2O ratio estimated from CF-IRMS data; total N2O fluxes also estimated for 20-hour incubations to align with DN2O rates when necessary.
- Decision rules for DN2O attribution:
  - If TN2O fluxes are negative but DN2O fraction increases, all N2O attributed to denitrification.
  - If TN2O fluxes are zero but DN2O is detectable, all N2O attributed to denitrification.
  - If DN2O exceeds TN2O by up to 10%, attribute 100% of N2O to denitrification.
  - Some samples (about 3%) lack successful DN2O measurement and are not used for the ratio.
- Purpose: Quantify proportion of N2O emissions derived from denitrification versus other sources.

## Soil sampling and properties
- End-of-study composites: Five soil samples per site (0–10 cm) collected near plots within 50 cm.
- Analyses focused on: nitrate, total dissolved nitrogen, ammonium, bulk density, C/N ratio, dissolved organic carbon, moisture, organic matter, pH, soil temperature, and water-filled pore space.
- Samples stored on ice and analyzed under controlled lab conditions.

## Data outputs and units
- Data files:
  - Denitrification_data_N20.csv: N2 flux (µg N2O-N m-2 h-1).
  - GHG_data_CH4.csv: CH4 flux (µg CH4-C m-2 h-1).
  - GHG_data_CO2.csv: CO2 flux (mg CO2-C m-2 h-1).
  - GHG_data_DN20TN2O.csv: DN2O/TN2O ratio (%).
  - GHG_data_N2O.csv: Total N2O flux (µg N2O-N m-2 h-1).
  - Soil_propertes_Nitrate.csv: NO3--N (mg m-2 at 10 cm depth).
  - Soil_propertes_Total_dissolved_nitrogen.csv: TDN (mg m-2 at 10 cm).
  - Soil_properties_Ammonia.csv: NH4+-N (mg m-2 at 10 cm).
  - Soil_properties_Bulk_density.csv: Dry bulk density (g cm-3).
  - Soil_properties_Carbon_to_nitrogen_ratio.csv: C/N ratio.
  - Soil_properties_Dissolved_organic_carbon.csv: DOC (g m-2 at 10 cm).
  - Soil_properties_moisture_content.csv: Soil water content (% wet basis).
  - Soil_properties_Organic_matter_content.csv: Organic matter (%).
  - Soil_properties_Soil_pH.csv: Soil pH.
  - Soil_properties_Soil_temperature.csv: Soil temperature (°C).
  - Soil_properties_Water_filled_pore_space.csv: WFPS (%).
- Units and variable names correspond to flux measurements and soil properties as described above.

## Timeline and sampling dates
- Sampling months (representative): Apr 2013, May 2013, Jun 2013, Jul 2013, Aug 2013, Sep 2013, Oct 2013, Dec 2013, Feb 2014, Mar 2014, Apr 2014, May 2014, Jun 2014, Jul 2014, Aug 2014, Sep 2014, Oct 2014.
- Follow-up two-year monitoring period aligning with LTLS objectives.

## Data quality, metadata, and references
- Metadata formalized to link catchments, sites, land-use types, coordinates, and sampling context (grid references, X_BNG, Y_BNG).
- Quality assurance includes standardized QA processes, dataset storage, and uploading to appropriate portals.
- Key references span IPCC guidelines, 15N-gas flux methodology, and prior LTLS related studies (Sgouridis et al., Ullah & Moore, etc.) to support methodology and interpretation.

## Data management and accessibility
- Map links provided for Conwy and Ribble catchments to locate study sites (C-ML, C-RG, C-IG, C-WL, etc.; R-ML, R-WL, R-RG, R-IG).
- Empty cells indicate sampling or analytical failure, with null data represented accordingly.
- Acknowledges the need to increase dataset value by integrating with related datasets and ensuring access to underlying data used to generate outputs.