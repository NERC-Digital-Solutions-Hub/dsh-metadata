# Tethys-Chloris (T&C) Technical Reference

## 21.5 Environmental rate modifiers
- Water in soil (soil water potential) modulates decomposition and microbial activity via two functions: one for microbial activity and one for belowground litter decomposition, using Ψ_s in the biogeochemically active zone with parameters from Moyano et al. (2013) and Manzoni et al. (2012). Oxygen limitation near saturation is neglected.
- Macrofauna activity depends on effective saturation Se, with a peak near field capacity and diminishing to zero at very dry or very wet conditions (function f_aew, capped between 0 and 1).
- Soil pH affects microbial and macrofaunal activity: f_PH = 1 for pH 4.5–7.5, decreasing linearly to 0 at pH 2 and 12 (pH fixed at simulation start).
- The fraction of decomposed POC becoming MOC (f_d) is corrected for soil clay/silt content (F_cla, F_sil) and existing MOC (C_moc) via an Eq. (579) that increases f_d with C_moc and is moderated by texture; higher clay/silt provides more protection and can limit MOC formation.
- Clay content influences: (i) half-saturation constants for SOM decay (f_clay), (ii) fraction of dead microbes allocated to DOC (f_clay,2), and (iii) macrofaunal inhibition (f_clay,3); f_clay,3 = 1 if F_cla < 0.15, otherwise uses a decreasing function with clay content.
- Temperature modifiers: f_Tmic, f_T3, f_T4 adjust biogeochemical reactions, litter decomposition, and macrofaunal activity via Arrhenius-type relationships using activation energies and reference temperatures.
- DOC accessibility: f_ad is currently fixed at 1 (DOC always available to microbes); potential future dependence on effective saturation SE may be added.
- Food palatability for macrofauna (f_pal) depends on SOM C:N: f_pal = 1.6 − 0.04 × C_N_SOM.
- Note: these modifiers are simplified; future refinements may account for more nuanced interactions and uncertainties.

## 21.6 Nitrogen budget
- Soil organic nitrogen dynamics follow the same carbon-flux framework; target C:N ratios for microbial biomass are fixed (Table 7), enforcing mineralization or immobilization to maintain or approach these targets.
- Temporal dynamics include soil organic N (N_som), dissolved organic N (N_DON), plant-available N pools, and microbial/N-transport pools (N_bac, N_fun, N_AM, N_EM) with leaching and stabilization terms.
- Inorganic N pools (NH4+, NO3−) undergo nitrification, denitrification, and volatilization; external inputs (Ex_N) from deposition or fixation are included.
- Net immobilization/mineralization for bacteria, saprotrophic fungi, and mycorrhizae are calculated to preserve target CN ratios, with partitioning to NH4 and NO3 (approximately 0.9 and 0.1) and small constants to represent continued immobilization.
- Nitrification NO3 flux and denitrification N2 flux follow simplified first-order kinetics with moisture- and temperature-dependent modifiers (f_T5, f_moist,1, f_moist,2); volatilization depends on NO3 via a fixed rate constant.
- Leaching of inorganic N (L_k,NH4, L_k NO3) is controlled by solubility coefficients and water flux, integrated with soil volume V.
- Overall, the nitrogen budget couples C fluxes to microbial and plant N pools, with explicit processes for immobilization, mineralization, nitrification, denitrification, volatilization, and leaching.

## 21.7 Phosphorus budget
- Phosphorus follows a similar structure to nitrogen, tied to carbon fluxes with pool-specific C:P ratios for microbial and plant pools.
- Microbial immobilization/mineralization moves P toward target CP values (Table 7); inorganic P pools include P_min, P_pri, P_sec, and P_occ with exogenous inputs.
- Tectonic uplift provides new parent material, feeding primary mineral P (P_pri ex), while weathering drives secondary and occluded P; exchanges between inorganic P pools follow first-order kinetics with defined rate constants.
- Leaching of inorganic P (L_k,P) is described and integrated with DON/POP dynamics, while immobilization/mineralization fluxes maintain microbial CP targets.
- The model captures partitioning of P among microbial biomass and soil organic matter, with system-wide P budgets informed by turnover and leaching.

## 21.8 Potassium budget
- Microbial K content is neglected; a single organic potassium pool (K_som) is tracked, with high leaching potential relative to other nutrients.
- Four inorganic K pools are modeled: K_min, K_ex, K_nex, and K_pri. Uptake and leaching occur from K_min; K_pri converts to K_min via weathering, and uplift (T_up) supplies primary K through tectonics.
- First-order kinetics govern exchange between pools: K_ex,sol and K_fix,sol are described with fast adsorption/desorption dynamics (0.5 day−1 proxy).
- Numerical constants and parameters (K min, r_rel, KaK, KdK) control mineral and organic interactions and ensure plausible K dynamics.

## 21.9 Nutrient leaching
- Leaching is proportional to dissolved nutrient amounts and bottom-water leakage (L_k) divided by soil-column water volume (V).
- Seven leaching fluxes are computed: NH4, NO3, DON, P, DOP, K, and DOC, with solubility coefficients a_X (Table 8) shaping the fate of each solute.
- Leaching is applied to corresponding pools and integrated into the overall nutrient budgets.

## 21.10 Nutrient deposition
- Present-day and pre-industrial deposition maps are integrated: N deposition (wet + dry, reduced and oxidized forms) from Vet et al. (2014); pre-industrial N from Galloway et al. (2004, 2006); current P deposition from Mahowald et al. (2008); wet K deposition from ~480 stations (Vet et al., 2014).
- Deposition inputs are geospatially mapped to provide local inorganic nutrient inputs to the system.

## 21.11 Biological nitrogen fixation
- N_fix is computed from root exudation and a carbon cost: N_bnf = R_exmy / C_fix,N, conditional on the presence of plant species capable of root-nodule N fixation (e.g., certain tropical species).
- Fixed nitrogen is supplied to the NH4+ pool, maintaining coherence with carbon allocation patterns.

## 21.12 Supply of primary minerals
- Primary mineral supply from tectonic uplift (T_up) provides new phosphorus and potassium to the biogeochemically active zone; uplift can be neglected for decadal-scale runs (T_up ≈ 0).
- TP_up and TK_up are computed from uplift rate, rock density (ρ_rock = 2500 kg/m3), and element concentrations in parent material (C_el,P = 0.0005, C_el,K = 0.021).
- Nitrogen release from near-surface rocks is acknowledged but not included in the current formulation.

## Overall calibration and data implications
- The environmental modifiers and nutrient budgets rely on numerous parameters and bounding relationships (solubility coefficients, C:N/P ratios, turnover constants, attack rates, and kinetic coefficients) drawn from literature and tables referenced in the model.
- Calibration targets include hydraulic responses, LAI/phenology, litter quality and turnover, soil organic matter pools and enzyme dynamics, and nutrient budgets (N, P, K) across species and soils.
- Data challenges align with Analysts’ needs: local-scale data gaps, heterogeneity in soils and vegetation, data access hurdles, and integrating diverse datasets (soil hydraulics, litter chemistry, microbial pools, deposition data) to constrain uncertainties in energy, moisture, carbon, and nutrient flux predictions.