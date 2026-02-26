# Antibiotic susceptibility tests and resistance genes in Escherichia coli bacteria from humans, poultry and environmental samples: protocol

## Overview
- Protocol for studying antibiotic resistance in Escherichia coli isolated from humans (fecal), poultry (caecal), and the environment (water, wastewater, surface water, soil, solid waste, poultry litter; cattle samples where available).
- Focus on isolates resistant to third-generation cephalosporins and carbapenems; susceptibility tested against multiple antibiotic classes; resistance genes detected by real-time PCR.
- Ethical approvals obtained; informed consent collected; study conducted in rural households, small-scale poultry farms in Mirzapur, Tangail district, and urban markets in Dhaka, Bangladesh.

## Study Setting and Sample Collection
- Three data collection settings:
  - Rural households
  - Small-scale commercial poultry farms (broiler chickens) in rural Mirzapur, Tangail district
  - Urban food markets in Dhaka city
- Sample types and collection:
  - Humans: fecal samples from healthy adults
  - Poultry: caecal samples from poultry GI tract
  - Environment: water supply, wastewater, surface water, soil, solid waste, poultry litter/faeces
  - Cattle manure (where available)
- Collection rounds:
  - Round 1: February–April 2017 (winter)
  - Round 2: August–October 2017 (summer)
  - Water samples from farms/markets: October 2018
- Data collection conducted by trained icddr,b researchers.

## Laboratory Analyses and Data Generated
- Antibiotic susceptibility testing:
  - Isolates previously identified as resistant to third-generation cephalosporins and carbapenems
  - Disk diffusion method to measure zone of inhibition (mm)
  - Results categorized as susceptible, intermediate, or resistant per CLSI guidelines
- Molecular testing:
  - Real-time PCR to detect known antibiotic resistance genes
- SOPs and standards:
  - Standard operating procedures for susceptibility testing, DNA extraction, and PCR provided in supporting documentation
  - Analyses performed by trained personnel at the Food and Enteric Microbiology Laboratory, icddr,b
- Data capture:
  - Laboratory results recorded on paper or as automated outputs; later consolidated into a central dataset

## Data Management and Quality Assurance
- Data capture and entry:
  - Paper records entered into Excel by an experienced data manager
- Quality checks:
  - Random checks against original data collection sheets by an independent researcher
  - Frequency checks to identify out-of-range or erroneous values; corrections applied as needed
- Documentation and reproducibility:
  - Standard operating procedures and supporting documentation accompany the dataset

## Data Structure and Documentation
- Primary dataset: Ecoliastgenes.csv
  - Includes results for antibiotic susceptibility and resistance gene testing
  - Not done flag indicates a gene/test was not performed because the isolate did not show resistance to the relevant antibiotic
- Supporting documentation files:
  - Samplingstrategy.rtf
  - Microbiology.rtf
  - Dnaextraction.rtf
  - Realtimepcr.rtf
  - Susceptibility.rtf
  - VariablelistASTgenes.csv
- References:
  - CLSI guidelines (M100S) for antimicrobial susceptibility testing
  - WHO global foodborne infections network SOP for disk diffusion susceptibility testing

## Ethical Considerations
- Informed consent obtained from participants; right to withdraw at any stage
- Ethical clearances: icddr,b PR16071 and Loughborough University R17-P037

## Data Governance and Stewardship Implications
- Data standards and interoperability:
  - Clear linkage between phenotypic susceptibility data (disk diffusion) and genotypic resistance data (PCR) in a single file with accompanying metadata
  - Use of standardized CLSI categories and documented SOPs supports comparability and reuse
- Metadata and provenance:
  - Supporting documents provide methodological context; dataset includes Not done flags to indicate test omissions due to prior results
  - Timeline and setting information embedded in documentation, enabling traceability of samples and analyses
- Data quality and lifecycle:
  - Multiple quality controls (paper vs automated data capture, random checks, range checks) enhance data reliability
  - Future updates or additions would require versioning of Ecoliastgenes.csv and alignment with the supporting documentation
- Data access and sharing considerations:
  - Dataset and documentation are organized for discoverability (single CSV with rich supporting files)
  - Ensure ongoing accessibility of SOPs and variable definitions to enable reuse and reproducibility

## Reference Materials
- CLSI guidelines: Performance Standards for Antimicrobial Susceptibility Testing (M100S), 2016
- WHO SOP: Disk diffusion susceptibility testing for Enterobacteriaceae