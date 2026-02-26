# Phenyl urea and phenoxy acid herbicide data LOIS Core Programme

## Scope and purpose
- LOIS rivers project investigates occurrence, fate, and flux of micro-organics in rivers, focusing on Humber catchment to inform transfer to the estuary.
- Major study sites span industrial rivers (Aire, Calder, Trent, Don) with the Ouse as rural control.
- Datasets cover phenyl urea and phenoxy acid herbicides measured across multiple sites and time periods.

## Datasets and variables
- Phenyl urea herbicides (units: ug/l): 2,4-Dichlorophenoxyacetic acid; 4-(4-Chloro-O-tolyloxy) butyric acid; 4-Chloro-O-tolyloxyacetic acid; Chlorotoluron (dissolved); Diuron (dissolved); Isoproturon (dissolved); Linuron (dissolved); Mecoprop (dissolved).
- Phenoxy acid herbicides (units: ug/l): same set as above for phenoxy acids.
- Sites and measurement specifics:
  - Humber sites (Swale at Catterick Bridge S1; Swale at Thornton Manor S2; Ure at Boroughbridge U3; Nidd at Skip Bridge N4; Wharfe at Tadcaster W5; Ouse at Clifton Bridge O6; Derwent at Bubwith D7; Aire at Beal Bridge A8; Calder at Methley Bridge C9; Don at Sprotborough Bridge D10; Trent at Cromwell Lock T11; Ouse at Acaster Malbis O12).
  - Tweed sites (TW13 Boleside; TW14 Norham; TW15 Ormiston Mill).
  - For most sites: “Variable = All variables”; Tweed sites measure all variables except Linuron dissolved at TW13, TW14, TW15.
  - Linuron dissolved: not measured at O12 (Ouse Acaster Malbis) and not measured at Tweed sites TW13–TW15.

## Temporal coverage
- Humber data: 1994–1995 and 1994–1997 (site-specific periods noted).
- Tweed data: 1995 (specific site ranges).
- Sampling frequency: intended weekly sampling; occasional gaps due to processing constraints.
- Measurement timing caveat: Linuron dissolved measured only Apr 1994–Oct 1994 at relevant sites.

## Methods and processing
- Sample collection: chromic acid-washed 1 litre glass bottles.
- Concentration methods (Phenyl urea): 
  - Method 1: Solid phase extraction (SPE) using C18 cartridges with ethyl acetate elution.
  - Method 2: Similar to Method 1 with additional methanol:wate r wash prior to elution.
  - Method 3: Liquid-liquid extraction with dichloromethane (used for phenoxy acids and some ureas).
- Instrumental analysis:
  - Phenyl urea herbicides: High Performance Liquid Chromatography (HPLC) with UV/VIS detection.
  - Phenoxy acid herbicides: Gas Chromatography (GC) with Mass Selective Detector (MS).
- Quality control and standardization:
  - Randomly spiked samples per batch with mixed standards (>99% purity).
  - Participation in AQUACHECK inter-laboratory harmonisation for urea and acid herbicides.

## Data quality, limitations, and documentation
- Data quality variability due to:
  - Highly polluted rivers (Aire, Calder, Don, Trent) leading to complex chromatograms.
  - Most concentrations near detection limits.
  - Difficulties in extraction, especially with liquid-liquid extraction (emulsions).
- QA materials:
  - Box-and-whisker plots (zip file) per determinand showing range, median, IQR, and outliers to aid data quality assessment.
- Data provenance and laboratories:
  - Up to Nov 1994: York University and IFE Wareham for urea herbicides.
  - From Dec 1994: Wallingford IH for extraction and analysis.
- Documentation and references:
  - House et al. 1997 describes methods and LOIS monitoring framework.
  - Data lineage includes random spiking, lab participation in harmonisation, and site-specific measurement notes.

## Provenance, stewardship, and access
- Part of the LOIS Core Programme focusing on micro-organics in Humber and Tweed rivers.
- Metadata provided for each site (code, name, NGR coordinates) and for each variable.
- Accessibility note: a ZIP file containing box-and-whisker plots is provided to help users gauge data quality; full dataset description and methods are documented.

## Implications for Data Stewards
- Ensure consistent variable definitions across sites, particularly regarding Linuron dissolved being omitted at certain Tweed sites and O12.
- Maintain standard units (ug/l) and clearly document any deviations or site-specific exclusions.
- Preserve and link provenance to the sampling periods, lab methods, and instrument platforms; track changes in laboratories and methods over time.
- Keep QA/QC procedures transparent (spike procedures, standards purity, inter-lab harmonisation status) and provide accessible quality indicators (e.g., the box-and-whisker plots) alongside the data.
- Manage data gaps and sampling interruptions explicitly in metadata; note any periods with incomplete weekly sampling.
- Ensure documentation references (e.g., House et al., 1997) are linked to data records for reproducibility.
- Facilitate data sharing with clear embargo or access notes, and maintain a path for updates as new measurements or reanalyses become available.