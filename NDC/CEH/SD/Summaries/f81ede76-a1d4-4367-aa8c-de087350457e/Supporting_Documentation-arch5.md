# Domestic animal health data from Mambwe District, Zambia (2013)

## Overview
- Reports results from a 2013 survey on African trypanosomiasis, tick-borne infections, and brucellosis in domestic livestock in Mambwe District, Eastern Zambia.
- Conducted June–August 2013 alongside a human wellbeing survey as part of the Dynamic Drivers of Disease in Africa Consortium.
- Sampling frame based on a census of people and animals conducted Aug 2012 and Oct–Nov 2012; 3717 households recorded, 1354 with livestock.
- Target sample size for a one-stage cluster survey was 139 households, assuming 30% trypanosome prevalence in cattle, 90% confidence, 7% precision, and 0.18 homogeneity.

## Survey Design
- One-stage cluster sampling from a census-based frame.
- Household-level sampling with animal sampling across multiple species (cattle, goats, sheep, dogs, pigs).

## Sampling & Specimen Collection
- Animal sampling: June–August 2013.
- Species sampled: cattle, dogs (for all tested targets); goats and sheep (trypanosomes and brucellosis); pigs (trypanosomes only).
- Blood collection:
  - For trypanosomiasis and tick-borne infections: 75 µl heparinised capillary tubes from peripheral ear veins; two tubes per animal; blood spotted onto Whatman FTA Cards; cards dried and stored with desiccant.
  - For brucellosis: serum separated and stored in two tubes (plain and with sodium azide); stored refrigerated then frozen.
- Adult animal age thresholds used for sexually mature designation:
  - Goats > 4 months; cattle > 12 months; dogs > 7 months; sheep > 5 months.
- Sample counts:
  - Goats: 473
  - Cattle: 340
  - Pigs: 246
  - Dogs: 199
  - Sheep: 22

## Brucellosis Testing
- Serum tested using standard World Organisation for Animal Health (OIE) 2009 protocol:
  - Spots of 25 µl antigen applied, serum added, and agglutination assessed after 4 minutes.
  - For small ruminants, increased sensitivity used 75 µl serum per spot.
- Controls:
  - Negative control: sterile saline.
  - Positive control: antigen provided with test kit (tested daily).
- Sample preservation: serum split between plain and sodium azide-treated tubes to improve preservation.

## Trypanosomiasis and Tick-borne Infections: Laboratory Methods
- DNA extraction from Whatman FTA cards:
  - Five 3 mm discs punched from FTA card; washed with FTA wash and TE buffer with controls; discs dried and DNA eluted with 100 µl of 5% Chelex, 90°C for 30 minutes.
- Trypanosome PCR:
  - ITS PCR (Njiru et al., 2005) used to detect multiple Trypanosoma spp (T. congolense Kilifi/Savannah/Forest, Trypanozoon, T. simiae Tsavo, T. vivax, T. godfreyi).
  - Polymerases: Biotaq Red initially, later Mango Taq.
  - Controls: positive (DNA from T. brucei, T. vivax, T. congolense) and negative (wash controls, nuclease-free water).
  - Visualization: 1.5% agarose gel with GelDock imaging; 100 bp ladder for sizing.
- Tick-borne infection PCRs (RLB approach):
  - Three PCR targets per sample:
    - Theileria and Babesia (18S rRNA) – 460–540 bp.
    - Ehrlichia and Anaplasma (16S rRNA V1 region) – 460–520 bp.
    - Rickettsia (16S rRNA) – 350–400 bp.
  - Species covered include Theileria spp., Babesia spp., Ehrlichia spp., Anaplasma spp., and Rickettsia spp.
  - Only cattle and dogs were examined for tick-borne infections.
- Controls for RLB:
  - Positive: DNA from known pathogens (e.g., Theileria parva, Ehrlichia canis, Rickettsia spp. similar to R. africae).
  - Negative: PCR water that was autoclaved and UV-irradiated.

