# Arbuscular mycorrhizal fungi diversity data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

- Purpose and scope
  - Provides data on arbuscular mycorrhizal (AM) fungal diversity in roots of co-existing grass species from the Sourhope field experiment.
  - Uses a T-RFLP strategy to assess AM fungal diversity and how it responds to different soil amendments and insecticide treatment.
  - Demonstrates host-plant (grass species)–AM fungal community preferences and treatment effects on fungal diversity.

- The field site and experimental design
  - Location: Sourhope field station, near Kelso, Scotland (1.05-hectare semi-natural hill pasture).
  - Treatments (applied since May 1999): Control (C), nitrogen amendment (N), lime amendment (L), both nitrogen and lime (NL), biocide (B).
  - Design: Randomized design with five replicate plots per treatment.
  - Sampling date: 31 May 2001; core samples collected to 20 cm depth, two cores per plot/subplot.
  - Observed plant responses: shifts in plant community composition and above-ground biomass in N, L, NL plots; pH increased with lime; biocide plots showed plant composition similar to controls.

- Data collection and laboratory methods
  - Root sampling and DNA: Roots collected, washed, and DNA extracted from 100 mg of root material; an additional purification step performed.
  - Plant verification: Root samples checked for contamination by other grasses using PCR-RFLP of the trnL (UAA) intron; a grass-specific database was used for discrimination among A. capillaris, F. rubra, and P. pratensis.
  - AM fungal detection: Part of the small subunit (SSU) rRNA gene amplified with AM-specific primers NS31 and AM1, labeled for detection.
  - T-RFLP analysis: Two restriction enzymes (HinFI and Hsp92II) used to generate highly polymorphic terminal restriction fragments (TRFs); replicates included to guard against artefacts; peaks coded as presence/absence (1/0) of TRFs.
  - Data validation: Gels and sequencing used to validate TRF patterns; cross-checks with prior cloned sequence data to ensure adequacy of T-RFLP approach.

- Data structure and content
  - Dataset: 1004 — Arbuscular mycorrhizal (AM) Fungal Diversity Dataset (Sourhope) (P2108_FUNGAL_DIVERSITY1.csv).
  - File format: Comma-separated values (CSV) with the following columns:
    - SAMPLEID: unique sample identifier
    - SAMPLE_DATE: date of sampling
    - BLOCK: block number (1–5)
    - MAIN_PLOT: main plot label (A–F)
    - SUB_PLOT: sub-plot label (S, T)
    - SPECIES: sampled plant root species (A. capillaris, F. rubra, P. pratensis)
    - TREATMENT: soil treatment applied (Control, Lime, Nitrogen, Nitrogen + Lime, Biocide)
    - BAND1-68: encoded diversity signatures (0/1) for 68 TRFs representing AM fungal community in the sampled root
  - Sampling details: replicate core samples (6.3 cm diameter, depth 20 cm), collected from five soil treatments; 89 roots analyzed across three grass species.

- Key findings
  - AM fungal diversity detected by T-RFLP aligned with prior clone-library studies.
  - Clear host-plant preferences: AM communities in A. capillaris roots differed statistically from those in the other grasses.
  - Grass species evenness shifted with amendments, but AM fungal community composition within a given grass species remained relatively stable across treatments.
  - Insecticide-treated plots showed higher AM fungal diversity; in F. rubra, AM fungal communities were statistically distinct under this condition.

- Data quality and limitations
  - Strengths: replicated sampling and dual-restriction enzyme analysis; validation against existing sequence data; comprehensive metadata.
  - Limitations: NS31/AM1 primers may not amplify all AM fungal clades (e.g., Paraglomaceae and Archeosporaceae); results reflect detectable TRFs rather than a complete census of all AM fungi.
  - Data handling: presence/absence coding of TRFs provides robust comparability across replicates; two full sets of replicates and gel duplicates reduce artefact risk.

- Provenance, metadata and usage notes
  - Context: Supporting Information for NERC Soil Biodiversity Programme; linked to broader Sourhope field data and related publications.
  - Access and citation: Data described with a primary reference (Vandenkoornhuyse et al., 2003) and related sources; available as Supporting Information through the EIDC catalogue.
  - Quality assurance: Numeric range checks, format checks, and logical integrity checks described; NERC disclaims warranty and assumes no liability for data use.
  - Reuse considerations: Data suitable for comparative analyses of AM fungal diversity across hosts and treatments; appropriate caveats regarding primer limitations and the scope of detectable TRFs.