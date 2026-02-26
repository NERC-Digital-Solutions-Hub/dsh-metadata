# Arbuscular mycorrhizal fungi diversity data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

## Overview
- AM fungi diversity data derived from the Sourhope field experiment (Scotland) using a terminal restriction fragment length polymorphism (T-RFLP) approach.
- Focused on arbuscular mycorrhizal (AM) fungi colonizing roots of three co-occurring grass species and examined effects of soil amendments and insecticide on AM fungal community structure.
- Data organized as a CSV (Dataset 1004) with presence/absence of 68 TRFs across samples, enabling comparisons of AM fungal diversity among host plants and treatments.

## Field site and experimental design
- Location: Sourhope field station, near Kelso, Scotland (1.05-ha semi-natural hill pasture).
- Treatments (applied since May 1999) in a randomized design: Control (C), Nitrogen (N), Lime (L), Nitrogen + Lime (NL), Biocide (B).
- Five replicate plots per treatment; mainPlot and subPlot identifiers (A-F and S/T) across blocks (1–5).
- Sampling: 31 May 2001; cores of 6.3 cm diameter to 20 cm depth from each plot/sub-plot (two per plot, total 10 cores per treatment).

## Data collected and laboratory methods
- Plant material: Roots from three grass species in the same plots (Agrostis capillaris, Festuca rubra, Poa pratensis) were collected, identified, cleaned, and frozen.
- DNA extraction: Total DNA from 100 mg root tissue, with purification steps.
- Plant identity verification: PCR-RFLP targeting the plastid trnL intron to confirm grass species identity (adapted for grasses).
- AM fungal detection: Part of the SSU rRNA gene amplified with AM-specific primers (NS31 and AM1) labeled for detection.
- T-RFLP analysis: Restriction enzymes HinF I and Hsp92 II used to generate TRFs, fragments resolved on an ABI 377 sequencer; two independent PCRs and digestions per sample with duplicated gels to ensure reliability.
- Data coding: TRF peaks recorded as presence (1) or absence (0); no minimum peak height threshold applied due to replication-based noise assessment.

## Data structure (Dataset 1004)
- Dataset: Arbuscular mycorrhizal (AM) Fungal Diversity Dataset (Sourhope) (P2108_FUNGAL_DIVERSITY1.csv)
- Key fields:
  - SAMPLEID: unique sample identifier
  - SAMPLE_DATE: 2001-05-31
  - BLOCK: block number (1–5)
  - MAIN_PLOT: main plot letter (A–F)
  - SUB_PLOT: sub-plot letter (S, T)
  - SPECIES: sampled plant root (Agrostis capillaris, Festuca rubra, Poa pratensis)
  - TREATMENT: soil treatment (Control, Lime, Nitrogen, Nitrogen + Lime, Biocide)
  - BAND1-68: presence (1) or absence (0) of each TRF (68 TRFs total)
- Note: The dataset captures diversity signatures across replicates and treatments, reflecting host-plant preferences and treatment effects on AM fungal communities.

## Key findings
- AM fungal diversity detected via T-RFLP aligns with previous clone-library studies, confirming robust detection of community diversity.
- Host-plant preference observed: AM fungal communities in Agrostis capillaris roots are statistically distinct from the other grasses.
- Grass species evenness shifted with soil amendments, yet AM fungal community composition within a given grass species remained comparatively stable across amendments.
- Insecticide (biocide) plots showed higher AM fungal diversity, with Festuca rubra exhibiting a notably different AM fungal community under certain conditions.

## Quality control and caveats
- Quality checks included numeric range, formatting, and logical integrity; replicated measurements and gels help mitigate artefacts.
- NERC disclaims guarantee of data accuracy or fitness for a particular use; data are provided without liability for misuse.
- Limitations:
  - Some AM fungal clades may not be amplified by the NS31/AM1 primer set (e.g., Paraglomaceae, Archeosporaceae), so the dataset may not capture all AM fungal diversity.
  - TRF-based presence/absence coding provides a discrete, rather than quantitative, view of diversity.

## GIS relevance and how to visualise
- Spatial context and design: Plot-level (BLOCK, MAIN_PLOT, SUB_PLOT) and treatment data enable spatial mapping of AM fungal diversity across the field site.
- Potential visualisations:
  - Map of plot layout with treatments and blocks to correlate spatial patterns with AM fungal TRF presence/absence.
  - Raster or point layers showing binary TRF presence across samples, aggregated by species and treatment to display diversity hotspots.
  - Overlay environmental attributes (pH changes from lime treatment, as reported) to examine associations with AM community composition.
  - Multivariate visualisations (e.g., NMDS) linked to spatial units to explore how geography, host species, and management influence AM fungi.
- Data integration: Combine BAND1-68 (TRF presence/absence) with metadata (species, treatment, sample date, plot design) for GIS-based analyses of diversity structure and treatment effects.

## References and further reading
- Vandenkoornhuyse, P., Ridgway, K.P., Watson, I.J., Fitter, A.H. and Young, J.P.W., 2003. Co-existing grass species have distinctive arbuscular mycorrhizal communities. Molecular Ecology, 12(11), 3085-3095.
- Burt-Smith G. (2002) Report III results from the Sourhope field experiment. Macaulay Institute.
- Gardes M, Bruns TD (1993). ITS primers with enhanced specificity for basidiomycetes; Molecular Ecology.
- Helgason T, Daniell TJ, Husband R, Fitter AH, Young JPW (1998). Ploughing up the wood-wide web? Nature.
- Schüßler A, Schwarzott D, Walker C (2001a). Glomeromycota: phylogeny and evolution. Mycological Research.
- Taberlet P, Gielly L, Pautou G, Bouvet J (1991). Universal chloroplast primers. Plant Molecular Biology.
- Vandenkoornhuyse P, Husband R, Daniell TJ et al. (2002a). Arbuscular mycorrhizal community composition with two grass species in a grassland. Molecular Ecology.
- Scott et al. (2003). SOURHOPE FIELD DATA HANDBOOK 2003. Available via EIDC.
- Usher et al. (2006). Understanding biological diversity in soil: UK's Soil Biodiversity Research Programme. Applied Soil Ecology.