# 21.5 Environmental rate modifiers

- Purpose: Define functions that introduce environmental dependencies into biogeochemical kinetics (building on Section 21.4). They regulate microbial activity, litter decomposition, and other biogeochemical processes in response to soil moisture, temperature, pH, texture, and carbon-N-P-K stoichiometry.

- Groundwater and soil moisture drivers:
  - Soil water potential Ψs controls microbial activity (f_SM.Microbe) and belowground litter decay (f_SM.Litter) using empirically derived functions from Moyano et al. (2013) and Manzoni et al. (2012).
  - Macrofauna activity is governed by effective saturation Se via f_aew, with maximal activity near field capacity and reductions under very dry or very wet conditions.

- Temperature and rate modifiers:
  - Temperature enters through f_Tmic (activation-energy–based microbe kinetics) and through litter decomposition modifiers f_T1 and f_T2; macrofaunal temperature responses are captured by f_T3 and f_T4 (based on soil and root-zone temperatures; reference temperatures T_ref and T_bg).

- Soil chemistry and texture effects:
  - Clay content modifies half-saturation constants for soil organic matter decay (f_clay) and the fraction of dead microbes allocated to DOC (f_clay,2); macrofauna activity is also inhibited by high clay through f_clay,3.
  - Soil pH controls f_PH, with activity at pH 4.5–7.5 and linear decline toward pH 2 or 12.

- DOC accessibility and palatability:
  - Fraction of dissolved organic carbon accessible to microbes f_ad is currently fixed at 1 (possible future dependence on Se).
  - Macrofauna food palatability f_pal depends on the soil organic matter C:N ratio.

- Leaf/biomass age effects:
  - Relative photosynthetic efficiency e_rel for certain vegetation types (deciduous, tropical evergreen) ties to leaf age and photoperiod; some groups (grasses, normal evergreens) may use a constant e_rel ≈ 1 due to uncertainty.

- Summary impact:
  - These modifiers collectively determine how environmental conditions shape microbial activity, litter decomposition, DOC production, and macrofauna behavior, thereby influencing carbon and nutrient cycling rates across the soil-plant system.

- Data stewardship context (cross-cutting):
  - The environmental rate modifiers rely on many parameters and state-dependent flags; documenting their sources, units, and activation within simulations is essential for reproducibility and uncertainty assessment.

- Related sections (basis for integrated budgeting):
  - These modifiers feed into nitrogen (21.6), phosphorus (21.7), potassium (21.8) budgets, leaching (21.9), deposition (21.10), biological N fixation (21.11), and primary mineral supply (21.12). They underpin how environmental conditions translate into fluxes between litter, soil organic matter, microbial/fermentative pools, and inorganic pools.

## 21.6 Nitrogen budget

- Carbon-driven dynamics govern soil organic nitrogen pools (N_som), dissolved organic nitrogen (DON), and nitrogen pools in macrofauna and microbial groups (N_bac, N_fun, N_AM, N_EM).
- Microbial CN targets govern immobilization/mineralization fluxes to approach target microbial C:N; immobilization and mineralization are calculated daily with rapid turnover.
- Processes include: leaching (NH4, NO3), nitrification, denitrification, ammonia volatilization, DON stabilization, and DON leaching; inputs from litter decomposition and mineralization feed inorganic pools.
- Microbial and macrofauna stoichiometry is standardized (Table 7), with fixed C:N and C:P ratios to constrain flows.
- Nitrogen fixation (N_bnf) via root nodules is calculated from carbon exported to roots and fixed via C_fix,N; occurs only if plant species capable of nodulation are present.
- Data inputs for N budget include litter inputs, mineralization/immobilization fluxes, leaching coefficients, and deposition/fixation terms.

## 21.7 Phosphorus budget

