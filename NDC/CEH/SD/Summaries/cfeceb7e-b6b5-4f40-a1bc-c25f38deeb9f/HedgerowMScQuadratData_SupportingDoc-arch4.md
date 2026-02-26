# Plant community basal data from a hedgerow cutting experiment in England, 2016

## Overview
- Dataset of vegetation abundance (basal flora) collected from hedgerow management experiments (Experiment 2) at four sites, 2010–2016.
- Originates from an MSc project focused on how cutting regimes affect species richness and habitat resources.
- Data underpin a publication: Stanbury et al. (2020) Biodiversity and Conservation.

## Experimental design
- Randomised block experiment with full factorial treatments (2 × 2 × 3) and three replicates per treatment per site.
- Treatments cover:
  - Time of cutting: autumn vs late winter
  - Intensity of cutting: standard vs incremental (raising cutter bar over time)
  - Frequency of cutting: annual, every two years, every three years
- Four field sites:
  - WO: Woburn, hawthorn-dominated, Buckinghamshire
  - WB: Waddesdon blackthorn-dominated, Oxfordshire (winter treatments not applied due to hedge availability)
  - WC: Waddesdon mixed species hedgerow, Oxfordshire
  - YC: Yarcombe, Devon (traditional mixed hedge)
- Cutting schedules span September 2010 to January/February 2016; full factorial treatments applied to contiguous 15–20 m hedge sections.

## Data collection & sampling
- Vegetation data collected from both sides of each hedgerow plot.
- Two quadrats per side: inner (1 m wide × 10 m long) and outer (adjacent to inner), placed about 5 m from hedge start to avoid edge effects.
- Inner quadrat samples underground/under hedge; outer samples beside hedge.
- Vegetation surveyed to 80 cm height; cover recorded as:
  - 5% increments for 5–100% cover
  - 1% increments for 1–4% cover
  - 0.1% for <1% (e.g., single seedlings)
- Quality controls include a standard protocol, trained surveyors, expert data checks, and anomaly screening.

## Data structure & metadata
- File: HedgerowMScQuadratData.csv containing vegetation abundance data for hedgerow basal flora.
- Key columns:
  - EXPERIMENT (experiment number)
  - SITE (site code: WO, WB, WC, YC)
  - BLOCK_NO (block number)
  - PLOT_NO (hedge plot number)
  - TREATMENT (treatment code 1–13; definitions linked to experimental design)
  - VISIT_DATE (sample date)
  - VISIT_YEAR (year of sampling)
  - QUADRAT (inner or outer)
  - SPECIES_NAME (scientific name; includes bare ground and litter)
  - COVER (percentage cover)

## Data quality, provenance & usage
- Methodology aligned with Countryside Survey practices (Carey et al. 2008).
- Data quality controls documented: standardized protocol, qualified surveyors, expert verification, and anomaly checks.
- Funded by Defra project BD2114; UK Centre for Ecology & Hydrology managed the long-running hedgerow experiments; MSc student supported by University of Reading with field staff assistance.

## Access, publication & citations
- The dataset contributed to the publication Stanbury et al. (2020) in Biodiversity and Conservation (accepted April 2020).

## Practical considerations for data leaders
- Provides a clear provenance trail from experimental design to data capture and quality checks, enabling reuse for hedgerow management and biodiversity analyses.
- Rich metadata (site codes, treatments, visit dates, quadrat locations) supports traceability and data integration.
- Some limitations to consider in interpretation: access restrictions affected some sampling; winter cutting treatments were not applied at WB.