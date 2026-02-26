# Arbuscular mycorrhizal fungi diversity data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme] P. VANDENKOORNHUYSE, K. P. RIDGWAY, I. J. WATSON, A. H. FITTER and J.P.W. YOUNG

## Purpose and context
- Part of the NERC Soil Biodiversity Thematic Programme (1999–2001) focused on linking soil biodiversity with ecological processes.
- Aimed to understand AM fungal diversity in plant roots and how host plant and environmental factors influence AM communities.
- Data derived from the Sourhope field experiment examining soil amendments and insecticide effects.

## Field site and experimental design
- Location: Sourhope field station, Kelso, Scotland; 1.05-hectare semi-natural hill pasture.
- Treatments (starting May 1999), in randomized design across five replicates per treatment:
  - C (control)
  - N (nitrogen amendment)
  - L (lime amendment)
  - NL (nitrogen + lime)
  - B (biocide/insecticide)
- Nitrogen: NH4NO3, 24 g/m2 annually; Lime: CaCO3, 600 g/m2; Biocide: chlorpyrifos, 0.15 mL/m2 after mowing.

## Sampling and data collection
- Sampling date: 31 May 2001.
- Core sampling: 6.3 cm diameter, 20 cm depth; two cores per plot (10 cores per treatment).
- Plants identified; roots collected, washed, and frozen.
- DNA extraction: from 100 mg fresh weight root tissue; subsequent purification steps described.
- Plant identification verification: plastid trn L (UAA) intron PCR-RFLP to confirm grass species (A. capillaris, F. rubra, P. pratensis).

## Molecular methods for AM fungi
- Target region: part of the SSU rRNA gene; AM-specific amplification with NS31 and AM1 primers (fluorescently labeled).
- Acknowledgement of primer limitations: some AM clades may not be amplifiable; interpretation focuses on detectable AM diversity.
- PCR products purified for downstream analyses.

## T-RFLP analysis (terminal restriction fragment length polymorphism)
- In silico and empirical selection of restriction enzymes: HinFI and Hsp92II chosen for high polymorphism.
- Digestion: purified, fluorescently labeled AM fungal amplicons digested, fragments separated by capillary electrophoresis on ABI377.
- Replicates: two independent PCRs and two independent digestions per sample; gels replicated to ensure reliability.
- Data processing: TRFs coded as presence/absence (0/1) due to peak variability; dataset validated against prior cloned/sequenced data.

## Data outputs and structure
- Dataset: 1004, Arbuscular mycorrhizal (AM) Fungal Diversity Dataset (Sourhope) (P2108_FUNGAL_DIVERSITY1.csv).
- Key columns:
  - SAMPLEID, SAMPLE_DATE, BLOCK, MAIN_PLOT, SUB_PLOT
  - SPECIES (rooted plant species: A. capillaris, F. rubra, P. pratensis)
  - TREATMENT (Control, Lime, Nitrogen, Nitrogen + Lime, Biocide)
  - BAND1-68 (0/1 presence/absence signatures for 68 TRFs)
- Sampling date: 31 May 2001; cores 6.3 cm diameter to 20 cm depth.

## Key findings
- AM fungal communities show host-plant preferences; A. capillaris roots differed statistically from the other grass species.
- Grass species evenness changed with soil amendments; the composition of AM fungal communities within a given grass species remained relatively stable across treatments.
- Biocide plots showed plant community similarity to controls, while insecticide application was associated with higher AM fungal diversity, notably in F. rubra roots.

## Data quality, access, and limitations
- Quality control included numeric range checks, formatting validation, and logical integrity checks.
- Data are provided with standard disclaimers: NERC cannot warrant accuracy or fitness for a particular use; liability for data use is disclaimed.
- Data described as supporting information, with references and guidance for reuse; useful for comparative soil biodiversity and AM fungal monitoring studies.

## Relevance to environmental monitoring
- Demonstrates a standardized approach to capturing soil fungal diversity in relation to plant hosts and management practices.
- Provides a time-stamped, QA-informed dataset suitable for assessing the ecological consequences of soil amendments and pest management within grassland ecosystems.
- Aligns with monitoring aims to document environmental health and policy-relevant outcomes through structured, replicable data products.

## References and further reading
- Core dataset description and methods: Vandenkoornhuyse et al. (2003); Co-existing grass species have distinctive arbuscular mycorrhizal communities. Molecular Ecology.
- Background and methodological references on AM fungi, PCR-RFLP, and T-RFLP protocols cited within the document.