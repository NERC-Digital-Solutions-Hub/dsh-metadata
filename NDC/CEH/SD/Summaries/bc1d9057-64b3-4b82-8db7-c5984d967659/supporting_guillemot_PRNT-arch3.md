# Great Island virus seroprevalence in common guillemots on the Isle of May

## Purpose and scope
- Aimed to quantify strain-specific seroprevalence of Great Island virus (tick-borne) within a population of common guillemots.
- Part of a NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Maximum of 12 virus strains tested across the full dataset.

## Study site and sampling
- Field site: Isle of May, Firth of Forth, Scotland (56.2° N, 2.6° W) chosen for large, accessible guillemot population.
- Sample: 144 individual common guillemots captured 1993–1995; blood collected on filter paper.

## Assay methods
- Virus isolation and serology: plaque reduction neutralisation tests (PRNT) used to detect virus-specific neutralising antibodies.
- Virus strains tested include Maiden virus (MDNV), Colony B North virus (CBNV), Colony virus (COYV), Broadhaven virus (BRDV), and Above Maiden virus (AMDV); BRDV isolated from ticks at St Abbs Head, while others from Isle of May ticks.
- Procedure overview:
  - Virus prepared in Vero cells; eluted blood samples prepared in PBST.
  - Blood samples mixed with virus dilutions and incubated before adding to Vero cells.
  - Plates overlaid and incubated; plaques stained for counting.
- Two methodological variants exist:
  - MAN (Matthew/author MAN): adjusted volumes and incubation times; samples assayed four times.
  - KMW (KMW author): alternative volumes and timings; samples assayed four times.
- Controls: virus incubated in PBST or chicken blood eluted from filter paper; results expressed as average fold decrease in virus titre relative to controls.
- Replication: each bird’s sample tested in triplicate/quadruple setup depending on method.

## Data structure and variables
- BTO_Ring: unique bird identifier.
- Collection_date: date of blood collection.
- Subcolony: sampling site within the colony.
- Sex: sex of the bird.
- Status: breeding status (PB = pre-breeding, B = breeding).
- Virus_strain: strain tested (MDNV, CBNV, COYV, BRDV, AMDV).
- Sample_PFUx: number of plaque-forming units (PFU) observed in the sample or per ml.
- Sample_PFU_av: average PFU for the sample.
- Control_PFU_av: average PFU in control wells.

## Data provenance and references
- Part of dataset presented in Nunn et al. (2006) Parasitology 132: 233-240.
- Detailed methods align with Nunn et al., with explicit notes on differences between MAN and KMW parts.

## Data quality, standardization, and governance notes
- Longitudinal field data with explicit metadata (bird ID, date, site, sex, status) supports monitoring and trend analysis.
- Methodological differences (MAN vs KMW) indicate potential comparability issues; highlights the need for harmonized protocols and metadata to enable cross-study integration.
- Data are presented with explicit controls and replication, supporting QA and transparent interpretation of seroprevalence results.
- Public sharing of underlying data and detailed protocols (as evidenced by cross-reference to a published publication) aligns with data openness, though initial collection notes imply reliance on multiple investigators and potential variation in assay execution.