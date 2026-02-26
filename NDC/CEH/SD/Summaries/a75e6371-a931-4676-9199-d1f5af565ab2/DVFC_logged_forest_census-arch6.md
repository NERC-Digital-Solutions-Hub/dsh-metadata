# Dataset Summary and contextual information

- Context: Above Ground Carbon Density (ACD) estimated from tropical forest census surveys (1992–2016) in USFR and DVCA, Sabah, Malaysia. Mixed logged and unlogged forests; restoration treatments applied in parts of the study area.
- Scale: 257 plots, 51,803 individual tree measurements, spanning 45.56 ha of forest across three independent plot networks.
- Plot networks:
  - A. INDFORSUS (1996/7): 53 plots of 0.1 ha in logged and unlogged areas; later relocations/re-censuses in 2016.
  - B. Pinard and Putz (1992 base): 32 plots of 0.08 ha; re-censused in 1996 and 2005.
  - C. INFRAPRO/INFAPRO (2007): 205 plots of 0.2 ha across the logged area; re-censused in 2010 and some in 2015.
- Data provenance and quality:
  - Additional data on logging method, coupe, and year of logging provided by Yayasan Sabah.
  - Quality control included numeric range checks, formatting conformance, and logical integrity checks.
  - Data analysis and carbon modelling described by Philipson et al. (in press); analysis code available at Zenodo: https://doi.org/10.5281/zenodo.3885641.
- Fieldwork protocols and measurements:
  - Three networks used slightly different field protocols for measuring trees.
  - Measurements include DBH (diameter at 1.3 m, with adjustments where buttress roots required), tree height (measured or estimated), and taxonomic identity to the lowest possible rank.
  - Nested plot schemes used to capture smaller trees and quantify biomass more precisely.
- Allometric methods and carbon modelling:
  - Carbon content assumed to be 47% of above-ground biomass (AGB).
  - AGB estimated from DBH, height, and wood density using allometric equations:
    - AGB_est = 0.0673 × (ρ × DBH^2 × H)^0.976
    - DBH adjustments to standard 1.3 m height when necessary using a taper model:
      DBH_1.3m = DBH_POM / exp(-0.029 × (POM - 1.3))
    - Height estimation via a three-parameter Weibull-based model:
      H = 89.53 × [1 − exp(-0.0225 × DBH^0.7383)]
  - Wood density from global databases; where species data were missing, plot-averagewood density was used.
  - Carbon contents of individual trees summed per plot to yield ACD (Mg ha^-1).
  - Small-tree contributions in nested plots scaled and added to plot totals.
- Data structure and fields:
  - Per plot fields include:
    - Plot Identifier, Coupe Name, Plot identifier (plot network + plot number)
    - NAME of logging coupe, ACD (Mg ha^-1), FACE (restoration scenario) with values: Project Scenario, Baseline, or N/A
    - LoggingMethod (High lead, Tractor, UnLogged)
    - Year logged, Forest (Logged/UnLogged), YearsSinceLogging
    - MeasureTime (year of census), Dataset (INDFORSUS, FACE, or RIL_PinardLincoln)
- Units:
  - Above-ground Carbon Density (ACD) reported in Mg ha^-1.
- Documentation and references:
  - Core sources include Face the Future (2011), Foody et al. (2001, 2003), Tangki & Chappell (2008), Pinard & Putz (1996), Lincoln (2008), and the INFAPRO-related works.
  - The INFAPRO studies provide context for restoration and logging impacts on biomass and carbon balance.