# Concentration Levels of Resistance Genes in Wastewater and Receiving Environment Brief description of the dataset

## Summary at a glance
- Weekly measurements of the qnrS resistance gene in wastewater influent and effluent across five WWTPs, SW UK (June–October 2015).
- Includes river water sampling upstream and downstream of effluent discharge (where available).
- Data collected over a 7-day period per week with varied sampling approaches and treatment technologies.
- Laboratory workflow from DNA extraction to digital PCR quantification (dPCR) of qnrS, with QA steps.
- Data format: gene concentrations reported as copies per microliter.

## Dataset scope and context
- Purpose: Track concentrations of the qnrS resistance gene in wastewater and receiving water within a single river catchment.
- Study area: Five major wastewater treatment plants (WWTPs) in SW UK, covering ~2,000 km2 and ~1.5 million people (>75% of catchment population).
- Relevance for data strategy: Demonstrates end-to-end data lifecycle from field sampling to molecular quantification and data formatting, with implications for data discoverability, quality, and cross-site comparability.

## Sampling design and sites
- Wastewater sampling
  - Influent and effluent collected for 7 consecutive days mid-2015 (Wednesday to Tuesday).
  - Sites: five WWTPs contributing to one river catchment.
  - Technologies: mix of activated sludge (AS), trickling filters (TF), and sequencing batch reactors (SBRs).
- River sampling
  - Collected upstream and downstream of effluent discharge; distance varied by accessibility.
  - Site E lacked river sampling due to direct discharge to the estuary.
- Sample timing
  - Influent: volume-proportional 24 h composites with subsamples ~15 minutes apart.
  - Effluent: time-proportional sampling (less variation over 15-minute intervals).
  - River: 8 L grab samples.

## Laboratory methods and data processing
- DNA extraction
  - Starting with 1 mL unfiltered wastewater, followed by a lysozyme/PK-based extraction and filter-based purification.
  - Final elution in pre-warmed 60°C buffer and storage at -20°C.
  - DNA quantity checked with a Nanodrop instrument.
- qnrS quantification
  - Digital PCR system: QuantStudio 3D with a qnrS TaqMan assay.
  - Reaction setup includes master mix, assay mix, nuclease-free water, and DNA sample; loaded onto high-density nanofluidic chips.
  - Thermal cycling: 95°C denaturation, 60–98°C cycling, final hold at 60°C.
  - Data analysis: QuantStudio AnalysisSuite software to obtain targeted gene quantification.
- Data handling
  - Concentrations expressed as copies per microliter (µL) for influent, effluent, and river samples.
  - References provided for method validation and context.

## Data format, structure, and accessibility
- Format: Concentration values of qnrS gene per sample across all sites and water matrices (influent, effluent, river).
- Temporal coverage: One monitoring week within June–October 2015, with serial sampling across WWTPs and river points.
- Metadata considerations: Study design, sampling frequency, treatment technologies, and sampling point descriptions are documented to support interpretation, replication, and cross-site comparisons.

## Data quality, caveats, and limitations
- River sampling not conducted at Site E due to direct estuary discharge.
- Differences in sampling approaches between matrices (24 h composites for influent vs time-proportional effluent, grab river samples) may affect comparability across matrices.
- Method details include extensive QA steps (DNA extraction controls, Nanodrop QC), but the summary notes potential variability inherent to field sampling and laboratory workflows.
- Data interpretation should account for treatment technology differences and site-specific catchment characteristics.

## Practical implications for Data Leaders
- Data governance and standardization
  - Establish clear metadata standards (sampling method, timing, matrix, site, treatment technology) to enable interoperability across sites and studies.
  - Document QA/QC procedures and detection limits to support data quality assessments.
- Data strategy and value creation
  - Create a reusable data product: weekly qnrS concentrations by WWTP and river node, enabling trend analysis and cross-site benchmarking.
  - Integrate with broader antimicrobial resistance surveillance datasets to inform policy and community health outcomes.
- Data discovery and stewardship
  - Ensure dataset discoverability with consistent naming, descriptive metadata, and reference to the underlying protocols and validation studies.
  - Plan for data updates and versioning if extended monitoring is pursued to support longitudinal analyses.
- Gaps and opportunities
  - Consider expanding river sampling at all sites or documenting reasons for gaps to improve completeness.
  - Harmonize sampling frequency and matrices where feasible to strengthen cross-site comparability.

## References
- Castrignano, E., A. M. Kannan, E. J. Feil, and B. Kasprzyk-Hordern. 2018. Enantioselective fractionation of fluoroquinolones in the aqueous environment using chiral LC-MS/MS. Chemosphere 206:376-386.
- Castrignano, E., et al. 2020. (Fluoro)quinolones and quinolone resistance genes in the aquatic environment: A river catchment perspective. Water Research 182.
- Petrie, Bruce, et al. 2016. Multi-residue analysis of 90 emerging contaminants in liquid and solid environmental matrices by UHPLC-MS/MS. Journal of Chromatography A 1431.