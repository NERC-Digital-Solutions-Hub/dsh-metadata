# Data Collection

- Purpose and context:
  - NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
  - Aims to quantify strain-specific seroprevalence for Great Island virus within the common guillemot population.

- Study site and sampling frame:
  - Isle of May, Firth of Forth, Scotland (56.2°N, 2.6°W) chosen for its large, accessible guillemot population.
  - 144 individual common guillemots captured between 1993 and 1995; blood samples collected on filter paper.

- Dataset scope:
  - Maximum of 12 Great Island virus strains tested.
  - Part of dataset described in Nunn et al. (2006) Parasitology 132: 233-240; detailed methods also from that publication with noted differences.

- Data collection methods (high-level):
  - Virus isolation from tick homogenates and plaque assays on cell lines (BHK21 and Vero).
  - Preparation of blood samples eluted from filter paper into PBST with antibiotics.
  - Serological testing via plaque reduction neutralisation tests (PRNT); samples tested in multiple replicates.
  - Results expressed as fold decrease in viral titre relative to controls; controls included PBST and chicken blood eluted from filter paper.
  - Incubation, plaque development, and staining steps described; differences in incubation times noted between parts of the dataset (MAN vs KMW).

- Data structure and key variables:
  - BTO_Ring: Unique ID for each bird.
  - Collection_date: Date of blood sample collection.
  - Subcolony: Site where the bird was observed.
  - Sex: Sex of the bird.
  - Status: Breeding status (PB = pre-breeding, B = breeding).
  - Virus_strain: Strain tested (MDNV, CBNV, COYV, BRDV, AMDV; up to 12 strains considered overall).
  - Sample_PFUx: Number of plaque-forming units (PFU) or PFU per ml in the well with blood sample.
  - Sample_PFU_av: Mean PFU value across replicates.
  - Control_PFU_av: Mean PFU value in control wells (PBST or chicken blood eluate).

- Provenance and documentation:
  - Methods and data provenance linked to Nunn et al. (2006); explicit notes of two method variants (MAN and KMW) within the dataset.

- Data quality and interoperability considerations:
  - Multiple assay replicates (typically 4 per sample) and averaging.
  - Clear labeling of virus strains and units (PFU, PFU/ml).
  - Documentation needed for method variant (MAN vs KMW) to ensure reproducibility.
  - Metadata should preserve collection date, site, bird ID, and breeding status to enable seroprevalence analyses by strain and host factors.

- Governance and reuse notes for data stewards:
  - Ensure consistent encoding of dates, subcolony names, and virus strain identifiers.
  - Maintain linkage to publication (Nunn et al. 2006) for methodological context.
  - Consider storing both raw assay outputs and derived averages to support re-analysis.
  - Clarify any partial datasets or differences between MAN and KMW portions to support transparent data reuse.