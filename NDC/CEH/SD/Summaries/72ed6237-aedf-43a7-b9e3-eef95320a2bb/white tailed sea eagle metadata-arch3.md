# Predatory Bird Monitoring Scheme

- Purpose and context
  - The dataset is generated as part of the Predatory Bird Monitoring Scheme (PBMS), whose outputs include long-term temporal trend analyses.
  - PBMS aims to monitor environmental health indicators in predatory birds to inform policy and future decision-making.
  - Results and reports are publicly accessible via the PBMS website (http://pbms.ceh.ac.uk/results.htm).

- Data scope and contents
  - The PBMS produces long-term trend analyses of contaminant data from predatory birds, with reports downloadable from the PBMS results page.
  - The dataset described includes a comprehensive table of contaminants measured in eggs (and, for some metrics, in liver) from nest sites.
  - Key variables and structure:
    - Egg number: unique identifier for each egg (note: numbering systems have changed over years; identifiers may be numeric or alphanumeric).
    - Year: the four-digit year in which the egg was laid.
    - Location: general location of the nest site.
    - Shell Index: an indicator of eggshell thickness (as described by Ratcliffe, 1970).
    - CF: concentration factor by which contaminant concentrations should be multiplied to convert to lipid-based concentrations.
    - A wide suite of contaminants including organochlorines (HCB, a-HCH, g-HCH, p,p-DDE, p,p-DDT, HEOD, p,p-TDE, Total PCB, TEQ, and multiple individual PCB congeners), with many entries marked NA (not analysed) or ND (none detected).
    - TEQ: Toxic Equivalencies calculated using WHO-defined TEFs for birds.
    - PCBs: concentrations reported for numerous congeners (e.g., PCB 8, PCB 18, PCB 28, PCB 52, PCB 77, PCB 101, PCB 105, PCB 114, PCB 118, PCB 123, PCB 126, PCB 128, PCB 138, PCB 141, PCB 149, PCB 153, PCB 156, PCB 157, PCB 163, PCB 167, PCB 169, PCB 170, PCB 171, PCB 180, PCB 183, PCB 187, PCB 189, PCB 194, PCB 199, PCB 201, PCB 205, PCB 206, PCB 209, etc.).
    - Matrix and units:
      - Egg contents: many contaminants expressed as mg/g (wet weight) or related units for egg contents.
      - Liver: several contaminants expressed as mg/g or related units on a wet weight basis.
      - Al, As, Cd, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Sb, Se, Zn: total element concentrations (many entries NA or ND; some data on dry weight basis for liver).
    - Data relationships:
      - Some measures are lipid-normalized using CF; others are reported on a wet weight or dry weight basis depending on the contaminant.
      - A mix of egg contents and liver measurements is used across contaminants.
    - Data quality indicators:
      - Many columns show NA (not analysed) or ND (none detected); some entries are Not Applicable or Not Analysed, reflecting incomplete data coverage for many contaminants and congeners.

- Outputs, analysis, and interpretation
  - The PBMS analyzes long-term temporal trends, enabling assessment of contaminant dynamics in predatory birds over time.
  - TEQ values provide an aggregated measure of toxicity potential from dioxin-like and related PCBs.
  - The dataset supports cross-contaminant comparisons and trend analyses at nest-site levels, contributing to environmental health monitoring.

- Metadata, standards, and governance
  - The data documentation references standardized contaminants and congeners consistent with environmental monitoring practices (e.g., WHO TEFs for PCBs).
  - Metadata elements included (e.g., Year, Location, Shell Index, CF) facilitate traceability, data transformation, and quality assurance.
  - Public data sharing is a feature, with outputs and underlying methods intended to be transparent to stakeholders and policymakers.

- Data quality, gaps, and challenges for monitoring frameworks
  - Challenges highlighted by the dataset include:
    - Incomplete data: large portions of analyses are NA or ND for many contaminants, indicating gaps in coverage.
    - Metadata adequacy: some records lack complete metadata, hindering rapid verification and reuse.
    - Data transformation: heterogeneous matrices (egg contents vs liver) and units require careful transformation and standardization (e.g., lipid normalization via CF, unit conversions).
    - Communication of findings: complexity of multi-contaminant results necessitates clear visualization and reporting to inform decision-makers.
  - These issues align with common monitoring framework challenges such as data gaps, siloed datasets, data-sharing barriers, and governance needs to ensure datasets meet standards and remain up to date.

- Implications for monitoring frameworks and policy decisions
  - PBMS demonstrates how a long-term, multi-contaminant monitoring program can support policy scrutiny and future decision-making.
  - The integration of lipid-normalized and non-lipid-normalized measures, TEQ calculations, and a broad PCB congener suite provides a comprehensive view of contaminant burden in predatory birds.
  - For effective monitoring governance, ensure:
    - Consistent metadata enhancement and documentation.
    - Comprehensive data sharing with appropriate quality assurance.
    - Standardized data formats and units across matrices (egg contents and liver).
    - Regular updates and transparent methodological descriptions to support reproducibility and policy use.