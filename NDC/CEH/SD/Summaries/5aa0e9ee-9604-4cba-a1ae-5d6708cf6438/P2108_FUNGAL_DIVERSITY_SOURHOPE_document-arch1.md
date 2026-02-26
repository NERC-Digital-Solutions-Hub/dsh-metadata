# Arbuscular mycorrhizal fungi diversity data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

## Background and aims
- Part of the NERC Soil Biodiversity Thematic Programme (1999) at Sourhope field station, focusing on soil biota diversity and functional roles in ecological processes.
- AM fungi diversity in roots of three grass species (Agrostis capillaris, Festuca rubra, Poa pratensis) and the impact of soil amendments (nitrogen, lime, nitrogen+lime) and insecticide on AM fungal communities.

## Field site and experimental design
- Location: Sourhope field station, Kelso, Scotland; 1.05-ha semi-natural hill pasture.
- Treatments (five): Control (C), Nitrogen (N), Lime (L), Nitrogen+Lime (NL), Biocide (B); each with five replicates in a randomized design.
- Amendments: Nitrogen as NH4NO3 at 24 g/m2 annually; Lime as CaCO3 at 600 g/m2; Biocide: chlorpyrifos at 0.15 mL/m2 after mowing.
- Botanical changes observed two years after treatments began (drift in plant community; biomass increase in N and NL; pH increased with lime).

## Sampling and lab methods
- Sampling: Core samples (6.3 cm diameter, 20 cm depth) from each plot; two cores per plot, total of 10 cores per treatment; collected on 31 May 2001.
- Plant identification: Roots from cores washed and plant species identified; two-step root verification via plastid trnL intron PCR-RFLP to confirm grass species identity.
- DNA work: Total DNA extracted from 100 mg root tissue; purification steps included.
- AM fungal detection: Target SSU rRNA gene region amplified with AM fungal-specific primers NS31 and AM1; fluorescent labeling for fragment analysis.
- Limitations: Some AM clades not amplified by NS31/AM1; primer bias acknowledged.
- T-RFLP protocol: In silico restriction mapping to select Hinfi and Hsp92II enzymes; digest, fragment analysis on ABI377; replicates included to reduce artefacts; TRFs coded as presence/absence (0/1).

## Data structure and contents
- Dataset: 1004 Arbuscular mycorrhizal (AM) Fungal Diversity Dataset (Sourhope) (P2108_FUNGAL_DIVERSITY1.csv), with sampling details and 68 TRF bands.
- Key columns: SAMPLEID, SAMPLE_DATE (31 May 2001), BLOCK (1-5), MAIN_PLOT (A-F), SUB_PLOT (S,T), SPECIES (A. capillaris, F. rubra, P. pratensis), TREATMENT (Control, Lime, Nitrogen, Nitrogen+Lime, Biocide), BAND1-68 (binary 0/1 presence/absence for each TRF).
- Coverage: Diversity signature per root sample across three grass species and five soil treatments.

## Key findings
- AM fungal communities show host-plant preference; A. capillaris roots differ significantly from the others (P < 0.05).
- Within a given grass species, AM fungal community composition remains relatively stable across soil amendments, though grass species evenness changes with amendments.
- Insecticide-treated plots exhibit higher AM fungal diversity; F. rubra roots show statistically different AM communities.
- Plant community drift and soil chemistry changes accompany treatments; N and NL increase above-ground biomass; lime raises soil pH (approx. 4.8 in control vs. ~6.2 in lime and NL).

## Quality control and limitations
- Quality assurance included numeric range checks, formatting, and logical integrity checks; data providers do not warrant full accuracy.
- Replication and duplicate gels/assays used to mitigate artefacts; TRF data treated as binary presence/absence due to variability in peak sizes.
- Primer limitations mean not all AM fungi are detected; TRFLP profiles are descriptive of detectable diversity, not an exhaustive census.

## Access, references, and further reading
- Primary data file: 1004 AM Fungal Diversity Dataset Sourhope (P2108_FUNGAL_DIVERSITY1.csv); date 31 May 2001; 68 TRFs recorded as BAND1-68.
- Core references: Vandenkoornhuyse et al. (2003) Molecular Ecology; Burt-Smith (2002); Helgason et al. (1998); Schüßler et al. (2001a); Taberlet et al. (1991); Gardes & Bruns (1993).
- Additional resources: Sourhope Field Data Handbook (2003); UK Soil Biodiversity Programme developments (Usher et al., 2006).