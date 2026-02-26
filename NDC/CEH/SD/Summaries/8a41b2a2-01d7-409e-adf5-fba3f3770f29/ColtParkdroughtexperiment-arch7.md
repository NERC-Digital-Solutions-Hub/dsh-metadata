# Summary of data regarding Colt Park drought experiment

## Geographic and Experimental Context
- Location: Colt Park meadows, Ingleborough National Nature Reserve, latitude 54°12'N, longitude 2°21'W.
- Part of a long-term grassland restoration experiment; drought treatment superimposed on fertiliser and seed addition treatments.
- Experimental layout described (Figure 1) with original plot numbers linked to Smith et al. (2000) and De Deyn et al. (2011).
- All plots cut for hay on 16 July 2013 and subsequently grazed by cattle and sheep.

## Experimental Design
- Treatments:
  - Grassland restoration: fertiliser application (fert) vs. no fertiliser (nofert); seed addition (seed) vs. no seed (noseed).
  - Drought: ambient (no rain-out shelter), drought (rain-out shelter), control shelter (rain-out shelter with holes).
- Drought shelters used from 5 June to 10 July 2013.
- Fertiliser applied since 1990 (with exceptions in 2009–2010); seed addition began in 1990 with 19 species.
- The design integrates both restoration management and climate manipulation to study effects on ecosystem function.

## Data Files and Main Variables (2013)
- Averagesoilmoisture2013
  - Key variables: unique.id, julian, date, year, plot, block, treatment, drought, seed, fertiliser, shelter, percent.mean (soil moisture).
- BacteriarelativeabundanceTRFLP2013
  - Key variables: unique.id, sample, plot, time; relative abundance for bacterial TRFLP peaks (columns X52–X505).
- ColtParkdailyprecipitation2013
  - Key variables: julian, mm (precipitation in mm per day).
- Ecosystemrespiration2013
  - Key variables: unique.id, date, plot, CO2flux (g CO2 m-2 hr-1), block, trt, dr, seed, fert, julian.
- FungirelativeabundanceTRFLP2013
  - Key variables: unique.id, sample, plot, time, block, treatment, drought, seed, fertiliser; relative abundance for fungal TRFLP peaks (columns X62–X485).
- NetEcosystemExchange2013
  - Key variables: unique.id, date, plot, CO2flux (g CO2 m-2 hr-1), block, trt, dr, seed, fert, julian.
- PARdata2013
  - Key variables: unique.id, date, julian, plot.no, PAR ( µmol m-2 s-1 ), soiltemp, airtemp.
- Plantcommunitycomposition2013
  - Key variables: plot, species cover columns (Agrostis capillaris to Veronica chamaedrys), trt, drht, fert, seed, block, sp.richness.
- Soilandairtemperature2013
  - Key variables: seq, time, soil and air temperature readings by logger (soil9886420–air9886452).
- Soildata2013
  - Key variables: unique.id, time (p=before drought, m=during drought, a=after drought), MBNmcg, MB.CN, DOCmcg, DONmcg, ph, BACTmcg, FUNGImcg, FBratio.
- Speciesdiversity2012restorationplots
  - Key variables: original.plot.number, plot.no, block, treatment, seed, fert, grss.dwt, legs.dwt, forbs.dwt, para.dwt, moss.dwt, other.dwt, root.dwt, sp.richness, grss.n, grss.c, grss.cn, forb.n, forb.c, forb.cn, legs.n, legs.c, legs.cn, para.n, para.c, para.cn.

- Notes:
  - Missing data indicated as NA.
  - All measurements accompanying the dataset are linked to the Colt Park drought experiment from 2013, with extensive methodological detail and measurement devices noted in the metadata.

## Data Coding and Quality
- Treatments coded consistently:
  - Fertiliser: fert vs. nofert
  - Seed: seed vs. noseed
  - Drought: dr (drought), csh (control shelter), c (ambient)
  - Shelter timing: before, during, after drought
- Plot and block identifiers enable spatial analyses and potential GIS integration.
- Unique identifiers (unique.id) accompany measurements across files.

## Spatial and GIS Considerations
- Data are organized by plot numbers within Colt Park meadows, enabling spatial analysis and map-based visualization of treatment effects.
- Geographic context (location and plot-level layout) supports integration with GIS for landscape-scale interpretation of drought and restoration impacts.

## Context and References
- Associated with the study: Cole, A. J. et al. 2019, Grassland biodiversity restoration increases resistance of carbon fluxes to drought, Journal of Applied Ecology.
- Underlying restoration and meadow-management research referenced (Smith et al. 2000–2011; Ward et al. 2013; Plassart et al. 2012; etc.).