# Tethys-Chloris (T&C) Technical Reference

## 21.5 Environmental rate modifiers
- Environmental dependencies are applied to biogeochemical kinetics.
- Soil water potential controls decomposition and microbial activity; two functions regulate microbial activity and belowground litter decomposition, based on Ψs, with empirically derived parameters.
- Macrofauna activity is modeled against effective soil moisture saturation Se, peaking near field capacity and declining under very dry or very wet conditions.
- Soil pH affects microbial and macrofauna activity through fPH, with activity highest between pH 4.5–7.5 and decreasing toward pH 2 or 12.
- Clay content influences decomposition and microbial partitioning:
  - f clay and f clay,2 modify half-saturation constants and the fraction of dead microbe allocation to DOC.
  - Macrofauna activity is also inhibited by high clay content via f clay,3.
- Temperature modulates: fTmic (microbial reactions), fT1/fT2 (litter decomposition), and fT3/fT4 (macrofaunal activity) using Arrhenius-like formulations with reference temperatures.
- The fraction of decomposed POC becoming DOC (f d) and the DOC accessibility for microbes (f ad) are parameterized, with f ad currently set to 1 (DOC always accessible).
- Food palatability for macrofauna depends on SOM C:N ratio (f pal).

## 21.6 Nitrogen budget
- Soil organic nitrogen dynamics follow carbon fluxes with pool-specific C:N ratios; microbial biomass has constrained target C:N values (Table 7).
- Nitrogen fluxes include immobilization and mineralization across microbial groups (bacteria, saprotrophic fungi, AM, EM) to maintain target C:N.
- Leaching of nitrogen (N leaching fraction λn and DON leaching S DON) is included; DON stabilization term prevents unbounded DON growth.
- Inorganic N pools (NH4+, NO3−) dynamics include input I som,nit, immobilization/mineralization fluxes, nitrification, denitrification, volatilization, leaching, and external inputs (Ex N) such as deposition, fixation, and fertilization (assumed as NH4+ for simplicity).
- Partitioning of immobilization/mineralization between NH4+ and NO3− follows prescribed fractions; additional daily stabilization terms ensure mass balance.
- Nitrification and denitrification are modeled with first-order kinetics with moisture controls via Se; volatilization uses a fixed rate.
- Biological nitrogen fixation (N bnf) is included where plant species form nodules; N bnf = R_exmy / C fix,N, representing carbon cost of fixation; N bnf enters as NH4+.

## 21.7 Phosphorus budget
- Soil organic phosphorus dynamics mirror nitrogen with C:P constraints for microbial biomass (target R CP,mic, R CP,fun, R CP,AM, R CP,EM from Table 7).
- Immobilization/mineralization fluxes adjust to reach microbial target C:P; DON leaching and DOP stabilization are included.
- Litter inputs feed P pools; organic P pools (Psom, Pbac, Pfun, P AM, P EM) evolve with decomposition fluxes.
- Inorganic P pools follow CENTURY-model-inspired dynamics with mineral P sources and exchanges:
  - Pmin, Ppri, Psec, Pocc evolve via first-order exchanges; uplift and weathering supply primary mineral P (TP,up) and meshed exchanges between pools.
- Leaching of inorganic P (Lk,P) links to total P mineral pools and deposition; Ex P accounts for external inputs.

## 21.8 Potassium budget
- Potassium is highly soluble; microbial and macrofauna K content is not tracked explicitly. A single organic K pool (Ksom) is simulated alongside inorganic pools:
  - Kmin, Kpri, Kex, K nex, with weathering and uplift supplying primary minerals (TK,up).
  - Leaching (Lk,K) and first-order kinetics regulate exchanges between inorganic pools (Kmin, Kex, Kfix,sol, Kmin,rel).
- Adsorption/desorption between Kmin and Kex,sol and conversion from Kpri to Kmin are described with kinetic coefficients; uplift supplies new K to the active zone.
- External inputs (Ex K) from deposition/fertilization are included.

## 21.9 Nutrient leaching
- Leaching fluxes are proportional to dissolved nutrient amounts and bottom-leakage Lk, scaled by soil water volume V.
- Seven leaching fluxes are computed: Lk,NH4, Lk,NO3, Lk,DON, Lk,P, Lk,DOP, Lk,K, Lk,DOC.
- Solubility coefficients aX (Table 8) modulate the leaching for each solute (e.g., nitrate and DOC have high solubility; phosphorus is more strongly adsorbed).

## 21.10 Nutrient deposition
- Nutrients from atmosphere are mapped globally:
  - Present-day N deposition combines wet and dry deposition (reduced and oxidized forms).
  - Present-day P deposition maps come from literature syntheses.
  - Wet deposition data for K available from station networks; spatial interpolation used to produce local inputs.
- Data sources include Vet et al. (2014), Mahowald et al. (2008), and related deposition datasets.

## 21.11 Biological nitrogen fixation
- Symbiotic N fixation is included when plant species allocate carbon to root nodules.
- N fixed is converted to NH4+ with a carbon cost constraint (C fix,N) and is linked to root export (R exmy).
- N bnf is modeled only if nodulating species are present in the vegetated patch.

## 21.12 Supply of primary minerals
- Primary mineral P and K inputs come from tectonic uplift (T up), supplying new parent material for weathering.
- T P,up and T K,up are computed from uplift rate, rock density, and element concentrations in parent material (C el,P, C el,K).
- Representative element concentrations are used (C el,P ≈ 0.0005; C el,K ≈ 0.021); nitrogen release from near-surface rocks is noted but not included in this version.
- For decadal-scale simulations, uplift can be set to zero if negligible.

## Monitoring implications and outputs (relevant to Analysts Monitoring the Environment)
- The framework yields budgets for energy, water, and nutrients, enabling direct comparison with observations and remote-sensing proxies.
- Outputs of interest include:
  - Infiltration and runoff budgets; snow processes.
  - Root-zone soil moisture and potentials; plant C and nutrient pools; tissue turnover and litter exports.
  - Soil organic carbon pools (POC, MOC, DOC); litter decomposition dynamics; microbial and enzyme fluxes; macrofauna contributions.
- For site- or region-specific monitoring, hourly forcing data and vegetation/soil properties feed the policy-relevant assessments.