# Function and taxonomic diversity of mycorrhizas in grassland.

## Overview and aims
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biota diversity and the functional roles of soil organisms.
- 24 research projects studied soil structure, soil processes (carbon and nitrogen cycles), and biota groups (Bacteria, Nematoda, Protozoa, Fungi, microarthropods, invertebrates, meso- and macro-fauna).
- This component examined arbuscular mycorrhizal (AM) fungal diversity in a grassland microcosm experiment to understand how plant communities influence AM diversity and community composition.

## Experimental design and setup
- Location and system: unfertilized limestone grassland soil microcosms established at the Buxton Climate Change Impacts Laboratory; rendzina soil prepared and packed into acrylic boxes.
- Plant material and treatments (3-year establishment): 
  - Bare soil (control)
  - Monoculture of Carex flacca (nonmycotrophic sedge)
  - Monoculture of Festuca ovina (mycotrophic grass)
  - 12-species mixture (diverse plant assemblage)
- Plant assemblages: three broad functional groups (sedges, grasses, forbs) with randomized, replicated microcosms (16 treatments total across replicates).
- Bioassay setup: in 2000, 5-day-old Plantago lanceolata seedlings grown as a bioassay in autoclaved calcareous sand were transplanted into three of the four replicate microcosms per treatment; seedlings grown for 12 weeks.

## AM fungal diversity assessment
- Sample processing: Roots of P. lanceolata seedlings were washed, DNA-extracted, and purified for analysis.
- Molecular approach: SSU rRNA gene region amplified with universal primer NS31 and AM fungal-specific primer AM1 to target AM fungi diversity in roots.
- Diversity fingerprinting: Terminal-restriction fragment length polymorphism (T-RFLP) using two restriction enzymes (HinFI and Hsp92II) to maximize polymorphism at fragment ends.
- Data capture: Fragment sizes (TRFs) generated via an ABI377 sequencer and sized with GeneScan; only presence/absence of TRFs (not their relative abundance) recorded as species richness.
- Quality control: Reproducibility confirmed with internal replicates; size range kept between 45 and 450 bp; smaller/greater fragments excluded from analyses.

## Data structure and content
- Dataset: Dataset 1005 – Arbuscular mycorrhizal (AM) fungal diversity dataset (microcosm experiment at Sheffield University).
- Focus: Diversity of AM fungi within bioassay plantlets (P. lanceolata) analyzed by T-RFLP.
- Columns and meaning:
  - MICROCOSMID: sample type (bare soil, monoculture of C. flacca, monoculture of F. ovina, 12-species mixture).
  - TREATMENT: Sourhope soil treatment.
  - SPECIES: plant assemblage (C. flacca monoculture, F. ovina monoculture, or 12-species mixture).
  - BAND1-60: presence (1) or absence (0) of each of 60 TRFs (diversity signature).
- Data type: text for categorical fields; numeric 0/1 for TRF presence/absence.
- Output: Only species richness is reported (binary presence/absence of TRFs); evenness (peak height/area) not included.

## Data quality, limitations, and use
- Quality controls include numeric range checks, formatting conformity, and logical consistency checks.
- The data are subject to quality assurance but come with no warranty of accuracy or fitness for a particular use; no liability for outcomes from data use.
- Utility: useful for examining how plant community composition affects AM fungal diversity and community composition in grassland microcosms; can be cross-referenced with related soil biodiversity studies and field data.

## Key references and further reading
- Johnson et al. 2004. Plant communities affect arbuscular mycorrhizal fungal diversity and community composition in grassland microcosms. New Phytologist, 161(2), 503-515.
- Vandenkoornhuyse & Leyval 1998. SSU rDNA sequencing and PCR fingerprinting reveal genetic variation within Glomus mosseae. Mycologia, 90:791-797.
- Helgason et al. 1998. Ploughing up the woodwide web? Nature, 394:431.
- Helgason et al. 1999. Molecular diversity of AM fungi in bluebell woodlands. Molecular Ecology, 8:659-666.
- Schüßler et al. 2001. A new fungal phylum, Glomeromycota: phylogeny and evolution. Mycological Research, 105:1413-1421.
- Additional readings: SOURHOPE Field Data Handbook (2003); Understanding biological diversity in soil (Applied Soil Ecology, 2006).

## Potential applications and users
- Researchers examining plant-AM fungal interactions in grassland ecosystems.
- Data analysts integrating AM diversity data with plant community composition and soil variables.
- Practitioners exploring biodiversity-informed management of grasslands and restoration projects.