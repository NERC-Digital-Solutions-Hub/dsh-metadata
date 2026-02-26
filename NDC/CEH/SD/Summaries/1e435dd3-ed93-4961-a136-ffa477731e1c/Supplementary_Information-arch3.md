# Hurungwe_tsetse_PCR.csv

- Overview
  - Molecular analysis of trypanosomes and tsetse endosymbionts in two tsetse species (Glossina pallidipes and Glossina morsitans morsitans) from Hurungwe District, Mashonaland West, Zimbabwe.
  - Sampling Feb–Nov 2014; part of research on trypanosomiasis, well-being, and ecosystems (DDDAC); funded by NERC project NE/J000701/1 with ESPA support.

- Sampling and laboratory methods
  - Field: 10 km interval transect along a 110 km Zambezi Valley corridor; 3 km fly rounds at 12 sites, repeated 11 times over seven months; additional traps deployed as needed.
  - Specimens: 101 Gmm and 108 Gp tsetse flies analyzed; microscopic trypanosome screening conducted on 2092 flies.
  - Laboratory workflow: DNA extraction from crushed tsetse; PCR analyses using:
    - FliC to detect the endosymbiont Wigglesworthia glossinidius.
    - ITS-PCR to differentiate African trypanosome species/subspecies.
    - SRA gene target for human serum resistance in T. brucei s.l. positives.
    - GroEL PCR for Sodalis glossinidius; FtsZ and wsp primers for Wolbachia.
  - Quality controls: negative and positive controls for all PCR assays; electrophoresis on 1.5% agarose with GelRed; amplicon sizes compared to a 100 bp ladder.
  - Sample handling: tsetse stored in cryotubes with desiccants, surface-sterilized, DNA stored at -20°C.

- Dataset and structure
  - Data file: Hurungwe_tsetse_PCR.csv.
  - Variables (as described in Table 1):
    - Species (Gmm or Gp), Sex (Male or Female).
    - Trypanosoma_vivax, Trypanosoma_godfreyi, Trypanosoma_simiae_Tsavo, Trypanosoma_simiae, Trypanosoma_congolense, Trypanozoon, Trypanosoma_brucei_rhodesiense (all coded Positive=1, Negative=0).
    - Sodalis_glossinidius (Positive=1, Negative=0).
    - Wolbachia_ftsZ (Positive=1, Negative=0).
    - Wolbachia_wsp (Positive=1, Negative=0).
  - Data provenance: designed to support reuse for monitoring vector infection status and endosymbiont prevalence.

- Data quality, completeness and processing notes
  - Four samples excluded due to insufficient DNA, indicating quality-control decisions in the molecular workflow.
  - Microscopy and molecular analyses complemented each other to determine infection status.
  - -20°C storage of DNA ensures traceability and potential re-analysis.

- Metadata and governance
  - Metadata includes explicit variable definitions and coding (Table 1), enabling consistent interpretation and cross-study reuse.
  - Methodological references provided for PCR targets and protocols, supporting reproducibility.
  - Data sharing format (CSV) promotes machine-readability and integration into monitoring dashboards or analyses; no licensing details stated in the text.

- Relevance for monitoring frameworks
  - Provides a structured, assay-based dataset linking vector species, infection status, and endosymbiont prevalence, suitable for environmental health surveillance and policy evaluation.
  - Demonstrates end-to-end data workflow from field collection to laboratory analysis and data encoding, aiding assessment of data governance, openness, and metadata quality.
  - Data can inform risk assessments for sleeping sickness and vector ecology, supporting targeted interventions and resource allocation.

- Limitations and considerations for use
  - Geographic and temporal scope limited to Hurungwe District, Zimbabwe, during 2014; generalizability to other regions/times should be assessed.
  - Moderate sample size per species; potential biases from non-random trap locations and time sampling.
  - PCR-based detections have inherent sensitivity/specificity considerations; results may require confirmation with complementary methods when used for policy decisions.

- References (method and background)
  - Baldo et al. 2006; Cheng et al. 2000; Dennis et al. 2014; Hamidou Soumana et al. 2014; Matthew 2007; Njiru et al. 2005; Picozzi et al. 2008; Shereni et al. 2016.