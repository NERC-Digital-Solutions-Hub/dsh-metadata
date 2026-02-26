# Tethys-Chloris (T&C) technical reference

## 21.5 Environmental rate modifiers
- Describes functions that impose environmental dependencies on biogeochemical kinetics.
- Soil water potential controls: 
  - microbial activity (f_SM.Microbe)
  - belowground litter decomposition (f_SM.Litter)
- Macrofauna activity (f_aew) depends on effective saturation (S_e) around field capacity; declines at very dry or very wet conditions.
- Soil pH effects: f_PH modulates microbial and macrofaunal activity; pH is prescribed and constant during simulations.
- Litter decomposition and MOC formation depend on clay content (f_clay, f_clay,2, f_clay,3) influencing degradation and DOC allocation.
- Temperature modifiers:
  - f_Tmic, f_T3, f_T4 adjust reaction rates and macrofaunal activity with soil/air temperatures; references to activation energy and reference temperatures.
- DOC accessibility (f_ad) currently set to 1 (microbial access to DOC assumed always available).
- Food palatability (f_pal) for macrofauna depends on soil organic matter C:N ratio.
- These rate modifiers feed into environmental dependencies of biogeochemical reactions and organism activities, affecting monitoring-relevant fluxes and pool sizes.

## 21.6 Nitrogen budget
- Soil organic nitrogen dynamics track C fluxes through pools:
  - N_som, DON, N_new
  - microbial pools: N_bac, N_fun, N_AM, N_EM
  - macrofauna: N_ew
- Leaching of nitrogen (λ_n) and leaching fluxes (L_k,NH4, L_k NO3) are included; leaching interacts with mineralization/immobilization processes.
- Immobilization vs mineralization:
  - governed by target C:N ratios of microbial groups; rapid adjustment over daily time steps.
  - distribution of immobilization/mineralization between NH4 and NO3 follows predefined partitions.
- N transformations:
  - NH4 and NO3 pools updated by inputs from litter, immobilization/mineralization, mineralization fluxes, and microbial turnover.
  - Nitrification, denitrification, and volatilization are modeled with simplified first-order kinetics and moisture/temperature controls.
- Biological nitrogen fixation (N_bnf):
  - depends on carbon exported to roots and presence of symbiotic nodulating plants; produces NH4 in a form available to plants.
- Nitrogen stock and fluxes are tied to microbial biomass C:N targets and leaching dynamics; deposition and external inputs are included.

## 21.7 Phosphorus budget
- Soil organic phosphorus dynamics mirror nitrogen structure:
  - pools: P_som, DOP, microbial pools P_bac, P_fun, P_AM, P_EM
  - immobilization/mineralization to reach target microbial C:P ratios
- Inorganic P pools follow CENTURY-style exchanges:
  - P_min (mineral P), P_pri (primary minerals), P_sec (secondary minerals), P_occ (occluded P)
  - exchanges among pools governed by first-order kinetics with defined rate constants
- External inputs:
  - tectonic uplift supplies new P via Tp_up; deposition Ex_P adds P from atmospheric sources
- Microbial immobilization/mineralization of P is regulated to maintain target C:P ratios for microbial groups
- Net phosphorus fluxes balance organic and inorganic pools and leaching dynamics
- Phosphorus cycling is integrated with plant uptake and soil processes to inform monitoring indicators of soil fertility and nutrient budgets

## 21.8 Potassium budget
- Potassium is highly soluble and largely leached; microbial and macrofauna K contents are not tracked.
- A single organic pool K_som holds K in decomposing organic matter; mineral and exchangeable K pools (K_min, K_pri, K_ex, K_nex) are modeled with dynamic exchange and weathering.
- Decomposition generates soluble K_min; weathering and uplift supply K_pri; adsorption/desorption and exchanges regulate K availability.
- Uptake and leaching originate from K_min; leaching and weathering control the distribution among pools.

## 21.9 Nutrient leaching
- Leaching is proportional to dissolved nutrient pools and bottom-leakage flux L_k divided by soil water volume V.
- Seven leaching fluxes computed:
  - L_k,NH4, L_k NO3, L_k,arg DON, L_k,P, L_k,DOP, L_k,K, L_k,DOC
- Solubility coefficients (a_X) tailor the solubility and leaching behavior for each solute.
- Leaching is applied to surface soil layers and biogeochemically active zone dynamics, affecting downstream nutrient budgets.

## 21.10 Nutrient deposition
- Atmospheric deposition data integrated for key nutrients:
  - nitrogen (wet and dry forms, reduced and oxidized)
  - phosphorus (present-day and pre-industrial maps)
  - potassium (wet deposition data from monitoring stations)
- Deposition inputs are spatially resolved to inform local nutrient inputs and budget balances.

## 21.11 Biological nitrogen fixation
- Nitrogen fixation by symbiotic bacteria is computed from carbon export to root nodules:
  - N_bnf = R_exmy / C_fix,N, with N_bnf provided as NH4
  - Only occurs if plant species in a patch allocate carbon to nodules
- Fixation links carbon costs to available nitrogen input, maintaining carbon-nitrogen balance coherence.

## 21.12 Supply of primary minerals
- Primary mineral supply through tectonic uplift for P and K:
  - Tp_up and Tk_up determine new mineral input based on rock density and element concentrations in parent material
  - Representative el concentrations for P and K are provided; N release from rocks is noted as a potential addition not yet included
- For decadal-scale sims, uplift can be set to zero if negligible over the timescale

## Implications for environmental health monitoring (key takeaways)
- The sections define mechanistic, nutrient-cycling processes (N, P, K) linked to soil pools, leaching, deposition, fixation, and mineral weathering, enabling policy-relevant indicators of soil fertility and nutrient losses.
- Monitoring indicators to derive from these sections include:
  - rates of microbial activity and litter decomposition under varying moisture/temperature
  - dynamics of N, P, and K pools in soil organic matter and microbial biomass
  - immobilization/mineralization fluxes and their effect on plant nutrient uptake
  - leaching fluxes of NH4, NO3, DON, P, DOP, K, and DOC
  - changes in inorganic nutrient pools (NH4, NO3, P_min, P_sec, etc.)
  - effects of deposition and fixation on soil nutrient budgets
  - responses to tectonic uplift-derived mineral inputs (where relevant)
- Data inputs and governance considerations:
  - necessitates detailed soil properties (clay/silt content, C:N:P:K ratios, pH), moisture and temperature regimes, and moisture-dependent rate modifiers
  - requires deposition maps and historical baselines for atmospheric inputs
  - careful calibration against observed nutrient fluxes, pool sizes, and plant uptake data
  - emphasis on data provenance, transparency, and reproducibility due to complex, multi-pool interactions and numerous assumptions
- The framework supports policy evaluation of nutrient cycling, soil fertility, and ecosystem responses to climate and management, while acknowledging uncertainties in microbial stoichiometry and mineral interactions.