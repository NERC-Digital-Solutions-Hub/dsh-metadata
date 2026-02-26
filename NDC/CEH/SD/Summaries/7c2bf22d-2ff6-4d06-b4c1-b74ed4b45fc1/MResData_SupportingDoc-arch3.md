# Moth community and parasitoid data from a hedgerow cutting regime experiment in Cambridgeshire, England, 2011

## Overview and purpose
- Dataset from long-running hedgerow experiments in Cambridgeshire (Monks Wood) assessing how hedgerow cutting regimes affect wildlife habitat quality, resources, and associated moth communities and their parasitoids.
- Aimed to inform monitoring of agricultural-environment policy by linking management regimes to biodiversity, habitat structure, and resource provision (flowers, berries) for wildlife.
- Related publication: Facey et al. 2014 on moth communities, diversity, abundance, and parasitism under agrienvironment schemes; Defra project BD2114 funded by Defra and managed by UKCEH.

## Experimental design and site
- Long-running, randomised plot experiment conducted 2006–2014 at Monks Wood, Cambridgeshire (approx. 52.4026°N, -0.2357°W) on former arable land converted to grassland.
- Four hedgerows planted in 1961; 32 contiguous plots of 15 m length per hedge.
- Treatments allocated in factorial combinations:
  - Cutting frequency: annual, biennial (every two years), triennial (every three years)
  - Cutting timing: autumn vs winter
- Two unmanaged control plots per hedge (never cut in current experiment; 15+ years without cutting in autumn 2005 baseline)
- Replication: 8 replicates for annual plots; 4 replicates for two- and three-year plots (per treatment combination)
- Experimental data focus for Experiment 1: timing and frequency effects on hawthorn flowering, berry provision for overwintering wildlife, and hedgerow structure.

## Data collection and measurements
- Moth sampling and parasitoid rearing (May–Sept 2011)
  - Methods: timed search within 1 m x 0.5 m quadrats; hedgerow beating with gutter sampling to dislodge larvae; identification to species; rearing larvae to adulthood to determine parasitism
  - Outcome: moth species data, associated parasitoid data, and emergence records
  - Data files: MResMothLarvaeParasitoids.csv
- Hedgerow architecture and resource availability
  - Measurements taken June 2011: hedgerow height, width, branching density, and length; biomass of leaves (per quadrat), leaf counts, and leaf weights
  - Data files: MResDimensions.csv, MResLeaves.csv, MResBranches.csv, MResBranchTips.csv
- Foliar quality
  - Carbon and nitrogen concentrations measured from freeze-dried leaves to assess foliar quality as a potential driver of moth abundance/diversity
  - Data file: MResCN.csv
- Datasets include explicit metadata fields for site, experiment, block, plot, treatment, visit date/year, replicate, and sampling method
  - References to dataset schemas: described per-file data tables in the accompanying document

## Data structure and quality control
- Data tables and schema
  - MResMothLarvaeParasitoids.csv: detailed larva-level records with fields for experiment, site, block, plot, treatment, visit date/year, collection method, sample ID, moth name, parasitism status, parasitoid name/family/subfamily, and notes
  - MResDimensions.csv: hedge height/width measurements by replicate
  - MResLeaves.csv: leaf counts and dry weights per plot/replicate
  - MResBranches.csv: total branches per quadrat per plot
  - MResBranchTips.csv: branch length and counts of growing tips (1-, 2-, 3-year) and thorn tips per quadrat
  - MResCN.csv: foliar carbon and nitrogen percentages per plot
- Quality control
  - Standard protocols followed; experienced field surveyors collected data
  - Expert verification of species identifications
  - Data checks for anomalies; missing values attributed to survey error and corrected during data upload to Oracle database
- Data provenance and references
  - Data tied to a Defra research project (BD2114) with published methodology and supporting literature

## Data usage and outputs
- Measures aligned with environmental health and monitoring objectives:
  - Biodiversity indicators: moth species richness and abundance; parasitism rates
  - Habitat quality indicators: hedgerow architecture (height, width, branching) and structural complexity
  - Resource indicators: hawthorn flowering and berry production
  - Primary plant quality indicator: foliar C and N concentration
- Output formats designed for policy monitoring and analysis:
  - Structured CSV data files with rich metadata to support replication and cross-study comparability
  - Clear linkage between management treatments and ecological responses
- Publication and impact
  - Findings contributed to understanding how hedgerow cutting regimes influence biodiversity, abundance, and trophic interactions within hedgerow ecosystems

## Funding and references
- Funded by Defra (BD2114); managed by UK Centre for Ecology & Hydrology (UKCEH)
- Key references include methodological and ecological background on hedgerow restoration, moth identification guides, and related habitat studies (e.g., Bremner & Tabatabai 1971; Croxton et al. 2004; Maudsley et al. 2002; Sparks & Croxton 2007; Waring & Townsend 2009)

## Implications for monitoring frameworks
- Demonstrates a multi-maceted approach to environmental health monitoring:
  - Combines biodiversity surveys, habitat structure assessments, and plant nutritional quality to interpret ecological responses to policy-driven management
  - Provides long-term, replicated evidence to evaluate the effectiveness and trade-offs of hedgerow management schemes
  - Emphasizes robust metadata, standardized protocols, data permanence, and governance suitable for open-data sharing while acknowledging field-related data gaps and error handling
- Offers a concrete, policy-relevant case study for designing monitoring frameworks that integrate ecological indicators with management practices and data governance considerations