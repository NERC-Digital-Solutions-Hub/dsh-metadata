# Location

## Overview
- The document describes geochemical sampling and analysis of streams, springs, and borehole waters from 21 sites within Cyprus’ Troodos ophiolite area (mid-May 1985), with the aim of understanding water chemistry, dissolved CO2, and mineral saturation processes.
- It provides context on Cyprus’ geography, climate, land use, and geology to frame the sampling sites and hydrologic setting.

## Study design and sampling scope
- 21 sampling sites selected to represent major waters of the Troodos ophiolite area (informed by the Geological Survey of Cyprus).
- Site selection and sampling conducted with local colleagues; sample types include surface and groundwater sources across the ophiolite region.

## Field sampling and in-situ measurements
- Samples filtered in the field through 0.45 μm membranes.
- In-field pH measured with a combination electrode immediately after collection, with minimal atmospheric contact to prevent CO2 exchange.
- Alkalinity measured acidimetrically to pH ~4.0; reduced sulfur measured with an ion-selective electrode.
- For alkalinity and reduced sulfur, samples stored in filled bottles and analyzed promptly to minimize CO2 equilibration and gas loss.

## Sample handling and laboratory analyses
- Samples transported to the UK for further chemical analyses.
- Analytical methodologies:
  - Colorimetric methods for major anions, bromide, and total iodine (iodide/iodate).
  - Inductively coupled plasma optical emission spectroscopy (ICP-OES) for major cations, trace metals, and boron.
- Sample preservation:
  - Metals: stored in polypropylene bottles cleaned with acid and preserved with 1% nitric acid.
  - Anions: stored in glass bottles with high-purity water cleaning.
- Data processing for dissolved inorganic carbon species and related calculations relies on established thermodynamic models.

## Thermodynamic treatment and key calculations
- Dissolved carbon dioxide (CO2) saturation and related factors:
  - EpCO2 defined as the ratio of dissolved CO2 in the sample to CO2 in pure water at the same temperature/pressure; used to assess CO2 sources and exchange processes.
  - Factors influencing EpCO2 include atmospheric/biogenic CO2 inputs, soil/ groundwater weathering, plant photosynthesis and respiration, gaseous exchange with the atmosphere, and possible mantle-derived CO2 inputs.
- Mineral saturation analysis:
  - Saturation indices (SI) calculated for minerals (e.g., calcite) using activity products and thermodynamic constants (K values) as a function of temperature, pressure, and ionic strength.
  - For calcite: SI_CaCO3 = log10({Ca2+}*{CO3^2-}) - log10(K_CaCO3).
  - For other minerals, similar SI formulations are used (e.g., magnesium hydroxide/brucite), with activity terms and corresponding constants.
  - PHREEQC thermodynamic model (Parkhurst, 1995) used for calculating saturation indices.
- Handling of data below detection limits:
  - When determinands fall below the lowest quotable value, saturation indices are calculated using half of that value to compare with cases where detection limits are not an issue.
  - In tables, such low-value cases are shown in italics; the lowest quotable value is defined as twice the detection limit.
  - Aluminium and magnesium are specifically noted as the only determinants where this issue is relevant, yielding an upper bound rather than a precise value.

## Data quality, provenance, and documentation
- Field and lab methods are specified to support reproducibility and auditability.
- Data presentation:
  - Results and calculated indices are organized in tabular form in a later section (not included in this excerpt), with explicit notes about italicized low-value entries.
- References used for methods and interpretation:
  - Neal (1988, 1992, 1998a) on bicarbonate estimation, forestry impacts on water quality, and excess CO2 partial pressures.
  - Pantazis (1978) and Parkhurst (1995) for regional context and PHREEQC software, respectively.

## Data management implications for Data Stewards
- Data types and formats:
  - Field measurements (pH, alkalinity, reduced sulfur) and lab-derived concentrations (anions, cations, trace metals, boron) with preservation details.
  - Derived data: EpCO2 values and mineral saturation indices (SI) based on thermodynamic modeling.
- Metadata and provenance:
  - Site-level metadata, sampling date, field procedures, handling instructions, and laboratory protocols are essential for traceability and reuse.
- Data quality considerations:
  - Handling of detection limits and use of upper bounds for certain elements (Al, Mg) require clear documentation.
  - CO2-related measurements are sensitive to atmospheric exchange; field and storage protocols mitigate (to an extent) these effects.
- Accessibility and reuse:
  - Data are described as being tabulated in a later section, with methodologies and references provided to enable replication and secondary analyses (e.g., PHREEQC-based modeling of saturation states).

## References (selected)
- Neal, C. (1988, 1992, 1998a) – bicarbonate estimation, forestry impacts on upland water quality, and CO2 partial pressures in natural waters.
- Pantazis, T.M. (1978) – thermal mineral waters of Cyprus.
- Parkhurst, D.L. (1995) – PHREEQC user’s guide for geochemical modeling.