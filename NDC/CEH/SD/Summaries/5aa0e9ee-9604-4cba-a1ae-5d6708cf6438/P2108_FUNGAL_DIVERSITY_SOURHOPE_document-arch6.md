# Arbuscular mycorrhizal fungi diversity data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

## Overview
- Data describe arbuscular mycorrhizal (AM) fungal diversity within roots of three co-occurring grass species, collected from a long-term field experiment (Sourhope) in Scotland.
- Focus on how AM fungal community composition varies with host plant species and soil amendments, using a terminal restriction fragment length polymorphism (T-RFLP) approach.

## Field site and experimental design
- Location: Sourhope field station near Kelso, Scotland, UK.
- Area: 1.05 ha semi-natural hill pasture, plots treated since May 1999.
- Treatments (five plots per treatment, randomized design): Control (C), Nitrogen (N), Lime (L), Nitrogen+Lime (NL), Biocide (B).
- Replication: Five replicate plots per treatment.
- Plant community changes observed two years after treatments; ground-truthing showed shifts in species abundances and soil pH differences (pH ≈ 4.8 in control vs pH ≈ 6.2 in lime and NL).

## Sampling and laboratory methods
- Sampling: Core samples (6.3 cm diameter) to 20 cm depth from each plot/subplot; two cores per plot, total of 10 cores per treatment.
- Plants identified and roots were collected, washed, and stored; sampling date: 31 May 2001.
- DNA extraction: Total DNA from 100 mg of root tissue; additional purification steps applied.
- Plant identity verification: PCR-RFLP of trnL intron to confirm root plant species (A. capillaris, F. rubra, P. pratensis).
- AM fungal detection: PCR amplification of SSU rRNA gene fragment using AM-specific primers (AM1 and NS31) labeled for fluorescence.
- T-RFLP: Two restriction enzymes (Hin fI and Hsp92II) chosen for high polymorphism; duplicate PCRs and digestions, plus duplicated gels to ensure reliability.
- Data encoding: Presence/absence (1/0) of 68 terminal restriction fragments (TRFs) per sample.

## Data structure and variables
- Dataset: 1004 – Arbuscular mycorrhizal (AM) Fungal Diversity Dataset (Sourhope) with P2108_FUNGAL_DIVERSITY1.csv.
- Key columns:
  - SAMPLEID: Unique sample identifier
  - SAMPLE_DATE: Sampling date
  - BLOCK: Experimental block
  - MAIN_PLOT: Main plot letter (A–F)
  - SUB_PLOT: Subplot letter (S, T)
  - SPECIES: Sampled plant root species (A. capillaris, F. rubra, P. pratensis)
  - TREATMENT: Soil treatment (Control, Lime, Nitrogen, Nitrogen+Lime, Biocide)
  - BAND1-68: Binary presence (1) / absence (0) of each TRF (the 68 TRFs constitute the AM fungal diversity signature)

## Data processing and quality control
- Replication: Independent PCRs and digestions with two enzymes; gels duplicated to mitigate artefacts.
- Data coding: TRF peaks treated as discrete presence/absence characters (0/1) to accommodate cross-replicate variability.
- Validation: TRFLP profiles cross-checked against sequences from cloned AM fungal data; methodology previously validated against known AM fungal sequences.

## Findings and interpretation
- AM fungal communities show host-plant preference: A. capillaris roots harbor statistically distinct AM communities compared with the other grasses.
- Within a given grass species, AM fungal community composition remained relatively stable across different soil treatments, though grass species evenness shifted in amended soils.
- Biocide treatment did not dramatically alter plant community composition but was associated with higher AM fungal diversity in F. rubra roots.
- Overall, AM fungal diversity patterns align with prior Molecular Ecology findings and indicate distinct AM communities co-occurring with specific host grasses.

## Usage and access
- Primary data file: P2108_FUNGAL_DIVERSITY1.csv (Sourhope AM fungal diversity).
- Data collection date: 31 May 2001; sampling across five treatments with five replicates each.
- Related references and documentation:
  - Vandenkoornhuyse et al., 2003 (core findings on host-plant-specific AM communities)
  - Sourhope Field Data Handbook (2003)
  - Additional methodological and background references listed in the document
- Availability: Supporting Information noted to be accessible via the EIDC catalogue record; broader context available in cited literature.

## Limitations and caveats
- Primer coverage: NS31/AM1 primers amplify most AM fungi but may not capture all clades (e.g., Paraglomaceae and Archeosporaceae) due to primer specificity.
- TRFLP scope: TRF presence/absence provides a signature of AM fungal community structure but may not reflect absolute abundances or all diversity present.
- Inference scope: Conclusions about diversity and host-plant associations are based on root-associated AM communities within this specific grassland system and experimental treatments.

## References (key and supplemental)
- Key: Vandenkoornhuyse, P., Ridgway, K.P., Watson, I.J., Fitter, A.H. & Young, J.P.W., 2003. Co-existing grass species have distinctive arbuscular mycorrhizal communities. Molecular Ecology, 12(11), 3085-3095.
- Supporting materials and related readings: Burt-Smith 2002; Gardes & Bruns 1993; Helgason et al. 1998; Schüßler et al. 2001a; Taberlet et al. 1991; Vandenkoornhuyse et al. 2002a; Scott et al. 2003; Usher et al. 2006.