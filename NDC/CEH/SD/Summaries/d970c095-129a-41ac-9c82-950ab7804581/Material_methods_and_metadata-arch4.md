# Materials, methods and metadata for Denitrification and greenhouse gas emissions in natural and semi-natural terrestrial ecosystems [LTLS]

## Overview
- Two UK catchments studied: Conwy (N. Wales) and Ribble-Wyre (NW England), focusing on natural and semi-natural rural land uses.
- Objective: quantify in situ N2 and N2O fluxes from denitrification, plus CH4 and CO2 fluxes, to understand N, C and P exchanges between soil, water and air under changing climate.
- Approach combines field gas flux measurements with a 15N tracer method to partition denitrification-derived N2O.

## Study area and design
- Catchments and sites
  - Conwy: four sites (peat bog, unimproved grassland, improved grassland, mixed woodland).
  - Ribble-Wyre: four sites (unimproved grassland, improved grassland, heathland, deciduous woodland).
- Land-use types (as identified in analyses)
  - Organic soils (OS), Improved Grassland (IG), Semi-improved Grassland (SIG), Mixed Woodland (MW), Deciduous Woodland (DW), etc.
- Site details
  - Each study site characterized by dominant soils, altitude and rainfall ranges; sampling and management practices vary by site (e.g., grazing intensity, fertilization).
- Data scope
  - Sampling period: April 2013 through October 2014 (17 months), with November 2013 and January 2014 not sampled.
  - Plot structure: five plots per study site per campaign (40 plots per monthly campaign), with soil collars and chambers for gas sampling.

## Measurements and sampling protocol
- Gas flux measurements
  - Method: static chambers, gas sampling at 0, 1, and 2 hours after chamber enclosure.
  - Volume and area: collar volume 4 L, basal area 0.05 m2.
  - Gas analysis: two sample sets per plot
    - Set 1: 15N-labeled N2 and N2O measured with a CFIRMS (continuous flow isotope ratio mass spectrometer).
    - Set 2: total N2O (14N+15N), CH4, and CO2 measured with GC methods.
- 15N tracer application
  - Tracer: labeled K15NO3 (98 at.%), injected in 10 injections per plot to achieve rates between approximately 0.03 and 0.50 kg N ha-1.
  - Application mirrors ambient deposition for natural land uses and daily fertilizer rate for grasslands.
  - Adjustments to tracer solution to match soil moisture content.
- Sampling and processing
  - Gas samples stored in pre-evacuated vials and analyzed within 8 weeks.
  - MDCD (minimum detectable concentration difference) used to determine flux significance; only samples above MDCD used for flux calculations; otherwise treated as zero flux.
  - Flux calculations
    - Based on linear regression of gas concentration vs time, corrected to standard conditions, then scaled to flux density (per area and time).
- Data handling and interpretation
  - Denitrification-derived N2O fraction (DN2O/TN2O) estimated from CF-IRMS data; when DN2O flux is negative or TN2O is zero or below detection, rules applied to assign N2O source.
  - If DN2O exceeds TN2O by more than 10% of the sample pool, all N2O is attributed to denitrification.
  - Interpolation used to estimate annual fluxes from monthly measurements over the two-year period.
  - Global warming potential (GWP) calculated over 100 years, converting N2O and CH4 fluxes to CO2-equivalents using IPCC factors (N2O = 298, CH4 = 34).
- Additional soil data
  - Five composite soil samples per study site (0–10 cm) collected at the end of flux measurement campaigns.

## Data products and structure
- Data files
  - Denitrification_data_N20.csv: N2O flux (μg N2O-N m-2 h-1)
  - N2_flux.csv: N2 flux (μg N2 m-2 h-1)
  - GHG_data_CH4.csv: CH4 flux (μg CH4-C m-2 h-1)
  - GHG_data_CO2.csv: CO2 flux (mg CO2-C m-2 h-1)
  - GHG_data_DN20TN2O.csv: DN2O/TN2O ratio (%)
  - GHG_data_N2O.csv: Total N2O flux (μg N2O-N m-2 h-1)
  - Soil_properties_*.csv: various soil properties (nitrate, total dissolved nitrogen, ammonium, bulk density, C/N ratio, DOC, moisture, organic matter, pH, soil temperature, WFP)
- Units and naming conventions
  - Consistent units provided for each dataset; files include detailed metadata such as site codes, land-use type, coordinates, grid references, and sampling dates.
- Metadata and links
  - Site coordinates provided in degrees, minutes, seconds and decimal degrees; Grid References included.
  - Conwy and Ribble map links included for plot locations.
  - Sampling dates span 2013–2014, with explicit note of missing months.
- Data quality notes
  - Empty cells denote missing data due to sampling or analytical failure.
  - MDCD-based detection limits govern when data are used for flux calculations.

## Data quality and validation
- Detection limits and precision
  - MDCD values established for N2O, CH4, and CO2; only values exceeding MDCD used for flux calculations.
  - Instrument precision reported as <1% RSD for all gases.
- Data processing rules
  - Fluxes for DN2O/TN2O derived with documented decision rules; when measurements are inconclusive or inconsistent, DN2O contributions are treated as described to avoid misattribution.
- Temporal and spatial variability
  - Acknowledgement of high spatial variability in N2O emissions; multiple plots per land-use type help mitigate this.
  - Interpolation across months used to derive annual flux estimates, with justification based on prior analyses showing robustness to differing incubation durations.

## Data links, accessibility and usage
- Catchment-specific map links (Conwy Map Link, Ribble Map Link) for plot locations.
- Data are organized into multiple CSV files, enabling analysis of:
  - Denitrification-specific N2O fluxes
  - Total N2O, N2, CH4, CO2 fluxes
  - Denitrification-derived DN2O proportions
  - Surrounding soil properties and site metadata
- The dataset supports analysis of land-use controls on GHG fluxes, denitrification processes, and GWP implications across natural and semi-natural terrestrial ecosystems.

## Applications and implications
- Enables assessment of how denitrification and associated greenhouse gas fluxes vary across land-use types and catchments.
- Provides a framework to partition N2O sources using 15N tracers, informing nitrogen cycle understanding in soil–atmosphere exchanges.
- Supports regional or UK-scale carbon and nitrogen balance assessments, and informs policy-relevant analyses on nutrient deposition and climate interactions.
- Data can feed ecological and biogeochemical models of soil GHG emissions and help identify management practices that influence N cycling and GHG outputs.

## Limitations and caveats
- Some months have missing data (Nov 2013, Jan 2014).
- High spatial variability requires caution when extrapolating from plots to larger areas.
- Complex attribution rules for denitrification-derived N2O require careful interpretation of DN2O/TN2O values.
- Results are landscape- and management-specific to the Conwy and Ribble-Wyre catchments.

## Key references
- Sgouridis, F., Ullah, S., and colleagues (2014–2017) on denitrification and 15N-Gas Flux method
- IPCC (2013) guidance for GWP calculations
- Related methodological papers on tracer application and gas flux analysis
- Catchment and land-use context papers (e.g., Morton's land cover references)