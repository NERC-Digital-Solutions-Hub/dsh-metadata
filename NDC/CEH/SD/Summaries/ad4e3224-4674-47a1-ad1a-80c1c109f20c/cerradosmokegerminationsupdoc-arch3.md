# CerradoSpeciesGermination_BrazilianSmokeWater.csv

## Overview
- Dataset evaluating the effect of smoke-water on seed germination for Cerrado species.
- Two related data structures describe experiment results and daily observations, with explicit collection and treatment details.

## Data structure and metadata
- CerradoSpeciesGermination_BrazilianSmokeWater.csv
  - Columns: Species, Collection_site, Collection_date, Experiment_date, Treatment, Replicate, Viable_seeds, Dead_seeds, Total_seeds.
- CerradoSpeciesGermination_BrazilianSmokeWaterMetadata.csv
  - Columns: Species, Treatment, Replicate, Day, Germinated.
- Table 1 (collection sites) provides standardized site abbreviations, full names, locations, and precise coordinates for multiple Brazilian sites (EEI, RNST, Jalapão, SC, Pirenópolis, EESB, PNSV).

## Collection sites (details)
- Variants and abbreviations used for sites include EEI, RNST, Jalapão, SC, Pirenópolis, EESB, PNSV with corresponding coordinates and locations.

## Experimental design and treatments
- Smoke solution treatments
  - Control (distilled water) or smoke-water treated (SW) solutions.
  - Smoke solutions prepared from 5 g biomass, exposed to 200°C for 30 minutes, soaked in 50 ml distilled water for 10 minutes, then filtered; separate replicates to avoid pseudoreplication.
  - Imbibition period of 24 hours before sowing.
- Germination setup
  - Seeds placed on double-layer filter paper in 60-mm Petri dishes, soaked with distilled water or smoke solution.
  - Germination chambers maintained at 27°C with a 12 h light/12 h dark cycle; water added as needed.
  - Observations every two days for 30 days; germination defined by radicle emergence.
  - Microbial contamination monitored; filter paper changed as needed.
- Quality control
  - Manual data recording and curation.
  - Viability tests (tetrazolium assay) performed on non-germinated seeds to constrain potential germination.

## Replication and measurements
- Replicates: typically 5 replicates per experiment.
- Measurements: daily germination counts; viability data for non-germinated seeds.

## Data usage and governance considerations
- Data are structured to enable reproducibility and cross-site comparisons, with clear metadata and collection/site details.
- Public sharing of underlying datasets and metadata is a potential barrier to data use in some contexts; the dataset includes explicit documentation to support data governance and transparency.

## References (methods context)
- Fichino et al., 2016; Jäger et al., 1996; Lakon, 1949; Le Stradic et al., 2015; Moreira et al., 2010.

---

# CerradoSpeciesGermination_RegenSmokeWater.csv

## Overview
- Dataset documenting germination responses of Cerrado species to two smoke-water concentrations and a control, expanding the BrazilianSmokeWater experiment with an additional regeneration/regen treatment dataset.

## Data structure
- Columns include: Species, Treatment (Control, Smoke_I 2.5%, Smoke_II 5.0%), Replicate, Day, Germinated.
- Additional information fields:
  - Species, Species_details, Family, Life_form.
  - Collection_site, Collection_date, Seed_storage_months, Seeds_per_replicate.
  - Experimental setup notes: non-scarified diaspores, Petri dish or acrylic box setup, imbibition and germination conditions (24 h in darkness, then 12 h photoperiod), and volumes per replicate (3 mL for small diaspores, 5 mL for larger diaspores).
  - Observational protocol: daily checks for up to 30 days or until stabilization (no germination for 10 consecutive days).

## Experimental design and treatments
- Treatments
  - Control (distilled water), Smoke_I (2.5% liquid smoke), Smoke_II (5.0% liquid smoke).
- Replication and conditions
  - 3 to 5 replicates per species and treatment.
  - Seeds incubated at 27°C, darkness for imbibition, then 12 h photoperiod.
  - Two concentrations of liquid smoke derived from Regen 2000®; three treatments applied per replicate.

## Collection and germination details
- Collection_site and Collection_date fields capture provenance and timing.
- Seed storage and seeds per replicate documented to support data interpretation and potential viability considerations.

## Observations and duration
- Daily germination counts recorded for up to 30 days or until germination stabilizes (no germination for 10 consecutive days).

## References
- Includes methodological references linked to smoking- and germination-studies (as in the BrazilianSmokeWater dataset).

## Data governance considerations
- The RegenSmokeWater dataset, like the Brazilian dataset, emphasizes detailed metadata and standardized procedures to support monitoring, reproducibility, and cross-study comparisons, addressing a key monitoring framework concern around transparent data structure and provenance.