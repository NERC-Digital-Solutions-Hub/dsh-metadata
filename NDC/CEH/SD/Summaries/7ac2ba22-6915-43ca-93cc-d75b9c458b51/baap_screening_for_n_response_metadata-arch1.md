# BAAP Screen Aberdeen: Data on trait values for 229 rice cultivars under 0%N and 100%N treatments

## Overview
- Two CSV data sheets containing trait measurements for 229 rice cultivars grown for 6 weeks under two nitrogen (N) levels: 0N (no added nitrogen) and 100N (urea-fed) treatments.
- Traits recorded per plant: plant height (cm), number of tillers, nitrogen balance index (NBI), chlorophyll content (ChI), and shoot biomass (g, dry weight).
- Data scope: raw values for each plant; 0N and 100N datasets provided separately.
- Location and timing: School of Biological Sciences, University of Aberdeen, UK; September–October 2020.
- Personnel and supervision: Yehia Hazzazi, Aadil Tantray; supervised by Adam Price and Gareth Norton.
- Context: BAAP (Bengal and Assam Association Panel) rice cultivars with an associated SNP database (~2 million markers); linked to prior work on GWAS for biomass traits.

## Experimental design and materials
- Genetic material: 229 BAAP rice cultivars (aligned with Norton et al., 2018), grown in a controlled environment.
- Experimental unit and replication: four replicates per treatment in a paired 0%N vs 100%N box design; seeds sown in a 23 x 10 grid, two seeds per genotype, thinned to one plant; four replicates per treatment pair.
- Growth medium: equal-volume soil mix of Insch soil and builder’s sand; boxes sized 160 cm x 70 cm x 27 cm; about 600 kg soil/sand per box.
- Replication note: replicate 1 of the 100N treatment was removed from analysis due to a leak causing a different soil/water environment.
- Randomization: within each box, 230 genotypes sown randomly; four replicates for each treatment paired as one 0%N and one 100%N box.

## Treatments and environment
- Treatments:
  - 0%N: no added nitrogen during the experiment.
  - 100%N: 16.12 g of urea per box, representing 40 kg N ha-1 in the first split of a typical field application ( Bangladesh reference), with three splits planned for 120 kg N ha-1 in total.
- Nutrient management: first two weeks the soil remained moist and aerobic; after two weeks, flooding was introduced to ~5 cm above soil level.
- Controlled environment conditions: day/night temperatures of 28°C/25°C (±1°C); 12-hour photoperiod; approximately 400 μmol m-2 s-1 PAR; relative humidity >50%.

## Measurements and harvest
- Start of measurements: from two weeks after sowing.
- Traits measured weekly:
  - Plant height (cm) from soil to tip of longest leaf.
  - Tillers per plant (count).
  - Nitrogen Balance Index (NBI) via Dualex (no unit).
  - Chlorophyll content (ChI) via Dualex (no unit).
- Harvest: at six weeks; shoots dried at 80°C for 48 hours; shoot dry weight recorded (g).

## Data structure and variables
- Data files contain 11 columns:
  - Columns A–F: Replicate, Treatment, BAAP number (unique ID), BAAP name (cultivar), X (position in X), Y (position in Y).
  - Columns G–K: measured traits—Plant_height (cm), Tiller_number (count), NBI (unitless), Chl (unitless), Shoot_biomass (g).

## Quality control
- One 100N replicate removed due to experimental inconsistency (leak in pond liner).
- Initial data entry checked with Minitab for unusual observations; corrections made only for data-entry errors.

## Data files and key statistics
- BAAP_Screen_Aberdeen_0N.csv: raw data for zero-nitrogen treatment; five traits reported with summary means:
  - Plant_height: 74.1 cm
  - Tiller_number: 2.09
  - NBI: 17.0
  - Chl: 12.2
  - Shoot_biomass: 0.70 g
- BAAP_Screen_Aberdeen_100N.csv: raw data for 100% nitrogen treatment; five traits reported with summary means:
  - Plant_height: 77.4 cm
  - Tiller_number: 2.69
  - NBI: 34.0
  - Chl: 26.2
  - Shoot_biomass: 0.96 g

## Context, usage, and references
- Related data resource: BAAP genetic panel with ~2 million SNP markers accessible for association analyses.
- Primary reference: Norton GJ, et al. 2018. Genome-wide association mapping of grain and straw biomass traits in the rice Bengal and Assam Aus Panel (BAAP). Frontiers in Plant Science, 9:1223.
- Funding and support: UK-funded GCRF South Asia Nitrogen Hub; YH scholarship (Saudi Arabian government); AT SERB Overseas Visiting Doctoral Fellowship (Government of India).