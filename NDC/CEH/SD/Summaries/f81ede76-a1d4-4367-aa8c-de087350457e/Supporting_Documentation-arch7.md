# Domestic animal health data from Mambwe District, Zambia (2013)

- Purpose: Report results of a survey assessing African trypanosomiasis, tick-borne infections, and Brucella in domestic livestock, conducted June–August 2013 in Mambwe District, Eastern Zambia. Part of the Dynamic Drivers of Disease in Africa Consortium research project.
- Sampling frame and design: Based on a census of people and animals in Aug 2012 and Oct–Nov 2012. Census recorded 3,717 households, with 1,354 having livestock. Targeted a one-stage cluster survey with predefined parameters (expected cattle trypanosome prevalence, 30%; 90% confidence; 7% precision; homogeneity 0.18) and a target of 139 households.
- Data scope: Laboratory results linked to individual animals; dataset includes species, age, sex, and infection status across multiple pathogens. Data managed in Microsoft Excel with 1/0/ND encoding (positive/negative/not tested).

- Survey design and sampling details:
  - Households selected from census; sampling conducted within the study area (June–August 2013).
  - Animals sampled: cattle, goats, sheep, pigs, and dogs. Distribution: 473 goats, 340 cattle, 246 pigs, 199 dogs, 22 sheep.
  - Age and sex definitions provided to categorize samples (e.g., sexually mature thresholds by species).

- Sample collection and storage:
  - Blood for trypanosomes and tick-borne infections collected from peripheral veins (ear) into heparinised capillary tubes; paired tubes collected per animal.
  - Blood dried on Whatman FTA cards, then stored with desiccant.
  - Brucellosis samples collected from sexually mature animals (except pigs) from jugular or cephalic veins into plain vacutainers; serum stored for testing.
  - Brucella testing samples preserved with and without sodium azide for preservation; tested per OIE 2009 protocol.

- Brucellosis testing:
  - Serum processed into two tubes (plain and with sodium azide); agglutination assessed with standard Rose Bengal–complement fixation-type approach.
  - Protocol adjusted for small ruminants to increase sensitivity (increased serum volume).

- Trypanosomiasis and tick-borne infections laboratory methods:
  - DNA extraction from Whatman FTA cards: six 3 mm discs punched, washed (FTA wash then TE), then eluted with 5% Chelex at 90°C.
  - Trypanosome PCR (ITS PCR, Njiru et al. 2005): detects T. congolense (Kilifi/savannah/forest), Trypanozoon, T. simiae (Tsavo), T. vivax, T. godfreyi; used Biotaq Red or Mango Taq polymerases; positive controls included T. brucei, T. vivax, T. congolense; negative controls with wash controls and sterile water.
  - Gel visualization: 1.5% agarose, GelRed, 100 bp ladder; imaging with a GelDock system.
  - Tick-borne infection PCRs (RLB method): three PCRs targeting Theileria/Babesia (18S rRNA), Ehrlichia/Anaplasma (16S rRNA V1 region), and Rickettsia (16S rRNA); conducted for cattle and dogs.
  - Positive controls (e.g., Theileria parva, Ehrlichia canis, rickettsial DNA); negative controls included autoclaved/UV-inactivated water.
  - Data reporting: results captured as presence/absence per pathogen and per sample; multiple probes per species possible (e.g., Ehrlichia ruminantium_1 and _2).

- Data management and presentation:
  - All laboratory results recorded in Excel; positive = 1, negative = 0, not tested = ND.
  - Table 1 (variables) defines a comprehensive set of pathogen targets and specimen metadata (species, age, sex, multiple Trypanosoma species, multiple Ehrlichia/Anaplasma targets, Theileria/Babesia targets, Rickettsia targets, Brucella, Rose Bengal results).
  - Reporter conventions include catch-all PCR results (EA_CA for Ehrlichia/Anaplasma, TB_CA for Theileria/Babesia, R_CA for Rickettsia) and species-specific primers; some samples may yield positive catch-alls with no single-species positives, indicating potential other species.

- Data structure and GIS considerations:
  - Dataset is animal-level with fields for species, age, sex, and multiple pathogen status indicators; spatial linkage would require household location data (likely from the census) to enable geographic mapping within Mambwe District.
  - One-stage cluster design implies potential weighting or variance considerations when mapping prevalence across units; presence of not-tested (ND) entries should be accounted for in spatial analyses.
  - Strengths for GIS: rich, multi-pathogen infection status by animal and species; lab-validated results with explicit controls; clear data standardization (1/0/ND).
  - Limitations for GIS: explicit geographic coordinates are not stated in this summary; ensure linkage to census household coordinates and accounting for sampling design when creating choropleth or hotspot maps.

- Practical uses for GIS:
  - Map prevalence and co-infection patterns by species, age, and sex at household or sub-district level.
  - Integrate with human wellbeing data (from the same study) to explore spatial disease drivers.
  - Support risk assessment and targeting of veterinary or public health interventions in Mambwe District.