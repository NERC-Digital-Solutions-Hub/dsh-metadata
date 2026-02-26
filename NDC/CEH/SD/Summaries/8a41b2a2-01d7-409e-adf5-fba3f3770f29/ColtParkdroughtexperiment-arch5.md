# Summary of data regarding Colt Park drought experiment

## Overview
- Dataset linked to the publication: Cole et al. 2019, Grassland biodiversity restoration increases resistance of carbon fluxes to drought (Journal of Applied Ecology).
- Location: Colt Park meadows, Ingleborough National Nature Reserve (54°12'N, 2°21'W).
- Experimental context: drought experiment superimposed on a long-term grassland restoration study.
- Restoration treatments: fertiliser application and seed addition.
- Drought treatments: ambient (no rain-out shelter), control shelter (rain-out shelter with holes), and drought (rain-out shelter).
- Experimental layout and plot references tie to earlier work (Smith et al. 2000; 2003; 2008; De Deyn et al. 2011).
- Hay cut and subsequent grazing: all plots cut on 16 July 2013; grazed by cattle and sheep thereafter.

## Experimental design and treatments
- Fertiliser treatment: since 1990, half of plots fertilised, half not; 2009–2010 exception (no fertiliser). Fertiliser: inorganic NPK 20:10:10, 25 kg N ha-1, applied spring (21 May 2013).
- Seed addition treatment: started in 1990 with 19 species.
- Drought treatment: three levels – ambient, drought (rain-out shelter), and control shelter; shelters in place 5 June–10 July 2013.
- Measurement window: plots cut July 16, 2013; post-cut grazing occurred.

## Data files included (structure and purpose)
- Averagesoilmoisture2013
  - Measurements: soil moisture per plot (average of three readings).
  - Key columns: unique.id, julian, date, year, plot, block, treatment, drought, seed, fertiliser, shelter.
  - Codes: treatment (c, cs, f, sf); drought (dr, csh, c); seed (seed, noseed); fertiliser (fert, nofert); shelter (before, during, after).
- BacteriarelativeabundanceTRFLP2013
  - Microbial community data (bacteria) via TRFLP.
  - Key columns: unique.id, sample, plot, time; columns X52–X505 for relative abundances.
- ColtParkdailyprecipitation2013
  - Daily precipitation: julian, mm.
- Ecosystemrespiration2013
  - CO2 flux measurements (g CO2 m-2 h-1) by IR gas analyzer.
  - Key columns: unique.id, date, plot, CO2flux, block, trt, dr, seed, fert, julian.
- FungirelativeabundanceTRFLP2013
  - Fungal TRFLP data.
  - Key columns: unique.id, sample, plot, time; columns X62–X485 for relative abundances.
- NetEcosystemExchange2013
  - Net ecosystem exchange flux (g CO2 m-2 h-1) by IR gas analyzer.
  - Key columns: unique.id, date, plot, CO2flux, block, trt, dr, seed, fert, julian.
- PARdata2013
  - Photosynthetically active radiation (PAR), soil temp, and air temp.
  - Key columns: unique.id, date, julian, plot.no, PAR, soiltemp, airtemp.
- Plantcommunitycomposition2013
  - Plant species composition per plot; central 706 cm2 survey.
  - Key columns: plot; species columns (e.g., Agrostis capillaris … Veronica chamaedrys); trt, drht, fert, seed, block; sp.richness; biomass metrics (grss.dwt, legs.dwt, forbs.dwt, para.dwt, moss.dwt, other.dwt, root.dwt); nutrient content metrics (grss.n, grss.c, grss.cn, etc.).
- Soilandairtemperature2013
  - Soil and air temperatures from 30-minute measurements.
  - Key columns: seq, time; soil9886420–air9886452 (temperature readings with logger-coded identifiers).
- Soildata2013
  - Soil chemical and microbial indicators.
  - Key columns: unique.id, time (p=before drought, m=during, a=after, n=November); MBNmcg, MB.CN, DOCmcg, DONmcg, ph; BACTmcg, FUNGImcg, FBratio.
- Speciesdiversity2012restorationplots
  - 2012 pre-drought restoration plot data (before drought experiment).
  - Key columns: original.plot.number, total (vascular plant species in 2m x 2m quadrat), plot.no, block, treatment, seed, fert; grss.dwt, legs.dwt, forbs.dwt, para.dwt, moss.dwt, other.dwt, root.dwt; sp.richness; grss.n, grss.c, grss.cn, forb.n, forb.c, forb.cn, legs.n, legs.c, legs.cn, para.n, para.c, para.cn.

## Metadata and data quality notes
- Data provenance: clearly linked to the Colt Park restoration and drought experiment; methodology referenced from multiple foundational studies (Smith et al., Bardgett et al., Ward et al., etc.).
- Data dictionaries and column schemas provided per file; column codes and units documented (e.g., trt codes: c, cs, f, sf; drought codes: dr, csh, c).
- Missing data: indicated by NA.
- Measurement methods: described for each dataset (e.g., ThetaProbe for soil moisture, IR gas analyzers for CO2 flux, TRFLP for microbial communities, PLFA for microbial biomass, TOC analyses for carbon content).
- Dataset interoperability considerations: multiple data types (soil, plant, microbial, climate) and variable coding schemes; harmonization will require consistent interpretation of treatment codes and timepoints (before/during/after drought).

## Data governance, sharing, and stewardship considerations
- Provenance and documentation are comprehensive, but explicit licensing or usage rights are not stated in the summary (consult data provider or metadata for license).
- For reuse and integration:
  - Map treatment and drought codes to human-readable labels when joining datasets.
  - Align time references across files (e.g., julian vs actual dates; before/during/after designations).
  - Ensure unit consistency across chemical and biological measurements (e.g., MBNmcg, DOCmcg, FBratio).
- Update and maintenance:
  - If integrating with ongoing data systems, establish a data dictionary and versioning strategy.
  - Consider a centralized metadata file to accompany all datasets to ease discovery and reuse.

## References (context and provenance)
- Core associated publications and methodological references include:
  - Cole et al. 2019 (J. Applied Ecology)
  - Smith et al. (2000, 2003, 2008)
  - De Deyn et al. (2011)
  - Ward et al. (2013)
  - Bardgett et al. (1996)
  - Plassart et al. (2012)
  - Brookes et al. (1985)
  - White et al. (1979), among others