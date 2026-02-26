# Domestic animal health data from Mambwe District, Zambia (2013)

## Overview
- Survey of trypanosomiasis, tick-borne infections and brucellosis in domestic livestock conducted June–August 2013 in Mambwe District, Eastern Zambia.
- Conducted alongside a structured questionnaire on human wellbeing as part of the Dynamic Drivers of Disease in Africa Consortium.
- Data were collected from a sample of households based on a prior census of people and animals (August 2012 and Oct–Nov 2012).

## Survey Design and Sampling
- Population frame: 3,717 households recorded in the census; 1,354 had livestock.
- Target sampling: one-stage cluster survey; sample size determined using expected cattle trypanosome prevalence of 30%, 90% confidence, 7% precision, and a homogeneity rate of 0.18; calculated with C Survey (v2.0).
- Target households: 139.
- Household and animal sampling linked to a broader census frame from 2012.

## Animals Sampled and Sample Sizes
- Species sampled: goats, cattle, pigs, dogs, and sheep.
- Sample sizes: 473 goats, 340 cattle, 246 pigs, 199 dogs, 22 sheep.
- Brucellosis testing: conducted on all sexually mature animals except pigs.
- Brucellosis/testing and handling varied by species and maturity status.

## Field Sampling and Sample Handling
- Blood collection methods:
  - Trypanosomiasis and tick-borne infections: 75 µl heparinised capillary tubes from peripheral ear veins; two tubes per animal; blood spotted onto Whatman FTA cards; cards dried and stored with desiccant.
  - Brucellosis: serum separated from whole blood, stored in plain and Na azide-containing tubes; samples stored in fridge prior to freezing.
- Sexually mature animals defined by species-specific age thresholds (e.g., cattle >12 months, goats >4 months, dogs >7 months, sheep >5 months).
- Brucellosis sampling from jugular vein (ruminants) or cephalic vein (dogs); samples stored in cooler boxes with ice.

## Laboratory Analyses
- Brucellosis
  - Rose Bengal test performed on serum with appropriate positive and negative controls.
  - Protocol adjustments for small ruminants to increase sensitivity (75 µl serum).
- Trypanosomiasis and Tick-borne infections
  - DNA extraction from Whatman FTA cards using a disc-based method; washing steps included with controls.
  - Trypanosome PCR (ITS PCR) to detect T. congolense (Kilifi, Savannah, Forest), Trypanozoon, T. simiae (Tsavo), T. vivax, T. godfreyi; used Biotaq Red DNA polymerase initially, then Mango Taq when Biotaq stopped.
  - Tick-borne infections: reverse line blot (RLB) PCR approach using three target PCRs:
    - 18S rRNA for Theileria and Babesia (TB region)
    - 16S SSU rRNA for Ehrlichia and Anaplasma (EA region)
    - 16S rRNA for Rickettsia (R_CA region)
  - Positive controls included relevant pathogens; negative controls included autoclaved and UV-irradiated PCR water.
- Data generation methods
  - Species- and pathogen-specific primers used; catch-all primers also employed to indicate presence of any species within a genus.
  - Positive control references and detailed primer/probe sets are documented in supporting literature.

## Data Management and Presentation
- Results recorded in Microsoft Excel; coded as 1 (positive), 0 (negative), and ND (not determined/not tested).
- Table 1 describes all variables and their definitions; includes multiple entries for some pathogens where more than one probe was used (e.g., Ehrlichia_ruminantium_1 and _2).
- Data presentation categories for tick-borne infections:
  - EA_CA (Ehrlichia/Anaplasma catch-all)
  - TB_CA (Theileria/Babesia catch-all)
  - B_CA1, B_CA2 (Babesia catch-all or species-specific probes)
  - Theileria and Babesia species-level entries (e.g., Theileria_annulata, Babesia bigemina, etc.)
  - R_CA (Rickettsia catch-all) and species-level entries (e.g., Rickettsia conorii)
  - Rose_Bengal (Brucella serology result)
- The dataset includes ND entries where testing did not occur for a given animal or pathogen.

## Variables Presented in the Dataset (Key Categories)
- Host and demographics: Species (cattle, goats, dogs, etc.), Age (months), Sex (male/female).
- Trypanosoma infections: Trypanosoma_congolense and subtypes (Kilifi, vivax, godfreyi, simiae; including Tsavo designation for simiae).
- Brucellosis: Rose_Bengal result; species-specific brucellosis testing outcomes.
- Tick-borne infections: 
  - EA_CA (Ehrlichia/Anaplasma catch-all) and multiple species-specific entries (e.g., Anaplasma_marginale, Ehrlichia_ruminantium variants, etc.).
  - TB_CA (Theileria/Babesia catch-all) with species-specific entries (Theileria parva, Theileria annu l ata, Babesia canis canis variants, etc.).
  - Rickettsia entries (R_CA catch-all and specific Rickettsia species).
- Data integration considerations: Potential multiple tests per animal; ND entries indicate missing data; use of both catch-all and species-specific probes for comprehensive detection.

## Data Quality, Controls, and Documentation
- Rigorously documented laboratory controls (positive and negative) and procedural steps to minimize contamination and false results.
- DNA extraction, PCR amplification, and gel visualization procedures described to enable reproducibility.
- Clear metadata and variable definitions to facilitate secondary analyses and meta-analyses across species and pathogens.
- Limitations noted include uneven species sample sizes (e.g., only 22 sheep) and not all animals tested for every pathogen, with ND indicating missing data.

## Potential Data Uses for Analysts
- Estimating prevalence of trypanosomes, tick-borne pathogens, and Brucella by species and age/sex strata.
- Investigating co-infection patterns across livestock species.
- Assessing associations between host demographics and infection status.
- Cross-referencing with human wellbeing data from the same study for One Health analyses.
- Evaluating data quality and standardization benefits for regional surveillance in similar settings.