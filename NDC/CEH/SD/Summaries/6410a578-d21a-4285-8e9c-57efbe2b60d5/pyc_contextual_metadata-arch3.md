# Soil pyrogenic carbon (PyC) data from across the Amazon Basin

- Data overview
  - Dataset name: pyc.csv
  - Content: measurements of soil pyrogenic carbon (PyC), the ratio of PyC to bulk carbon (PyC/OC or PyC_Cbulk), and organic carbon (OC) across a soil fertility gradient in old-growth forests of the Amazon Basin.
  - Samples and plots: 395 soil samples from 49 forest plots (covering a gradient), with 37 plots previously sampled and 12 plots sampled in 2017.
  - Project and funding: part of the NERC grant "Do past fires explain current carbon dynamics of Amazonian forests?" and Brazilian CAPES/CNPq support; additional project and institutional support listed.
  - Related publications: data underpin papers on soil PyC interactions with soil, climate, and aboveground biomass; first estimates of deep PyC storage in the Amazon Basin.

- Collection methods
  - Sampling design: in plots ≥1 ha, a minimum of five locations (four corners + center); in plots <1 ha, three locations (two corners + center).
  - Depths: samples collected to 2 m depth, with intervals 0-5, 5-10, 10-20, 20-30, 30-50, 50-100, 100-150, 150-200 cm; composites created per depth interval per plot.
  - Tools: soil auger used for collection.

- Data analysis
  - Laboratory methods: samples air-dried, sieved, and analyzed for PyC, TOC, and non-PyC fraction of OC at James Cook University.
  - PyC quantification: hydrogen pyrolysis (HyPy) method used to quantify PyC relative to TOC.

- Nature and Units of recorded values
  - Cpyc and OC: reported as percentage of the sample.
  - Cpyc_Cbulk: ratio of PyC to bulk carbon, expressed as a percentage.

- Quality control
  - PyC percentage corrected for black carbon bias using Equation 2 from Wurster et al. (2012).
  - Failed runs or non-convergent results discarded and not included in the dataset.

- Details of data structure
  - File: pyc.csv (comma-separated values).
  - Columns:
    - Plot_number: plot code
    - Latitude, Longitude: geographic coordinates
    - depth_range: depth interval of sampling
    - Cpyc: PyC concentration (%)
    - Cpyc_Cbulk: PyC to bulk carbon ratio (%)
    - OC: organic carbon concentration (%)
    - forests_status: forest type (old-growth or disturbed)
    - Rep: number of repetitions for the same plot/depth

- Relevance for monitoring and policy (for the monitoring-framework archetype)
  - Provides standardized, geo-referenced soil PyC data suitable for monitoring soil carbon dynamics and the legacy effects of fire in Amazon forests.
  - Documented methods (HyPy) and depth-resolved sampling enable reproducibility and comparability across studies and time.
  - Clear data governance through metadata (locations, depth ranges, sample counts) and quality control steps enhance data reliability for policy evaluation and environmental health dashboards.
  - Data provenance reflects multiple funders and collaborations, illustrating transparent data sharing and traceability valuable for governance and accountability in monitoring programs.

- References
  - Ascough et al. (2009); Quesada et al. (2010); Wurster et al. (2012); de Oliveira et al. (2022); Koele et al. (2017).