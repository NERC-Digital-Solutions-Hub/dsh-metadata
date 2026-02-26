# Phenyl urea and phenoxy acid herbicide data LOIS Core Programme

## Overview
- Investigates occurrence, fate, and flux transfer of micro-organic herbicides in LOIS rivers, focusing on Humber catchment and its rivers draining to the North Sea; includes a rural control on the Ouse.
- Major dataset covers 12 Humber catchment sites (1994–1995 and 1994–1997) and 3 Tweed catchment sites (1995).
- Data support background information for specialized LOIS topics and are intended for map-based visualization and spatial analysis.

## Spatial and temporal coverage
- Spatial scope:
  - Humber catchment: 12 sites (S1, S2, U3, N4, W5, O6, D7, A8, C9, D10, T11, O12)
  - Tweed catchment: 3 sites (TW13, TW14, TW15)
- Temporal scope:
  - Phenyl urea herbicides: 1994–1995 (Humber); 1994–1997 (Humber)
  - Phenoxy acid herbicides: December 1994–September 1995 (S1–S2); December 1994–February 1997 (S2, D7, A8, C9, D10, T11, O12); January–September 1995 (TW13–TW15)
  - Linuron dissolved: measured only April–October 1994
- Data quality and sampling:
  - Attempts to sample weekly; interruptions occurred
  - Some sites show incomplete time coverage due to sampling gaps

## Variables
- Phenyl urea herbicides (ug/l): 2,4-Dichlorophenoxyacetic acid; 4-(4-Chloro-O-tolyloxy) butyric acid; 4-Chloro-O-tolyloxyacetic acid; Chlorotoluron (dissolved); Diuron (dissolved); Isoproturon (dissolved); Linuron (dissolved)

- Phenoxy acid herbicides (ug/l): same suite as above (with dissolved specification noted for certain compounds)

- Note on measurement: Linuron dissolved data limited to Apr–Oct 1994; some sites record all variables except Linuron dissolved

## Locations and coordinates (site codes)
- S1 Swale at Catterick Bridge — NGR SE225994
- S2 Swale at Thornton Manor — NGR SE433715
- U3 Ure at Boroughbridge — NGR SE482561
- N4 Nidd at Skip Bridge — NGR SE482561
- W5 Wharfe at Tadcaster — NGR SE487435
- O6 Ouse at Clifton Bridge — NGR SE589528
- D7 Derwent at Bubwith — NGR SE706364
- A8 Aire at Beal Bridge — NGR SE534255
- C9 Calder at Methley Bridge — NGR SE409258
- D10 Don at Sprotborough Bridge — NGR SE538014
- T11 Trent at Cromwell Lock — NGR SE807612
- O12 Ouse at Acaster Malbis — NGR SE594445
- TW13 Tweed at Boleside — NGR NT498334
- TW14 Tweed at Norham — NGR NY898477
- TW15 Tweed at Ormiston Mill — NGR NT702280

- Variable availability note:
  - Ouse at Acaster Malbis (O12) and Tweed sites (TW13–TW15): all variables except Linuron dissolved
  - Linuron dissolved: data available at some Humber sites primarily during Apr–Oct 1994; not consistently available at all sites/time periods

## Sampling and measurement methods
- Sample collection: 1 litre chromic acid-washed glass bottles
- Concentration methods for phenyl urea herbicides:
  - Method 1: Solid phase extraction (SPE) using C18 cartridges; elution with ethyl acetate
  - Method 2: SPE with an additional methanol rinse before elution with methanol
  - Method 3: Liquid-liquid extraction with dichloromethane
- Concentration method for phenoxy acid herbicides: Method 3 (liquid-liquid extraction)
- Instrumentation:
  - Phenyl urea herbicides: High Performance Liquid Chromatography (HPLC) with UV/VIS detection
  - Phenoxy acid herbicides: Gas Chromatography (GC) with Mass Spectrometry (MS) detection
- Quality control:
  - Randomly spiked samples with mixed standards
  - Use of certified grade standards (>99%)
  - Participation in AQUACHECK inter-laboratory harmonisation for urea and acid herbicides

## Data quality and limitations
- Data quality is variable due to:
  - Highly polluted sites yielding complex chromatograms
  - Concentrations often near detection limits
  - Difficulties in extraction, especially with liquid-liquid methods (emulsions)
- Box-and-whisker plots (zip file) provided for each determinand to illustrate data distribution (site-level ranges, medians, IQRs, outliers)

## Data provenance and access
- Laboratory analysis:
  - Until Nov 1994: York University and IFE Wareham
  - From Dec 1994: Wallingford IH
- Reference: House et al. 1997, Micro-organic compounds in the Humber rivers, Sci. Total Environ. 194/495, pp. 357–371

## GIS-ready notes for map-based analysis
- Both concentration data and site coordinates enable spatial visualization across Humber and Tweed river systems.
- Time-series by site allow examination of spatial patterns over the 1994–1997 window, with particular attention to Linuron data availability (Apr–Oct 1994) and variable inclusion (some sites exclude Linuron).
- Data quality caveats (near-detection limits and complex chromatograms) should be considered when creating thematic layers or performing trend analyses.