# Overview of data

- Purpose and scope
  - Compilation of results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer (Queen Mary University of London).
  - Focus on lateral exchange in the seaward flux of C, N and P; field data on oxygen fluxes in streams of the Hampshire Avon catchment.
  - Dataset accompanies one file: O2fluxes_Avon.CSV.

- Methods and measurement approaches
  - Benthic O2 fluxes measured with aquatic eddy covariance (AEC); processing followed Attard et al. (2014) and Rovelli et al. (2015).
  - Water-column O2 fluxes measured by 24-h bottle incubations (100 mL) with optical O2 sensors.
  - PAR and daylight data collected at the streambed (benthic) and near the water surface (water column).

- Campaigns, sites, and timing
  - Four field campaigns spanning spring 2013, summer 2013, autumn 2013, and winter 2014.
  - Six tributaries/sites in the Hampshire River Avon catchment: CE1 (Ebble), GA2 (Avon), GN1 (Nadder), CW2 (Wylye), AS1 (Sem tributary), AS2 (Sem).
  - Some caveats: CE1 not sampled in winter; GA2 data from autumn/winter and winter were omitted due to quality concerns.

- Data structure and key variables
  - Columns include:
    - Campaign: season of data collection.
    - Site: site identifier within each campaign.
    - Depth: average stream depth (m) from flow transects.
    - Day flux (b): daytime benthic O2 flux (mmol/m2/h) with SE; sample size in parentheses.
    - Night flux (b): nighttime benthic O2 flux (mmol/m2/h) with SE.
    - Total PAR (b): 24h integrated PAR at the streambed (mol/m2/d).
    - Daylight (b): daytime duration (h) at the streambed; nighttime threshold set at 2 µmol quanta/m2/s.
    - Day flux (w): daytime water-column O2 flux (µmol/L/h) with sample size; values below detection marked <0.1.
    - Night flux (w): nighttime water-column O2 flux (µmol/L/h) with sample size; values below detection marked <0.1.
    - Total PAR (w): 24h integrated PAR in the water column near the surface (mol/m2/d).
    - Daylight (w): daytime duration (h) measured in the water column near the surface.
  - Data quality notes: some data marked as nd (not determined) due to technical issues or sampling contamination.

- Data quality, limitations, and access
  - Some datasets (GA2 autumn/winter, CE1 winter) omitted due to quality issues.
  - Data for AS2, CW2, GN1 discussed in Rovelli et al. (submitted).
  - Data may contain gaps (nd) and variability in sampling across campaigns and sites.
  - The dataset is designed for cross-site, seasonal comparisons of benthic and water-column metabolism and their relation to light (PAR) and depth.

- References and provenance
  - Methodological and processing references include Berg et al. (2003); Attard et al. (2014); Rovelli et al. (2015, 2016).
  - Additional related work: Rovelli et al. (2016) on reach-scale river metabolism and light/hydrology interactions; Rovelli et al. (submitted) on AS2, CW2, GN1.
  - The dataset is archived with accompanying metadata and a DOI/link: https://doi.org/10.5285/16df35a9-90ab-4273-8b6c-5ef3648ec76d.