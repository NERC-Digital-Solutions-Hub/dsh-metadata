# Brief description of the dataset

## Overview
- Weekly concentrations of fluoroquinolones and the qnrS resistance gene in the South West UK, measured in wastewater influent and effluent and in the receiving river water.

## Spatial and temporal coverage
- Study area: five major wastewater treatment plants (WWTPs) contributing to one river catchment in South-West UK, covering ~2,000 km² and ~1.5 million people (>75% of catchment population).
- Time frame: seven consecutive days, Wednesday to Tuesday, between June and October 2015.
- Sample types and locations: wastewater influent and effluent; river water upstream and downstream of the effluent discharge point (except Site E, which discharges to the estuary and had no river sample).

## Sampling design
- Influent wastewater: 24 h flow-proportional composites with ~15-minute subsamples (average frequency ~15 min) using ISCO 3700 autosampler; samples cooled to 4°C and pooled after 24 h.
- Effluent wastewater: time-proportional sampling due to limited variation.
- River water: grab samples (8 L) collected upstream and downstream of the discharge point at varying distances.
- Sample handling: all samples transported on ice to the laboratory for processing.

## Analytical methods
- Analytes: multiple fluoroquinolones including ofloxacin and its derivatives, lomefloxacin, moxifloxacin, several salts/esters, ciprofloxacin and its derivatives, norfloxacin, nalidixic acid; plus the qnrS resistance gene.
- Preparation: filtration (GF/F 0.7 µm), spiking with isotopically-labelled internal standards, solid-phase extraction (SPE) on Oasis HLB cartridges, elution with methanol, evaporation, reconstitution.
- Instrumental analysis: chiral liquid chromatography–tandem mass spectrometry (LC-MS/MS) using a CHIRALCEL OZ-RH column; isocratic mobile phase of 10 mM ammonium formate/methanol 1:99 with 0.05% formic acid; positive electrospray ionization; duplicate analyses.
- Quality assurance: method fully validated (as described in referenced literature).

## Data content and format
- Measurements: concentrations of quinolones (and qnrS) in influent, effluent, and receiving river water.
- Units: ng/L.
- Data format: organized by measurement context (influent, effluent, river upstream, river downstream) and analyte, for the monitoring week.

## Data accessibility and references
- References documenting methods and applications:
  - Castrignano et al. 2018: enantioselective fractionation of fluoroquinolones via chiral LC-MS/MS.
  - Castrignano et al. 2020: (Fluoro)quinolones and quinolone resistance genes in the aquatic environment (river catchment perspective).
  - Petrie et al. 2016: multi-residue analysis of emerging contaminants by UHPLC–MS/MS.

## GIS-relevant opportunities and considerations
- Potential GIS products:
  - Time-series maps of antibiotic concentrations at each WWTP and river sampling point.
  - Spatial comparison of influent vs. effluent vs. river concentrations to assess attenuation and dispersion.
  - Catchment-wide exposure maps integrating population data and WWTP discharge points.
- Data integration ideas:
  - Link concentrations to precise sampling coordinates and distances downstream from discharge points.
  - Combine with hydrological layers (river network, flow data) to model transport and dilution.
  - Use alongside land-use and remediation data to identify hotspots of antibiotic resistance gene presence.
- Data quality considerations for GIS:
  - Handle non-detects (nd) and values below method quantification limit (MQL) appropriately in analyses.
  - Account for differing sampling approaches between influent (composite) and effluent (time-proportional) in spatial-temporal modeling.
  - Site E lacking river data; consider this in catchment-scale mappings.

## Limitations and cautions
- Temporal scope is limited to a single monitoring week; may require additional datasets for robust trend analysis.
- Spatial resolution limited to five WWTP sites and associated river points; may constrain fine-grained spatial analyses in some contexts.
- Some abbreviations and data flags (e.g., nd, <MQL) require careful interpretation during data integration.

## Abbreviations and notes
- nd: not detected
- <MQL: below method quantification limit
- Conc.: concentration
- Influent: wastewater influent
- Effluent: wastewater effluent
- River upstream/downstream: river water relative to discharge point
- Site E: WWTP discharges directly to estuary (no river sample)