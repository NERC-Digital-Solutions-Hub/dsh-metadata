# Data access and citation details

- This data record documents the dung beetle community data from a before-and-after El Niño experiment in the Brazilian Amazon, published as França et al. (2019). The dataset is hosted by the NERC Environmental Information Data Centre, with licensing and reuse details available via the provided DOI.
- Proper citation: França, F.M.; Oliveira, V.H.; Louzada, J.N.C.; Vaz-de-Mello, F.Z.; Ferreira, J.N; Berenguer, E.; Gardner, T.; Lees, A.; Barlow, J. (2019). Dung beetle community data from a beforeand-after El Niño experiment in the Brazilian Amazon. NERC Environmental Information Data Centre. https://doi.org/10.5285/799db965-3ce7-4e9b-8590de6a8624d652

## Overview of the data

- Dataset name: ECOFOR_AFIRE_RAS_dung-beetles
- Content: time-series of dung beetle abundance collected with dung-baited pitfall traps at multiple plots
- Time points: 2010 (before El Niño), 2016 and 2017 (after El Niño, around six years before and 6 months after for 2016, and 18 months after for 2017)
- Geographic scope: Brazilian Amazon (Paragominas and Santarém/Belterra/Mojuí dos Campos, Pará)
- Data structure: four CSV datasheets
  - Species-all.sites_2010: plot-level beetle abundance for 381 plots (2010)
  - Species-subset.sites_2016: plot-level abundance for a subset of 36 plots (2016)
  - Species-subset.sites_2017: plot-level abundance for the same 36 plots (2017)
  - Plot-position: geographical coordinates for each study plot
- Context: part of the NERC HTMF program; funded by NERC, Darwin Initiative, EMBRAPA, CNPq, INCT Biodiversidade e Uso da Terra na Amazônia, and Formas

## Experimental design and sampling regime

- Regions and sampling framework:
  - Regions: Paragominas (PGM) and Santarém/Belterra/Mojuí dos Campos (Santarém, STM)
  - 18 catchments (32–61 km²) with 8–12 plots per catchment
  - Plot types: 234 forest plots (175 primary, 59 second-growth) and 75 non-forest plots (76 pasture, 31 mechanised agricultural lands)
  - Sampling density: ~1 plot per 4 km²
- Sampling intensity:
  - 2010: 381 plots, 3429 pitfall traps total
  - 2016/2017: subset of 36 forest plots sampled (333 pitfall traps per year)
- Disturbance gradient for 2016/2017 plots: undisturbed, logged forest, logged-and-burned forest, secondary forest
- Temporal scope:
  - 2010: April–June
  - 2016: July
  - 2017: March–April
- Plot selection and permissions: fieldwork authorized by landowners; governmental permits for protected areas

## Data collection methods

- Dung beetle sampling:
  - Pitfall traps baited with 50 g dung (80% pig, 20% human)
  - Killing solution: 5% detergent, 2% salt
  - Trap layout: traps at corners of a 3-m equilateral triangle along a 300-m transect; three sampling points (0, 150, 300 m)
  - Duration: left in field for 48 hours
- Consistency: sampling methods replicated exactly in 2016 and 2017
- Permits: verbal permissions from landowners; SISBIO/IBAMA permits for surveys in private and protected areas
- Purpose: quantify changes in dung beetle communities to understand effects of human- and climate-induced stressors on tropical biodiversity
- Authorship and responsibilities: study design, plot selection, data collection, identification, and interpretation contributed by the listed authors

## Data files and structure

- dung-beetles_ECOFOR_AFIRE_RAS_all.sites_2010.csv
  - Type: plot-level abundance matrix
  - Rows: species/morphospecies
  - Columns: plots (381 total) with plot codes (e.g., 100_1, 100_10)
- dung-beetles_ECOFOR_AFIRE_RAS_subset.sites_2016.csv
  - Type: plot-level abundance matrix for 36 plots
  - Same structure as 2010 file but with 36 plot columns
- dung-beetles_ECOFOR_AFIRE_RAS_subset.sites_2017.csv
  - Type: plot-level abundance matrix for 36 plots
  - Same structure as 2010 file but with 36 plot columns
- dung-beetles_ECOFOR_AFIRE_RAS_all_plot-position.csv
  - Plot-level coordinates
  - Columns: Plot, Municipality, UTM_X, UTM_Y
  - Note: UTM zones vary by location (Paragominas in 22M; Santarém/Belterra in 21M)

## Licensing, access and reuse

- Citation and reuse details:
  - Data should be cited as França et al. (2019) via the provided citation
  - Detailed reuse limitations and licensing information are available at the DOI link: https://doi.org/10.5285/799db965-3ce7-4e9b-8590-de6a8624d652
- Access pathway: data is published through the NERC Environmental Information Data Centre; license and terms are accessible via the DOI

## Governance and stewardship notes

- Provenance and provenance checks:
  - Clear authorship responsibilities and field protocols, permits, and funding sources documented
  - Consistent sampling design across years with a defined disturbance gradient
- Metadata and usability:
  - Describes dataset structure, file names, and plot identifiers to support discoverability and reuse
  - Includes precise sampling methods, trap layout, and coordinates (UTM) to facilitate spatial analyses
- Update and maintenance considerations:
  - Dataset currently spans three time points; any future updates should maintain consistent plot identifiers and documented methodological notes
  - Ensure licensing remains current and that citations reflect any updates in data access information
- Challenges relevant to data stewards:
  - Aligning user needs with data products (e.g., species-level vs. plot-level analyses)
  - Timely acquisition and updating of datasets across time points
  - Harmonizing metadata across multiple datasets and formats
  - Handling large numbers of plots and complex spatial coordinates across different UTM zones
  - Managing evolving permission and licensing restrictions across jurisdictions and protected areas