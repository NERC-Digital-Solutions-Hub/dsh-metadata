# Macro_CBPeru_Dry

- Dataset description: Benthic macroinvertebrate taxonomic and abundance data from 10 rivers in glacial valleys of the Cordillera Blanca, Ancash, Peru. Related to the article on biodiversity responses to glacial retreat.
- Data files: Macro_CBPeru_Wet.csv (wet season) and Macro_CBPeru_Dry.csv (dry season).
- Purpose for data users: Enable exploration, comparison across seasons, and analyses of biodiversity changes with glacier cover; supports self-serve data products and potential dataset enhancement.

## What is in the data

- Taxa and abundances: 41 total identified taxa (38 in Dry, 39 in Wet); abundance values per site per taxon.
- Site layout: Rows correspond to sampling sites; columns include taxa and a replication column.
- Replicates: Each site sampled with 6 subsamples (5 subsamples at P01 in the Dry season); second column denotes replication number (1–6).
- Taxonomic resolution: Most taxa identified to genus level where possible (e.g., Trichoptera, Ephemeroptera, Plecoptera); many Chironomidae identified to subfamily/morphotype level; full taxon list provided in the metadata (Sp1–Sp41 with descriptions).

## Collection and processing methods

- Sampling design: At each site, a 15-meter reach with six subsamples (composite of 5 subsamples per 250 μm net) from riffles, pools, and bankside habitats.
- Preservation and processing: Substrate collected in the field, preserved in 96% ethanol, lab processing involved sieving and manual sorting to identify macroinvertebrates.
- Identification: Lab identification to the lowest possible taxonomic level using standard keys (Domínguez & Fernández 2009; Prat et al. 2011).
- Seasonality: Wet season data correspond to October 2020; Dry season data correspond to October 2019.

## Site and geographic metadata

- Sites: 10 sites coded P01–P10, representing rivers across Parón, Huaytapallana, and Llanganuco valleys.
- Geographic and environmental variables (per site): UTM coordinates, valley, basin area, glacier area, glacier coverage (GCC), distance from glacier, slope, and altitude.
- Data completeness: Site-specific GCC values range widely (e.g., from 0% to ~61.6%), with coordinates, basin areas, and altitudes recorded for each site.

## Data structure and taxonomic details

- Data structure: Abundance data organized with sites in the first column and taxa in the first row; the second column lists replication (1–6).
- Taxa documentation: Table of taxa includes site, description, family/subfamily, and order; notes which taxa are identified to genus level.
- Species list: Includes a broad suite of Ephemeroptera, Plecoptera, Trichoptera, Diptera (Chironomidae and other families), and other insect orders; many entries reflect morphotypes or subfamilies where genus-level ID is not possible.

## Quality control and provenance

- Consistency: The same person collected substrate at all sites; processing occurred within 48 hours; taxonomic identifications corroborated by a subject expert; records verified by two professionals.
- Versioning and contributors: Version 1.0; data collection and analysis contributions from Palacios, Medina, Loarte, Gamboa, Brown, Castañeda, Polo, Tapia, and Pellicciotti.

## How to use this dataset

- Potential analyses: Seasonal biodiversity comparisons, community composition and diversity metrics across gradients of glacier coverage, correlation of taxa abundance with GCC and other site variables, and data-driven development of self-serve dashboards or reports.
- Data integration: Combine with site metadata (geography, GCC, altitude) and with seasonal differences to explore drivers of macroinvertebrate biodiversity.
- Reference materials: Identification keys and standard methods cited (Domínguez & Fernández 2009; Prat et al. 2011) for taxonomic verification.

## References

- Domínguez, E., & Fernández, H. (2009). Macroinvertebrados bentónicos sudamericanos. Sistemática y biología.
- Prat, N., Acosta, R., Villamarín, C., & Rieradevall, M. (2011). Guía para el reconocimiento de larvas de Chironomidae (Diptera) de ríos altoandinos de Ecuador y Perú.