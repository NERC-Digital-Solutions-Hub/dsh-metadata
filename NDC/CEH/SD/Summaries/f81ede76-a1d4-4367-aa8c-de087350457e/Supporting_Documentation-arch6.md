# Domestic animal health data from Mambwe District, Zambia (2013)

## Overview
- This resource reports results from a 2013 survey of domestic livestock for African trypanosomiasis, tick-borne infections, and brucellosis in Mambwe District, Eastern Zambia.
- Conducted alongside a human wellbeing questionnaire as part of the Dynamic Drivers of Disease in Africa Consortium.
- Sampling based on a census of people and animals conducted in 2012; the study area included 3717 households, 1354 of which had livestock.

## Sampling design
- Target sample size: 139 households (one-stage cluster survey) using a prevalence assumption of 30% for cattle trypanosomes, 90% confidence, 7% precision, and homogeneity of 0.18.
- Sample size determined with C Survey (v2.0).

## Sample collection and storage
- Animal species sampled:
  - Cattle and dogs: African trypanosomes, tick-borne infections, Brucella
  - Goats and sheep: African trypanosomes, Brucella
  - Pigs: African trypanosomes only
- Blood collection and processing:
  - For trypanosomiasis and tick-borne infections: 75 µl heparinised capillary tubes from ear vein; two tubes per animal; blood applied to Whatman FTA Card; cards dried and stored with desiccant.
  - For Brucellosis: additional samples from sexually mature animals collected from jugular (ruminants) or cephalic vein (dogs); serum split into two tubes (plain and with sodium azide); stored refrigerated prior to freezing.
- Sexually mature age thresholds:
  - Goats > 4 months
  - Cattle > 12 months
  - Dogs > 7 months
  - Sheep > 5 months
- Sample counts: 473 goats, 340 cattle, 246 pigs, 199 dogs, 22 sheep.

## Brucellosis testing
- Serum processed into two tubes (plain and with sodium azide) and stored in a fridge prior to freezing.
- Laboratory testing followed OIE (2009) standard methods:
  - Antigen spots on a tile with serum; agglutination read after four minutes.
  - Small ruminants tested with 75 µl serum to increase sensitivity.
  - Negative control: sterile saline; positive control: kit antigen.

## Trypanosomiasis and tick-borne infections testing
- Sample preparation for molecular assays:
  - DNA extracted from Whatman FTA cards by punching discs, washing with FTA wash and TE buffer, using blank wash controls, then eluting DNA with 5% chelex at 90°C.
- Trypanosome PCR:
  - ITS PCR used to detect multiple Trypanosoma species (e.g., T. congolense lineages, T. vivax, T. evansi, T. godfreyi, T. simiae).
  - Polymerases evolved from Biotaq Red to Mango Taq; positive controls included DNA from parasites; negative controls used wash controls and water controls.
  - Products visualised on 1.5% agarose gel with a 100 bp ladder.
- Tick-borne infection PCRs (reverse line blot, RLB):
  - Three PCRs per sample:
    - 18S rRNA fragment for Theileria and Babesia (460–540 bp)
    - 16S SSU rRNA V1 region for Ehrlichia and Anaplasma (460–520 bp)
    - 16S rRNA for Rickettsia (350–400 bp)
  - Positive controls included species like Theileria parva, Ehrlichia canis, and Rickettsia spp.; negative controls used autoclaved, UV-irradiated PCR water.
- Data handling for lab results:
  - Results recorded in Excel as 1 (positive), 0 (negative), or ND (not determined).
  - Some animals had multiple probe sets for the same species (e.g., Ehrlichia ruminantium_1 and _2).

## Data management and variables
- Dataset structure: includes variables for species (cattle, goats, dogs, etc.), animal age, sex, and pathogen results.
- Key variable groups (example entries from Table 1):
  - Trypanosoma_congolense, Trypanosoma_congolense_Kilifi, Trypanosoma_vivax, Trypanosoma_brucei, Trypanosoma_godfreyi, Trypanosoma_simiae (and subtypes)
  - EA_CA (Ehrlichia and Anaplasma catch-all), Ehrlichia_ruminantium_1, Ehrlichia_ruminantium_2, Ehrlichia_sp._Omatjenne, Ehrlichia_chaffeensis, Anaplasma_bovis, Anaplasma_marginale, etc.
  - TB_CA (Theileria and Babesia catch-all), Theileria_parva, Babesia_bigemina, Babesia_bovis, Babesia_divergens, etc.
  - R_CA (Rickettsia catch-all), Rickettsia_conorii, Rickettsia_helvetica, Rickettsia_massiliae, etc.
  - Brucella_abortis/melitensis (Rose_Bengal)
- Data interpretation notes:
  - A “catch-all” PCR result may be positive with species-specific primers negative, suggesting a different species within the genus.
  - The dataset includes both species-specific and catch-all results, enabling broader pathogen surveillance.

## Timeline
- Fieldwork conducted from June to August 2013.

## Data Uses and implications (data-support perspective)
- Provides a rich, multi-pathogen livestock health dataset suitable for cross-species analysis and surveillance.
- Supports development of dashboards or self-service tools to explore pathogen prevalence by species, age, sex, and location, with clear data quality controls (blank/wash controls, positive/negative controls).
- The structured, Excel-based dataset with explicit coding (1/0/ND) facilitates reuse, sharing, and iterative product development, aligning with needs to transform complex lab results into understandable end-user outputs.