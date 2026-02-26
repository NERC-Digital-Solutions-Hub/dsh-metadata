# Supporting information for: Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates

## Purpose and scope
- Provides supporting information for a phenotypic dataset from an experimental infection study on house finches using Mycoplasma gallisepticum isolates.
- Part of the NERC project Evolution of phenotypic plasticity in an emerging pathogen.
- Aims to test how phenotypic plasticity in hosts and pathogens relates to infection dynamics and host resistance.

## Data access, licensing and citation
- Data licensed under the Open Government Licence.
- Access via DOI: https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d
- Reuse citation: Bonneaud, C. (2019). Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates. NERC Environmental Information Data Centre. https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d

## Governance, ethics and provenance
- Protocols approved by IACUCs at Auburn University (PRN 2015-2721) and Arizona State University (15-1438R); Institutional Biological Use Authorizations at Auburn University (BUA 500); University of Exeter ethics committee.
- Study involved wild house finches captured in Arizona (N=171) and Alabama, with health screenings prior to inclusion, and subsequent controlled infection experiments.

## Study design and sampling
- Birds and isolates
  - 171 wild house finches (93 males, 78 females) captured in summer 2015.
  - 53 birds from Alabama and 59 birds from Arizona inoculated with one of 56 M. gallisepticum isolates collected during a multi-year epidemic (1994–2015).
  - Isolates prepared and stored; inoculation performed in controlled aviary settings.
- Inoculation and housing
  - Inoculation via 20 μL containing 1×10^4 to 1×10^6 color-changing units/mL, administered to eyes.
  - Arizona birds housed in pairs with one inoculated partner.
- Health status and ethics
  - Pre-screening to confirm absence of prior M. gallisepticum infection; birds screened for other diseases and treated as needed.
  - Experimental endpoint: euthanasia at day 35 or as per licencing.

## Data collection and outcomes
- Phenotypic measurements
  - Eye lesion scoring (0–5) for each eye at days 3, 6, 8, 14, 21, 25, 28, 34 post-inoculation.
  - Body mass measured at days -7, 0, 3, 8, 14, 21, 28, 34 post-inoculation.
- Infection status and pathogen metrics
  - Pathogen clearance assessed by PCR on conjunctival/tracheal swabs at days 8, 14, 21, 28.
  - Quantitative pathogen load (MG load) recorded for certain time points (e.g., Pload_8, Pload_14, Pload_21, Pload_28).
  - PCR detection data for non-infected birds across multiple days (PCR_2t through PCR_35t).
  - Specific qPCR primers and probes used to quantify pathogen DNA (Mgc110 and Rag1 targets) with detailed cycling conditions provided.
- Data completeness
  - Data structure notes include missing measurements (e.g., days without measurements or failed assays) and non-detections in molecular assays.

## Dataset structure and variables (highlights)
- Bird-level identifiers and metadata
  - ID (unique bird identifier), Sex (f/m), Pop (population origin, e.g., AO/Auburn; GT/Tempe), Pathogen (year of sampling).
- Morphometrics and phenotypes
  - Mass_d-7, Mass_0, Mass_d3, Mass_d8, Mass_d14, Mass_d21, Mass_d28, Mass_d34 (body mass in grams at specified days).
  - RE_score.dX and LE_score.dX (right/left eye lesion scores at various days; 0–5 scale).
- Infection status and pathogen metrics
  - MG_PCR_d8, MG_PCR_d14, MG_PCR_d21, MG_PCR_d28 (binary 0/1 for PCR detection in swabs at those days).
  - Pload_8, Pload_14, Pload_21, Pload_28 (MG load measured as cell copies).
  - PCR_2t, PCR_3t, ..., PCR_35t (PCR detection in non-infected bird swabs across multiple days; 0/1).
- Data type and units
  - Descriptions, units (where applicable), and data types documented (numbers for measurements, text for sex/pop, etc.).
- Data completeness notes
  - Missing measurements flagged; some assays unsuccessful; field-level notes reference potential data gaps.

## Data quality, standards and governance considerations (Data Steward perspective)
- Data provenance
  - Clear attribution to the project, investigators, and ethics approvals; datasets anchored to a defined experimental protocol.
- Metadata and interoperability
  - Rich metadata on species, isolates, sampling days, and assay methods; standardized timepoints (days post-inoculation) and consistent naming (e.g., Mass_dX, RE_score.dX).
- Data quality and missing data
  - Acknowledgement of incomplete measurements and assay failures; explicit documentation of data gaps to support robust analyses.
- Ethical and licensing clarity
  - Open Government Licence facilitates reuse; explicit citation requirements aid traceability and attribution.
- Usability for governance and reuse
  - Comprehensive data structure description supports data sharing across systems; time-series measurements enable longitudinal analyses of host responses and pathogen dynamics.
- Potential challenges for data stewards
  - Harmonizing data across institutions and systems; handling large time-series with numerous variables; updating datasets as new measurements or corrections become available.

## Availability, usage, and linking
- Access via the provided DOI under Open Government Licence.
- Reuse requires proper citation as specified.
- Dataset designed to be discoverable and usable by researchers and data managers for downstream analyses and meta-studies on phenotypic plasticity in hosts and pathogens.