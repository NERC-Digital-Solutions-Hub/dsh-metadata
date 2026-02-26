# Soil organic matter fractions

- The study acknowledges soil organic matter (SOM) as highly heterogeneous and uses density fractionation to separate SOM into pools with differing stability, aligning with common turnover-model fractions: DOC, LF, OF, and MAOM.
- In this work, DOC and OF are discarded for analysis; only LF and MAOM fractions are analyzed for carbon and nitrogen. The OF fraction is derived by mass balance.

## Context: Countryside Survey and UK-SCAPE

- Countryside Survey is a long-running UK assessment of natural resources, with a rolling monitoring program initiated in 2019 and continuing to 2023.
- UK-SCAPE funds this phase to monitor soil condition and changes across GB, focusing on topsoil properties and co-located vegetation data.
- The rolling design samples 500 1-km2 squares over five years, with 100 squares visited annually, selected across landscape strata and excluding squares >75% urban or >90% sea.
- Soil sampling occurs within each square using vegetation-linked X-Plots; samples are collected as 15 cm cores and archived for later analysis (100 samples analyzed for SOM fractionation in spring 2022).

## Sampling design and scope

- 500 x 1-km2 squares sampled over five years; 100 squares visited each year.
- Randomly selected squares exclude predominantly urban or sea areas.
- Within each square, up to 5 fixed locations provide soil samples for analysis; samples are co-located with vegetation surveys.
- Topsoil density fractionation and related measurements were performed on archived samples (2 mm sieved, air-dried).

## Laboratory methods and fractions

- SOM density fractionation used sodium polytungstate (SPT) with density adjusted to 1.8 g cm-3 to separate LF (light particulate) and MAOM (mineral-associated) fractions; the OF fraction is recovered by mass balance after LF and MAOM are determined.
- Dissolved organic carbon (DOC) and the OF fraction are not analyzed in this dataset; DOC is discarded, OF is calculated by difference.
- LF fraction: isolated by filtration after density separation and drying; MAOM fraction: residual material after LF removal is washed and dried.
- Total carbon and total nitrogen measured on LF and MAOM fractions, plus a subsample of archived soil using an Elementar Vario-Elemenal analyzer (UKAS SOP3102).
- LOI (loss-on-ignition) via TG/DTGA analysis (TGA701) to determine SOM content, hygroscopic water content, and CaCO3 content through multi-step heating (25–1000°C).
- CaCO3-derived carbon content corrected for calcite-C, using a 2.27 factor derived from CaCO3 decomposition.
- SOC (soil organic carbon) calculated as total carbon minus calcite-C; LF-C and MAOM-C derived from LF/MAOM masses and their carbon percentages; POM-C and OF-C derived by mass balance and correction for hygroscopic water.
- Fractions defined and calculated:
  - LF-C, MAOM-C, OF-C, POM-C
  - LF-N, MAOM-N, OF-N, POM-N
  - SOC (corrected for calcite-C); TN
- Data corrections:
  - Hygroscopic water content correction applied to LF, MAOM, SOC; OF and POM corrected through mass-based calculations.
  - Cases where OF-C or OF-N calculated negative due to measurement uncertainty set to zero before deriving POM-C/N.
- Divisions and relationships:
  - OF-C and OF-N derived by difference: SOC minus LF-C minus MAOM-C; OF-N similarly
  - POM-C and POM-N computed as LF-C + OF-C and LF-N + OF-N, with corrections as necessary.

## Data structure and fields

- Dataset contains 13 columns and 101 rows; no-analysis entries marked NA.
- Key fields include:
  - Year, SQ_ID (square identifier)
  - LF_C_gperg, MAOM_C_gperg, OF_C_gperg, POM_C_gperg (carbon fractions; g C per g soil)
  - LF_N_gperg, MAOM_N_gperg, OF_N_gperg, POM_N_gperg (nitrogen fractions; g N per g soil)
  - SOC_gperg (soil organic carbon per g)
  - TN_gperg (total nitrogen)
  - SOM_gperg (SOM as g per g, measured by LOI)
- Data provenance notes:
  - LF, MAOM fractions measured; OF derived by mass balance
  - DOC not included in this dataset

## Quality control and data corrections

- Quality controls include two internal standards per batch and 10% replicated samples to assess accuracy and precision.
- Corrections applied for hygroscopic water content and for inorganic carbon (calcite-C) in MAOM and SOC fractions.
- Negative OF-derived values adjusted to zero to reflect measurement uncertainty; mass-balance derived fractions (POM, OF) rely on corrected inputs.
- Detailed methodology and QA/QC steps described in the full method (Reinsch et al. 2024).

## Data availability, provenance, and accessibility

- Part of the UK-SCAPE program; datasets published through UKCEH and archived in the NERC Environmental Data Centre (NERC EDS) / Environmental Information Data Centre (EIDC).
- Related topsoil physico-chemical properties for GB Great Britain 2018–2019 and 2020 (with updated v2) data published (Bentley et al., 2023a,b).
- Funding: UK-SCAPE (NE/R016429/1) with contributions from AI4SoilHealth project (Grant No. 101086179).

## Usage notes and caveats for data stewards

- The dataset provides LF and MAOM carbon/nitrogen fractions, plus SOC and LOI-based SOM, for 101 samples from 2019–2020 (archived samples measured in 2022); OF and DOC are not directly measured but OF is inferred via mass balance.
- Data are part of a rolling GB soil monitoring program; users should consider the five-year rolling sampling window and potential year-to-year variability when aggregating across years.
- Unit consistency and documentation are crucial: fractions are expressed as g per g (mass fractions); LOI-based SOM is reported as g per g; any aggregation should consistently use the same units.
- Data quality relies on calibration against internal standards, replication, and corrections for hygroscopic water and calcite-C; users should review QA notes and provenance when integrating with other datasets.
- For further methodological detail and data usage guidance, refer to Reinsch et al. 2024 (full SOM fractionation protocol) and the UK-SCAPE and Countryside Survey data products (Bentley et al. 2023a,b; Scott 2008; Reynolds et al. 2013).