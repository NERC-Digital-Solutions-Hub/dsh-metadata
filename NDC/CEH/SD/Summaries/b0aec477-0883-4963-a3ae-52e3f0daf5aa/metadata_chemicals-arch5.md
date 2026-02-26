# Experimental design/sampling method

- Objective and design
  - Track changing chemical profiles of caterpillars (Maculinea rebeli) reared with each ant (Myrmica schencki, M. sabuleti) across regions (Pyrenees, Poland, France) and timepoints.
  - Timepoints: uncontaminated pre-adoption final instars; six weeks after adoption; later after isolation from ants for 5 days to allow semio-chemicals to dissipate and caterpillars to release their own secretions.
- Sampling framework
  - Hexane extracts of surface chemicals collected from:
    - (i) Unparasitized ants from study sites (M. schencki and M. sabuleti) in Pyrenees, Poland; naïve ants in France (n = 5 workers from 5 nests per locality).
    - (ii) Eight batches per region of pre-adoption pre-contact M. rebeli larvae (n = 5 larvae per batch; total 40 per type of M. rebeli).
    - (iii) M. rebeli larvae after 6 weeks with naïve French ants (n = 5 for Spanish+schencki; n = 4–5 for Spanish+sabuleti and Polish+schencki/sabuleti, depending on subgroup).
    - (iv) M. rebeli larvae from (iii) then isolated from ants and kept unfed for 5 days (n = 3–5 per subgroup).
- Regional and host-ant combinations
  - Cross-regional sampling including Spain, Poland, and France; host ants include M. sabuleti and M. schencki; multiple colony-level samples per locality.
- Data scope and sample counts
  - Variable sample sizes across groups (e.g., n = 3–5 per combination) reflecting regional and treatment diversity.
- Data handling timeline
  - Each sequence includes pre-adoption, post-adoption (6 weeks with ants), and post-isolation stages to assess changes in cuticular/secreted chemicals.
  
## Analytical method and quality assurance

- Instrumentation and settings
  - Gas chromatography with mass spectrometric detection (GC-MSD) using HP 5890II GC and HP 5971A MSD; ultra-high purity helium carrier gas; column head pressure 10 psi.
  - Mass spectra acquired in full scan mode from 40–600 m/z.
- Peak detection and identification
  - Initial hydrocarbon screening via ion chromatogram at m/z 57; peak areas integrated with a threshold of 12.
  - Equivalent Chain Length (ECL) used to position peaks relative to n-alkane standards (n-C20 to n-C36).
  - Peaks tentatively identified by ECL plus full-scan MS spectra and comparison to NIST-97/08 databases.
  - Exclusion criteria: column bleed, siloxanes, phthalate plasticizers (identified by characteristic ion at m/z 149).
- Data processing
  - For statistics, peak areas are expressed as the proportion of the sum of all peaks in each chromatogram.
- Quality assurance
  - Chromatograms checked for interferences and peak integrity; peak shapes and separations ensured before quantification.

## Data storage format and column labels

- Storage format
  - CSV text file.
- Column label explanation
  - Labels follow a structured format (e.g., Rebeli_sab_0_ES_1141) with components indicating:
    - Sample type and organism (e.g., Rebeli = Maculinea rebeli; sab = Myrmica sabuleti; sch = Myrmica schencki).
    - Timepoint or condition (e.g., 0 = pre-adoption; 5 = after 5 days isolation; 5_ES = Spain; 0_PL = Poland; 0_FR = France).
    - Country of origin and sample number (e.g., ES, PL, FR; sample no: 1141, 1155, etc.).
  - Examples include:
    - Rebeli_sab_0_ES_1141: Maculinea rebeli reared with M. sabuleti, Spain, sample 1141.
    - Rebeli_sab_5_ES_1155: same group after 5 days isolation, Spain, sample 1155.
    - Rebeli_sch_0_Es_1111: Maculinea rebeli reared with M. schencki, Spain, sample 1111.
    - Sabuleti_Fr_1082: sample from Myrmica sabuleti, France.
    - rebeli_none_pre_PL_1029: pre-adoption Maculinea rebeli, Poland, sample 1029.
- Metadata coverage
  - Descriptions encode species/host interactions, country of origin, and sample identifiers to support provenance and cross-study comparability.

## Data provenance and governance considerations (Data Stewards view)

- Metadata completeness and standardization
  - Use consistent naming conventions to capture host-ant species, region, country, treatment stage, and sample number for easy discovery and reuse.
- Provenance and reproducibility
  - Document analytical workflow (GC-MSD parameters, peak identification approach, ECL calculation) to enable replication.
- Data quality and interoperability
  - Exclude non-informative peaks (column bleed, siloxanes, phthalates) and report proportion-based metrics to facilitate cross-sample comparisons.
- Data sharing readiness
  - CSV format and rich column-label schema support uploading to data portals and catalogues; explicit sample provenance aids discoverability and reuse.
- Handling complexity
  - Anticipate multi-region, multi-host designs and variable sample counts; maintain clear mappings between column labels and experimental groups to prevent misinterpretation.

## Key takeaways for data stewardship

- The dataset captures region-dependent chemical profiles across multiple host-ant interactions and timepoints, using a standardized GC-MS pipeline with detailed metadata.
- Stored as CSV with a rigorous, descriptive labeling scheme to ensure traceability, reuse, and cross-study comparability.
- Clear QA steps and filtering criteria are applied to peak identification, with proportional data enabling robust downstream analyses.