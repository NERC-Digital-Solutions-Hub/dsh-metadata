# Domestic animal health data from Mambwe District, Zambia (2013)

## Overview
- Report of a livestock health survey (trypanosomiasis, tick-borne infections, and brucellosis) conducted June–August 2013 in Mambwe District, Eastern Zambia.
- Integrated with a human wellbeing survey as part of the Dynamic Drivers of Disease in Africa Consortium.
- Aimed at providing standardized data to monitor environmental health and policy performance over time, focusing on data verification, quality assurance, and clear outputs (datasets, reports, maps, charts).

## Study design and sampling
- Sampling frame based on a full census of people and animals from August 2012 and October–November 2012.
- Census: 3,717 households; 1,354 with livestock.
- Target sample: 139 households for one-stage cluster survey, with assumptions of 30% trypanosome prevalence in cattle, 90% confidence, 7% precision, and 0.18 homogeneity.
- Sample size calculated using C Survey (v2.0).

## Household and animal sampling
- Species and numbers sampled: 473 goats, 340 cattle, 246 pigs, 199 dogs, 22 sheep.
- Sampling specifics by species:
  - Cattle and dogs: tested for African trypanosomes, tick-borne infections, and Brucella.
  - Goats and sheep: tested for African trypanosomes and Brucella.
  - Pigs: tested for African trypanosomes only.
- Blood collection:
  - Trypanosomiasis and tick-borne infections: 75 µl heparinised capillary tubes from ear veins; two tubes per animal; onto Whatman FTA Cards; drying and storage with desiccant.
  - Brucellosis: serum separated into plain and sodium azide–mixed tubes; stored before freezing; additional sampling from sexually mature animals (excluding pigs) via jugular (ruminants) or cephalic (dogs) veins; stored in vacutainers with ice.

## Laboratory analyses

### Brucellosis
- Serology: Rose Bengal–type agglutination test following OIE (2009) guidelines; modifications for small ruminants (75 µl serum) to improve sensitivity.
- Controls: negative saline controls; daily positive controls supplied with test kit.

### Trypanosomiasis and tick-borne infections
- Sample preparation: DNA extracted from Whatman FTA cards; discs washed with FTA wash and TE buffer; Chelex extraction with heating at 90°C.
- Trypanosome PCR (ITS PCR, Njiru et al., 2005): detects T. congolense (Kilifi/savannah/forest), Trypanozoon, T. simiae (Tsavo), T. vivax, T. godfreyi; positive controls (T. brucei, T. vivax, T. congolense); gel-based visualization.
- Tick-borne infections (RLB PCR): three PCR targets per sample
  - 18S rRNA (Theileria and Babesia spp.)
  - 16S rRNA (Ehrlichia and Anaplasma spp.)
  - 16S rRNA (Rickettsia spp.)
- Species and genus coverage: cattle and dogs only; includes multiple Theileria, Babesia, Anaplasma, Ehrlichia, and Rickettsia species with both catch-all and species-specific probes.
- Controls: positive controls using known pathogen DNA; negative controls with PCR water treated and irradiated; process described with references for validation.

## Data management and presentation
- All laboratory results recorded in Microsoft Excel.
- Encoding: positive = 1, negative = 0, not tested = ND.
- Variables and dataset structure described (Table 1 in document), including:
  - Pathogens at species/complex level (e.g., Trypanosoma_congolense, T. vivax, etc.).
  - Tick-borne pathogen groups (EA_CA, TB_CA, with multiple specific targets).
  - Specific pathogens (e.g., Ehrlichia ruminantium, Anaplasma phagocytophilum, Babesia bigemina, Rickettsia spp., etc.).
  - Distinguishing between catch-all PCR results and species-specific results.
- Sample metadata includes animal-level attributes: species, age (months), sex, and age/sex definitions used for brucellosis sampling.

## Relevance for environmental monitoring
- Provides baseline, methodologically standardized data on livestock diseases linked to environmental and ecological drivers (vector presence, wildlife interfaces, husbandry practices).
- Facilitates temporal comparisons and integration with human wellbeing data within One Health frameworks.
- Data standardization and clear methodological documentation support reuse, quality assurance, and transparent reporting for policy evaluation and environmental health monitoring.

## References and methodological grounding
- Methods align with established guidelines and prior studies on trypanosome and tick-borne pathogen detection (e.g., Njiru 2005; Georges et al. 2001; Bekker et al. 2002; Lorusso et al. 2016; Blasco et al. 1994; OIE 2009).
- Technical specifics and controls described to ensure data reliability and comparability across monitoring efforts.