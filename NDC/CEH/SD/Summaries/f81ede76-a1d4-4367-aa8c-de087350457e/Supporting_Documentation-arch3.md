# Domestic animal health data from Mambwe District, Zambia (2013)

- Overview
  - Aimed to survey domestic livestock for trypanosomiasis, tick-borne infections, and brucellosis in Mambwe District, Eastern Zambia (June–August 2013).
  - Part of the Dynamic Drivers of Disease in Africa Consortium; linked to a human wellbeing survey.
  - Based on a census-based sampling frame from August 2012 and October–November 2012; 3717 households recorded, 1354 with livestock.
  - Target sample size: 139 households (one-stage cluster design) with assumptions of 30% cattle trypanosome prevalence, 90% confidence, 7% precision, and homogeneity 0.18.
  - Actual scope described: comprehensive laboratory testing and data collection across multiple species.

- Survey design
  - One-stage cluster survey using a frame from a full census of people and animals.
  - Sample size calculated with C Survey (v2.0); target 139 households.
  - Data collection coordinated with a parallel human wellbeing survey.

- Sample collection and storage
  - Species and tests by animal type:
    - Cattle and dogs: tested for African trypanosomes, tick-borne infections, and Brucella.
    - Goats and sheep: tested for African trypanosomes and Brucella.
    - Pigs: tested for African trypanosomes only.
  - Blood collection:
    - For trypanosomiasis and tick-borne infections: 75 µl heparinised capillary tubes from ear veins; two tubes per animal; blood transferred to Whatman FTA Cards; cards dried and stored with desiccant.
    - For Brucellosis: blood collected into plain vacutainers (jugular for ruminants; cephalic for dogs); serum separated, stored in two tubes (one plain, one with sodium azide) and refrigerated before freezing.
  - Sampling details:
    - Sexually mature animals designated by age thresholds (goats > 4 months; cattle > 12 months; dogs > 7 months; sheep > 5 months).
    - Sample sizes: 473 goats, 340 cattle, 246 pigs, 199 dogs, 22 sheep.

- Brucellosis
  - Serological testing performed on sera using standard World Organisation for Animal Health (OIE) 2009 method.
  - Procedure:
    - Spots with 25 μl antigen placed on a tile; 25 μl serum added; 4-minute incubation observed for agglutination.
    - For small ruminants, protocol modified to use 75 μl serum to increase sensitivity.
    - Negative control (sterile saline) used; daily positive control with kit-provided antigen.
  - Sample handling:
    - Serum stored in two tubes (plain and sodium azide–mixed) for preservation.
    - Brucella testing conducted on cattle and dogs as part of the study.

- Trypanosomiasis and Tick-borne Infections
  - Sample preparation and DNA extraction:
    - DNA extracted from Whatman FTA card; five 3 mm discs punched per sample; discs washed with FTA wash and TE buffer; wash controls included.
    - Elution performed with 100 μl of 5% Chelex; heating at 90°C for 30 minutes.
  - Trypanosome PCR (ITS PCR):
    - Detects T. congolense (Kilifi/savannah/forest), Trypanozoon, T. simiae (Tsavo), T. vivax, and T. godfreyi.
    - Primers: as described by Njiru et al. (2005); positive controls included T. brucei and T. vivax/congolense DNA.
    - Visualization via 1.5% agarose gel; imaging with GelDock system.
  - Tick-borne infection PCRs (Reverse Line Blot; RLB PCR):
    - Three PCRs per sample:
      - 18S rRNA gene fragment (460–540 bp) for Theileria and Babesia (TB_CA).
      - 16S SSU rRNA gene (460–520 bp) for Ehrlichia and Anaplasma (EA_CA).
      - 16S rRNA gene (350–400 bp) for Rickettsia (R_CA).
    - Positive controls included DNA from relevant pathogens; negative controls used autoclaved UV-treated PCR water.
    - Targets cover multiple species within each genus; “catch-all” primers included to detect broader groups.
  - Data handling for results:
    - Results recorded in Microsoft Excel; coded as 1 (positive), 0 (negative), or ND (not determined).
    - Some animals tested with two different probe sets for the same genus/species (e.g., Ehrlichia ruminantium_1 and _2).

- Data management and presentation
  - Laboratory results were compiled into a dataset with explicit variable definitions (see Table 1 in the resource).
  - Data structure accommodates multiple test modalities (species-specific and catch-all PCR results) and cross-species comparisons.
  - Quality controls embedded in laboratory workflow:
    - Use of blank/disc wash controls at intervals, positive controls, and appropriate negative controls to ensure reliability.
  - Data gaps and uncertainty acknowledged via ND coding; detailed metadata accompany the dataset to aid interpretation and reuse.

- Dataset variables (Table 1) - key categories
  - Species and host category (Cattle, sheep, goats, dogs, pigs) and age/sex definitions.
  - Trypanosoma spp. variables (e.g., T. congolense, Kilifi, T. vivax, T. brucei s.l., T. godfreyi, T. simiae and subtypes).
  - Tick-borne infections groupings (EA_CA for Ehrlichia/Anaplasma; TB_CA for Theileria/Babesia; R_CA for Rickettsia) and species-specific entries (e.g., Ehrlichia ruminantium, Anaplasma spp., Theileria spp., Babesia spp., Rickettsia spp.).
  - Specific pathogen names and variant designations (e.g., Ehrlichia sp. Omatjenne, Theileria parva, Babesia bigemina, Babesia canis canis, etc.).
  - Additional entries include Brucella-related results (Rose Bengal) and a Rose Bengal–related status indicator.

- References
  - Bekker CP et al. 2002; Blasco JM et al. 1994; Georges K et al. 2001; Kong F, Gilbert GL 2006; Lorusso V et al. 2016; Nijhof AM et al. 2007; Njiru ZK et al. 2005; World Organisation for Animal Health 2009.