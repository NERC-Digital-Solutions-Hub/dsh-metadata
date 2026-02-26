# Summary of data regarding Colt Park drought experiment

## Overview
- Data set accompanies the paper: Cole et al. (2019) Grassland biodiversity restoration increases resistance of carbon fluxes to drought.
- Location: Colt Park meadows, Ingleborough National Nature Reserve (54°12'N, 2°21'W).
- Context: drought experiment superimposed on a long-term grassland restoration experiment (fertiliser and seed addition).
- Timeline: experimental plots cut for hay on 16 July 2013, grazed by cattle and sheep afterward.
- Drought treatment: rain-out shelters implemented 5 June–10 July 2013 with ambient and control shelter comparisons.
- Original plot numbering and layout referenced from earlier restoration studies (Smith et al. 2000; 2003; 2008; De Deyn et al. 2011).

## Experimental design and treatments
- Grassland restoration treatments (since 1990):
  - Fertiliser applied vs. no fertiliser.
  - Seed addition vs. no seed addition.
- Drought treatment (three levels) superimposed on restoration treatments:
  - Ambient (no rain-out shelter).
  - Control shelter (rain-out shelter with holes).
  - Drought (rain-out shelter).
- Shelters were transparent PVC structures (dimensions provided) and the drought period spanned early June to early July 2013.
- Treatments are encoded in dataset columns (e.g., c, cs, f, sf for restoration; dr, csh, c for drought, ambient, etc.).

## Data files and key variables

- Averagesoilmoisture2013
  - Purpose: daily/periodic soil moisture measurements averaged per plot.
  - Key columns: unique.id, julian, date, year, plot, block, treatment, drought, seed, fertiliser, shelter, percent.mean.
  - Measurement method: three readings per plot (ML3 ThetaProbe, Delta-T, Cambridge); units in percent moisture.
  - Data notes: missing data marked NA; treatment codes explained.

- BacteriarelativeabundanceTRFLP2013
  - Purpose: bacterial community relative abundances by TRFLP peaks.
  - Key columns: unique.id, sample, plot, time, plus X52–X505 for peak abundances.
  - Methods: DNA extraction and 16S rRNA markers; TRFLP peak abundances.

- ColtParkdailyprecipitation2013
  - Purpose: daily precipitation (mm).
  - Key columns: julian, mm.
  - Source: Colt Park automatic weather station.

- Ecosystemrespiration2013
  - Purpose: ecosystem respiration flux (g CO2 m^-2 h^-1).
  - Key columns: unique.id, date, plot, CO2flux, block, trt, dr, seed, fert, julian.
  - Measurement: IRGA with two-minute headspace closures; methodology per Ward et al. (2013).

- FungirelativeabundanceTRFLP2013
  - Purpose: fungal community relative abundances by TRFLP peaks.
  - Key columns: unique.id, sample, plot, time, plus X62–X485 for peak abundances.
  - Time codes: 1 before drought, 2 during drought, 3 after drought (August), 4 after drought (November).
  - Methods: fungal ITS markers; TRFLP peaks.

- NetEcosystemExchange2013
  - Purpose: net ecosystem CO2 exchange flux.
  - Key columns: unique.id, date, plot, CO2flux, block, trt, dr, seed, fert, julian.
  - Measurement: IRGA with two-minute closures; follows Ward et al. (2013).

- PARdata2013
  - Purpose: photosynthetically active radiation and microclimate context.
  - Key columns: unique.id, date, julian, plot.no, PAR, soiltemp, airtemp.
  - Units: PAR (µmol m^-2 s^-1); temperatures in °C.

- Plantcommunitycomposition2013
  - Purpose: plant species composition per plot.
  - Key columns: plot, trt, drht, fert, seed, block; species columns (e.g., Agrostis capillaris, Veronica chamaedrys) with percentage cover.
  - Includes total vascular plant cover per plot in central 706 cm^2 survey area (29 June–4 July 2013).

- Soilandairtemperature2013
  - Purpose: soil and air temperatures at high temporal resolution.
  - Key columns: seq, time, soil9886420–air9886452 (individual logger readings; soil/air distinguished by code in column names).

- Soildata2013
  - Purpose: soil biogeochemistry and microbial properties.
  - Key columns: unique.id, time, MBNmcg, MB.CN, DOCmcg, DONmcg, ph, BACTmcg, FUNGImcg, FBratio.
  - Measurements: microbial biomass, dissolved organic carbon/nitrogen, pH, PLFA markers for bacteria and fungi.

- Speciesdiversity2012restorationplots
  - Purpose: plant diversity and biomass metrics from 2012, pre-drought baseline.
  - Key columns: original.plot.number, total, plot.no, block, treatment, seed, fert, grss.dwt, legs.dwt, forbs.dwt, para.dwt, moss.dwt, other.dwt, root.dwt.
  - Additional metrics: sp.richness (vascular species count), procentual N/C content in dominant biomass fractions (grss.n, grss.c, grss.cn, etc.).

## Data structure, relationships and integration
- Common identifiers:
  - plot, block, treatment codes (fert, seed, dr, etc.) across files enable cross-file joins.
  - unique.id serves as a per-measurement identifier in several datasets; julian/date fields anchor temporal alignment.
- Time and drought context:
  - drought-related columns (dr, csh, ambient) link soil moisture, CO2 flux, respiration, TRFLP profiles, and plant measures to drought stage (before/during/after).
- Unit and method consistency:
  - Explicit unit notes per file (e.g., soil moisture in percent, CO2 flux in g CO2 m^-2 h^-1, PAR in µmol m^-2 s^-1, PLFA in µg g^-1 soil dwt, etc.).
  - Measurement methods referenced (e.g., ThetaProbe for soil moisture, IRGA for fluxes, Bligh-Dyer PLFA extraction).

## Data quality, limitations, and notes
- Missing data indicated as NA in files.
- Data are derived from long-term restoration experiments with careful documentation of treatments and plotting; some data (e.g., pre-drought 2012 values) come from earlier campaigns but are integrated for context.
- User should account for multi-year and multi-treatment structure when aggregating (e.g., baseline vs. treatment effects, drought response).

## Usage guidance
- Suitable for multi-factor analyses of drought effects on soil moisture, microbial communities, plant community composition, and carbon fluxes.
- Enables creation of dashboards or self-serve analyses by linking plots, treatments, timepoints, and measured responses across datasets.
- Can support cross-sectional (plot-level) and longitudinal (temporal) investigations into restoration success and drought resilience.

## References
- Core paper: Cole, A. J. et al. 2019. Grassland biodiversity restoration increases resistance of carbon fluxes to drought. Journal of Applied Ecology.
- Foundational restoration and meadow studies cited within the data description (Smith et al. 2000; 2003; 2008; De Deyn et al. 2011) and methodological references (Ward et al. 2013; Bardgett et al. 1996; White et al. 1979; Plassart et al. 2012).