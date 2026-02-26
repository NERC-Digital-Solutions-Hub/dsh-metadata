# Turf2Surf - Nutrient addition experiment

- Aims to assess how additions of carbon (C) and nutrients (N, P) affect soil respiration, N2O fluxes, and nitrogen mineralization across different land-use types, and to inform integration with ecosystem models (e.g., JULES).
- Built on a pilot study to calibrate sensitivity and incubation timing, followed by a main experiment across multiple sites in the Conwy catchment.

## Overview of the experimental approach

- Pilot experiment
  - Soils: topsoil (0–15 cm) from bog, conifer woodland, and grassland at Aber Henfaes, Clocaenog, and related sites.
  - Treatments: varied C, N, and P amounts and combinations (including CN, CP, NP, CNP; C with glycine or glucose; root-exudate mimics).
  - Design: multiple replicates per soil type; nutrient solutions added after pre-conditioning soil to field capacity; artificial rain solution used to reach field capacity without leaching nutrients.
  - Measurements: gas samples to quantify CO2 production; incubation times tested (0–3 days, extended to 1–3 days post-second nutrient addition) to determine emission dynamics.
  - Outcome: informed the choice to apply nutrients more than once in the main experiment to activate microbial communities and stabilize responses.

- Main experiment
  - Sites: four turf/pasture/land-use types in the Conwy catchment (bog, acid grassland, improved grassland, arable land).
  - Sampling: intact soil cores to 1 m depth; cores split into top (0–15 cm) and deep (85–100 cm); 216 cores in total.
  - Treatments: full factorial of eight treatments – Control, C, N, P, CN, CP, NP, CNP.
  - Nutrient dosing: total 1.20 mg C g⁻¹ soil (split over 3 days); N and P added to achieve C:N ≈ 10 and C:P ≈ 70 based on pilot results.
  - Incubation schedule: measurements at multiple days (4, 5, 6, 8, 10, 12 days) after the first nutrient additions to capture postponed responses; a mercury control was included to gauge nutrient distribution effectiveness.
  - Water management: artificial rain solution applied to maintain soil moisture; leachate collected to monitor leaching dynamics.
  - Measurements: CO2 and N2O production via gas sampling; N mineralization measured after flushing soils with rain solution for 4–5 days and incubating for 2 more weeks at 10°C; soil analyses included nitrate, ammonium (via 1 M KCl extraction), dry weight, and loss-on-ignition (LOI) for organic matter.

## Data collection and structure

- Data products
  - Pilot experiment dataset: experimental data on carbon, nitrogen, and phosphorus additions to topsoil/subsoil cores (CSV).
  - Main experiment dataset: data from nutrient additions across plots/cores, including gas production (CO2, N2O), soil weights, land-use, depth, and incubation details (CSV).
  - Nitrogen mineralization dataset: measures of NO3-N, NH4-N, and total N mineralization per core, across plots and depths (CSV).
- Data fields and organization
  - Datasets include metadata on campaign, date, core numbers, land-use type, soil depth, gas concentrations and production, incubation times, moisture adjustments, and soil physical properties.
  - Units and definitions are explicitly documented (e.g., CO2 and N2O concentrations and production, soil weights, LOI, 0–15 cm vs 85–100 cm depths).
- Roles and contributors
  - Field sampling and laboratory work conducted by a specified team; data analyses and calculations led by a designated researcher.

## Relevance for monitoring and frameworks

- Demonstrates a rigorous, data-rich approach to environmental health monitoring:
  - Multivariate, factorial design across land-use types enables assessment of how nutrient inputs impact soil microbial activity and greenhouse gas fluxes.
  - Longitudinal sampling and multiple incubation time points capture both immediate and delayed responses.
  - Inclusion of N mineralization measurements provides insight into nitrogen cycling under nutrient perturbations.
- Emphasizes data quality and accessibility:
  - Detailed metadata definitions, standardized protocols, and clearly structured datasets support data sharing and reuse, addressing common monitoring challenges around metadata adequacy and data governance.
  - Data outputs align with ecosystem modeling needs (e.g., coupling with JULES), illustrating how field experiments can inform policy-relevant environmental health indicators.

## Practical implications for monitoring programs

- Use of full factorial designs across land uses can help policymakers understand system-wide responses to nutrient inputs and guide nutrient management policies.
- Pilot studies are valuable for calibrating dosing, timing, and incubation parameters to ensure robust, interpretable results in larger-scale monitoring.
- Standardized sampling, controlled moisture management, and transparent data structures facilitate comparability, replication, and integration with existing datasets and models.
- Data governance and metadata clarity are essential to overcome barriers to data sharing and to maximize the policy impact of environmental monitoring efforts.