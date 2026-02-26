# Field experiment

- Overview
  - Field experiments conducted at two UK locations: Migneint (North Wales) and Peaknaze (Northern England).
  - At each site, plots established on two soil types: peat and peaty podzol; 12 plots per site across four experimental designs (Migneint Peat, Migneint Podzol, Peaknaze Peat, Peaknaze Podzol).
  - Experimental design: randomised blocked with four replicates of control, acid, and alkaline treatments.
  - Treatments applied from Oct 2008 to Dec 2012, and re-established for this study from Jan 2015 to Oct 2016.
  - Acid treatments used sulfuric acid (H2SO4) with rainwater; alkaline treatments used NaOH and KOH, followed by MgCl2 and CaCl2 rinse to maintain base cation ratios. Doses chosen to reflect ambient acid deposition and soil buffering.
  - Control plots received rainwater only. All data collection and interpretation performed by Dr. Catharine Pschenyckyj as part of a PhD project.

- Data files and their content
  - Chemistry_PorewaterLitterSoil.csv
    - Sample types: pore water, decomposing surface litter, and soil.
    - Sampling: monthly pore water samples (Sept 2015–Oct 2016) from four locations per plot; litter and soil samples collected at 3 time points in 2016 (Apr, Jul, Oct).
    - Analyses: pH, electrical conductivity (EC), total organic carbon (TOC), dissolved organic carbon (DOC), and UV absorbance; SUVA254 calculated as proxy for DOC quality.
    - Processing: DOC in pore water and in extracts expressed per liter or per gram dry material; corrections applied for pathlength in spectroscopic measurements.
    - Units: pH, EC (μS), DOC (mg/L), SUVA254 (mg C−1 m−1).
    - Acronyms: M/Migneint, PN/Peaknaze, Pod/Podzol, PW/Pore water, DSL/Decomposing surface litter.
  - LitterBagData.csv
    - Litter bags used to study acidity effects on litter decomposition; litter types reflect dominant vegetation at each site (Calluna vulgaris, Eriophorum vaginatum, Festuca ovina, Pleurozium schreberi, Sphagnum spp.).
    - Procedure: litter collected from respective sites, prepared (species-specific dry masses), placed in 0.5 mm mesh litter bags, buried at 5 cm depth in Oct 2015; retrieved Oct 2016 after 12 months; additional incubation for 3, 6, and 9 months in control plots.
    - Analyses: mass loss (percentage), post-extraction DOC (via cold-water extraction), pH, EC, SUVA254, and total nitrogen (TN) in extracts; dry mass measured before and after extraction.
    - Units: pH, EC (μS), DOC (mg/L), SUVA254 (mg C−1 m−1), TN (mg/L), %ML (percentage mass loss), DOCmgg (mg/L).
    - Acronyms: M/ Migneint, PN/Peaknaze, Pod/Podzol; plant species abbreviations (CM/Calluna Migneint, CP/Calluna Peaknaze, F/Festuca, E/Eriophorum, S/Sphagnum, P/Pleurozium).
  - TBI_Data.csv
    - Tea Bag Index (TBI) methodology to estimate decomposition rate (kTBI) and stabilisation factor (S) as generalized litter decomp indicators.
    - Procedure: Green and Rooibos tea bags buried per plot (three sets per plot) for 90 days starting July 2016; retrieved Oct 2016; mass loss used to calculate kTBI and S.
    - Acronyms: M/Migneint, PN/Peaknaze, Pod/Podzol; S/Stabilisation factor; K/Decomposition rate.
    - References: Keuskamp et al. 2013; Duddigan et al. 2020; Evans et al. 2012 (background methods related to acidity and carbon cycling).
  
- Experimental design and sampling details
  - Plots are 9 m2; four replicates per treatment within each site/soil type combination.
  - Sampling schedule:
    - Pore water: monthly from Sep 2015 to Oct 2016; depth 10 cm; four locations per plot pooled into one sample per plot.
    - Litter and soil: collected 2016 (Apr, Jul, Oct) with careful extraction from 10–20 cm depth; litter bags buried Oct 2015 and retrieved Oct 2016; additional quarterly sampling during the post-incubation period.
    - Tea bags: buried for 90 days starting July 2016; retrieved Oct 2016.
  - Sample processing and analyses:
    - DOC quantified by Thermalox TC-TN analyser; TIC subtracted from TC to obtain DOC.
    - UV–visible spectroscopy for DOC quality; SUVA254 calculated from corrected absorbance and DOC.
    - Litter extracts: cold-water extraction (litter to water ratios 1:20) followed by centrifugation and filtration; measurements for pH, EC, DOC, SUVA254.
  - Data interpretation and QA
    - All data collection and interpretation performed by Dr. Catharine Pschenyckyj as part of a PhD project.
    - Data and methods linked to published studies (Evans et al. 2012; Keuskamp et al. 2013; Duddigan et al. 2020) for context and comparability.

- Metadata, conventions, and data quality notes
  - Data files include clear acronyms, units, and site labels (M/Migneint, PN/Peaknaze, Pod/Podzol) to enable cross-site comparability.
  - Metadata describes sample types, collection depths, extraction protocols, instrument usage, and conversion calculations (e.g., SUVA254, DOC normalization).
  - Potential data considerations for users
    - Patchy data across years and sites; multiple formats across data types.
    - Data require integration across three related data files to analyze acidity effects on carbon cycling.
    - Some outputs (e.g., DOC in different matrices) are reported in different units or normalization (per L vs per g dry material); care needed when merging datasets.
  - Data quality challenges typical for field data
    - Time gaps between campaigns; varying sample preservation conditions; need for careful QA when combining site and treatment effects.
    - Communication of complex results may require simplifying outputs for end-users.

- How this data can be used
  - Assess how acidity (acid vs alkaline) affects carbon dynamics in organic soils via pore water chemistry, litter decomposition, and stabilisation processes.
  - Compare site- and soil-type differences (peat vs podzol) in response to treatments.
  - Derive interlinked indicators (DOC mobility, SUVA254 as a DOC quality proxy, litter mass loss, kTBI and S) to model decomposition and carbon stabilization under differing pH conditions.
  - Reuse in meta-analyses of acidification effects on carbon cycling, leveraging the Tea Bag Index alongside conventional DOC and decomposition metrics.

- References and provenance
  - Evans et al. 2012; Duddigan et al. 2020; Keuskamp et al. 2013; Pschenyckyj (PhD work) for data provenance and methodologies.