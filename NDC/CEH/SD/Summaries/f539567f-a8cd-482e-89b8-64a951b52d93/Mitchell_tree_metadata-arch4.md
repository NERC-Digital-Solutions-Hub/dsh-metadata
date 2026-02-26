# Functional and epiphytic biodiversity differences between nine tree species in the UK.

## Overview
- Addresses global concern about tree pests and pathogens and the ecological consequences of shifts in tree species composition.
- A UK study combining biodiversity (bryophytes and lichens) with functional soil and bark measurements across nine tree species at six UK sites.
- Aims to understand how loss or decline of key tree species (Quercus petraea, Q. robur, Fraxinus excelsior) and potential replacements affect ecosystem functions and biodiversity.

## Data scope and study design
- Sites: six locations across the UK ( Knightshayes Court, Bodnant, Dinefwr, Westonbirt, Crathes, Mount Stuart ).
- Trees: 230 trees sampled (approximately 35–40 per site) across nine species including Quercus petraea, Q. robur, Fraxinus excelsior, Acer pseudoplatanus, Castanea sativa, Fagus sylvatica, Quercus cerris, Quercus rubra, Tilia x europaea.
- Measurements span:
  - Tree and bark characteristics (DBH, height, bark pH, bark features, ridge/furrow metrics, bark hardness).
  - Soil properties around each tree (mineralized N, total C and N, LOI, pH in water and CaCl2, soil moisture indicators, mineralizable N).
  - Decomposition processes using litter bags and wooden sticks.
  - Soil temperature near the decomposition site (hourly measurements).
  - Lichen and bryophyte communities on trunk and, for some trees, branches and twigs.
  - Bark chemistry and physical traits (water holding capacity, pH, conductivity, bark density).
  - FTIR spectral data of the soil for chemical characterization.
- Data management: designed to be stored in a relational database with a central Trees table and linked tables for all other data files.

## Experimental design and data collection
- Tree-level data collection around each tree:
  - Girth/DBH, height, surrounding habitat, sectoral layout (four cardinal sectors), distance to nearest tree, and species/DBH of neighbors.
  - Site habitat context categorized as semi-natural woodland, grassland/parkland, or garden.
- Decomposition protocol:
  - Four Whatman filter papers in a nylon mesh bag, buried 3 m south of each tree with a wooden stick; monitored for  time and weight changes to derive decomposition rates.
- Soil sampling:
  - Eight soil cores per tree (25 mm diameter, 100 mm depth) around the trunk, bulked per tree.
  - Analyses include mineralized N, LOI, pH (H2O and CaCl2), total C and N, and subsequent FTIR analysis on milled soil.
- Lichen and bryophyte surveys:
  - Survey of all species from ground level to 1.75 m on trunk; additional surveys on branches if reachable.
- Canopy and bark metrics:
  - Canopy estimates using spherical densiometer; bark pattern, fissures, furrows, ridges; bark hardness (durometer) across eight measurements per quadrat.
- Temporal and instrumental details:
  - Hourly soil temperature logging (iButton DS1922L).
  - FTIR measurements using Bruker Vertex 70 with ATR/KRS-5; spectra pre-processed with Savitzky-Golay derivatives.

## Data files and structure
- Relational database design with central table:
  - Trees (ANS_Tree_code) as central hub; all other data tables link via this code.
  - Associated files/tables include: Habitat_structure, Decomposition, Temperature, Soil, FTIR, Bark_chemistry, Bark_plot, Bryophytes, Lichens.
  - Lichen_names and Bryophyte_names provide taxonomic authority and codes for standardization.
- Table-level descriptions (examples):
  - Trees: tree identity, site, species, tags, GPS, DBH, height, date, sector attributes, bark/soil sampling indicators, and re-detection notes.
  - Habitat_structure: sectoral proximity to nearest tree, distance measurements, and neighbor DBH.
  - Decomposition: burial date, retrieval date, time in soil, weight changes, decomposition constants (K_paper, K_stick), and notes.
  - Temperature: date-time and soil temperature readings.
  - Soil: LOI, pH (H2O and CaCl2), weight used, total C/N, mineralizable N before/after incubation, and related measurements.
  - FTIR: lab code and spectrum range data for soil chemistry.
  - Bark_chemistry and Bark_plot: bark dryness, water holding capacity, density, pH, conductivity; plot-level bark pattern, fissure/ridge characteristics, and bark hardness.
  - Bryophytes/Lichens: presence/absence data per tree (and branches/twigs where measured) linked to Taxon_names tables.
- Documentation and metadata:
  - Tables 1–14 provide explicit metadata for each data file, including variable definitions, units, and data collection notes.
  - Figure 1 diagrams the relational links between files to enable data reassembly.

## Data stewardship, provenance, and access
- Data are organized to support discoverability, discoverable metadata, and clear linkage across data types.
- Files are structured to facilitate integration with other datasets within a single relational database framework.
- Acknowledgments note funding sources and project scope:
  - Funded by Defra through the BBSRC PuRpOsE grant BB/N022831/1.
  - Additional funding from the Scottish Government’s Rural and Environment Research and Analysis Directorate (RERAD).

## Implications for data leadership and reuse
- The dataset provides a comprehensive, multi-scale view of tree-associated biodiversity and ecosystem function across multiple UK sites and species.
- Strong data governance features:
  - Centralized Tree-centric schema with clear cross-references to ecological measurements, enabling traceability from data to field observations and analyses.
  - Taxonomic standardization through separate names tables for lichens and bryophytes.
- Considerations for users and data strategy:
  - Rich metadata and explicit data tables support reuse, cross-site comparisons, and integration with other biodiversity or soil function datasets.
  - The dataset emphasizes user needs for data discoverability, interoperability, and context (site history, sampling design, and measurement protocols).
- Limitations and scope:
  - The document is a data descriptor; it outlines data collection and structure but does not present analytical results or conclusions.

## References and acknowledgments
- Cited related ecological and methodological sources (e.g., Allen 1989; McLean 1982; Pella & Colombo 1973; Ellis et al. 2015; Mitchell et al. 2014, 2019) to support methods and context.
- Funding acknowledgments as noted above.