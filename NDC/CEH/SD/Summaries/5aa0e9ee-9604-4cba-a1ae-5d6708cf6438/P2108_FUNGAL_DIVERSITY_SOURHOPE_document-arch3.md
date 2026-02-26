# Arbuscular mycorrhizal fungi diversity data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme] P. VANDENKOORNHUYSE, K. P. RIDGWAY, I. J. WATSON, A. H. FITTER and J.P.W. YOUNG

## Overview
- Describes arbuscular mycorrhizal (AM) fungi diversity data from the Sourhope field experiment (Scotland) conducted in 2001 as part of the NERC Soil Biodiversity Thematic Programme.
- Aims to understand AM fungal diversity in relation to host plants (grass species) and environmental treatments, and to relate AM diversity to plant community changes and soil amendments.

## Background and aims of the programme
- NERC Soil Biodiversity Thematic Programme (started 1999) studied soil biota diversity and their functional roles in key ecological processes.
- Twenty-four projects funded to examine soil structure, processes (C and N cycles), and biota (microfauna to macro-fauna).
- The Sourhope field experiment examined how soil amendments and other factors influence aboveground productivity, plant community composition, and soil biota, including AM fungi.

## Field site and experimental design
- Location: Sourhope field station, Scottish Borders (1.05-ha semi-natural hill pasture).
- Treatments (randomized, five replicates each): Control (C), Nitrogen (N), Lime (L), Nitrogen + Lime (NL), Biocide (B).
- Application details: Nitrogen as NH4NO3 at 24 g/m2/year; Lime as CaCO3 to raise soil pH; Biocide was chlorpyrifos insecticide.
- Observations two years after treatments began showed shifts in plant community composition and above-ground biomass in some treatments; soil pH increased with lime and NL treatments.

## Sampling, laboratory methods, and data generation
- Soil cores: 6.3 cm diameter, to 20 cm depth; two cores per plot, five replicate plots per treatment (10 cores per treatment).
- Plant root processing: Roots washed, identified, and frozen; total DNA extracted from 100 mg fresh weight of root tissue.
- Plant identification and root purity: Used plastid trnL (UAA) intron PCR-RFLP to verify root identity for the three grass species studied (Agrostis capillaris, Festuca rubra, Poa pratensis).
- AMF diversity assessment: Extracted SSU rRNA gene fragment (550 bp) amplified with AMF-specific primers NS31 and AM1; fluorescent labels used for downstream detection.
- T-RFLP: Screened AMF community composition using two restriction enzymes (HinFI and Hsp92II) on fluorescent amplicons; replicates (two independent PCRs and digestions) to ensure reliability; gels duplicated to confirm fragment peaks.
- Data handling: Each AMF TRF peak treated as a presence/absence character (0/1) to build a binary community profile per sample.
- Data validation: Cross-checked TRFLP results against existing cloned sequences; overall method aligned with known AMF diversity patterns.

## Data structure and dataset details
- Dataset title: Arbuscular mycorrhizal (AM) Fungal Diversity Dataset (Sourhope) (P2108_FUNGAL_DIVERSITY1.csv) with 18-68 TRF bands encoded as presence/absence.
- Key fields in the dataset:
  - SAMPLEID, SAMPLE_DATE, BLOCK, MAIN_PLOT, SUB_PLOT
  - SPECIES (root sample type: A. capillaris, F. rubra, P. pratensis)
  - TREATMENT (Control, Lime, Nitrogen, Nitrogen + Lime, Biocide)
  - BAND1-68 (binary columns indicating presence/absence of each TRF; up to 68 bands observed)
- Sampling context: Replicate core samples (6.3 cm diameter, 20 cm depth) collected on 31 May 2001; samples span five soil treatments and multiple plots.
- Dataset usage notes: Primers designed to target AM fungi; some AM clades (e.g., Paraglomaceae, Archeosporaceae) may be underrepresented due to primer specificity; TRFLP provides a consistent, comparable proxy for AMF diversity across samples.

## Key findings
- AM fungal communities show host-plant preference: AM assemblages differ among the three co-occurring grass species; A. capillaris roots host distinct AM communities compared with the other grasses (P < 0.05).
- Within-plant stability: For a given grass species, AM fungal community composition remained relatively stable across different soil treatments, though grass species evenness did shift with amendments.
- Treatment effects on diversity: Insecticide (biocide) plots exhibited higher AM fungal diversity, with F. rubra roots showing a statistically distinct AM community under this treatment.
- Overall plant-AM interactions: Evidence supports distinct AM associations among host species and treatment-dependent changes in diversity, contributing to understanding of how soil amendments and management practices influence root-associated fungal communities.

## Data quality, governance, and accessibility
- Quality control: Included numeric range checks, formatting checks, and logical integrity checks; multiple replicates and duplicate runs used to mitigate artefacts and ensure reliability.
- Limitations and caveats: While robust for the dataset, the authors note primer limitations and the fact that not all AM fungal clades may be amplified by NS31/AM1; results should be interpreted as relative diversity and community composition rather than a full catalogue of all AMF taxa.
- Data rights and liability: The dataset is provided with standard quality assurances, but the issuing body (NERC) does not warrant accuracy or fitness for a specific use and disclaims liability for outcomes from using the data.
- Access and related resources: The data are available as Supporting Information; related materials include the Sourhope Field Data Handbook (2003) and other foundational publications; further methodological context is available in cited literature.
- Potential data use: Suitable for meta-analyses of AMF diversity in grassland systems, comparative studies across host species, and evaluation of management practices on root-associated fungal communities.

## References and further reading (selected)
- Vandenkoornhuyse et al. 2003. Co-existing grass species have distinctive arbuscular mycorrhizal communities. Molecular Ecology.
- Burt-Smith 2002; Scott et al. 2003; Gardes & Bruns 1993; Helgason et al. 1998; Schüßler et al. 2001a; Taberlet et al. 1991; Vandenkoornhuyse et al. 2002a.
- SOURHOPE FIELD DATA HANDBOOK (2003) and UK Soil Biodiversity Programme reviews for broader context.