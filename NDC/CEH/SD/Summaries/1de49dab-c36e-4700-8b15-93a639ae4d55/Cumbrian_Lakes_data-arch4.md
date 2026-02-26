# Cumbrian Lakes plankton and fish data, used for turning points and early warnings analysis (1940 to 2013)

## Overview
- Dataset describing phyto- and zooplankton counts, chlorophyll concentration, and fish catch data from the Cumbrian Lakes (Blelham Tarn, Esthwaite Water, Windermere north and south basins).
- Used to support turning points and early warnings analysis (Burthe et al. 2015); data span 1940–2013 with variable series lengths across species/sites; Windermere fish data available only for Windermere.
- Original data collected by the Freshwater Biological Association (FBA) and then by CEH and predecessors since 1989. A data reuse note recommends contacting the data authors before reuse.

## Data assets and structure
- Four CSV datasets with dataset-specific fields:
  - Windermere_fish_annual_catches.csv (23 KB)
  - Cumbrian_Lakes_phyto_allsites.csv (2,505 KB)
  - Cumbrian_Lakes_zoo_allsites.csv (286 KB)
  - Cumbrian_Lakes_chl_allsites.csv (288 KB)

## Content details by dataset
- Windermere_fish_annual_catches.csv
  - Columns: date, Year of sampling, site (NBAS/SBAS), Species (Arctic charr, perch, pike), variable (CPUE type), Catch (values)
  - Notes: CPUE units vary by species and method (nets, anglers, traps); covers annual catches from Windermere north and south basins.
- Cumbrian_Lakes_phyto_allsites.csv
  - Columns: month, year, site (BLEL, ESTH, NBAS, SBAS), taxon (phytoplankton genus code), value (cells/ ml), counter, chamber, form
  - Notes: Phytoplankton counts per ml; counts aggregated to genus level to reduce analyst variability; chlorophyll data not in this file but in separate chl file; data used 1978–2003/2005 for analysis.
- Cumbrian_Lakes_zoo_allsites.csv
  - Columns: month, year, site, variable (zooplankton counts, e.g., Daphnia, Bosmina, total calanoids/cyclopoids, total zooplankton), value (individuals per litre), confound.var
  - Notes: Species-level data (Windermere North Basin) and aggregate filter-paper counts across lakes; data used 1964–2009 (filters) and 1979–2010 (species-level).
- Cumbrian_Lakes_chl_allsites.csv
  - Columns: date, month, year, site, variable (chlorophyll data code), value (mg m^-3), confound.var
  - Notes: Chlorophyll a concentration per ml; methods/processing details linked to chlorophyll extraction; data used 1964–2009.

## Temporal and spatial coverage
- Spatial sites: Blelham Tarn (BLEL), Esthwaite Water (ESTH), Windermere North Basin (NBAS), Windermere South Basin (SBAS).
- Windermere data provide fish CPUE from 1940s onward; other lakes have phytoplankton, zooplankton, and chlorophyll data across varying periods (mid-1960s to 2009+ for some variables; phytoplankton 1978–2003/2005 for counts).

## Collection methods and processing
- Sampling regime: weekly to biweekly at the deepest point of each lake.
- Collection methods:
  - Phytoplankton: weighted tube sampling, Lugol’s fixative for counts, Lund chambers for enumeration; counts summed to genus level prior to analysis to reduce inter-analyst differences.
  - Chlorophyll: filtration, methanol extraction, spectrophotometric analysis.
  - Zooplankton: net tows over upper 40 m (species-level Windermere data) and filter-paper counts from chlorophyll water samples.
  - Fish: Arctic charr, perch, and pike data collected via angler catch-and-effort records, gill nets, and standardized trap methods (historic records and ongoing sampling since mid-20th century).
- Analytical methods:
  - Phytoplankton: counts per chamber, genus-level aggregation.
  - Chlorophyll: spectrophotometric concentration (mg m^-3).
  - Zooplankton: microscopic enumeration; aggregation of some taxa to total calanoids/cyclopoids.
  - Fish: annual mean CPUE calculations by basin and method; age/effort standardization via netting protocols and angler-record data.

## Provenance, rights, and reuse
- Original data produced by FBA; subsequently maintained/collected by CEH and predecessors.
- Rights notice: Database Right/Copyright © NERC - Centre for Ecology & Hydrology/ Freshwater Biological Association (FBA).
- Reuse guidance: strongly recommended to contact the data authors directly before re-use to ensure proper understanding of context and metadata.

## Data governance and usability implications for Data Leaders
- Data scope is multi-taceted (phytoplankton, zooplankton, chlorophyll, and fish CPUE) across four lakes with long historical records.
- Metadata clarity issues to watch:
  - Variable units and CPUE definitions across species and methods.
  - Some datasets log plant/animal counts with multiple counting/measurement conventions; cross-dataset alignment requires careful mapping.
  - Data overlap and consistency vary by lake and time period; counts aggregated to genus level for phytoplankton to mitigate analyst differences.
- Data quality considerations:
  - Fragmented data continuity across early years and across sites; requires validation when reusing for new analyses.
  - Access restrictions and provenance caution due to rights; ensure proper author liaison for data reuse.
- Opportunities for data leaders:
  - Use as a case study for end-to-end data lifecycle: data collection, processing, metadata capture, and long-term preservation.
  - Demonstrates importance of standardizing units, documenting counting methods, and maintaining provenance for multi-series ecological datasets.
  - Potential to align with broader data-sharing practices, ensuring discoverability (through metadata standards) and co-ownership with data producers.