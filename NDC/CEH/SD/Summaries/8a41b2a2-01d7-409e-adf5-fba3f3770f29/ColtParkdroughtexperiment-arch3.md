# Summary of data regarding Colt Park drought experiment

- This dataset accompanies the paper by Cole, A. J., Griffiths, R. I., Ward, S. E., Whitaker, J., Ostle, N. J. & Bardgett, R. D. (2019) Grassland biodiversity restoration increases resistance of carbon fluxes to drought (Journal of Applied Ecology). It combines a long-running grassland restoration experiment with a drought manipulation conducted in 2013 at Colt Park meadows, Ingleborough National Nature Reserve, UK (54°12'N, 2°21'W).
- The study investigates how fertiliser application and seed addition (restoration treatments) influence ecosystem responses to drought, including plant and soil processes and carbon fluxes.
- The experimental layout links to earlier restoration research (Smith et al. 2000; 2003; 2008; De Deyn et al. 2011) and uses original plot identifiers from those studies.

## Experimental design and treatments

- Restoration treatments (since 1990)
  - Fertiliser application: half of plots received inorganic fertiliser (NPK 20:10:10; 25 kg N ha^-1) in spring; fertiliser applied in most years except 2009–2010.
  - Seed addition: introduction of 19 locally sourced species starting in 1990.
- Drought treatment (applied to the restored plots in 2013)
  - Ambient: no rain-out shelter.
  - Control shelter: rain-out shelter with holes.
  - Drought shelter: rain-out shelter creating drought conditions.
  - Shelters used from 5 June to 10 July 2013.
- Management details
  - All plots hay-cut on 16 July 2013, then grazed by cattle and sheep.
- Plot information
  - Original plot numbers are provided in italics and relate to the long-term restoration layout.

## Datasets included (key data files and their focus)

- Averagesoilmoisture2013
  - Soil moisture (percent mean) per plot, from three readings combined.
  - Columns include unique.id, julian day, date, year, plot, block, treatment (c, cs, f, sf), drought (dr, csh, c), seed (seed, noseed), fertiliser (fert, nofert), and shelter timing.
- ColtParkdailyprecipitation2013
  - Daily precipitation (mm) at Colt Park weather station.
- NetEcosystemExchange2013
  - Net ecosystem exchange (CO2 flux, g CO2 m^-2 h^-1) per plot, with block, dr, seed, fert, julian, etc.
- Ecosystemrespiration2013
  - Ecosystem respiration (CO2 flux) per plot, with block, dr, seed, fert, julian, etc.
- PARdata2013
  - Photosynthetically active radiation (PAR), soil temperature, and air temperature measurements; linked to unique ids and plot numbers.
- Soilandairtemperature2013
  - 30-minute soil and air temperature measurements from logging sensors; includes seq identifiers.
- Soildata2013
  - Soil biogeochemistry and microbial indicators
  - Microbial biomass N (MBN), microbial CN ratio, dissolved organic carbon and nitrogen (DOC/DON), soil pH, bacterial and fungal PLFA indicators (BACTmcg, FUNGImcg), fungal:bacterial ratio (FBratio), etc.; time points before/during/after drought.
- BacteriarelativeabundanceTRFLP2013
  - Relative abundance of bacterial TRFLP peaks; includes sample and plot identifiers.
- FungirelativeabundanceTRFLP2013
  - Relative abundance of fungal TRFLP peaks; includes time (before/during/after drought) and plot.
- NetEcosystemExchange2013
  - Already listed above; focuses on NEE (CO2 flux) per plot with treatment/drought/seed/fertiliser codes and julian day.
- PARdata2013
  - Already listed above; key plant and environment context for photosynthesis and energy balance.
- Plantcommunitycomposition2013
  - Percent cover for each vascular plant species in central 706 cm^2 of each plot; conducted 29 June–4 July 2013; includes plot, treatment, drought, fertiliser, seed, and block.
