# Amazon Fertilization Experiment (AFEX)

## Study area and experimental design
- Located within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Brazil.
- Climate: humid/wet with mean temperature ~26.7°C and 2400 mm annual rainfall; dry season July–Sept; rain peak in Mar–Apr.
- Soils: clayey red-yellow podsols and yellow latosols, highly weathered, acidic, low fertility (WRB ferrasols).
- AFEX (initiated March 2017) is a full factorial fertilization experiment with seven treatments plus a control.
- Treatments: N (125 kg N ha-1 y-1 as urea), P (50 kg P ha-1 y-1 as triple superphosphate), and cations (K, Ca, Mg) applied as KCl and dolomitic limestone.
- Design: 32 plots total (7 treatments + control × 4 replicates) arranged in at least four blocks separated by ≥250 m.
- Plot size: 50 × 50 m; blocks/plots chosen to be similar in soil, vegetation, and topography.
- Fertilization applied annually in three applications to reduce nutrient loss.

## Data collected and sampling design
- Ant sampling within AFEX plots: five 1 × 1 m sub-plots per 50 × 50 m plot, totaling 20 sub-plots per treatment and 160 sub-plots overall.
- Sampling method: Winkler extractor; litter collected, placed in Winkler sacks, and processed for 48 hours; ants fixed in 90% alcohol.
- Sampling years: 2018 (October) and 2019 (September), i.e., two annual samplings in the dry season.
- Identification: ants identified by subfamilies and genera using taxonomic keys (Baccaro et al. 2015); species-level identifications to be confirmed with additional keys and comparisons to INPA collections.
- Data sources for identifications: AntCat online catalog (Bolton 2020) and INPA invertebrate collection for reference.
- Data products: ant community data used to assess richness, composition, relative abundance, and frequency across treatments and years.

## Data spreadsheet and data structure
- Dataset: litterfall_ants.csv (Litterfall ants data spreadsheet) stored in EIDC.
- Key columns and meaning:
  - YEAR: sampling year (2018 October; 2019 September)
  - BLOCK: experimental block (1–4)
  - PLOT: plot within block (1–5)
  - TRT: treatment or combination (as defined in AFEX 2.0)
  - SUBFAMILIES: ant subfamily
  - GENERA: ant genus
  - INDIVIDUAL: number of individuals
- Example data representation shows hierarchical entries by year, plot, and treatment, with counts by subfamily and genus.
- Data documentation includes a data dictionary-like structure describing column roles (e.g., YEAR, BLOCK, PLOT, TRT, SUBFAMILIES, GENERA, INDIVIDUAL).

## Data management, provenance, and sharing
- Data deposition: dataset deposited into the EIDC data repository (eIDC/EIDC).
- Metadata and provenance: explicit field definitions and sampling protocol described (plot layout, sub-plot sampling, Winkler method, and fixation).
- Documentation and reuse: taxonomic references and keys cited; data intended to support reuse by researchers investigating ant communities under fertilization treatments.
- Data updates: the text implies ongoing work (e.g., continuing identifications with multiple keys and INPA comparisons), suggesting potential future updates to taxonomy or counts.

## Opportunities and challenges for data stewards
- Data standardization: clear field definitions (YEAR, BLOCK, PLOT, TRT, SUBFAMILIES, GENERA, INDIVIDUAL) facilitate interoperability, though some entries show abbreviations and formatting inconsistencies that may require harmonization.
- Metadata completeness: taxonomic identification plans rely on multiple keys and external references; ensure full metadata for identifications (taxonomic level, keys used, reference specimens) accompanies the dataset.
- Timeliness and provenance: two sampling years are documented; future updates should capture additional years and any re-identifications or data corrections.
- Cross-reference and interoperability: use of external catalogs (AntCat) and INPA collections should be captured in metadata with accession numbers or identifiers for traceability.
- Data quality controls: maintain consistent coding for plots, blocks, and treatments; document any data cleaning or transformations applied before sharing.
- Access and reuse: data shared via EIDC; stewardship should ensure access rights, licensing, and any embargoes or usage restrictions are clearly stated.

## Relevance to data governance and stewardship aims
- The AFEX dataset exemplifies the role of a data steward in ensuring structured, well-documented, and sharable data for large, multi-treatment ecological experiments.
- Actions align with governance goals: standardized data schemas, metadata-rich deposition, use of recognized taxonomic references, and open data sharing to support discovery and reuse.
- Anticipated future work (identifications, dataset updates) highlights the importance of maintaining data provenance and versioning for ongoing usability.