# Data Collection

## Overview
- Part of a NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Field site: Isle of May, Firth of Forth, Scotland, chosen for its large common guillemot population.
- Aim: quantify strain-specific seroprevalence of Great Island virus within the guillemot population.
- Full dataset includes up to 12 Great Island virus strains tested; 144 guillemots captured (1993–1995) with blood samples collected on filter paper.
- Plaque reduction neutralisation tests (PRNT) performed to detect virus-specific neutralising antibodies.
- Part of dataset reported in Nunn et al. (2006); methodological differences between two parts of the dataset are noted as MAN and KMW.

## Methods (Laboratory)
- Virus isolation: clarified tick homogenate applied to BHK21 cells; two rounds of plaque picking on Vero cells.
- BRDV (Broadhaven virus) isolated from a tick pool (10 nymphal ticks) from St Abbs Head; other strains from Isle of May.
- Sample preparation: filter paper blood spots eluted in PBST (phosphate-buffered saline with Tween 20 and antibiotics) at 4 °C.
- PRNT assay: eluted samples mixed with virus dilutions and incubated before applying to Vero cell wells; plaques counted after incubation and staining.
- Results expressed as average fold decrease in virus titre relative to controls (PBST-only and chicken blood eluates).
- Controls and replication: multiple control wells and repeated assays per sample; MAN and KMW denote slight methodological differences between parts of the dataset.

## Data and Metadata
- Data fields and structure:
  - BTO_Ring: unique bird identifier.
  - Collection_date: date of blood sample collection.
  - Subcolony: site of capture.
  - Sex: sex of the bird.
  - Status: pre-breeding (PB) or breeding (B).
  - Virus_strain: tested strains (MDNV, CBNV, COYV, BRDV, AMDV, etc.).
  - Sample_PFUx: plaque-forming units per well or per ml in the test sample.
  - Sample_PFU_av: mean PFU value for the sample.
  - Control_PFU_av: mean PFU value in control wells.
- Scope: up to 12 strains tested per bird; 144 birds sampled across 1993–1995.

## Field Site and Timeline
- Location: Isle of May, Scotland (56.2° N, 2.6° W).
- Field sampling period: 1993–1995.
- Sample type: blood collected on filter paper for serological testing.

## Data Management and Monitoring Implications
- Standardised laboratory methods (PRNT) and clearly defined data formats support consistent environmental health monitoring and cross-study comparability.
- Data are organized for storage and upload to appropriate data portals, aligning with best practices for dataset accessibility.
- Noted methodological differences (MAN vs. KMW) highlight the importance of harmonisation when integrating multiple parts of a dataset to maximize data value and usability.

## Relevance for Environmental Monitoring
- Enables assessment of seroprevalence of a tick-borne virus in a wild seabird population over time and by virus strain.
- Provides metadata (location, timing, host status, subcolony, sex) useful for exploring associations between host factors and pathogen exposure.
- Supports broader analyses of pathogen dynamics in ecological systems and informs monitoring of environmental health and wildlife disease risk.