- Speciesdiversity2012restorationplots
  - Baseline (2012) restoration plot data before the drought experiment
  - Outputs include total vascular species per 2m x 2m quadrat, plot, block, grss.dwt (grass dry weight), legs.dwt, forb.dwt, para.dwt, moss.dwt, other.dwt, root.dwt, species richness, and tissue chemistry indicators (grss.n, grss.c, grss.cn, forb.n, forb.c, forb.cn, legs.n, legs.c, legs.cn, para.n, para.c, para.cn).

## Measurements and methodologies (highlights)

- Gas flux measurements
  - Net Ecosystem Exchange and Ecosystem Respiration measured with infrared gas analyzers (EGM4, PP Systems) using two-minute headspace closures and opaque chambers; methods follow Ward et al. 2013.
- Soil and plant measurements
  - Soil moisture, soil chemistry (MBN, DOC, DON, pH), microbial PLFA analyses, bacterial/fungal community markers (TRFLP), and fungal/bacterial biomarkers follow established protocols (e.g., Bardgett et al. 1996; White et al. 1979).
- Vegetation and biomass
  - Plant species cover surveys and biomass weights by functional group (grasses, legumes, forbs, parasitic plants, mosses, others, roots) in 2012 restoration plots; dry weights determined after oven-drying.
- Climate context
  - Daily precipitation data and PAR/temperature context to support interpretation of drought and energy balance.

## Data structure, metadata, and quality considerations

- Metadata and coding
  - Datasets use consistent codes for restoration treatments and drought levels:
    - Treatment: c (control), cs (seed addition only), f (fertiliser only), sf (fertiliser and seed)
    - Drought: dr (drought), csh (control shelter), c (ambient)
    - Seed: seed, noseed
    - Fertiliser: fert, nofert
  - Time points labeled as before, during, and after drought where applicable.
- Data integrity and accessibility
  - Missing data are explicitly indicated as NA in files.
  - Each file includes detailed column-level descriptions (e.g., unique identifiers, plot numbers, Julian day, treatment codes, and specific measurement variables), enabling traceability and reuse.
- Data scope
  - Combines long-term restoration experiments with a targeted drought manipulation, enabling assessment of restoration treatment effects on drought resilience across multiple ecosystem functions.

## Data governance and usage considerations for monitoring frameworks

- Comprehensive metadata and standardized coding support cross-domain monitoring (soil, plant, microbial, and gas-flux indicators) under a common experimental framework.
- The dataset enables assessment of:
  - How restoration treatments modify resistance or sensitivity of carbon fluxes to drought.
  - Interactions among soil properties, microbial community structure, plant community composition, and gas flux dynamics under drought stress.
- For effective reuse, attention should be given to:
  - Correct interpretation of treatment and drought codes when aggregating across years or treatments.
  - Alignment of measurements with monitoring objectives (e.g., focusing on carbon balance, soil health, or biodiversity outcomes).
  - Referencing the accompanying methodological sources for measurement approaches ( Ward et al. 2013; Bardgett et al. 1996; White et al. 1979; Plassart et al. 2012; etc.).

## References

- Bardgett, R.D., Hobbs, P.J. & Frostegard, A. (1996). Changes in soil fungal:bacterial biomass ratios following reductions in the intensity of management of an upland grassland.
- Brookes, P.C., Landman, A., Pruden, G. & Jenkinson, D.S. (1985). Chloroform fumigation and the release of soil nitrogen.
- De Deyn, G.B. et al. (2011). Additional carbon sequestration benefits of grassland diversity restoration.
- Plassart, P. et al. (2012). Evaluation of the ISO standard 11063 DNA extraction procedure for assessing soil microbial abundance and community structure.
- Smith, R.S. et al. (2000; 2003; 2008). Series on meadow grassland restoration and management.
- Ward, S.E. et al. (2013). Warming effects on greenhouse gas fluxes in peatlands are modulated by vegetation composition.
- White, D.C. et al. (1979). Determination of the sedimentary microbial biomass by extractible lipid phosphate.