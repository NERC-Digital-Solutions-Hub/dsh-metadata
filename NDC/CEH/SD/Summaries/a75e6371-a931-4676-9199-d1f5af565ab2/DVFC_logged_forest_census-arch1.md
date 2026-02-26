# Dataset Summary and contextual information

## Context and experimental design
- Focus on Above Ground Carbon Density (ACD) estimated from forest census surveys conducted 1992–2016 in tropical lowland dipterocarp forest within the Ulu Segama Forest Reserve (USFR) and Danum Valley Conservation Area (DVCA), Sabah, Malaysia.
- USFR details: 1268 km2 of forested land; heavily impacted by logging (1972–1993) using tractor or high-lead methods; restoration treatments (climber cutting and tree planting) applied 1993–2004 in patches of 83–1745 ha across coupes.
- Tree census data come from 257 plots, yielding 51,803 individual tree measurements over 45.56 ha.
- Data assembled from three independent plot networks:
  - A. INDFORSUS (1996/97): 53 plots of 0.1 ha in logged and unlogged areas.
  - B. Pinard and Putz (1992–1996; re-censused 1996 and 2005): 32 plots of 0.08 ha (with nested smaller plots).
  - C. INFAPRO/INFRAPRO (2007; re-censused 2010 and 2015 in some plots): 205 plots of 0.2 ha (across logged areas).
- Field data, logging metadata, and restoration context provided by Yayasan Sabah Group and project teams; data analysis and modelling described in Philipson et al. (in press) with code available at Zenodo.
- Restoration context: FACE project scenarios include Project Scenario (restoration measures), Baseline (no restoration), and N/A for unlogged areas.

## Fieldwork protocol and measurements
- Each plot network used slightly different field protocols:
  - A. INDFORSUS: plots with 17.84 m radius; measure free-standing woody plants ≥20 cm DBH (and nested circles for smaller sizes) at 1.3 m height; DBH measured with adjustments for buttress roots.
  - B. Pinard & Putz: measure DBH and taxonomic identity for free-standing woody plants ≥20 cm DBH across whole plots; nested plots for smaller DBHs (400 m2, 100 m2, 25 m2).
  - C. INFAPRO: plots defined by four circles (0.05 ha each) on a cross; measurements across multiple DBH classes with nested circles to capture smaller trees.
- Measurements collected include DBH (1.3 m height when possible), tree height (measured or estimated), and species identity to the lowest taxonomic level possible.

## Units of recorded values
- Above-ground Carbon Density (ACD) reported in Mg ha^-1.

## Allometric methods and carbon modelling
- Carbon content assumed to be 47% of above-ground biomass (AGB); AGB estimated from DBH, height, and wood density using allometric equations:
  - AGB_est = 0.0673 × (ρ × DBH^2 × H)^0.976
  - Units: DBH in cm, H in m, ρ in g cm^-3.
- Height data:
  - Direct measurements for 5214 trees; height for 50,646 trees estimated using a three-parameter Weibull-based equation:
    - H = 89.53 × [1 − exp(−0.0225 × DBH^0.7383)]
- POM (point-of-measure) adjustments:
  - If DBH_POM used (to avoid buttress roots), DBH_1.3m = DBH_POM / exp[−0.029 × (POM − 1.3)]
- Wood density:
  - Sourced from global wood density database; preferred species-average values; otherwise use nearest taxonomic unit average; for ~20% of stems with missing taxonomic data, assign plot-average density.
- ACD per plot:
  - Sum carbon contents across all trees; add contributions from small trees on nested plots to reported plot totals.
- Data underpin modelling of carbon dynamics and restoration effects.

## Details of data structure
- Per plot fields include:
  - Plot Identifier
  - Coupe Name
  - Plot identifier (plot number and network)
  - Name of logging coupe
  - ACD (Mg ha^-1)
  - FACE (Forest restoration scenario): Project Scenario, Baseline, or N/A
  - LoggingMethod (High lead, Tractor, UnLogged)
  - Year logged
  - Forest status (Logged or UnLogged)
  - YearsSinceLogging
  - MeasureTime (year of census)
  - Dataset (INDFORSUS, FACE, or INFAPRO)
- Data backed by published references and project documentation; dataset networks include INDFORSUS, FACE, and INFAPRO.

## Quality control, data handling, and access
- Quality control steps included numeric range checks, formatting consistency, and logical integrity checks.
- Data analysis and modelling code are publicly accessible at the provided Zenodo link: https://doi.org/10.5281/zenodo.3885641
- Aimed to harmonise data across three independent networks, while acknowledging protocol differences.

## References
- Face the Future (2011). INFAPRO Rehabilitation of logged-over dipterocarp forest in Sabah, Malaysia.
- Foody, G.M. et al. (2001). Mapping biomass of Bornean tropical rainforest from remotely sensed data.
- Foody, G.M. & Cutler, M.E.J. (2003). Tree biodiversity in protected and logged Bornean tropical rain forests.
- Tangki, N.A. & Chappell, N.A. (2008). Biomass variation and remote sensing prediction.
- Philipson, C.D. et al. (in press). Active restoration accelerates the carbon recovery of human modified tropical forests.
- Pinard, M.A. & Putz, F.E. (1996). Retaining forest biomass by reducing logging damage.
- Lincoln, P.R. (2008). Stalled gaps or rapid recovery – the influence of damage on post-logging forest dynamics. PhD Thesis, University of Aberdeen.