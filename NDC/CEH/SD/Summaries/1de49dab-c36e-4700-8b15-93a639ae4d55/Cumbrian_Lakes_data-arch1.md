# Cumbrian Lakes plankton and fish data, used for turning points and early warnings analysis (1940 to 2013)

## Scope and contents
- Dataset describing phytoplankton, zooplankton, chlorophyll, and fish catch data from four Cumbrian lakes.
- Used for turning points and early warnings analysis (Burthe et al. 2015).
- Time series lengths vary by species and site; fish data available only for Windermere.

## Datasets included
- Windermere_fish_annual_catches.csv
  - Columns: date, Year of sampling, site (NBAS/SBAS), Species, variable (catch-per-unit-effort type), Catch (CPUE values).
- Cumbrian_Lakes_phyto_allsites.csv
  - Columns: month, year, site (BLEL, ESTH, NBAS, SBAS), taxon (four-letter genus code), value (cells/ml), counter, chamber, form (CELL/COLO).
- Cumbrian_Lakes_zoo_allsites.csv
  - Columns: month, year, site, variable (zooplankton taxa counts), value (individuals per litre), confound.var.
- Cumbrian_Lakes_chl_allsites.csv
  - Columns: date/month, year, site, variable (TOCA for chlorophyll), value (chlorophyll a in mg/m^3), confound.var.

## Study lakes and locations
- Windermere North Basin (NBAS) and Windermere South Basin (SBAS)
- Esthwaite Water (ESTH)
- Blelham Tarn (BLEL)
- Approximate grid references provided for each site.

## Sampling regime
- Weekly to biweekly sampling at the deepest point of each lake.

## Collection and processing methods
- Phytoplankton:
  - Collected with weighted tubes; fixed with Lugol’s iodine for counts.
  - Concentrated, examined in Lund counting chambers; counts summed to genus level for consistency.
  - Chlorophyll samples processed separately for later extraction.
- Chlorophyll:
  - Filter water through GF/C filters; extracted in methanol; measured spectrophotometrically.
- Zooplankton:
  - Species-level Windermere NB data (1979–2010) from vertical net tows; ethanol-fixed then formalin-preserved.
  - Crustacean zooplankton counts from GF/C filters (1964–2009).
- Fish (Windermere):
  - Arctic charr CPUE from anglers (1966–present) and gill nets on spawning ground (1940–present).
  - Perch CPUE from standardized traps (1943–present).
  - Pike CPUE from gill nets (1944–present).

## Analytical methods and data processing
- Phytoplankton counts:
  - Dominant species sums used to generate genus-level data for consistency.
  - Data used in Burthe et al. 2015 spanning 1978–2003/2005 for phytoplankton.
- Chlorophyll:
  - Concentrations used from 1964–2009 in analyses.
- Zooplankton:
  - Species-level data (Windermere NB) and aggregated crustacean counts used (1979–2010 and 1964–2009 respectively).
- Fish:
  - Annual mean CPUEs calculated for each species, method, basin, and year (1940–2013 for fish data in analyses).
- General notes:
  - Data span varies by dataset; cross-dataset integration enables multi-taxa, multi-lake time-series analyses.

## Data provenance and reuse
- Original data collected by Freshwater Biological Association (FBA); later by CEH and predecessor IFE since 1989.
- Strong recommendation to contact data authors prior to reuse (metadata and data rights considerations).
- Full details and supplementary context referenced in Burthe et al. 2015 and associated sources.

## Key references
- Le Cren (2001); Lund (1949); Talling (1974, 2003); Thackeray et al. (2013); Winfield et al. (2008a, 2008b).