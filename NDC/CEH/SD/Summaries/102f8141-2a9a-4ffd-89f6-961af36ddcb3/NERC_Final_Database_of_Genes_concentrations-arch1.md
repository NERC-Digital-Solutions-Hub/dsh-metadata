# Concentration Levels of Resistance Genes in Wastewater and Receiving Environment Brief description of the dataset

## Overview
- Weekly concentrations of the qnrS resistance gene in wastewater and the receiving river within the South West UK.
- Aims to support understanding of how resistance genes move from wastewater treatment to the environment.

## Study area and sampling
- Five major wastewater treatment plants (WWTPs) in a single river catchment, ~2000 km², population ≈ 1.5 million (>75% of catchment population).
- Sampling period: 7 consecutive days (Wednesday to Tuesday) between June and October 2015.
- WWTPs use various treatment technologies (activated sludge, trickling filters; some with sequencing batch reactors).
- Sample types:
  - Influent wastewater (24 h composites)
  - Effluent wastewater (time-proportional sampling)
  - River water (grab samples from upstream and downstream of discharge; not collected for Site E)
- River sampling distances varied by accessibility; all samples transported on ice to the lab.

## Data collection and laboratory methods
- DNA extraction from 1 mL unfiltered wastewater using a Roche kit; multiple enzymatic steps and purification, with DNA eluted and stored at -20°C.
- DNA extraction success checked by Nanodrop quantification.
- qnrS gene quantified by digital PCR (dPCR) on a QuantStudio 3D system.
  - Reaction mix details and cycling conditions provided.
  - Data analyzed with AnalysisSuite software to obtain gene copy quantifications.
- Sub-sample processing specifics (e.g., 80 mL subsamples for influent, 14.5 μL reaction aliquots, etc.) described to ensure reproducibility.

## Data variables and format
- Primary variables: concentrations of qnrS gene in influent, effluent, and river samples.
- Unit: copies per microliter (copies/μL).
- Spatial scope: data from five WWTPs within one catchment; river concentrations measured upstream and downstream of effluent discharge points.
- Temporal scope: a single 7-day monitoring week within 2015.
- Data format specifics are described for the dataset, including laboratory methods and QC steps.

## Measurement quality and references
- DNA extraction and qnrS quantification procedures are detailed, enabling assessment of methodological uncertainty.
- QC: DNA quantified with Nanodrop; dPCR data analyzed with dedicated software.
- Key references detailing related methodology and context:
  - Castrignano et al. 2018; 2018 Chemosphere
  - Castrignano et al. 2020; Water Research
  - Petrie et al. 2016; Journal of Chromatography A

## Potential uses for analysts
- Assess correlations between WWTP influent/effluent concentrations and downstream river concentrations.
- Compare treatment technologies and their association with reduction or persistence of qnrS.
- Inform risk assessments of resistance gene dissemination within catchments.
- Serve as a data point for extrapolation studies or model calibration in similar catchments, with caution due to limited temporal scope.

## Limitations and considerations
- Temporal limitation: data from a single 7-day week; may not capture seasonal or inter-annual variability.
- Spatial limitation: one river catchment; may limit generalizability to other settings.
- Unit interpretation: concentrations reported as copies/μL; careful normalization may be needed for wastewater volumes.
- Data access and reuse: dataset requires careful handling of sampling context (influents, effluents, river segments) for valid comparisons.

## References
- Castrignano, E., et al. 2018. Enantioselective fractionation of fluoroquinolones in the aqueous environment...
- Castrignano, E., et al. 2020. (Fluoro)quinolones and quinolone resistance genes in the aquatic environment: A river catchment perspective. Water Research 182.
- Petrie, B., et al. 2016. Multi-residue analysis of 90 emerging contaminants in liquid and solid environmental matrices... Journal of Chromatography A 1431.