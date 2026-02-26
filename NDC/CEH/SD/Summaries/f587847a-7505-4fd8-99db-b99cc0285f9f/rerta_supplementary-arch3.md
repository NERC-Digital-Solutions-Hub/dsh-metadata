# Nitrous oxide and methane fluxes from different riparian restoration treatments in Oil Palm plantations in Riau, Indonesia 2019-2021

## Overview
- Investigates N2O and CH4 (and CO2) emissions from four riparian buffer treatments in oil palm plantations, to inform growers and policy makers about environmental impact of riparian management.
- Context: riparian buffers can improve water quality and biodiversity; limited knowledge on their influence on greenhouse gas emissions.
- Part of the Riparian Ecosystem Restoration in Tropical Agriculture (RERTA) project within BEFTA; aims to guide management practices and legislative riparian requirements.

## Experimental Design
- Two RERTA sites: Kandista estate (2016) and Ujung Tanjung estate (2019); greenhouse gas study conducted at Ujung Tanjung only.
- Four treatments in 50 x 400 m riverbank zones:
  1) Immature oil palm – no restoration, replanting to river margin
  2) Mature oil palm – no restoration, 50 m buffer of mature palms
  3) Native trees – enrichment planting with forest trees in a 50 m buffer, removal of all mature oil palm
  4) Mature oil palm and native trees – enrichment planting with forest trees and maintenance of mature oil palm
- 40 static chambers distributed across treatments and surrounding plantation (six replicates per treatment, 16 in plantation).

## Field Collection Methods and Laboratory Instrumentation
- Chamber setup: 40 cm diameter collars inserted ~7 cm deep; seals achieved with a lid and draft excluder.
- Sampling: 100 mL samples drawn at 0, 15, 30, and 45 minutes; analyzed for CH4, CO2, N2O at UKCEH Edinburgh using GC with μECD (N2O) and FID (CH4, CO2).
- Soil moisture measured at sampling with a Theta probe at three points around each chamber.
- Permits: Foreign Research Permit Division, MoRT/NRI; two permits issued for the project years 2019 and 2020.

## Analytical Methods and Quality Control
- Gas concentrations quantified by GC, calibrated with a four-point mixed gas standard.
- Fluxes calculated with RCFlux R package, using six regression models; best-fit model selected per chamber.
- Fluxes expressed as micromoles per square meter per second; each flux has a 95% confidence interval.
- Quality control: visual review of regression plots; data marked as valid/invalid; outliers treated cautiously due to soil microbiome variability.
- Data products include multiple flux estimates per chamber (linear, quadratic, HMR, asymptotic, best-fit) and associated statistics (R^2, adj. R^2, 95% CIs).

## Data Structure and Outputs
- rerta_ghg_rcflux.csv: fluxes for each chamber, sampling occasion; includes gas type, multiple flux estimates (six methods) and best-fit method, year, month, day, chamber, treatment, location, soil moisture, and other metadata.
- rerta_chambers.csv: details for the 40 chambers (code, position, plot, treatment_zone, treatment, installation date, location coordinates, chamber dimensions, etc.).
- Columns documented with units and descriptions; NA entries indicate non-applicable fields.

## Data Management and Governance
- Data generated under international collaboration; specific chamber and sampling metadata included to enable reproducibility and re-use.
- Calibration, model choices, and quality control are documented to support transparency and auditability.
- Underlying data sharing is acknowledged as a potential barrier in broader monitoring contexts, due to governance and openness considerations.

## Relevance to Monitoring Frameworks
- Demonstrates a structured, multi-model flux estimation approach with explicit metadata, calibration, and QA/QC steps suitable for monitoring frameworks.
- Highlights challenges common in environmental monitoring: data gaps, access to high-quality metadata, data transformation needs, and governance around data sharing.
- Provides a reproducible workflow for assessing riparian restoration impacts on greenhouse gas fluxes, informing policy decisions and best-practice guidelines for riparian management in oil palm landscapes.