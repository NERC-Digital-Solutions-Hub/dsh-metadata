# Müllerian mimicry of a quantitative trait despite contrasting levels of genomic divergence and selection

## Overview
- Dataset from a study on clinal variation in Heliconius erato and Heliconius melpomene in the Chocó-Darien ecoregion (between the Andes and Pacific in Ecuador and Colombia, and the Pacific coast of Darien, Panama).
- Aims to document sampling locations, specimen collection, and genomic and image data to support GIS-based analyses of spatial patterns.

## Data collection and sampling metadata
- Sampling conducted across five trips:
  - May 2014 and May 2015 in the Mashpi reserve area, Pichincha, Ecuador
  - January 2015 in Cauca Valley and Chocó regions, Colombia
  - February 2015 in the southwest Darien region, Panama
  - March 2016 in the Chocó region, Colombia
- GPS coordinates collected for sampling locations using a Garmin etrex 10; recorded as decimal degrees (lat, long) and altitude (m) for most sites (altitude not recorded for some near sea level).
- A single position was recorded per sampling site; samples collected within ~2 km of this point.
- Collection method: hand nets targeting all observed Heliconius individuals, with emphasis on H. melpomene and H. erato; collecting effort varied by day (not standardized).
- Species identities confirmed by at least two experts; subspecies based on wing pattern; sex determined from genital morphology.

## Specimen handling and storage
- Wings removed on day of collection; bodies preserved in NaCl-saturated 20% DMSO with 0.25 M EDTA.
- Specimens stored at the University of Sheffield.

## Genomic data
- Genomic assays:
  - RAD sequencing (single-digest with PstI) for 265 H. erato individuals
  - Whole-genome re-sequencing for 36 H. melpomene individuals
- Data deposited in the European Nucleotide Archive (ENA) under project PRJEB32848.
- Individual sample accessions listed in butterflyCollectionData2014to2016.csv.

## Imaging data
- Digital wing images captured with a Nikon D7000 (AF-S DX Micro NIKKOR 40 mm f/2.8G) under standardized lighting.
- Up to two images per specimen: dorsal and ventral sides.
- Ventral images named <specimenid>_v_x; dorsal images named <specimenid>_d_x.
- Images include an X-Rite ColorChecker passport for color accuracy.

## Data access and structure
- Genomic data: ENA project PRJEB32848.
- Metadata and sample identifiers: butterflyCollectionData2014to2016.csv.
- Imaging and specimen metadata aligned to specimen IDs for GIS-linking with spatial data.

## Considerations for GIS use
- Spatial data include precise GPS coordinates but some altitude data are missing; plan for handling seabed-adjacent sites and potential elevation gaps.
- Sampling was not standardized across days, which may affect spatial bias; consider integrating with other datasets for robust spatial analyses.
- Multiple data types (genomic, morphometric imagery, and locality data) are co-located via specimen IDs, enabling multi-layer GIS visualizations and spatial analyses.

## Reference
- Curran, E.V., Stankowski, S., Pardo-Diaz, C., Salazar, C., Linares, M., Nadeau, N.J. 2020. Müllerian mimicry of a quantitative trait despite contrasting levels of genomic divergence and selection. Molecular Ecology. https://doi.org/10.1111/mec.15460