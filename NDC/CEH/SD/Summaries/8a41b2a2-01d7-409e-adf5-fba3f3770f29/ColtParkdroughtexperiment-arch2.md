# Summary of data regarding Colt Park drought experiment.

## Overview
- Drought experiment embedded within the long-term Colt Park grassland restoration study.
- Linked to the paper: Grassland biodiversity restoration increases resistance of carbon fluxes to drought (2019).
- Location: Colt Park meadows, Ingleborough National Nature Reserve (54°12'N, 2°21'W).
- Restoration treatments: fertiliser application and seed addition; drought applied on top of these treatments.
- Sampling period includes a hay cut on 16 July 2013 and subsequent grazing by cattle and sheep.
- Measurements cover plant and soil responses to drought, enabling assessment of environmental health and carbon flux dynamics under different management histories.

## Experimental design

### Plot treatments
- Four restoration treatments:
  - Control
  - Seed added
  - Fertiliser added
  - Fertiliser and seed added
- Original plot numbers referenced from Smith et al. (2000) and De Deyn et al. (2011).

### Drought treatments
- Three drought levels:
  - Ambient (no rain-out shelter)
  - Drought (rain-out shelter)
  - Control shelter (rain-out shelter with holes)
- Shelters installed from 5 June to 10 July 2013.

### Fertiliser and seed history
- Fertiliser: since 1990, half plots fertilised and half not; 2009–2010 exceptions; inorganic fertiliser NPK 20:10:10 at 25 kg N ha−1 applied in spring (21 May 2013).
- Seed addition: initiated in 1990 with 19 species of locally collected/commercial seed.

## Measurements and data structure

### General
- Data files include methodologies, missing data NA, and data file-specific descriptions.
- Aims to capture soil moisture, carbon fluxes, microbial community structure, plant community composition, and environmental conditions under drought and restoration treatments.

### Data files (key contents at a glance)
- Averagesoilmoisture2013
  - Plot-level soil moisture; columns include unique.id, julian, date, year, plot, block, treatment, drought, seed, fertiliser, shelter.
  - Codes explain treatment combinations (e.g., c, cs, f, sf; dr, csh, c; seed, noseed; fert, nofert).
- NetEcosystemExchange2013
  - Net ecosystem exchange (g CO2 m−2 h−1); includes unique.id, date, plot, block, trt, dr, seed, fert, julian.
- Ecosystemrespiration2013
  - Ecosystem respiration flux (g CO2 m−2 h−1); includes unique.id, date, plot, block, trt, dr, seed, fert, julian.
- PARdata2013
  - Photosynthetically active radiation (PAR), soil and air temperature; columns unique.id, date, julian, plot.no, PAR, soiltemp, airtemp.
- Soilandairtemperature2013
  - 30-minute soil and air temperature readings; seq, time, and multiple logger-specific temperature columns.
- Soildata2013
  - Soil chemistry and microbial measurements; time (p/m/a/n for before/during/after drought); MBN, MB.CN, DOC, DON, pH; microbial biomass PLFA (BACTmcg) and fungal PLFA (FUNGImcg); lipid-based ratios (FBratio).
- BacteriarelativeabundanceTRFLP2013 and FungirelativeabundanceTRFLP2013
  - Relative abundance of bacterial and fungal TRFLP peaks; sample identifiers; plot; time (before/during/after drought for fungi); block; treatment, drought, seed, fertiliser.
- Plantcommunitycomposition2013
  - Species cover (central 706 cm2) for a wide range of vascular plants; plot; treatment; drought (drht); fertiliser; seed; block; sp.richness; and biomass-derived metrics by functional groups (grss.dwt, legs.dwt, forbs.dwt, para.dwt, moss.dwt, other.dwt, root.dwt) plus carbon and nitrogen content indicators (grss.n, grss.c, grss.cn, etc.).
- Speciesdiversity2012restorationplots
  - Pre-drought baseline (2012) restoration data; original plot number; total species per plot; grss.dwt, legs.dwt, forbs.dwt, para.dwt, moss.dwt, other.dwt, root.dwt; sp.richness; grss.n, grss.c, grss.cn, and similar nutrient/stoichiometry metrics by plant group; treatment codes (c, cs, f, fs) and seed/fert statuses.
- Soilandairtemperature2013 and related files provide context for environmental drivers (light, temperature) influencing carbon flux and plant responses.
- References accompany data files to anchor methodologies (Chloroform fumigation, PLFA analysis, TRFLP, ISO DNA procedures, and restoration history).

## Data interpretation and usage notes
- Data are structured to enable cross-variable analyses of drought effects across restoration histories (fertiliser/seed) and management practices.
- Missing data are indicated as NA; measurements follow standardized methods and are accompanied by methodological descriptions.
- The dataset supports evaluation of how biodiversity restoration and management interventions influence resistance or sensitivity of carbon fluxes and soil–microbial dynamics to drought.
- Linkages to prior and related studies (Smith et al.; Bardgett et al.; Ward et al.) provide a broader context for interpretability and synthesis.

## Context for environmental monitoring
- Aligns with the Analysts Monitoring the Environment aim: standardized, verifiable data to assess environmental health and policy-relevant outcomes over time.
- Data are designed to be combined with other datasets to increase usefulness beyond single-use applications.
- Outputs can be presented in formats suitable for reporting environmental health across time and treatments (e.g., carbon flux metrics, soil health indicators, plant diversity, and microbial community structure).