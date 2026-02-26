# Plant community basal data from a hedgerow cutting experiment in England, 2016

## Overview
- Contains vegetation abundance data from the basal area of hedgerow plots collected during an MSc project.
- Aimed to assess how hedgerow cutting regimes affect species richness of basal flora.
- Built on the experimental setup of long-running hedgerow experiments; linked publication: Stanbury et al. 2020 in Biodiversity and Conservation (accepted Apr 2020).
- Data were gathered from Experiment 2 across four field sites between 2010 and 2016; data were used to examine flower production, berry yield, pollinator visitation, and invertebrate habitat structure.

## Experimental design
- Randomised block experiment (Experiment 2) with full factorial treatments: 2 × 2 × 3.
- Treatments cover:
  - Time of cutting: early autumn vs. late winter
  - Intensity of cutting: standard (to old cut line) vs. incremental raising of cutter bar
  - Frequency of cutting: annually, every two years, or every three years
- Three replicates of each treatment at each site, with hedgerow sections 15–20 m long.
- Cutting dates span September 2010 to January/February 2016.

## Field sites
- Woburn, Buckinghamshire (WO) – hawthorn-dominated hedgerow
- Waddesdon Estate, Oxfordshire – blackthorn-dominated hedgerow (WB)
- Waddesdon Estate, Oxfordshire – mixed-species hedgerow (WC)
- Yarcombe, Devon – traditional mixed-species hedge (YC)
- Note: Winter cutting treatments not applied at WB due to hedgerow limitations; access constraints affected sampling at some blocks/sites.

## Data collection and measurements
- Plant community data collected from both sides of each hedgerow plot.
- Two 1 m × 10 m quadrats per side per plot:
  - Inner quadrat: 1 m out from hedge center (samples under the hedge)
  - Outer quadrat: adjacent to inner quadrat (samples beside the hedge)
- Quadrats placed ~5 m from plot start to minimize edge effects.
- Vegetation surveyed to 80 cm height.
- Species cover recorded as:
  - 5–100% with 5% increments
  - 1–4% as 1% increments
  - <1% treated as 0.1%
- Data quality controls included standard protocols, expert verification, and anomaly checks.
- Some sites had access constraints, affecting quadrat placement in a few blocks.

## Data file structure
- HedgerowMScQuadratData.csv
- Key columns:
  - EXPERIMENT: Experiment number (2)
  - SITE: Site code (WB, WC, WO, YC)
  - BLOCK_NO: Block number (1–3)
  - PLOT_NO: Hedge plot number (1–39)
  - TREATMENT: Treatment code (1–13; definitions correspond to the full factorial design)
  - VISIT_DATE: Sample date (DD/MM/YYYY)
  - VISIT_YEAR: Year of sampling (YYYY; 2016 in the dataset)
  - QUADRAT: Location (inner or outer)
  - SPECIES_NAME: Scientific name (includes bare ground and litter)
  - COVER: Percent cover of the species

## Quality assurance
- Standard protocol followed; field data collected by experienced surveyors.
- Expert-verified species lists and checks for anomalous values.

## Usage and potential analyses
- Enables exploration of how different cutting regimes influence basal flora communities and species richness.
- Suitable for calculating species richness and cover-based metrics, and for linking to Ellenberg indicator values (as per related published work).
- Findings contribute to assessments of hedgerow management and restoration options under agri-environment schemes.
- Data can support dashboards, self-serve analytics, or reports for practitioners and policymakers.

## References and Funding
- Caretaker references: Care y PD et al., Countryside Survey UK results (2007) for methodology context.
- Publication using the data: Stanbury D., Pescott OL, Staley JT (2020) Hedgerow management experiment relevant to agrienvironment schemes: cutting regime impacts species richness of basal flora and Ellenberg indicator profiles. Biodiversity and Conservation (accepted April 2020).
- Funding: Defra BD2114; UK Centre for Ecology & Hydrology (UKCEH); University of Reading (travel/subsistence and field support).