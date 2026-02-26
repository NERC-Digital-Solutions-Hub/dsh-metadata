# Cumbrian Lakes plankton and fish data, used for turning points and early warnings analysis (1940 to 2013)

## Overview
- Dataset describing phyto- and zooplankton counts, chlorophyll concentration, and fish catch data from the Cumbrian Lakes: Windermere (North and South basins), Esthwaite Water, and Blelham Tarn.
- Time span: 1940–2013 (phytoplankton/chlorophyll data cover various subperiods; fish data extend to present in the catch records).
- Original data sources: Freshwater Biological Association (FBA) and Centre for Ecology & Hydrology (CEH) and predecessor institutes; CEH has continued data collection since 1989.
- Usage note: Strongly recommended to contact the data authors prior to reuse; data are provided with rights reserved (Database Right/Copyright © NERC - CEH/FBA).

## Data files and schema (CSV)
- Windermere_fish_annual_catches.csv (23 KB)
  - Columns: date, site (NBAS, SBAS), Species (Arctic charr, perch, pike), variable (catch-per-unit-effort definitions), Catch (values).
  - Focus: annual CPUE data from anglers and gill-netting records for Windermere basins.
- Cumbrian_Lakes_phyto_allsites.csv (2,505 KB)
  - Columns: month, year, site (BLEL, ESTH, NBAS, SBAS), taxon (phyto genera code), value (cells/ml, organism units per ml), counter, chamber, form.
  - Focus: phytoplankton abundance by genus across all sites.
- Cumbrian_Lakes_zoo_allsites.csv (286 KB)
  - Columns: month, year, site, variable (zooplankton counts by taxon/summary), value (individuals per litre), confound.var.
  - Focus: zooplankton data (e.g., Daphnia, Bosmina, calanoids, cyclopoids) across sites.
- Cumbrian_Lakes_chl_allsites.csv (288 KB)
  - Columns: date, month, year, site, variable (chlorophyll data identifier TOCA), value (mg m^-3), confound.var.
  - Focus: chlorophyll a concentrations across sites and times.
- Note: Data include site-specific identifiers and context about counting techniques, analysts, and processing.

## Spatial and temporal footprint
- Sampling locations (approximate NGR grid references):
  - Windermere North Basin: NY383006
  - Windermere South Basin: SD382914
  - Esthwaite Water: SD358972
  - Blelham Tarn: NY366006
- Spatial granularity: lake basins (not gridded GIS layers); data are aggregated at lake-basin level with time-stamped observations.
- Temporal coverage:
  - Fish CPUE and annual catches: 1940–2013.
  - Phytoplankton and chlorophyll: varying series, with key usage in 1964–2009 (phytoplankton) and 1964–2009 (cristal/ chlorophyll processing window); some species-specific series extend to 2003–2005.
  - Zooplankton: 1964–2009 (filter counts) and 1979–2010 (species-level data for Windermere North Basin).

## Sampling design and methods (GIS-relevant context)
- Sampling regime: weekly to biweekly collection at the deepest point of each lake.
- Collection and preservation:
  - Phytoplankton: Lund tubes; fixation with Lugol’s iodine for counts.
  - Chlorophyll: filtration and methanol extraction; spectrophotometric measurement.
  - Zooplankton: two sources (species-level net tows for Windermere North Basin; aggregate filter counts from chlorophyll samples).
  - Fish: Arctic charr (angler CPUE and gill nets), perch (standard traps), pike (gill nets); standardised long-term effort records.
- Data processing:
  - Phytoplankton counts converted to genus-level totals to reduce analyst inconsistencies.
  - Zooplankton and chlorophyll data derived from standard methods described in supporting references.
- Analytical use (context for GIS work): data underpin turning points and early warning analyses; useful for multi-decadal, multi-taxa spatial-temporal visualization and trend detection.

## Data quality, standards, and caveats
- Analysts’ variability addressed by genus-level aggregation for phytoplankton.
- Consistent long-term methodology described across references (Lund 1949; Talling 1974, 2003; Le Cren 2001; Winfield et al. 2008).
- Data rights and re-use restrictions; recommended direct contact with data authors for re-use.

## Practical GIS considerations
- Data integration:
  - Combine lake-level time series across four sites; align by site and basin identifiers (BLEL, ESTH, NBAS, SBAS).
  - Merge phytoplankton, zooplankton, chlorophyll, and fish CPUE datasets by site and year/month where appropriate.
- Spatial visualization:
  - Map-based displays can plot site-level time series and compare basins (North vs South Windermere; Esthwaite Water; Blelham Tarn).
- Temporal alignment:
  - Be mindful of differing temporal resolutions (monthly/weekly counts for phytoplankton/zooplankton; annual for fish CPUE; multi-year aggregations).
- Data preparation steps:
  - Validate site codes and corresponding lake basins.
  - Normalize CPUE definitions by method when comparing across species or basins.
  - Consider converting to standardized indices for cross-taxa temporal comparisons.
- Re-use guidance:
  - Contact authors prior to data reuse; acknowledge data provenance and the Burthe et al. (2015) context where applicable.

## References and related material
- Burthe et al. (2015) – turning points and early warnings analysis (data usage context).
- Supplementary Table S1 in Burthe et al. 2015 for full details.
- Key methodological references: Lund (1949); Talling (1974, 2003); Thackeray et al. (2013); Winfield et al. (2008a, 2008b).