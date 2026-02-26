# Domestic animal health data from Mambwe District, Zambia (2013)

- A survey addressing trypanosomiasis, tick-borne infections, and brucellosis in domestic livestock conducted June–August 2013 in Mambwe District, Eastern Zambia.
- Related human wellbeing survey conducted under the Dynamic Drivers of Disease in Africa Consortium; data collected from the same study area.
- Data designed to support epidemiological analysis and integration with broader health datasets.

## Data Source, Population and Sampling

- Population basis: households from a census of people and animals in Aug 2012 and Oct–Nov 2012.
- Census counts: 3,717 total households; 1,354 with livestock.
- Sample size planning: one-stage cluster survey targeting 139 households, assuming 30% trypanosome prevalence in cattle, 90% confidence, 7% precision, and homogeneity of 0.18.
- Sampling frame and design documented in CS Survey (v2.0).

## Data Collected and Sample Collection

- Animal sampling window: June–August 2013.
- Species and tests:
  - Cattle and dogs: tested for African trypanosomes, tick-borne infections, and Brucella.
  - Goats and sheep: tested for African trypanosomes and Brucella.
  - Pigs: tested for African trypanosomes only.
- Blood collection and storage:
  - Trypanosomiasis and tick-borne infections: blood collected into 75 μl heparinised capillary tubes from ear veins; two tubes per animal; blood spotted onto Whatman FTA Cards; cards dried and stored with desiccant.
  - Brucellosis: blood drawn from jugular (ruminants) or cephalic (dogs); serum stored in plain and sodium azide–preserved tubes; refrigerated before freezing.
- Sample sizes by species:
  - Goats: 473
  - Cattle: 340
  - Pigs: 246
  - Dogs: 199
  - Sheep: 22
- Age definitions for sexually mature status:
  - Goats > 4 months; cattle > 12 months; dogs > 7 months; sheep > 5 months.

## Laboratory Analyses and Data Capture

- Brucellosis testing (OIE, 2009 method):
  - Serum applied to antigen spots on a tile; 25 μl serum per spot (adjusted to 75 μl for small ruminants to increase sensitivity); negative control with sterile saline; daily positive control.
- Trypanosomiasis and tick-borne infections (molecular methods):
  - DNA extraction from Whatman FTA cards; five 3 mm discs per sample with multi-step washes; elute DNA with 100 μl of 5% Chelex, heat to 90°C.
  - Trypanosome PCR (ITS PCR, Njiru et al., 2005): detects T. congolense (Kilifi/savannah/forest), Trypanozoon, T. simiae (Tsavo), T. vivax, T. godfreyi.
  - Tick-borne infections: reverse line blot (RLB) PCRs with three targets:
    - Theileria/Babesia (18S rRNA)
    - Ehrlichia/Anaplasma (16S SSU rRNA, V1 region)
    - Rickettsia (16S rRNA)
  - Controls:
    - Positive: DNA from relevant pathogens (e.g., T. brucei, T. vivax, T. congolense; Theileria parva; Ehrlichia canis; Rickettsia spp.)
    - Negative: autoclaved PCR water
  - Target organisms: cattle and dogs only for tick-borne tests; includes multiple species-specific and catch-all probes.
- Data recording and dataset structure:
  - Laboratory results entered into Microsoft Excel.
  - Coding: positive = 1, negative = 0, not tested = ND (not determined).
  - Some animals tested with two different probe sets for the same species (e.g., Ehrlichia ruminantium_1 and _2).
  - Results organized by broad “catch-all” PCR outcomes and species-specific primers (e.g., EA_CA, TB_CA, T_CA, R_CA plus individual species names).

## Data Management and Variables

- Dataset documentation:
  - Table 1 defines variables for each specimen/species (e.g., age, sex, multiple Trypanosoma and tick-borne pathogen indicators).
  - Variables include multiple entries for certain pathogens (e.g., Trypanosoma_congolense vs. Trypanosoma_congolense_Kilifi; Ehrlichia_ruminantium_1 vs. Ehrlichia_ruminantium_2).
- Data presentation:
  - Results summarized as binary presence/absence at the sample level; ND marks indicate untested samples.
  - Separate “catch-all” PCR results to indicate potential presence of a genus-level pathogen when species-specific primers are negative.

## Data Use, Relevance and Documentation

- Data relevance:
  - Provides multi-pathogen, multi-species prevalence data linked to a well-defined census-based sampling frame.
  - Suitable for cross-analysis with the related human wellbeing dataset from the same study area.
- Data standards and transparency:
  - Uses established laboratory methods (OIE Brucellosis protocol; ITS PCR for trypanosomes; reverse line blot for tick-borne pathogens) with explicit controls and references.
  - Clear documentation of sample handling, storage (FTA cards), and DNA elution method.
- Potential applications for data leaders:
  - Assess data availability, quality, and provenance for integrated data ecosystems.
  - Inform data governance around multi-pathogen surveillance datasets, metadata richness, and cross-domain linkage (animal health and human wellbeing).
  - Demonstrate end-to-end data lifecycle: from field collection and biobanking to molecular analysis and structured data export (Excel) with explicit ND handling.
- Limitations and considerations:
  - Small sheep sample (n=22) may limit species-specific inferences for that group.
  - Tick-borne pathogen testing limited to cattle and dogs.
  - Data stored in Excel with complex variable naming; consider metadata onboarding for discoverability and reuse in larger data networks.

## References (methodological benchmarks)

- Bekker et al. (2002) – Reverse line blot for Anaplasma/Ehrlichia detection.
- Blasco et al. (1994) – Brucellosis diagnostics in small ruminants.
- Georges et al. (2001); Kong & Gilbert (2006); Lorusso et al. (2016) – Tick-borne pathogen detection and backward compatibility.
- Nijhof et al. (2007); Njiru et al. (2005) – PCR methods for trypanosomes and tick-borne pathogens.
- World Organisation for Animal Health (2009) – Bovine Brucellosis testing manual.