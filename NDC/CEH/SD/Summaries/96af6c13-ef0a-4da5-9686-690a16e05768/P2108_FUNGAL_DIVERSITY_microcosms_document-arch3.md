# Supporting Information

- Background and programme
  - Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focusing on soil biodiversity and functional roles of soil organisms.
  - Centreed on a large field experiment at Sourhope (Scottish Borders) with 24 funded projects investigating soil structure, processes (C and N cycles), microfauna, flora, and macrofauna.
  - Primary aim: understand soil biota diversity and functional roles; AM fungi diversity data collected from grassland microcosm experiments using different plant assemblages.

- Experimental setup and treatments
  - Grassland microcosms established in 1997 using rendzina soil from limestone grassland; contained in 600 × 600 mm acrylic boxes (150 mm deep).
  - 192 mature plants transplanted per box in a 14 × 14 grid (with some corners empty); four replicates per treatment in randomized blocks (16 microcosm treatments total).
  - Three vegetated treatments: monoculture of Carex flacca, monoculture of Festuca ovina, and a 12-species mixture (four forbs, four grasses, four sedges).
  - Plant assemblages represented three functional types common to limestone grasslands; regular weeding and annual clipping to maintain composition and turf.

- AM fungal diversity data collection (bioassay)
  - July 2000: 5-day-old Plantago lanceolata seedlings grown as a bioassay in autoclaved calcareous sand transplanted into three replicates per microcosm treatment.
  - Seedlings harvested after 12 weeks; roots collected for DNA analyses.

- Molecular assessment of AM diversity (T-RFLP)
  - DNA extracted from root samples; SSU rRNA gene region amplified using universal eukaryotic primer NS31 and AM fungal–specific primer AM1.
  - PCR products end-labeled with fluorescein dyes; products purified and digested with two restriction enzymes (Hinfi and Hsp92II) to enhance polymorphism of terminal fragments.
  - Fragment analysis performed on an ABI377 sequencer; TRF sizes determined with GeneScan; internal standard used for accurate sizing (45–450 bp range).
  - Reproducibility confirmed with two internal replicates; data used as presence/absence of TRFs (species richness), not abundance/evenness.

- Data structure and contents
  - Dataset 1005: AM fungal diversity dataset from Sheffield microcosms; matrix reflects presence/absence of TRFs in Plantago lanceolata bioassays.
  - Key fields:
    - MICROCOSMID: sample type (bare soil, monoculture C. flacca, monoculture F. ovina, 12-species mixture)
    - TREATMENT: Sourhope soil treatment
    - SPECIES: plant assemblage (C. flacca, F. ovina, or 12-species mix)
    - BAND1-60: 60 TRF bands (1 = present, 0 = absent) for each sample
  - Only richness data (presence/absence) reported; evenness not included.

- Data quality control and limitations
  - Quality control included numeric range checks, formatting conformity, and logical integrity checks.
  - Data are subject to QA procedures but no warranty by NERC regarding accuracy or fitness for particular uses; dataset provided without liability for misuse.

- References, guidance, and potential users
  - Key reference: Johnson et al. 2004 on plant communities affecting AM fungal diversity in grassland microcosms.
  - Additional foundational references on AM fungal diversity assessment and molecular techniques.
  - Useful for researchers and practitioners seeking to understand how plant community composition influences AM fungal diversity using a standardized microcosm and TRFLP approach.
  - Includes notes on related datasets and handbooks (e.g., Sourhope Field Data Handbook 2003) for broader data integration.

- Relevance for monitoring frameworks
  - Demonstrates a structured approach to monitoring soil biota diversity across contrasting plant communities.
  - Provides a clear data schema (presence/absence of molecularly defined diversity signatures) and documentation of methods, enabling data governance, metadata capture, and future data integration.
  - Highlights data processing choices (focusing on richness) and reproducibility practices, important for reporting and decision-making in environmental health monitoring.