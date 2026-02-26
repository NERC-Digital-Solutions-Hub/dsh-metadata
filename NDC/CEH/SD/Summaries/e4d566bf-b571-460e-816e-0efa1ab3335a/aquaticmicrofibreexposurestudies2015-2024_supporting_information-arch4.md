# AquaticMicrofibreExposurestudies2015-2024 Supporting information

## Overview
- Describes the dataset "TraitResponsesofAquaticOrganismsfromMicrofibreExposurestudiespublished20152024.csv" derived from published laboratory studies on microfibres (<5 mm) and their effects on aquatic organism traits (development, fecundity, feeding, growth, hatching, health, survival).
- Global contributor base; data compiled for a meta-analysis comparing petroleum-based vs non-petroleum microfibres.
- Data accessible as of 19 June 2024, covering studies from 2015–2024.
- Ben Parker led data collection and dataset compilation.
- Only eligible studies/responses are included; positive responses emphasized (converted from some negative-yet-desirable directions).

## What the dataset contains
- Extracted study data for laboratory microfibre exposure impacts on aquatic organisms.
- Exposures are for microfibres <5 mm, single polymer type (no mixtures), with mean measures and associated errors available for exposure and control conditions.
- Key biological traits included: Development, Fecundity, Feeding, Growth, Hatching, Health, Survival.
- Across studies, final timepoints or life stages are used when multiple timepoints were available.
- Excluded: co-contaminant exposures; non-final timepoints; non-single-polymer exposures.
- Data sources include manuscript text, supplementary information, and figures (digitised when needed).

## Collection and curation process
- Identification: Topic search in Web of Science with terms related to microfibre exposure (conducted 19/06/2024).
- Screening stages:
  - Stage 1: Titles/ant abstracts screened for relevance to organism responses to microfibre exposure.
  - Stage 2: Forward/backward searches from Stage 1 results screened for relevance.
  - Stage 3: Eligible studies subjected to full eligibility review.
- Eligibility criteria:
  1) Aquatic organisms used
  2) Controlled microfibre exposure >1 µm and <5 mm, single polymer
  3) Mean measures with errors available for both exposure and control
- Data extraction: Means and SDs extracted from MS/SI/text or figures using a plot digitiser where needed; responses converted to a single positive direction when necessary.

## Data structure and units
- Primary file: AquaticMicrofibreExposurestudies2015-2024.csv
- Example fields (described at a high level):
  - Study identifiers: Study.no, Reference, Authors, Title, Year
  - Study origin: FA.country (country of first author affiliation), Environment (Freshwater, Marine, Estuarine)
  - Organism details: Species, Source (wild, lab stock, etc.), Taxonomic.grouping
  - Exposure details: MF.category (petroleum-based vs other polymers), Length.mm, Duration/exposure days, Study.exposure and Study.exposure.units, Standard.exposure (log scale categories), S.cat (units for standardised exposure)
  - Response data: C.N, C.mean, C.SD (control), E.N, E.mean, E.SD (experimental), Response.units, Data.source, Converted.measure (whether a conversion was applied)
  - Response classification: C.N and E.N relate to final timepoint; C.mean/SD and E.mean/SD provide quantified effects
  - Time aspect: Time.series flag indicating sequential data presence
  - Time/exposure categorisations: Days.exposed and Days.cat
  - Source of data: MS or SI
- Units and standardisation follow the described scheme, with final-timepoint data used for analysis.

## Quality control and transparency
- Rigorous screening to ensure: aquatic organism focus, controlled single-polymer microfibre exposure, and extractable mean-and-error data.
- Positive-response emphasis; any non-beneficial directions re-categorised as positive for inclusion.
- Duplicates removed; data standardised across studies where possible.
- Metadata and data extraction provenance preserved via explicit fields (source, timepoint, exposure, units, etc.) to support discoverability and reuse.

## Study references (representative examples)
- Au et al. (2015); Hyalella azteca responses to microplastic exposures
- Blarer & Burkhardt-Holm (2016); Gammarus fossarum assimilation under microplastics
- Bour et al. (2022); three-spined stickleback exposure to textile microfibers
- Bunge et al. (2022); sticklebacks dietary microfibers
- Cheng et al. (2021, 2024); microplastic fibers effects on zebrafish and microalgae
- Choi et al. (2021, 2022); Mytilus galloprovincialis responses to PET microfiber
- Cole et al. (2020); Mytilus spp. responses to microplastics/microfibres
- Coppock et al. (2019); Calanus helgolandicus feeding changes
- Cui et al. (2022); Lemna minor growth under petroleum- and cellulose-based fibers
- DiBona et al. (2021, 2022); Oryzias latipes developmental impacts
- Hu et al. (2020); chronic microfiber exposure in medaka
- Jabeen et al. (2018); virgin microplastics effects on goldfish
- Jemec et al. (2016); Daphnia magna uptake and effects
- Jiang et al. (2023); Daphnia carinata mitochondrial and oxidative stress responses
- [Additional references provided within the resource]