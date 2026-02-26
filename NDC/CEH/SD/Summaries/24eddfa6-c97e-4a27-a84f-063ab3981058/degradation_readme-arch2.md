# Degradation characteristics of bio-based teabags buried in soil, UK, November 2021 - June 2022

## Purpose and scope
- Investigates chemical deterioration and material changes of three anonymised bio-based PLA: cellulose blend teabags after 7 months buried at 10 cm in UK soil (Nov 2021–Jun 2022).
- Supported by NERC BIO-PLASTIC-RISK project.
- Aimed at informing environmental monitoring and policy-relevant understanding of bio-based plastics in soil.

## Data files included
- Degradation_crystallinity.csv: crystallinity changes after soil burial (7 months) for anonymised teabags A and B; no data for C.
- Degradation_Mass.csv: mass loss measurements for teabags A, B, and C after 7 months; includes initial mass, final mass, mass loss (g) and mass loss (%).
- Degradation_PLA.csv: proportion of PLA in teabags and its change after burial; includes data for A and B; no data for C.
- Degradation_prGCMS_TbagA.csv: Py-GCxGC-TOF MS composition for Tbag-A.
- Degradation_prGCMS_TbagB.csv: Py-GCxGC-TOF MS composition for Tbag-B.
- Degradation_prGCMS_TbagC.csv: Py-GCxGC-TOF MS composition for Tbag-C.

## Methods and analytical details
- Burial: teabags buried in UK soil at approximately -10 cm depth for 7 months.
- Mass loss calculation: mass_loss_percent = (1 - final_mass / initial_mass) × 100.
- PLA proportion: determine cellulose:PLA by dissolving PLA in chloroform (30 minutes at room temp), filtering, evaporating solvent, and calculating cellulose:PLA ratio from dried PLA mass.
- Crystallinity: measured by Dynamic Scanning Calorimetry (DSC) using Discovery DSC25; sample heated/cooled with a specific program (20 °C min−1 ramps, nitrogen purge); crystallinity calculated as (ΔHm − ΔHcc) / ΔH100% × 100, with ΔH100% = 93 J g−1 for PLA.
- Chemical composition: initial teabag chemistry analyzed by pyrolysis coupled to 2D GC and TOF MS (Py-GCxGC-TOF MS) with triplicate analyses per teabag type (A, B, C).
- Instrumentation details: Pyroprobe with DISC, Agilent GC, BenchTOF2-TI MS, INSIGHT flow modulator, specified columns, helium carrier gas, and data processing with ChromSpace; compounds identified against NIST library.
- Samples: teabags from at least five boxes across stores (July–October 2021) to capture variability; tea leaves removed prior to mass measurements; samples preserved at 4°C until analysis.
- Data structure notes: NAN denotes no data; Tbag-C data missing in Degradation_crystallinity.csv and Degradation_PLA.csv.

## Data processing and formulas
- Mass loss percent: 100 − (m / m0) × 100, where m is final mass and m0 is initial mass.
- Cellulose:PLA ratio: calculated from masses following PLA dissolution and drying.
- Crystallinity: computed from DSC results using the equation provided above (ΔHm, ΔHcc, and ΔH100% with PLA reference).

## Data quality, provenance, and context
- QC measures include sourcing teabags from multiple boxes/LOTS and stores; standardized sample handling, drying, and storage (4°C); calibrated analytical balance (four decimal places); DSC enthalpy precision of 0.1%; triplicate Py-GCxGC-TOF MS analyses for each teabag type.
- Teabag brands are anonymised (A, B, C).
- Data accompany the peer-reviewed article: Courtene-Jones et al. 2024, Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms (Science of the Total Environment). DOI: https://doi.org/10.1016/j.scitotenv.2024.172806

## Use and relevance for environmental monitoring
- Provides standardized, multi-faceted measurements (mass loss, crystallinity, PLA content, and detailed chemical composition) to assess environmental degradation of bio-based plastics in soil.
- Facilitates cross-study comparisons and integration with monitoring datasets to evaluate environmental health and policy performance over time.
- Data can inform risk assessments related to soil exposure of bio-based polymers and potential ecological effects (e.g., interactions with soil biota).