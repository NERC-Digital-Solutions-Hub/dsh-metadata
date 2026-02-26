# Plant community basal data from a hedgerow cutting experiment in England, 2016

- This dataset records plant abundance data from a long-running hedgerow experiment, originating from an MSc project that examined how cutting regimes affect basal flora species richness.
- The data underpin a publication on hedgerow management and biodiversity, linking cutting regime to basal flora richness and Ellenberg indicator profiles.

## Aim and scope

- Investigates the effects of hedgerow cutting management regimes on:
  - Species richness of basal flora
  - Flower production, berry yield
  - Utilisation of flowers by pollinators and invertebrate abundance and structure
- Part of a larger Defra-funded program to identify practical, low-cost hedgerow restoration/restoration options suitable for large-scale implementation under agri-environment schemes (ELS and HLS).

## Experimental design

- Design: Randomised block experiment (Experiment 2) conducted across four field sites.
- Treatments: Full factorial combinations of 13 treatments derived from 2 × 2 × 3 design plus a control:
  - Time of cutting: Autumn vs. Late winter
  - Intensity of cutting: Standard vs. Incremental (bar raised progressively)
  - Frequency of cutting: Annual, Once every two years, Once every three years
  - Control: No cutting
- Replication: Three replicates of each treatment per site.
- Plot size: Hedge segments 15–20 m long.
- Duration: Treatments implemented from 2010 to 2016 (sampling data up to 2016).

## Field sites

- WO: Woburn, Buckinghamshire – hawthorn-dominated hedge (Crataegus monogyna)
- WB: Waddesdon Estate, Oxfordshire – blackthorn-dominated hedge (Prunus spinosa)
- WC: Waddesdon Estate, Oxfordshire – mixed-species hedge (Countryside Stewardship)
- YC: Yarcombe, Devon – traditional mixed-species hedge on bank
- Note: Winter-cutting treatments not applied at WB due to site limitations.

## Data collection and sampling methodology

- Plant community data collected from each hedgerow plot side.
- Sampling units: Two quadrats per plot side, each 1 m wide × 10 m long.
  - Inner quadrat: measures plants under the hedge (extending 1 m from hedge center)
  - Outer quadrat: measures plants beside the hedgerow
- Quadrats placed ~5 m from plot start to minimize edge effects.
- Vegetation recorded to 80 cm height.
- Coverage estimation: 0.1% increments for <1% cover, 1% increments for 1–4%, 5% increments for 5–100%.
- Species included: all herbaceous/woody species in quadrats, plus bare ground and plant litter.
- Quality controls: Standard protocol, trained surveyors, expert data checks, anomaly checks.

## Data structure and file details

- Primary file: HedgerowMScQuadratData.csv
- Columns include:
  - EXPERIMENT (Experiment number; 2)
  - SITE (Site code: WB, WC, WO, YC)
  - BLOCK_NO (Block number: 1–3)
  - PLOT_NO (Hedge plot number: 1–39)
  - TREATMENT (Treatment code: 1–13)
  - VISIT_DATE (Sample date; DD/MM/YYYY)
  - VISIT_YEAR (Year of sampling; e.g., 2016)
  - QUADRAT (Inner or Outer)
  - SPECIES_NAME (Species name, including bare ground and litter)
  - COVER (Percent cover)
- Data collection corresponds to Experiment 2 across four sites, with 3 replicates per treatment and plots of 15–20 m.

## Data quality and provenance

- Standardized data collection protocol and expert validation of species lists.
- Anomalies checked to ensure data integrity.
- Data sources and sampling designs described to support reproducibility and meta-analysis.
- The long-running experiment is linked to a broader Defra project (BD2114) and managed by UKCEH; the MSc project benefited from university and field support.

## References and lineage

- Carey PD et al. (2008). Countryside Survey: UK Results from 2007. NERC/CEH.
- Stanbury D., Dean H.J., Pescott O.L., Staley J.T. (2020). Hedgerow management experiment relevant to agrienvironment schemes: cutting regime impacts species richness of basal flora and Ellenberg indicator profiles. Biodiversity and Conservation (accepted).

## Funding and support

- Long-running hedgerow experiments funded by Defra (BD2114) and managed by UKCEH.
- MSc student received travel/subsistence funds; fieldwork support from UKCEH staff.