# Overview of data

- Purpose and scope
  - Dataset from the NERC Macronutrients consortium study on lateral exchange in seaward flux of C, N and P.
  - Measures oxygen fluxes (O2) in the Hampshire Avon catchment, including benthic (streambed) and water column processes.
  - Four field campaigns: spring 2013, summer 2013, autumn 2013, winter 2014; sites span six tributaries with varying land-river connectivity.
  - Accompanies a single dataset: O2fluxes_Avon.CSV.

- Data collection and methodology
  - Benthic O2 fluxes obtained with aquatic eddy covariance (AEC); methods described in Berg et al. (2003) and Attard et al. (2014), Rovelli et al. (2015).
  - Water-column O2 fluxes measured via incubation in 100 mL bottles over 24 hours with optical O2 sensors.
  - Data processed following protocols in Rovelli et al. (2015, submitted) and related references.
  - Campaign timing: spring 23/04–09/05/2013; summer 31/07–16/08/2013; autumn 29/10–11/11/2013; winter 28/01–09/02/2014.

- Spatial scope and site details
  - Six surveyed tributaries/sites in the Hampshire River Avon system:
    - CE1: River Ebble (51.027499°N, -1.9217089°E)
    - GA2: River Avon (51.318289°N, -1.8600020°E)
    - GN1: River Nadder (51.043849°N, -2.1118158°E)
    - CW2: River Wylye (51.142475°N, -2.2033140°E)
    - AS1 (aka AP): tributary of River Sem (51.055413°N, -2.1568407°E)
    - AS2 (aka AS): River Sem (51.045826°N, -2.1104425°E)
  - Depth data: average stream depth in meters, derived from flow transects at each site.

- Data structure and variables
  - Benthetic data (benthic, b):
    - Day flux (b): daytime benthic O2 flux, mmol/m2/h ± SE
    - Night flux (b): nighttime benthic O2 flux, mmol/m2/h ± SE
    - Total PAR (b): daily PAR at the streambed, mol/m2/d
    - Daylight (b): daytime length, hours; nighttime threshold 2 µmol quanta/m2/s
  - Water-column data (w):
    - Day flux (w): daytime water-column O2 flux, µmol/L/h (values < 0.1 µmol/L/h considered below detection)
    - Night flux (w): nighttime water-column O2 flux, µmol/L/h
    - Total PAR (w): daily PAR in the water column near the surface, mol/m2/d
    - Daylight (w): daytime length in water-column measurements
  - Data quality indicators and data gaps are noted using n.d. (not determined).

- Data provenance, references, and access
  - Foundational references: Attard et al. 2014; Berg et al. 2003; Rovelli et al. 2015; Rovelli et al. 2016; Rovelli et al. (2015, submitted) and related Limnology/Oceanography works.
  - Dataset accessed via the NERC Environmental Information Data Centre; DOI/URL provided in the references.
  - The overview and dataset describe and discuss the O2 flux measurements and related methodologies and results. 

- Data quality, limitations, and caveats
  - Some data excluded due to quality criteria (GA2 autumn/winter data omitted; CE1 winter sampling not conducted due to flooding).
  - Missing data due to technical issues or sampling contamination indicated as n.d.
  - Data are multi-source (field campaigns, multiple sites), which may require harmonization for GIS analyses.

- GIS-oriented use cases
  - Map-based visualization of benthic and water-column O2 fluxes across sites and seasons.
  - Spatial comparisons of fluxes with depth, PAR, and daylight duration.
  - Integration with river network layers to explore connectivity and catchment-scale metabolism patterns.
  - Potential data cleaning and standardization steps to address gaps and varying resolutions.