# Kinder Scout Rainfall and Discharge 2010-2021

- Project and scope: Rainfall and runoff records from three experimental microcatchments (0.4–0.8 ha) on Kinder Scout upland peatland, UK; data span 2010–2021; aimed at assessing the impact of peatland restoration on storm flow response. Data managed under the Protect-NFM project (NERC grant NE/R004560/1).

- Experimental design: Before-After-Control-Intervention (BACI)
  - Firmin: unrestored control
  - Olaf: restoration (revegetation)
  - Nogson: restoration with revegetation, gully blocking, and later Sphagnum plug planting
  - Intervention timing: pre-2010/2011; restoration 2011–2012; additional Nogson treatment in 2015

- Data collection and resolution:
  - Discharge and rainfall measured continuously from June 2010 to December 2021 at 10-minute intervals
  - Methods:
    - Discharge: v-notch weirs with pressure transducers behind the weirs; barometric compensation; manual stageboard readings for calibration
    - Rainfall: tip bucket rain gauges; each tip = 0.2 mm
  - Data gaps: due to instrument failure; when a rain gauge failed, rainfall data from the nearest alternate gauge were used
  - Data quality notes: periods with potential discharge overestimation (e.g., debris in the v-notch) are identified and omitted; alternate rainfall gauge used and recorded in Alt TBRG

- Data processing and conversion:
  - Discharge conversion: depth of water above the v-notch converted to discharge using a site-specific calibration equation relating head to Q
  - Depth measurements calibrated against manual readings during data downloads

- Location and site identifiers:
  - Nogson: SK 08234 89464 (discharge weir), Nogson rain gauge: SK 08236 89456
  - Olaf: SK 08262 89464 (discharge weir), Olaf rain gauge: SK 08268 89454
  - Firmin: SK 08972 89442 (discharge weir), Firmin rain gauge: SK 08970 89438

- Data structure and access:
  - Data provided per calendar year for each microcatchment in CSV format
  - File naming convention: [site]_[microcatchment]_[year]_rainfall_discharge.csv
  - Columns in each CSV (in order):
    - DateTime (GMT): YYYY-MM-DD HH:MM:SS
    - Discharge (L/sec): float64
    - Rainfall (mm): float64
    - Alt TBRG: alternative rain gauge used (if any)
    - Notes: field notes relevant to data

- Analytical methods and outputs:
  - Analytical methods: Not applicable / not specified in the dataset description
  - Outputs intended for monitoring environmental health and informing restoration impact on stormflow dynamics

- Quality control and documentation:
  - Discharge: visual checks against rainfall to identify spurious observations; omissions noted as no data
  - Rainfall: cross-check across microcatchments; substitution from alternate gauges when needed; alt gauge noted

- References:
  - Shuttleworth, E.L. et al. (2019) Rest. of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge; Journal of Hydrology X, 2, p. 100006. doi:10.1016/j.hydroa.2018.100006

- Purpose aligned with the Analysists Monitoring the Environment archetype:
  - Verifies required data from established sources, quality assures, cleans, and transforms for standardized outputs
  - Presents findings in clear, standardized formats (CSV, annual per-site files)
  - Stores and links datasets to project portals or repositories for broader access and reuse
  - Emphasizes reproducibility through BACI design and explicit data processing steps