# Substrate utilisation profiles for saprotrophic fungi and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland, 2001 [NERC Soil Biodiversity Programme] - Supporting Information

## Overview

- Part of the NERC Soil Biodiversity Thematic Programme (launched 1999) focused on understanding soil biodiversity and the functional roles of soil organisms in key ecological processes.
- The Sourhope field experiment examined how decomposer (saprotrophic) fungi contribute to organic matter decomposition across diverse taxa and functional capabilities.
- Data include substrate utilisation profiles of saprotrophic fungi and soil moisture content, collected to link fungal diversity and function with decomposition processes.

## Data collected and purpose

- Substrate utilisation profiles for saprotrophic fungi (via BIOLOG method) to characterize functional capabilities across carbon sources.
- Soil moisture content data from soils sampled in July 2001.
- Metadata on site conditions, treatments, soil horizons, and sampling design to support interpretation of fungal function in relation to environmental factors.

## Methods and data collection

- Site: Sourhope, Roxburghshire, upland grassland at ~309 m elevation; brown forest soil; mean temp ~7.8°C; mean annual rainfall ~952 mm; vegetation dominated by several grasses.
- Experimental design: five replicates per treatment across plots with treatments including Control, Lime (CaCO3), Nitrogen (NH4NO3), and Lime+Nitrogen.
- Sampling and isolation:
  - Soil cores collected from litter fermentation (LF), humus (H), and mineral (A) horizons.
  - Fungal cultures isolated using Warcup soil plating methods; identifications confirmed by sequencing ITS regions.
  - Isolation frequencies calculated as percentages when multiple replicate plates yielded a taxon.
- Functional assays:
  1) Isolation and preliminary characterization of fungi from soil and standing-dead litter.
  2) Utilisation of specific substrates (cellulose, lignin, pectin, starch, chitin) on semi-defined media to assess differential substrate use.
  3) Utilisation of 95 low molecular weight carbon sources using BIOLOG SF-N2 plates for 12 isolates (6 frequent, 6 occasional), to generate detailed functional profiles.
  4) BIOLOG SF-N2 analyses extended with 12 isolates to compare functional capabilities within putative guilds; inoculum standardized for reproducibility.
- Data handling:
  - Inoculum density standardized to 0.22 absorbance at 590 nm for BIOLOG assays.
  - Plates incubated at 15°C; absorbance read periodically up to 25 days.
  - Total activity in BIOLOG assays used as a proxy for overall carbon utilisation capacity.

## Data structure and content

- Dataset 1105: Percentage Soil Moisture Content (P2111_PERCENT_SOIL_MOISTURE.csv)
  - Fields include ROWNO, SUID, SAMPLE_DATE, BLOCK, MAIN_PLOT, TREATMENT, HORIZON, weights, dry weights, and PERCENTAGE_MOISTURE.
- Dataset 1130: Substrate utilisation assay (BIOLOG_RESULTS.csv)
  - Fields include SPECIESID, REPLICATE, TIME, ISOLATE_TYPE, BIOLOGCELLID, OPTICAL_DENSITY.
- Dataset 1131: Details of BIOLOG SF-N2 microplates (BIOLOG_INFORMATION.csv)
  - Fields include BIOLOGCELLID, SUBSTRATE, SUBSTRATE_TYPE.
- Dataset 1132: Species examined (BIOLOG_SPECIES.csv)
  - Fields include SPECIESID, SPECIES_NAME.
- Data are accompanied by QA statements; full methodological details are provided in the cited Deacon et al. (2006) paper and the Sourhope Field Data Handbook.

## Findings and interpretation

- Functional redundancy: abundantly cultured fungi largely utilized similar substrates, indicating overlap in functional capabilities.
- Role of infrequent taxa: despite lower occurrence, infrequent taxa showed higher potential activity, broader substrate use, and greater competitiveness, suggesting important roles in decomposition.
- Interactions within communities: co-occurrence of abundant and occasional taxa sometimes enhanced decomposition (e.g., cellulose degradation) while competition could reduce lignin degradation.
- Temporal resilience: occasional taxa may confer resilience to decomposition processes, potentially compensating for changes in dominant taxa.
- Broader diversity: uncultured or unstudied taxa may contribute additional functional diversity not captured in the study.

## Data quality, sharing, and governance

- Public data sharing: data are provided with accompanying metadata; underlying data are subject to quality assurance, but no warranty on accuracy by NERC.
- Data usage: researchers are responsible for assessing fitness for intended use; data providers disclaim liability for misuse or misinterpretation.
- Metadata and accessibility: metadata completeness is essential for reuse; some barriers exist related to data sharing formats and standardization.
- Data governance: procedures described include data cleaning, transformation, and clear presentation of findings; data management standards emphasized, though sharing may require navigating governance constraints.

## Related references and notes

- Deacon, L.J., et al. 2006. Diversity and function of decomposer fungi from a grassland soil. Soil Biology and Biochemistry, 38(1), 7-20.
- Sourhope Field Data Handbook (2003); available via EIDC catalogue record.
- Usher, M.B., et al. 2006. Understanding biological diversity in soil: UK Soil Biodiversity Research Programme. Applied Soil Ecology, 33(2), 101-113. DOI: 10.1016/j.apsoil.2006.03.006