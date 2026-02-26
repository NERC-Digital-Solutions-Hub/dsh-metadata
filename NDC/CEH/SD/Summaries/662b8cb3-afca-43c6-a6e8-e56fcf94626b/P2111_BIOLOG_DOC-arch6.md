# Substrate utilisation profiles for saprotrophic fungi and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland, 2001 [NERC Soil Biodiversity Programme] - Supporting Information

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999–2001) at Sourhope, Scottish Borders.
- Aimed to understand soil biota diversity and the functional roles of soil organisms in key ecological processes.
- 24 research projects studied soil structure, carbon and nitrogen cycles, micro- and macro-fauna, with a focus on decomposer fungi (saprotrophs).

## Data collected
- Substrate utilisation profiles for saprotrophic fungi (BIOLOG method) and soil moisture content.
- Collected from main Sourhope field plots in July 2001.
- Includes data from multiple soil horizons (Standing-dead litter LF, humus H, mineral A) and various treatments.
- Data files provided as four comma-separated values (CSV) datasets.

## Datasets and structure
- Dataset 1105: Percentage Soil Moisture Content (P2111_PERCENT_SOIL_MOISTURE.csv)
  - Fields include: ROWNO, SUID, SAMPLE_DATE, BLOCK, MAIN_PLOT, TREATMENT, HORIZON, plus weights and TOTAL_DRYWEIGHT and PERCENTAGE_MOISTURE.
- Dataset 1130: Substrate utilisation assay using BIOLOG SF-N2 microplates (P2111_BIOLOG_RESULTS.csv)
  - Fields include: SPECIESID, REPLICATE, TIME, ISOLATE_TYPE, BIOLOGCELLID, OPTICAL_DENSITY.
  - Replicates and time-series absorbance readings at 590 nm, plates incubated at 15°C.
- Dataset 1131: Details of the BIOLOG SF-N2 microplates (P2111_BIOLOG_INFORMATION.csv)
  - Fields include: BIOLOGCELLID, SUBSTRATE, SUBSTRATE_TYPE.
- Dataset 1132: Details of species examined with BIOLOG SF-N2 microplates (P2111_BIOLOG_SPECIES.csv)
  - Fields include: SPECIESID, SPECIES_NAME.

## Methods
- Isolation of fungal cultures
  - Field site: Sourhope upland grassland (309 m a.s.l., mean temp 7.8°C, precipitation 952 mm).
  - Treatments: Control, Lime (CaCO3), Nitrogen (NH4NO3), Lime + Nitrogen; pit sampling with horizons LF, H, A.
  - Isolation by Warcup soil plating method to estimate fungal occurrence frequency; identifications confirmed via sequencing (ITS regions) or external labs.
- Substrate utilisation assays
  - Phase 1: 48 isolates tested for utilisation of substrates (cellulose, lignin, pectin, starch, chitin) on semi-defined solid media.
  - Phase 2: 12 isolates selected (abundant vs occasional) for detailed BIOLOG SF-N2 95-carbon-source profiling.
  - Inoculum standardisation: spores/mycelial fragments in carageenan alginate matrix, adjusted to OD590 ~0.22, with MTT for color development.
  - BIOLOG testing: 3 replicates per taxon; plates inoculated and incubated at 15°C; readings up to 25 days; total activity (sum of OD across wells) used as a metric of carbon utilisation.
- Data processing and interpretation
  - Comparison of abundant vs occasional taxa; evaluation of functional diversity and potential guild structure.
  - Observed patterns of redundancy and niche differentiation; potential positive/negative interactions when taxa are co-inoculated on litter.

## Findings (highlights)
- High functional redundancy among culturable decomposer fungi; both frequent and infrequent taxa utilize similar substrates.
- Infrequent taxa can be more active and utilise a wider range of substrates.
- When abundant and occasional taxa from the same guild were combined, small positive effects on decomposition and cellulose degradation were observed; some negative effects on lignin degradation potentially due to interspecific interactions.
- Occasional taxa may contribute to temporal resilience of decomposition; greater overall functional diversity could be achieved by uncultured taxa not studied here.

## Quality, limitations and usage notes
- Data are subject to quality assurance procedures; no warranty on accuracy by NERC.
- Data relate to culturable fungi and may not capture the full soil microbial diversity.
- Caution advised when extrapolating to non-cultivable taxa or broader ecosystems.
- Related publications provide broader context and interpretation (e.g., Deacon et al., 2006).

## Related resources and references
- Deacon, L.J. et al. 2006. Diversity and function of decomposer fungi from a grassland soil. Soil Biology and Biochemistry, 38(1), 7-20.
- Sourhope Field Data Handbook (2003) and related UK Soil Biodiversity Programme literature (Usher et al., 2006).
- Supporting information available through the EIDC catalogue record and linked publications.