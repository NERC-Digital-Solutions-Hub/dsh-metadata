# Morphology phenotype data of 88 types of galls induced on oak trees by cynipid gallwasps from 6 sites in Hungary, 2000-2003: Supporting information

## Overview
- Dataset describing phenotypic attributes of galls induced on oak trees (Quercus spp.) by cynipid gallwasps (Hymenoptera: Cynipidae: Cynipini).
- 88 gall types across 69 cynipid species; 31 sexual generation galls and 58 asexual generation galls.
- Collected from 6 sites in Hungary; continuous measurements taken for samples from sites 1–5.
- Measurements use digital calipers and cover various internal and external gall properties that relate to defense against natural enemies.

## Data content and variables
The dataset comprises 17 data columns across separate rows for each cynipid species and generation (mature gall). Values are for the mature gall and units are mm or mm^3 where applicable. Missing values are coded as -999.

- Linnean species name — string
- Generation — Sexual or Asexual
- Hair — binary (1 = hairy surface, 0 = not hairy)
- Dense_spines — binary (1 = dense coating of fine spines <1 mm, 0 = not)
- Sparse_spines — binary (1 = sparse coating of larger spines >1 mm, 0 = not)
- Sticky — binary (1 = sticky resin on surface, 0 = not)
- Space — binary (1 = internal air space, 0 = no air space)
- Dummy — binary (1 = decoy inner chamber, 0 = not)
- Peduncle — binary (1 = connected by a peduncle, 0 = not)
- Nectar — binary (1 = secreting sugar-rich nectar, 0 = not)
- Dehisce — binary (1 = dehiscing at maturity, 0 = not)
- Tough — ordinal (1 to 4; 1 softest to 4 hardest)
- Shape — categorical (cone, cylinder, sphere)
- Radius — continuous (mm); radius for cone base if Shape = cone
- Height — continuous (mm); height for cones/cylinders; not applicable for spheres
- Gall_Size — continuous (mm^3), volume assuming the indicated Shape
- Locularity — categorical (Unilocular or Multilocular)

Notes:
- Values -999 indicate missing data.
- Continuous measurements are in millimeters (Radius, Height) or cubic millimeters (Gall_Size).

## Data collection and quality control
- Gall identifications based on diagnostic external features by experienced field staff; DNA barcoding used when necessary (mitochondrial cytochrome b and nuclear ITS2) for confirmation.
- Gall maturity confirmed by presence of fully mature larval/pupal in larval chambers.
- Ordinal Tough validated with continuous penetration scores (QTS-25) where available.
- Data have been carefully checked for errors.

## Data structure and sampling design
- Data are organized with separate rows for each cynipid species and generation, focusing on mature galls.
- 17 variables capture internal and external properties of gall structures.
- Sampling: 10 individual galls per gall type were measured across sites 1–5; total coverage spans 6 sites (as per map reference).
- All continuous measurements are in mm or mm^3; some data gaps exist (e.g., Height not recorded for spherical galls).

## Data availability, provenance, and references
- This document is supporting information accompanying a broader study.
- Measurements and methods are documented to enable reuse and verification.
- Key references informing methods and interpretation:
  - Bailey et al. (2009). Host niches and defensive extended phenotypes structure parasitoid wasp communities.
  - Nicholls et al. (2012). Mitochondrial barcodes diagnostic of shared refugia but not species in hybridising oak gallwasps.
  - Roskam (2019). Plant Galls of Europe.

## Limitations and caveats
- Some variables have missing values (-999) for certain species/generations.
- Height data are not available for spherical galls.
- The dataset reflects measurements from a specific temporal window (2000–2003) and geographic region (Hungary); broader generalization should consider potential regional variation.
- Data focus on mature galls; developmental stage prior to maturity is not captured.