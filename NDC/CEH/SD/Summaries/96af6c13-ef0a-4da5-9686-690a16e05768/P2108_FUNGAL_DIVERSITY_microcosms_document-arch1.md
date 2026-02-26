# Function and taxonomic diversity of mycorrhizas in grassland.

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focusing on soil biota diversity and their functional roles.
- Based on a large field experiment at Sourhope, Scottish Borders, with monitoring of aboveground productivity, species composition, and relative abundance.

## Study Context and Programme
- 24 projects funded to examine soil structure, processes (carbon and nitrogen cycles), and biota across microfauna, mesofauna, and macrofauna.
- This work specifically investigates arbuscular mycorrhizal (AM) fungi diversity within grassland microcosms and how plant communities affect AM diversity and community composition.

## Experimental Setup (Grassland Microcosms)
- Soil: Rendzina soil from limestone grassland removed from the surface 20 mm and packed into 600 × 600 mm, 150 mm deep acrylic boxes.
- Plantings (3-year establishment): 192 mature plants per microcosm in a 14 × 14 grid (with four replicate microcosms per treatment, one corner left empty).
- Treatments:
  - Bare soil
  - Monoculture of Carex flacca (nonmycotrophic sedge)
  - Monoculture of Festuca ovina (mycotrophic grass)
  - 12-species mixture (four forbs, four grasses, four sedges)
- Plant material sourced from limestone grasslands; short turf maintained by annual clipping.
- Bioassay: In July 2000, five-day-old Plantago lanceolata seedlings were transplanted into three of the four microcosm replicates per treatment and grown for 12 weeks.

## AM Fungal Diversity Assessment (Methods)
- AM diversity analyzed within roots of P. lanceolata seedlings using terminal-restriction fragment length polymorphism (T-RFLP).
- DNA extraction from roots, PCR amplification of a partial SSU rRNA gene using NS31 (universal eukaryotic primer) and AM1 (AM fungal-specific primer).
- PCR products labeled with fluorophores, purified, and digested with two restriction enzymes (Hinfi and Hsp92II) to maximize polymorphism detection.
- Fragment analysis performed on an ABI377 sequencer; fragments sized with GeneScan 400HD-ROX.
- Data processing focused on presence/absence of TRFs (band1-60); species richness (not evenness) recorded.
- Reproducibility confirmed with duplicate sequencing slab gels.
- Data file: Dataset 1005 (AM fungal diversity in microcosms), with fields including MICROCOSMID, TREATMENT, SPECIES, and BAND1-60 (0/1 for band presence/absence).

## Data Structure
- Comma-separated values file: P2108_FUNGAL_DIVERSITY2.csv.
- Key columns:
  - MICROCOSMID: sample type (bare soil, monocultures, or 12-species mixture)
  - TREATMENT: Sourhope soil treatment
  - SPECIES: plant assemblage (C. flacca, F. ovina, or 12-species mixture)
  - BAND1-60: 60 TRF bands with presence (1) or absence (0)

## Quality Control and Limitations
- Numeric range, formatting, and logical integrity checks applied.
- Data quality assurance procedures in place; however, NERC does not guarantee accuracy or fitness for a specific use.
- Provision of data carries no liability for accuracy; users should assess suitability for their intended analyses.

## References and Further Reading
- Core reference: Johnson et al. 2004. Plant communities affect arbuscular mycorrhizal fungal diversity and community composition in grassland microcosms. New Phytologist.
- Foundational methods and context: Vandenkoornhuyse & Leyval 1998; Helgason et al. 1998, 1999; Schüßler et al. 2001.
- Additional resources: Sourhope Field Data Handbook (2003); Understanding soil biodiversity in the UK Soil Biodiversity Programme (Usher et al. 2006).