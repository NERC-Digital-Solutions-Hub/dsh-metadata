# The T&C Model Documentation

## 21.7 Phosphorus budget
- Soil organic phosphorus pools: P_som (soil organic P), DOP (dissolved organic P), and microbial P pools for bacteria, fungi, and mycorrhizae (P_bac, P_fun, P_AM, P_EM).
- P dynamics: mineralization or immobilization to adjust microbial carbon-to-phosphorus ratios; litter inputs (I_som,pho) feed P_som and microbial pools.
- Litter and organic matter turnover transfer P to inorganic pools via leaching and immobilization/mineralization processes.
- Inorganic P pools: P_min (mineral P), P_pri (primary minerals), P_sec (secondary minerals), P_occ (occluded P). Exchanges governed by first-order kinetics; tectonic uplift adds new parent material (P_up) and weathering forms secondary/occluded pools; input from external sources (Ex_P); leaching L_k,P described separately.
- Leaching and stabilization: leaching fraction (λ_p) and stabilization term S_DOP prevent unbounded DOP accumulation; inorganic P fluxes to microbes follow target C:P ratios (R_CP,x) and immobilization/mineralization fluxes (P_b,imm/min, etc.) ensure coherence with carbon fluxes.
- Key mechanism: overall balance between organic P cycling, mineral P pools, uplift-derived inputs, and leaching processes.

## 21.8 Potassium budget
- Potassium in microbial biomass is neglected; potassium largely resides in organic matter with relatively small pools.
- Four inorganic K pools: K_min (mineral solution), K_ex (exchangeable), K_nex (non-exchangeable), K_pri (primary minerals).
- Flows: primary minerals weather to K_min; uplift provides new K via T_K,up with element concentration in parent material; exchanges between K_ex and K_nex and transfer to K_min via weathering and dissolution kinetics.
- Uptake and leaching: plant uptake and leaching occur from K_min; solubility and adsorption/desorption modeled with simple first-order kinetics; K nex may convert back to K_min, maintaining potential availability.
- Microbial K content is not tracked; environmental controls and weathering govern turnover and availability.

## 21.9 Nutrient leaching
- Leaching fluxes for seven solutes: NH4, NO3, DON, P, DOP, K, DOC.
- Leaching proportional to dissolved nutrient pools and bottom-of-soil water leakage (L_k) divided by soil volume (V); solubility coefficients (a_X) modulate each solute's leachability.
- Equations ensure realistic short-term dynamics and balance with long-term leaching in steady-state conditions.

## 21.10 Nutrient deposition
- Spatial maps provide deposition inputs for N and P (wet + dry for N; current and preindustrial for P); wet deposition data for K via stations (near real-time interpolation for local input).
- Data sources include Vet et al. (2014) for present-day N deposition, Mahowald et al. (2008) for present-day P deposition, and Vet et al. (2014) for K deposition coverage.

## 21.11 Biological nitrogen fixation
- N_bnf computed from carbon cost of fixation: N_bnf = R_exmy / C_fix,N, where R_exmy is carbon exported through roots and C_fix,N is the carbon cost per unit N fixed.
- Fixation occurs only if plant species in a patch allocate carbon to root nodules (i.e., conditions permit nodulation).
- Fixed nitrogen assumes ammonium form NH4+.

## 21.12 Supply of primary minerals
- Tectonic uplift supplies new phosphorus and potassium through parent material weathering; uplift rates can vary by order of magnitude but can be set to zero for decadal scales.
- Phosphorus uplift: T_P_up = T_up × ρ_rock × C_el,P normalized by area and geometric factors; C_el,P and ρ_rock are embedded constants (representative rock values: C_el,P ≈ 0.0005, ρ_rock = 2500 kg/m3).
- Potassium uplift: T_K_up = T_up × ρ_rock × C_el,K normalized similarly (C_el,K ≈ 0.021).
- Note: nitrogen release from near-surface rocks is recognized but not yet included in the current framework.
- Explanatory links to mineral pools: mineral P and K pools are updated through uplift and weathering fluxes, with mineralization/immobilization dynamics tied to the microbial and plant C budgets.

## 22 Vegetation Management
- Placeholder for future content.

Data-related considerations (for Data Leaders)
- Required inputs and data sources:
  - C:P target values for microbial groups and associated pools; turnover and immobilization/mineralization parameters.
  - Rates and pools for P and K (P_som, DOP, P_min, P_pri, P_sec, P_occ; K_min, K_ex, K_nex, K_pri) and their fluxes.
  - Leaching coefficients, solubility parameters (a_X), soil volume (V), and turnover inputs from litter and soil reservoirs.
  - Deposition maps and time-varying inputs for N, P, and K; uplift rates and rock composition constants.
  - N fixation parameters and carbon costs; presence of nodulating species to enable N_bnf.
- Governance and calibration:
  - Many parameters are ecosystem- or site-specific; require calibration targets, provenance, and uncertainty bounds.
  - Maintain consistent spatial-temporal resolution across phosphorus, potassium, and nitrogen modules; document data provenance and versioning for inputs and parameter sets.
  - Explicit metadata for inputs, parameters, and states to support cross-partner validation and reproducibility.
- Outputs of interest for decision support:
  - Litter P and K fluxes, SOC and P/K pools, enzyme-mediated processes, and microbial/macrofaunal activity.
  - Mineral and inorganic nutrient fluxes, leaching, and deposition impacts.
  - Potential scenario analyses for nutrient budgets under varying deposition, uplift, and phenological regimes.