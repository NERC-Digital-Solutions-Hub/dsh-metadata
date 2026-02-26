# Functional and epiphytic biodiversity differences between nine tree species in the UK.

## Overview
- Addresses global concern about tree pests and pathogens and the consequences for ecosystem functions and biodiversity.
- Study spans six UK sites with multiple tree species at each site to assess functional metrics and epiphytic biodiversity (bryophytes and lichens) on trees threatened by disease.
- Focused variables include soil processes (nitrogen mineralization, decomposition, total soil C and N, loss on ignition), soil chemistry (pH, temperature, moisture proxies), bark properties (water holding capacity, pH, conductivity), and epiphytic communities on trunks and, where possible, branches.
- Tree measurements include girth/DBH, height, canopy context, and spatial relationships to nearby trees.

## Dataset scope and structure
- Experimental framework and data are organized as a relational database designed for integrated analysis.
- Central table: Trees (ANS_Tree_code) with linked tables for each data domain.
- Data domains and corresponding files/tables:
  - Habitat_structure (surrounding habitat and spatial relations around each tree)
  - Decomposition (litter bag experiment and decomposition rates for paper and sticks)
  - Temperature (soil temperature logged hourly near each tree)
  - Soil (per-tree soil sampling with analyses for LOI, pH, total N and C, ammonium and oxidized N before/after incubation, mineralizable N)
  - FTIR (Fourier-transform infrared spectra of ball-milled soil, preprocessed)
  - Bark_chemistry (water holding capacity, bark pH/conductivity, density)
  - Bark_plot (bark patterns, fissures, ridge/furrow characteristics, bark hardness, and other per-quadrat measurements)
  - Bryophytes and Lichens (presence/absence data on trunk and reachable branches/twigs)
  - Taxon name reference files: Bryophyte_names and Lichen_names (with Taxon_code mappings)
- Data integration and linking: All files link to the central Trees table via ANS_Tree_code; Lichen_names/Bryophyte_names link to their respective presence data.

## Site selection and experimental design
- Six sites chosen for historical management context with old trees (often >150 years) to maximize species representation.
- Sites include The National Trust gardens (Knightshayes Court, Bodnant, Crathes), Westonbirt (Arboretum), Dinefwr (National Trust for Scotland), Mount Stuart (private garden).
- Target species include: Acer pseudoplatanus, Castanea sativa, Fagus sylvatica, Fraxinus excelsior, Quercus cerris, Quercus petraea, Quercus robur, Quercus rubra, and Tilia x europaea.
- Numerical sampling: 230 trees across sites, ~35–40 per site; species counts per site detailed in the dataset.

## Data collection and key variables
- Tree data: For each tree, record site, Latin species, tags, GPS/grid coordinates, slope/aspect, height, DBH, date of recording, records of semi-natural woodland vs garden settings, and indicators for bark sampling or soil sampling.
- Habitat structure: Sector-based around-tree measurements including distance to nearest tree/shrub and neighbor species.
- Decomposition: Decomposition experiments using four filter papers in a nylon mesh bag buried 3 m south of each tree; measured paper and stick mass loss over time and calculated K values; notes on bag/stick status.
- Soil: Eight soil cores per tree (25 mm diameter, 100 mm depth) around the trunk; analyses include:
  - LOI, pH in water and in CaCl2
  - Total N and C, after homogenization and milling
  - Mineralizable N and ammonium/oxidized N before and after incubation
- FTIR: Preprocessed spectra (4000–400 cm-1) with Savitzky-Golay derivatives; baseline corrections; data available in FTIR file with corresponding metadata.
- Bark chemistry and physical traits: Assessed water holding capacity, bark pH and conductivity, bark density; bark samples processed and analyzed with standardized methods.
- Bark plot characteristics: On four cardinal plots per tree, measured bark pattern (smooth, fissured, flaky, rugose, patterned), fissure shapes, ridge/furrow dimensions, ridge alignment, bark hardness (durometer), and other bark features; measurements include per-plot and per-tree summaries.
- Lichen and bryophyte communities: Surveyed on trunk from ground level to 1.75 m; branch/ twig sampling where reachable; presence/absence data collected and named using taxon reference lists.

## Data quality, preprocessing, and documentation
- FTIR data preprocessing performed with Savitzky-Golay derivatives to enhance discrimination among species and locations.
- Preprocessing and data processing steps are documented in the metadata (e.g., Table 8 for FTIR, Table 7 for soil, Table 9 for bark chemistry, Table 10 for bark plot).
- Data availability notes:
  - Some trees lacked ibutton temperature data due to resource constraints.
  - Branch lichens could not be sampled for all trees; lichen/bryophyte data are presence/absence and limited to accessible parts.
  - The dataset is designed for robust cross-domain analyses but contains inherent sampling limitations.

## Documentation, access, and provenance
- Metadata-rich dataset with explicit file/table descriptions (Tables 1–14) detailing content, units, and column definitions.
- Central data descriptor: Trees table as the linking hub; supplementary tables provide site, environmental, and biological observations.
- Data provenance: Authors and affiliations listed (The James Hutton Institute; independent lichenologist), with contact for data inquiries.
- Funding and acknowledgments: Defra/BBSRC PuRpOsE grant; Scottish Government program support; explicit funding sources.

## Reuse considerations and governance implications
- Strengths for data stewardship:
  - Rich, multi-domain ecological dataset with thorough metadata and clear relational structure.
  - Use of standardized taxon reference lists and coded linking keys (ANSTree_code, Taxon_code) facilitates interoperability and future integration.
  - Documented methods and instrumentation allow reproducibility and quality assessment.
  - Data organization supports cross-site and cross-species comparisons of biodiversity, functional soil processes, and epiphyte communities.
- Practical constraints for reuse:
  - Some data gaps (ibutton gaps, limited branch sampling) should be accounted for in analyses and interpretations.
  - No explicit licensing or data-access terms stated in the metadata; users should seek permission or contact the authors for reuse rights.
  - The dataset focuses on historic garden settings, which may influence generalizability to broader landscapes.

## Contact and references
- Contact: ruth.mitchell@hutton.ac.uk
- Acknowledged funders: Defra (PuRpOsE project) and Scottish Government program
- Representative methodological references cited within the metadata (e.g., standard soil and bark analysis methods) are provided to support reproducibility and comparability.

## Summary of usefulness for data stewardship
- Provides a comprehensive, well-documented, multi-domain biodiversity dataset suitable for archiving and future sharing.
- Demonstrates effective data governance practices: central canonical key, linked data across domains, and explicit taxon references.
- Highlights common stewardship challenges such as incomplete data, heterogeneous data types, and the need for clear licensing and access terms to facilitate reuse.