## Data Management & Dataset Structure
- Laboratory results recorded in a Microsoft Excel file.
- Binary coding: positive = 1, negative = 0; not tested = ND.
- Some animals tested with two different probe sets; e.g., Ehrlichia ruminantium_1 and Ehrlichia ruminantium_2.
- Data presentation includes both catch-all assay results and species-specific results; discordant results (catch-all positive but no species-specific positive) suggest presence of other species within a genus.

## Variables in Dataset (Table 1)
- Species: cattle, sheep, dogs, goats (definition of animal type).
- Age: age in months at sampling.
- Sex: male or female.
- Trypanosoma targets: congolense (and Kilifi), vivax, brucei, godfreyi, simiae (and Tsavo), evansi.
- Tick-borne infections: EA_CA (Ehrlichia/Anaplasma catch-all), Theileria/Babesia (TB_CA), Babesia (B_CA1, B_CA2), Theileria (T_CA and several species like annulata, buffeli, equi, parva, taurotragi, velifera, MSD4, duiker), Rickettsia (R_CA) and specific species (e.g., R. conorii, R. massiliae, Rickettsia sp. DnS14/raoulti, R. helvetica, etc.).
- Brucella: Rose_Bengal (Brucella abortus and B. melitensis).
- The table includes both broad “catch-all” PCR results and species-specific probes, enabling identification of the presence of pathogen groups and specific species where detected.

## Data Quality, Provenance & Documentation
- Clear documentation of sampling design, specimen handling, and laboratory workflows.
- Detailed description of QA controls (positive/negative controls for both PCR and serology).
- Explicit notes on how results are encoded and how to interpret discordant results between catch-all and species-specific assays.
- Multiple references provided for the PCR and RLB methods used (context for reproducibility and potential method harmonization).

## Data Access, Sharing & Usage Considerations for Data Stewards
- Data stored in an Excel spreadsheet with a comprehensive data dictionary (Table 1) and clear variable naming.
- Note potential harmonization needs due to:
  - Use of multiple probe sets for the same species.
  - Combination of catch-all and species-specific results requiring careful interpretation.
- Metadata captured includes sampling dates, species, age, sex, and laboratory methodologies, supporting traceability and reproducibility.
- Considerations for future use:
  - Preserve linkage between sample IDs, animal demographics, and lab results.
  - Standardize pathogen variable names for interoperability with other datasets.
  - Maintain full documentation of laboratory protocols and control outcomes to support auditability and re-analysis.

## Limitations & Challenges
- Incomplete alignment between catch-all PCR results and species-specific PCR outcomes may require careful harmonization.
- Methodological variations across pathogen targets and the use of older PCR/protocols may affect comparability with newer datasets.
- Data scope limited to sampled households and specific animal species; subset analyses may be necessary for cross-species comparisons.

## References
- Bekker CP, de Vos S, Taoufik A, Sparagano OA, Jongejan F (2002). Simultaneous detection of Anaplasma and Ehrlichia species in ruminants and detection of Ehrlichia ruminantium in Amblyomma variegatum ticks by reverse line blot hybridization. Vet Microbiol. 89:223-38.
- Blasco JM, et al. (1994). Efficacy of different Rose Bengal and complement fixation antigens for the diagnosis of Brucella melitensis infection in sheep and goats. Vet Rec 134:415-420.
- Georges K, et al. (2001). Detection of haemoparasites in cattle by reverse line blot hybridisation. Vet Parasitol. 99:273-86.
- Kong F, Gilbert GL (2006). Multiplex PCR-based reverse line blot hybridization assay. Nat Protoc. 1:2668-80.
- Lorusso V, et al. (2016). Tick-borne pathogens of zoonotic and veterinary importance in Nigerian cattle. Parasit Vectors 9:217.
- Nijhof AM, et al. (2007). Ticks and associated pathogens collected from domestic animals in the Netherlands. Vector Borne Zoonotic Dis. 7:585-95.
- Njiru ZK, et al. (2005). The use of ITS1 rDNA PCR in detecting pathogenic African trypanosomes. Parasitol Res. 95:186-92.
- World Organisation for Animal Health (2009). Bovine Brucellosis. Manual of diagnostic tests and vaccines for terrestrial animals.