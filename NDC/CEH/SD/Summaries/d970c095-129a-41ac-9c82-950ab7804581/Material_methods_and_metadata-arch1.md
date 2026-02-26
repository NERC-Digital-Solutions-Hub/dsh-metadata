# Materials, methods and metadata for Denitrification and greenhouse gas emissions in natural and semi-natural terrestrial ecosystems [LTLS]

## Overview
- Two UK river catchments were studied: Conwy (N. Wales) and Ribble-Wyre (NW England). Both are dominated by natural and semi-natural land uses.
- Objectives: quantify in situ N, C, and P fluxes among soil, water, and air under changing climate and perturbed C cycle; focus on denitrification-driven N2 and N2O fluxes using 15N tracers; support macro-nutrient cycle research (NERC Macronutrient Cycles Programme).

## Study sites and land-use types
- Conwy catchment (345 km2): four sites
  - C-PB: peat bog (organic soils, OS)
  - C-UG: unimproved grassland (semi-improved grassland, SIG)
  - C-IG: improved grassland (IG)
  - C-MW: mixed woodland (MW)
- Ribble-Wyre catchment (1145 km2): four sites
  - R-UG: unimproved grassland (SIG)
  - R-IG: improved grassland (IG)
  - R-HL: heathland (MW category in FA)
  - R-DW: deciduous woodland (DW)
- Land-use clustering (factor analysis): OS, IG, SIG, MW, DW as distinct natural/semi-natural categories.

## Sampling design and dates
- Sampling periods: April 2013 to October 2014 (17 months); except November 2013 and January 2014 not sampled.
- Monthly gas flux measurements; 40 plots per campaign (5 plots per study site × 4 sites per catchment × 2 catchments).
- Plot setup: 5 plots per study site; PVC collars inserted ~10 cm deep (15 cm for R-HL and C-PB); collars sealed with acrylic chamber for gas sampling.
- Soil sampling: five composite soil samples (0–10 cm) near each plot after gas measurements; kept on ice, stored at 4°C.

## Gas flux measurements and tracers
- Gases measured:
  - Nitrous oxide N2O and dinitrogen N2 via 15N tracer and non-equilibrium CFIRMS for isotope ratios.
  - Total N2O (14N + 15N), CH4, and CO2 via GC-μECD and GC-FID.
- 15N tracer application:
  - K15NO3 tracer (98 at.%) applied at rates between 0.03 and 0.50 kg N ha-1 (per plot) through multiple injections.
  - Tracer adjustments made to reflect ambient atmospheric deposition or fertilizer-like deposition, depending on land use.
  - Application volumes 50–200 mL; adjusted to 3–5% of volumetric water content.
- Gas sampling:
  - Samples collected at T=0 h (before chamber cover), T=1 h, T=2 h.
  - Samples stored in pre-evacuated vials for later analysis.
- Analytical methods:
  - CFIRMS for 15N-N2 and 15N-N2O (in-house continuous flow setup).
  - GC-μECD for total N2O; GC-FID for CH4 and CO2.
- Data quality and detection:
  - Minimum detectable concentration difference (MDCD) calculated for each gas; MDCDs: N2O ~0.008 ppm, CH4 ~0.036 ppm, CO2 ~3.6 ppm.
  - Fluxes computed from linear regression of chamber headspace concentrations vs time (0–2 h), adjusted to STP, then divided by chamber area and incubation time.
  - Instrument precision: <1% RSD for the gases.
- Flux interpretation rules:
  - Only samples exceeding MDCD used for flux calculations; others treated as zero flux.
  - Denitrification fraction (DN2O/TN2O) derived from CF-IRMS data; TN2O fluxes estimated for the same 20 h incubation when needed.
  - If TN2O flux is negative but DN2O proportion increases, all N2O assumed from denitrification; if TN2O = 0 but DN2O > 0, all N2O assumed from denitrification; if DN2O > TN2O by >10%, all N2O assumed from denitrification.
  - If DN2O flux is not measured reliably, the DN2O/TN2O ratio is not estimated.
- Temporal processing:
  - Annual fluxes estimated by interpolating monthly measurements for each year and averaging across the two-year monitoring period.
  - Global warming potential (GWP, 100-year horizon, including climate-carbon feedbacks) calculated as CO2-equivalent using IPCC factors: 298 for N2O and 34 for CH4.

## Soil measurements and properties
- Composite soil samples (0–10 cm) collected for five composite samples per study site after gas flux measurements.
- Analyses cover: nitrate (NO3-N), total dissolved nitrogen (TDN), NH4-N, bulk density, C/N ratio, dissolved organic carbon (DOC), soil moisture, organic matter, pH, soil temperature, and water-filled pore space.

## Data management, units and metadata
- Datasets and file naming:
  - Denitrification and N2/N2O flux data: N2_flux (N2 flux), N2O flux, DN2O/TN2O ratio, CH4 flux, CO2 flux.
  - Soil properties: nitrate, TDN, ammonia, bulk density, C/N, DOC, moisture, organic matter, pH, soil temperature, water-filled pore space.
- Units are specified for each dataset; examples include micrograms N2O-N m-2 h-1, mg CO2-C m-2 h-1, CH4 CH4-C m-2 h-1, etc.
- Data and metadata accessibility:
  - Catchment-level metadata with precise coordinates, grid references, and British National Grid (BNG) coordinates (X_BNG, Y_BNG) and grid references.
  - Conwy Map Link and Ribble Map Link provided for site locations.
  - Empty cells indicate sampling or analytical failures.
- Data provenance:
  - Detailed references linked to methods and prior studies for 15N-Gas Flux approach, flux calculations, and sampling protocols.
  - Acknowledges a suite of foundational methods and prior publications (e.g., Sgouridis et al., Ullah et al., Mosier & Klemedtsson, IPCC guidelines).

## Study implications and context
- The LTLS dataset enables examination of land-use–specific N2 and N2O fluxes driven by denitrification across natural and semi-natural ecosystems.
- Combines isotopic tracing with conventional gas flux measurements to apportion denitrification contributions and assess environmental controls (soil properties, moisture, pH, etc.).
- Supports cross-site comparison and long-term predictions of greenhouse gas emissions under climate variability and land-management changes.