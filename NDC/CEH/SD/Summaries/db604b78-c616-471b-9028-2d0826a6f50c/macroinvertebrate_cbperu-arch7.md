# Declining glacier cover drives changes in the biodiversity of aquatic macroinvertebrates in the Cordillera Blanca, Peru.

## Overview
- Dataset of taxonomic and abundance data for benthic macroinvertebrates from 10 rivers in glacial valleys (Parón, Huaytapallana, Llanganuco) in the Cordillera Blanca, Ancash, Peru.
- Examines biodiversity response to glacial retreat; linked to the article on this topic.
- Two seasonal datasets (wet and dry seasons) documenting abundances across sites and taxa.

## Data files
- Macro_CBPeru_Wet.csv — macroinvertebrate abundances for the wet season.
- Macro_CBPeru_Dry.csv — macroinvertebrate abundances for the dry season.
- Both datasets:
  - 41 total identified taxa (38 taxa in dry season; 39 taxa in wet season).
  - Structure: rows = sites, columns = taxa; first row contains taxa names.
  - Second column indicates repetition (1–6; P01 in dry season had 5 subsamples due to conditions).

## Sampling and methods
- Field sampling: October 2019 and October 2020.
- At each site: 15 m defined section; 6 subsamples collected (randomly) using a 250 μm mesh net; composite sample = 5 subsamples.
- Substrate preserved in 96% ethanol in the field; transported to lab.
- Laboratory processing: samples washed through 250 μm sieve; macroinvertebrates identified to lowest attainable taxonomic level.
  - Genus-level identifications for Trichoptera, Ephemeroptera, Plecoptera.
  - Many Chironomidae identified to subfamily using regional morphotype guides.
- Counts include larvae, nymphs, pupae (adult Coleoptera also counted where applicable).

## Site codes and geographic information
- Site codes: P01–P10 corresponding to the 10 studied rivers.
- Geographic variables per site (from Table 1):
  - UTM 18S coordinates (x, y)
  - Valley name
  - Basin area (km^2)
  - Glacier area (km^2)
  - Glacier Coverage (GCC, %)
  - Distance from glacier (km)
  - Slope (%)
  - Altitude (m above sea level)
- GCC ranges from 0.00% to 61.61%; other site characteristics include varied basin sizes, slopes, distances to glaciers, and altitudes.

## Data structure and units
- Abundance data: 41 total taxa identified (38 in dry season; 39 in wet season).
- Columns: Site (sampling site), Taxa descriptions; Rows: taxa; Sub-rows: repetition number (1–6).
- Taxa descriptions include family/subfamily and order (e.g., Sp1 = Baetidae, Ephemeroptera; Sp13 = Chironomidae/Orthocladiinae, Diptera, etc.).
- Italicized taxa indicate genus-level identifications.

## Quality control
- The same person collected all substrate samples at all sites.
- Processing occurred within 48 hours of collection.
- Taxonomic identifications corroborated by a subject-matter expert.
- Records cross-verified by two professionals.

## Data provenance and contributors
- Sample collection: Palacios, E.; Medina, K.; Loarte, E.
- Laboratory analysis: Palacios, E.; Gamboa, M.; Brown, L.
- Supporting information: Castañeda, A.; Polo, R.; Tapia, P.
- Planning and Management: Medina, K.; Loarte, E.; Brown, L.; Pellicciotti, F.

## References
- Domínguez, E., & Fernández, H. (2009). Macroinvertebrados bentónicos sudamericanos. Sistemática y biología.
- Prat, N., Acosta, R., Villamarín, C., & Rieradevall, M. (2011). Guía para el reconocimiento para larvas de Chironomidae (Diptera) de los ríos altoandinos de Ecuador y Perú.