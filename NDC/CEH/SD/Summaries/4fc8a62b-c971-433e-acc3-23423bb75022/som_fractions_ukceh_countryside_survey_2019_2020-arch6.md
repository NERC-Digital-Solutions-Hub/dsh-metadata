# Soil organic matter fractions

- This document describes methods to separate soil organic matter (SOM) into discrete fractions using density fractionation and to quantify carbon and nitrogen within these fractions. It focuses on the dissolved organic carbon (DOC), free light fraction (LF), occluded particulate fraction (OF), and mineral-associated organic matter (MAOM), but analysis in this study discards DOC and OF, concentrating on LF and MAOM (with OF derived by mass balance). It situates these analyses within the UK Countryside Survey (UKCEH) context.

## Overview and context

- SOM is highly heterogeneous and consists of pools with different residence times; modeling SOM dynamics requires identifying these pools.
- Density fractionation provides a means to separate SOM into physically/chemically distinct pools, enabling study of stabilization mechanisms and turnover.
- Increases in DOC concentrations have been observed in Europe and North America, highlighting the relevance of dissolved components.
- The data come from the UK-SCAPE-supported Countryside Survey rolling programme (2019–2023), which aims to monitor soil condition and function at a national scale and co-locate soil measurements with vegetation data.

## Countryside Survey design and sampling

- Rolling survey design: 500 x 1-km2 squares sampled over a five-year cycle, with 100 squares visited each year.
- Sampling frame: squares randomly selected within strata defined by the Land Classification of Great Britain; excludes urban-dominated (>75% urban) or sea-dominated (>90% sea) squares.
- Within each square: up to 5 topsoil samples collected at predetermined random locations using a 15 cm core, co-located with vegetation plots.
- Density fractionation performed on 100 archived soil samples (sieved to 2 mm, air-dried) collected in spring 2022.
- The Countryside Survey is supported by NERC through UK-SCAPE; data are linked to broader soil-vegetation assessments.

## Laboratory methods and data produced

- Loss-on-Ignition (LOI), hygroscopic water content, and CaCO3
  - Thermo-Gravimetric Analysis (TGA701) across four heating steps (25°C to 1000°C) to obtain hygroscopic water, SOM content (via LOI at 375°C), and CaCO3 content (via 650–1000°C differences).
  - Calculations convert weight losses to hygroscopic moisture, SOM, and Calcite-C; corrections applied for calcite recovery (95–100%).
- SOM density fractionation (Sodium polytungstate, SPT, 1.8 g cm-3)
  - Subsample (2.5 g) suspended in SPT, centrifuged to separate light fraction (LF) from mineral-associated material.
  - LF isolated by filtration; pellet washed, dried, and weighed to obtain LF mass.
  - Remaining pellet treated with ultrasonic sonication to disrupt aggregates; supernatant discarded to isolate occluded fraction (OF).
  - MAOM fraction retained after removing LF and OF; multiple DIW washes to remove SPT and ensure low conductivity.
  - Internal standards used; 10% replicated samples included for quality control.
  - Total carbon and total nitrogen measured on LF, MAOM, and archived soil by elemental analysis (SOP3102).
- Derived carbon and nitrogen fractions
  - SOC (soil organic carbon) calculated as total carbon minus Calcite-C; corrected for calcite-C.
  - LF-C and MAOM-C derived from fraction masses and regional TC concentrations.
  - OF-C and OF-N inferred by mass balance: OF-C = SOC - LF-C - MAOM-C; OF-N = TN - LF-N - MAOM-N.
  - POM-C and POM-N calculated as sums of LF-C/OF-C and LF-N/OF-N; corrected for hygroscopic water as applicable.
- Data corrections and constraints
  - Hygroscopic water content and calcite-C corrections applied to total soil and MAOM; LF, OF, and POM fractions corrected via their mass-based calculations.
  - If OF-C or OF-N computed negative due to measurement uncertainty, values set to zero before calculating POM-C/N.

## Data structure and outputs

- Dataset characteristics:
  - 13 data columns and 101 rows; values may be NA where not analyzed.
  - Key variables include: Year, SQ_ID, LF_C_gperg, MAOM_C_gperg, OF_C_gperg, POM_C_gperg, LF_N_gperg, MAOM_N_gperg, OF_N_gperg, POM_N_gperg, SOC_gperg, TN_gperg, SOM_gperg.
- What the data represent:
  - LF-C, MAOM-C, OF-C, POM-C: carbon content per gram of soil for each fraction.
  - LF-N, MAOM-N, OF-N, POM-N: nitrogen content per gram of soil for each fraction.
  - SOC and TN: total soil carbon and nitrogen (with calcite-C correction for SOC).
  - SOM: soil organic matter as measured by LOI.
- Data provenance and scope:
  - Data accompany topsoil physico-chemical properties for Great Britain (2018–2019 and 2020, v2); part of a national capability project to map stock and change in GB soils and to relate to vegetation surveys.
  - Data co-located with vegetation assessments to support integrated soil-vegetation analyses.

## Accessibility, funding, and references

- Funding and support:
  - UK-SCAPE programme (National Capability) funded by NERC (award NE/R016429/1).
  - AI4SoilHealth project supported (Grant No. 101086179).
- References and methodological basis:
  - Foundational experiments and prior Countryside Survey reports underpinning the sampling design, fractionation methods, and data interpretation (e.g., Six et al., Sohi et al., Reinsch et al., Cotrufo et al., Schrumpf et al., etc.).
- Data availability:
  - Datasets produced under UK-SCAPE and UKCEH guidelines; details linked to NERC Environmental Information Data Centre (EIDC) with accompanying methodological documentation.