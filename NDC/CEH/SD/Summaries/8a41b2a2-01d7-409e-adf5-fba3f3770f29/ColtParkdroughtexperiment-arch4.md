# Summary of data regarding Colt Park drought experiment

- Overview
  - Data accompany a drought experiment superimposed on a long-term grassland restoration study at Colt Park meadows, UK.
  - Aims: measure how restoration treatments and drought influence soil moisture, carbon fluxes, microbial communities, and plant community structure.
  - Timeframe: drought treatment implemented in 2013 with ambient, control shelter, and drought conditions; hay cut and post-cut grazing occurred in July 2013.

- Study site and experimental design
  - Location: Colt Park meadows, Ingleborough National Nature Reserve (54°12'N, 2°21'W).
  - Restoration treatments since 1990: fertiliser application and seed addition.
  - Drought treatment levels: ambient (no shelter), control shelter (holes), drought shelter (rain-out).
  - Plot arrangement references and original plot numbers align with prior Smith et al. restoration work; plots were cut for hay on 16 July 2013 and subsequently grazed by cattle and sheep.

- Treatments and experimental factors
  - Fertiliser treatment: fertiliser applied spring 2013 (NPK 20:10:10; 25 kg N ha^-1); ongoing fertiliser vs. no fertiliser (except 2009–2010 when not applied).
  - Seed addition: conducted since 1990 with 19 species; seed addition vs. no seed addition.
  - Drought: ambient, drought (rain-out shelter), and control shelter (holes) during 5 June–10 July 2013.
  - Measured factors coded in data files include combinations of fertiliser, seed, and drought treatments, plus shelter status.

- Data files (structure and purpose)
  - Averagesoilmoisture2013
    - Plot-level soil moisture by treatment and drought status; fields include unique.id, julian, date, year, plot, block, treatment, drought, seed, fertiliser, shelter.
  - BacteriarelativeabundanceTRFLP2013
    - Bacterial community composition via TRFLP; columns from X52 to X505; sample, plot, time.
  - ColtParkdailyprecipitation2013
    - Daily precipitation (mm); julian and mm.
  - Ecosystemrespiration2013
    - Soil CO2 efflux (g CO2 m^-2 h^-1) by plot; fields include unique.id, date, plot, block, trt, dr, seed, fert, julian.
  - FungirelativeabundanceTRFLP2013
    - Fungal community composition via TRFLP; columns X62–X485; sample, plot, time, block, treatment, drought, seed, fertiliser.
  - NetEcosystemExchange2013
    - Net ecosystem exchange CO2 flux (g CO2 m^-2 h^-1); similar structure to respiration data with plot, block, trt, dr, seed, fert, julian.
  - PARdata2013
    - Photosynthetically active radiation (PAR), soil and air temperature; fields include unique.id, date, julian, plot.no, PAR, soiltemp, airtemp.
  - Plantcommunitycomposition2013
    - Percent cover of vascular plant species per plot; plot, trt, drht, fert, seed, block; includes central 706 cm^2 sampling.
  - Soilandairtemperature2013
    - Soil and air temperatures from 30-min loggers; fields seq, time, and multiple soil/air temperature columns.
  - Soildata2013
    - Soil chemistry and biology: microbial biomass N, C/N, dissolved organic carbon/N, pH, microbial PLFA metrics (BACTmcg, FUNGImcg, FBratio), time.
  - Speciesdiversity2012restorationplots
    - 2012 pre-drought diversity and biomass data: original.plot.number, plot.no, block, treatment, seed, fert; includes grass, legume, forb, parasitic plant and moss/dwt components; root and total biomass; species richness; and biomass C/N data per functional group.

- Data structure, codes, and units
  - Codes for treatments across files:
    - trt: c (control), cs (seed only), f (fertiliser only), sf (fertiliser + seed)
    - dr (drought): dr (drought), csh (control shelter), c (ambient)
    - seed: seed (seed addition), noseed (no seed)
    - fert: fert (fertiliser), nofert (no fertiliser)
    - shelter: before, during, after (timing relative to drought)
  - Measurements and units (highlights):
    - Soil moisture: percent mean
    - CO2 flux: g CO2 m^-2 h^-1 (ecosystem respiration and net ecosystem exchange)
    - PAR: µmol m^-2 s^-1
    - Temperature: degrees Celsius (soil and air)
    - Biomass and tissue chemistry: mg or µg per g soil dry weight or per g biomass; C, N, CN ratios
    - Microbial biomarkers: PLFA concentrations (µg g^-1 soil dwt)
  - Data quality notes:
    - Missing data indicated as NA
    - Measurements taken with specified instruments (e.g., ThetaProbe, Delta-T, EGM4; gas analyzers; soil/air loggers)

- Data integration and potential uses
  - The dataset enables analysis of interactions among restoration treatments and drought on:
    - Soil moisture dynamics
    - Gas exchange and carbon flux responses
    - Microbial community structure (bacteria and fungi) and microbial biomass
    - Plant community composition, diversity, and biomass partitioning
  - Cross-file linkage is possible via plot numbers, treatment codes (trt, seed, fert), drought status (dr, csh, c), and time indicators (julian/date, time).
  - Suitable for evaluating short-term drought responses within a long-term restoration context and for informing data governance around multi-omics and ecosystem function datasets.

- References
  - Core publications and methodological references linked to the Colt Park experiment (e.g., Smith et al. 2000, 2003, 2008; De Deyn et al. 2011; Bardgett et al. 1996; Ward et al. 2013; Plassart et al. 2012; White et al. 1979; Brookes et al. 1985) and related methodological notes.