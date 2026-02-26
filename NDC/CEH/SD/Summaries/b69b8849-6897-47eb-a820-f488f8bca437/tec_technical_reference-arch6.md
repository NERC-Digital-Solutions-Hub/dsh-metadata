# Tethys-Chloris (T&C) Technical Reference

## 21.5 Environmental rate modifiers

- Soil water potential (Ψs) governs microbial activity and belowground litter decomposition via two functions with parameters derived from observations; Ψopt and Ψth define optimum and threshold values; explicit oxygen limitation near saturation is neglected.
- Macrofauna activity responds to effective saturation Se, with a0ew bounded between 0 and 1; activity peaks near field capacity and declines in very dry or very wet conditions.
- Soil pH modulates microbial/macrofaunal activity through f_PH, set to 1 between pH 4.5–7.5 and declining linearly to 0 at pH 2 and 12 (pH held constant over time).
- Fraction of decomposed POC that becomes MOC (f_d) is adjusted by soil clay/silt content (F_cla, F_sil) and existing soil MOC (C_moc); f_d increases with C_moc and approaches saturation as reactive surfaces become occupied.
- Clay content (f_clay) reduces SOM decay half-saturation and the fraction of dead microbes allocated to DOC (f_clay,2); macrofauna activity also inhibited by high clay (f_clay,3).
- Temperature modulates reaction rates: f_Tmic for microbial reactions, f_T3 for microbial growth, and f_T4 for macrofaunal activity; rate modifiers depend on soil/biogeochemically active zone temperatures and reference temperatures.
- DOC accessibility to microbes (f_ad) is currently assumed to be 1.
- Food palatability (f_pal) for macrofauna depends on SOM C:N ratio (f_pal = 1.6 − 0.04 CN_som).

## 21.6 Nitrogen budget

- Soil organic N pool dynamics include soil organic N som, dissolved organic N (DON), macrofauna N ew, and microbial N pools (N_bac, N_fun, N_AM, N_EM); HON/N input/outputs tied to litter inputs and mineralization/immobilization to reach target C:N ratios.
- Microbial C:N targets are fixed (e.g., bacteria ~5.2, fungi ~6.5, AM ~18, EM ~18; macrofauna ~10); mineralization or immobilization occurs to approach these targets, with rapid turnover on a daily step.
- DON leaching and stabilization (S DON) prevent unbounded DON growth; N leaching fractions (L_k,NH4, L_k,NO3) partition into NH4 and NO3 pools with a fixed split (e.g., 0.9 to NH4, 0.1 to NO3) and a small ongoing immobilization due to chemical stabilization.
- Nitrification, denitrification, and volatilization are modeled with first-order kinetics influenced by soil moisture (Se) and temperature (through f_T5, f_T6); losses and fluxes connect to NH4 and NO3 pools.
- Leaching fluxes and plant uptake are integrated with leaching from the soil biogeochemically active zone and subsequent plant uptake definitions.

## 21.7 Phosphorus budget

- Soil organic P dynamics mirror nitrogen logic, using C:P targets for microbial and other pools; immobilization/mineralization adjust to reach target C:P.
- Inorganic P pools follow a CENTURY-like framework: P_min (mineral P), P_pri (primary minerals), P_sec (secondary minerals), P_occ (occluded P); exchanges among pools are controlled by first-order kinetics and uplift/weathering processes.
- Leaching (L_k,P), dissolved organic phosphorus (DOP), and organic P leaching stabilization (S_DOP) are included; microbial immobilization/mineralization proceeds to balance C:P ratios.
- Nutrient fluxes to and from microbial pools (bacteria, fungi, AM, EM) reflect their respective target C:P ratios (Table 7); phosphorus is not tracked in macrofauna pools.

## 21.8 Potassium budget

- Potassium is treated with limited biological tracking due to high solubility; a single organic matter pool holds K, while inorganic K pools include K_min, K_pri, K_ex, K_nex.
- Leaching from litter and mineralization feed K_min; exchange/adsorption kinetics connect K_min to K_ex,sol and K_nex; uplift supplies primary K via tectonic processes.
- K_nex can be converted back to K_min, allowing some reversibility; macrofauna and microbial K contents are not explicitly tracked.

## 21.9 Nutrient leaching

- Leaching from the soil is proportional to dissolved nutrient amounts and bottom water flux, scaled by soil volume (V) to yield fluxes L_k,X for NH4, NO3, DON, P, DOP, K, and DOC.
- Seven leaching fluxes are computed with solubility coefficients (a_X) and the corresponding dissolved pools; unit conversions from soil-centered fluxes to area-based fluxes are applied.

## 21.10 Nutrient deposition

- Geographic deposition inputs are integrated from external datasets: present-day N deposition (wet + dry, reduced and oxidized forms), present-day total P deposition, and wet deposition for K; pre-industrial baselines are provided for N and P.
- Wet/dry deposition maps are incorporated to provide spatially explicit deposition inputs for the model.

## 21.11 Biological nitrogen fixation

- N_bnf is computed as N_bnf = R_exmy / C_fix,N, activating only if nodulating plant species are present (R_ex,3 > 0); the fixation process has a carbon cost tied to root carbon export (C_fix,N).
- Fixed nitrogen is assumed to enter as ammonium (NH4+), aligning with the carbon allocation framework.

## 21.12 Supply of primary minerals

- Primary mineral input from tectonic uplift (T_up) supplies new parent material; uplift-driven P and K fluxes (T_P,up and T_K,up) are calculated using rock density and element concentrations in parental material.
- Representative element concentrations (C_el,P and C_el,K) are used for simplicity; nitrogen release from near-surface rocks is noted but not currently included in the model.
- For decadal-scale simulations, uplift can be set to zero if minimal mineral input is expected.

Data-focused considerations (relevant to Data Support archetype)

- The environmental rate modifiers and nutrient fluxes are expressed through explicit functions and first-order kinetics, enabling structured calibration against observations and datasets.
- Parameters are drawn from literature sources and are designed to be traceable to inputs, enabling provenance-ready dashboards and scenario analyses.
- The framework integrates climate (temperature, moisture, deposition) and soil properties (clay/silt content, pH) to drive biogeochemical rates, supporting data-driven exploration of nutrient dynamics under various scenarios.
- The model emphasizes mechanistic links among litter, soil organic matter, microbial pools, macrofauna, and plant uptake, facilitating interpretation of observed nutrient fluxes and soil carbon responses.