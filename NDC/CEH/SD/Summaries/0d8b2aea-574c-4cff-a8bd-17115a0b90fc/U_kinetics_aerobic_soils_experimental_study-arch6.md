# Supporting documentation

## Overview
- Presents a dataset describing uranium speciation in soils after laboratory contamination with UO2^2+ and long-term incubation (619 days).
- Aim is to understand U(VI) transformations, binding strength, and long-term mobility in aerobic soils to inform models and risk assessments.

## Study design and scope
- 20 topsoil samples (0–15 cm) from central England with diverse properties and land uses (arable, grassland, moorland, woodland).
- Soils span a pH range of 3.41 to 8.00 and organic carbon content from 1.7% to 38.6%.
- Soils characterized with coordinates, land use, pH (0.01 M CaCl2), and organic carbon (FLASH CNS analyzer).
- Soils were contaminated in the lab with 5000 µg U VI per kg dry soil and incubated in field-moist conditions at 10.0 ± 1.0 °C for 619 days in darkness.
- Each soil was run as three microcosms (bottles) to capture replicate data.

## Fractions and data collected
- At multiple sampling times, U was fractionated into three pools:
  - Soluble U: extracted with 0.01 M KNO3 (freely extractable; µg U/kg DW).
  - Chemically exchangeable U: extracted with 1 M Mg(NO3)2 (electrostatically adsorbed to Fe/Mn oxides; µg U/kg DW).
  - Labile/isotopically exchangeable U: extracted with 1 M Mg(NO3)2 plus isotopic tracers (233U and 236U) to quantify isotopically exchangeable U (µg U/kg DW).
- Isotopic measurements using 233U, 236U, and 238U to determine isotopic exchangeability; data expressed as µg U per kg dry weight.
- Tracking performed over the 619-day incubation period, with data gaps indicated in Table 2 where data were not available.

## Analytical methods
- Inductively Coupled Plasma Mass Spectrometry (ICP-MS): iCAP-Q (Thermo Fisher) with autosampler and ASXpress rapid uptake module.
- Internal standard: Iridium (5 µg/L) added to samples.
- Instrument settings include specific dwell times and sweeps for total U and isotopic measurements; 233U/236U spike used every 12 samples to correct mass discrimination.
- Calculation of isotopically exchangeable U (U_E) using a defined equation that relates measured isotopic intensities to the exchangeable pool.

## Data structure and content
- Table 1: soil metadata for the 20 samples, including soil code, land use, latitude/longitude, organic C content (%), and pH.
  - Examples of soil codes: CO-A, EV-A, NP-A, SR-A, WK-A (arable); BH-G, DY-G, FD-G, SB-G, SR-G, TK-G (grassland); BC-M, DY-M (moorland); BH-W, BY-W, IH-W, PE-W, SR-W, WK-W (woodland).
  - Organic C % ranges from 1.7% to 38.6%; pH ranges from 3.41 to 8.00.
- Table 2: extraction schemes and U concentrations by soil and timepoint.
  - Fractions: XX-X_soluble_U (0.01 M KNO3), XX-X_exch_U (1 M Mg(NO3)2), XX-X_labile_U (1 M Mg(NO3)2 with isotopic exchange).
  - Units: µg U kg^-1 DW.
  - Notes: Some cells contain '-' where data are not available.

## Calculations and interpretation
- Isotopic exchangeability (U_E) calculated from 238U in soil-Mg(NO3)2 suspensions, the added extractant volume, soil mass, and distribution coefficients (K_d* derived from 233U/236U spike data).
- The data enable estimation of the labile/reactive fraction available for isotopic exchange, informing the potential bioavailability and long-term mobility of U(VI) in aerobic soils.

## Implications and potential uses
- Enables development and refinement of models for long-term U(VI) mobility and availability in temperate, aerobic soils.
- Supports assessment of uranium bioavailability to plants and potential environmental risk under controlled conditions.
- Provides a well-documented dataset with metadata across multiple soil types and land uses, suitable for cross-site comparisons and method benchmarking.

## Experimental timeframe
- November 2014 to August 2016 (incubation period of 619 days).