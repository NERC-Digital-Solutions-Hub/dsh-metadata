# Arbuscular mycorrhizal fungi diversity data from Sourhope field experiment site, Scotland, 2001 [NERC Soil Biodiversity Programme]

## Overview and purpose
- AM fungi diversity data from the Sourhope field experiment (NERC Soil Biodiversity Programme) focused on arbuscular mycorrhizal (AM) fungi colonizing roots of three co-occurring grass species.
- Study used terminal restriction fragment length polymorphism (T-RFLP) to assess AM fungal diversity in 89 roots from Agrostis capillaris, Festuca rubra, and Poa pratensis under different soil treatments.
- Objectives included understanding host-plant and environmental influences on AM fungal communities and evaluating the effect of soil amendments and insecticide application on AM diversity.

## The field site and experimental design
- Location: Sourhope field station, Kelso, Scotland (1.05-hectare pasture area).
- Treatments (applied to five replicates each, randomized): Control (C), Nitrogen (N), Lime (L), Nitrogen + Lime (NL), Biocide (B) using Dursban chlorpyrifos.
- Treatments began May 1999; soil pH increased with lime and NL treatments; above-ground plant responses tracked alongside soil changes.
- Sampling framework: core samples (diameter 6.3 cm, depth 20 cm) collected from all plots on May 31, 2001; two cores per plot, yielding 10 cores per treatment.

## Methods and data processing
- Plant material and DNA: roots collected, washed, and frozen; total DNA extracted from 100 mg of root tissue with additional purification steps.
- Plant identification: verification of root origin using plastid trnL (UAA) intron PCR-RFLP to distinguish among A. capillaris, F. rubra, and P. pratensis; sequencing used to design discriminating RFLP strategies.
- AM fungal detection: SSU rRNA gene fragment amplified with AMF-specific primers (AM1/NS31) labeled for detection; acknowledgement of primer limitations for some AMF clades.
- T-RFLP analysis: chosen restriction enzymes HinFI and Hsp92II produced high polymorphism; duplicate PCRs and digestions, plus duplicate gels, to ensure reliability; peaks coded as presence/absence (0/1) of TRFs.
- Coding and data transformation: TRFs converted to a binary matrix; 68 TRFs detected across samples (bands 1–68).

## Data structure and content
- Dataset: 1004 — Arbuscular mycorrhizal (AM) Fungal Diversity Dataset (Sourhope) (P2108_FUNGAL_DIVERSITY1.csv).
- Key fields:
  - SAMPLEID: unique sample identifier (text).
  - SAMPLE_DATE: sampling date (date).
  - BLOCK: block number (1–5) (numeric).
  - MAIN_PLOT: main plot identifier (A–F) (text).
  - SUB_PLOT: sub-plot identifier (S, T) (text).
  - SPECIES: sampled plant root species (Agrostis capillaris, Festuca rubra, Poa pratensis) (text).
  - TREATMENT: soil treatment (Control, Lime, Nitrogen, Nitrogen + Lime, Biocide) (text).
  - BAND1-68: binary indicators (0/1) for presence/absence of each TRF (1–68) representing the AM fungal community profile.
- Sampling and replicate details align with the Sourhope 2003 data-handling framework; dataset notes indicate the date and methodology of collection, along with the encoded diversity signatures.

## Findings and interpretation
- AM fungal community composition is host-plant dependent: statistically distinct AM communities found among the three grass species, with A. capillaris showing distinct AM profiles from the others (P < 0.05).
- Within a given grass species, AM fungal community composition remained relatively stable across soil amendments (N, L, NL) but was affected by certain treatments.
- In plots treated with an insecticide, AM fungal diversity tended to be higher, with F. rubra showing a statistically different AM fungal community under these conditions.
- Overall, results support host-plant preferences in AM-associated communities and illustrate how management practices can influence root-associated AM diversity.

## Quality control, limitations, and governance
- Quality control included numeric range checks, formatting conformity, and logical integrity checks; multiple replicates (PCR, digestion, gels) were used to mitigate artefacts and increase reliability.
- Limitations and biases:
  - The chosen AMF primers (NS31/AM1) do not amplify all AMF clades; some groups (e.g., Paraglomaceae, Archeosporaceae) may be underrepresented.
  - T-RFLP provides a presence/absence profile for detected TRFs rather than a complete census of all AMF taxa.
- Data stewardship and liability notes:
  - Data are provided with standard QA procedures, but the NERC cannot guarantee accuracy or fitness for a specific use; no liability for usage outcomes is assumed.
- Related materials and access:
  - Data are referenced in the 2003 Molecular Ecology paper (Vandenkoornhuyse et al., 2003) and linked to the Sourhope Field Data Handbook (2003); supporting information accessible via EIDC catalogue records.
  - Key references and further reading include methodological sources for trnL-RFLP plant identification, AMF primers, and T-RFLP analysis.

## Usage notes and applicability
- Suitable for examining AM fungal diversity and host-plant associations in grassland ecosystems, and for investigating treatment effects on root-associated fungal communities.
- Users should account for primer biases and the binary nature of TRF presence/absence data when performing diversity analyses.
- The dataset provides a structured, field-based AMF diversity profile aligned with the Sourhope long-term field experiment data framework.