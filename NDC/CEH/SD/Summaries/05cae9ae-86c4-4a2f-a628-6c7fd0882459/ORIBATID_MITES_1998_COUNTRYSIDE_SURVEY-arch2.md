# Oribatid mites 1998 [Countryside Survey], Great Britain

## Overview
- First and only national-scale monitoring of soil biodiversity in the UK, conducted as part of the Countryside Survey (CS) with CS2000 as the baseline dataset.
- Focuses on soil invertebrates collected via soil cores and analysed to provide standardized measures of biodiversity over time.
- Oribatid mites are a key taxon within the Acari component and are presented as part of the broader soil biodiversity dataset.

## Methods
- Soil cores collected in X-plots; five-day dry Tullgren extraction used to extract soil invertebrates; specimens preserved in 70% ethanol.
- Invertebrates identified to broad taxa; specimens of Acari (mites) separated and sent for specialist identification of oribatid taxa.
- Oribatid mites identified at ×400 magnification using a Watson Service 2 microscope; preparations cleared with lactic acid when needed and examined on slides.
- Taxonomic identifications guided by the Monograph of oribatid mites of the British Isles and other primary sources; ongoing updates from additional specialist literature.

## Datasets
- ORIBATID_MITES_CS2000_PLOT_RECORDS.csv: records of oribatid mite taxa across sampled plots.
  - Fields include SQUARE (1km square code), PLOT (plot within square), COUNTRY, TAXA_CODE, linking to taxon details.
- ORIBATID_MITES_CS2000_TAXA_DETAILS.csv: details for recorded oribatid mite taxa.
  - Fields include TAXA_CODE, SPECIES, AUTHORITY, and FAMILY; SPECIES combines to give full species name.

## Taxonomic updates and data standardisation
- Taxonomic revisions and synonymisations updated post hoc (e.g., Malaconothridae revisions; several genus/species changes).
- Examples of changes include: MALA1 = MALA2; ORIB4 = ORIB6; Rhysotritia -> Acrotritia; Ceratozetes thienemanni; Zygoribatula excavata; Brachychthonius hirtus; Oppiidae subgenera adjustments; Quadroppia reallocation; Zachvatinibates quadrivertex; Trichoribates incisellus; Scheloribates initialis.
- Revisions reflect alignment with contemporary taxonomy (Weigmann, Colloff & Cameron, Niedbala, etc.) and ensure consistency across datasets.

## Data quality, provenance and usage
- Data originate from Countryside Survey 2000; specimens identified by dedicated acarologists; quality control procedures referenced in accompanying publications.
- Clear documentation links between plot-level records and taxon details to support reproducible analyses.

## Access, attribution and rights
- All use of Countryside Survey data must include acknowledgement:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey ©; All rights reserved.
- Data are provided with explicit citation and usage notes consistent with CEH/NERC guidelines.

## References
- Black, H.I.J.; et al. (2016). Soil invertebrate data 1998 [Countryside Survey]. NERC Environmental Information Data Centre.
- Colloff, M.J.; Cameron, S.L. (2013). A phylogenetic analysis and taxonomic revision of the oribatid mite family Malaconothridae. Zootaxa.
- Emmett, B.A.; et al. (2008). Countryside Survey Technical Report No.03/07 Soils Manual. CEH.
- Niedbala, W. (2011). Ptyctimous mites (Acari: Oribatida) of the Palaearctic Region. Fauna Mundi.
- Weigmann, G. (2006). Hornmilben (Oribatida). Die Tierwelt Deutschlands.