- Similar to nitrogen in structure: soil organic P pools (P_som), dissolved organic P (DOP), and microbial P pools (P_bac, P_fun, P_AM, P_EM).
- Microbial immobilization/mineralization drives P allocation to match target carbon-to-phosphorus ratios (R_CP,mic, R_CP,fun, R_CP,AM, R_CP,EM).
- Inorganic P pools follow CENTURY-like dynamics with mineralization/immobilization and exchanges among P_min, P_pri, P_sec, and P_occ; primary minerals receive input from tectonic uplift (T_P,up) and weathering.
- DOP and P_DOc stabilization terms are included to prevent unbounded accumulation; leaching fluxes are described similarly to N.

## 21.8 Potassium budget

- Potassium is highly soluble; most K resides in inorganic pools; microbial and macrofauna K content is not tracked explicitly.
- A single organic pool (K_som) is modeled, with leaching and transfer to mineral pools; inorganic K pools include K_min, K_ex, K_nex, and K_pri with weathering and uplift dynamics.
- Exchange/adsorption kinetics (K_ex,sol, K_fix,sol, K_min,rel) regulate transfers among pools; leaching (L_k,K) feeds inorganic pools and is described with first-order kinetics.

## 21.9 Nutrient leaching

- Leaching fluxes are proportional to dissolved nutrient amounts and bottom-leakage L_k, scaled by soil water volume V in the active zone.
- Seven fluxes modeled: L_k,NH4, L_k,NO3, L_k,DON, L_k,P, L_k,DOP, L_k,K, L_k,DOC; solubility coefficients a_X determine dissolved-phase mobilization.

## 21.10 Nutrient deposition

- Atmospheric deposition inputs distributed geographically:
  - Nitrogen deposition includes wet plus dry deposition (reduced and oxidized forms); historical (pre-industrial) baselines referenced.
  - Phosphorus deposition maps for current and pre-industrial time.
  - Potassium wet deposition derived from station data with nearest-neighbor interpolation.

## 21.11 Biological nitrogen fixation

- N_bnf computed from carbon exported to roots (R_exm y) and C_fix,N; only active if nodulating plant species are present.
- Resulting N_bnf is allocated to the ammonium pool (NH4+).

## 21.12 Supply of primary minerals

- Tectonic uplift supplies new phosphorus and potassium through parent material weathering.
- Formulas convert uplift rate to g m^-2 day^-1 using rock density and element concentrations in parent material (C_el,P, C_el,K); default representative values provided.
- Note: a potential rock-derived nitrogen flux exists but is not yet included in the current formulation.

## Data stewardship implications (across sections 19–21)

- Data provenance and versioning:
  - The model links many interdependent processes with numerous parameter sets and evolving state variables; document all parameter sets, state variables, and configuration flags (e.g., plant hydraulics, litter decomposition options).
- Metadata requirements:
  - Inputs: meteorological drivers, soil properties, root fractions, LAI, canopy height, soil texture, temperature, etc.
  - Component-level parameters: e.g., f_d, f_clay, root/mycorrhizal parameters, litter CN values, decomposition rates, enzyme capacities, environmental modifiers.
  - Outputs: infiltration, K_sat, RWU_max,i, J_sx,i, θ_i, Ψ_sR, Ψ_L, NPP, GPP, carbon/N budgets, litter and soil fluxes with units and diagnostic flags.
- Data lineage and reproducibility:
  - Document computational flow from meteorology to SOC and vegetation carbon/nutrient budgets, including time steps, solvers, and any approximations or submodule choices (e.g., plant hydraulics enabled/disabled).
- Data quality and governance:
  - Heavy reliance on literature-default constants; implement uncertainty tracking and sensitivity analyses for key parameters; ensure consistent units and naming conventions; note which optional submodules are enabled.
- Practical guidance for data custodians:
  - Create a centralized metadata schema detailing module name, version, input datasets, parameter sets, state variables, outputs, and provenance links.
  - Use controlled vocabularies for vegetation categories and maintain consistent scaling for carbon and nutrient pools.
  - Enforce version control and reproducible runtime configurations to support traceability and auditability of results.