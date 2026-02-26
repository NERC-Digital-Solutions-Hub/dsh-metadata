# Weekly physical and chemical monitoring data for the River Thames and its tributaries (2009-2017) - Supporting Information

- Overview
  - Dataset of weekly water quality monitoring at seven sites along the River Thames and sixteen major tributaries from March 2009 to September 2017.
  - Parameters cover nutrients (phosphorus species, nitrogen species), silicon, temperature, pH, alkalinity, suspended solids, chlorophyll, major dissolved anions and cations, and dissolved metals (restricted to August 2010–February 2013).
  - Includes accompanying daily mean river flow data. Data collected as part of the UK Centre for Ecology & Hydrology’s Thames Initiative monitoring programme.
  - Missing data are represented as blanks.

- Dataset contents and parameters
  - Physical and chemical measurements:
    - Temperature, pH, conductivity, redox potential, Gran alkalinity, suspended solids, chlorophyll a.
  - Nutrients:
    - Total phosphorus (TP), total dissolved phosphorus (TDP), soluble reactive phosphorus (SRP).
    - Dissolved reactive silicon, ammonium, dissolved organic carbon, total dissolved nitrogen.
  - Major dissolved anions: fluoride, chloride, bromide, nitrite, nitrate, sulphate.
  - Major dissolved cations: sodium, potassium, calcium, magnesium, boron.
  - Total dissolved and total metal concentrations: iron, manganese, zinc, copper (limited to 2010–2013 for dissolved/total forms).
  - Flow: mean daily river discharge (m3/s) accompanying the chemical data.
  - Units are specified for each parameter (e.g., μg P/L for phosphorus, mg/L for nitrate, mg/L for ammonium, mg/L or μg/L for metals, etc.).

- Sampling and analytical methodology
  - Sampling schedule: bulk samples collected weekly (Monday or Tuesday) from the main flow of each river site.
  - Field measurements (2013–present): water temperature, pH, conductivity, redox potential using a Myron Ultrameter.
  - Sample processing: subsamples filtered in the field through 0.45 μm membranes; samples stored at 4°C in darkness before analysis.
  - Laboratory analyses (selected methods and instruments):
    - pH: Radiometer PHM210, calibrated with pH 4, 7, 10 buffers (NIST-traceable).
    - Alkalinity: acidimetric titration to pH 4 and 3 with 0.5N H2SO4.
    - Suspended solids: mass via filtration, drying, and reweighing.
    - Chlorophyll a: extraction in acetone, colorimetric spectrophotometry (Beckman 750 DU) per Marker et al. method.
    - TP/TDP: digestion with acidified potassium persulphate, colorimetry (molybdenum-blue) at 880 nm.
    - SRP: filtration and phosphomolybdate blue colorimetry (Murphy & Riley, modified by Neal et al.).
    - Silica: molybdo-silicic acid formation, reduced to silicomolybdenum blue, quantified spectrophotometrically.
    - Ammonium: indophenol-blue colorimetric method.
    - DOC/TDN: Thermal oxidation (Thermalox) (until 2010) and Elementar Vario Cube (from 2011).
    - Major anions/cations: ion chromatography (Dionex AS50 or equivalent) after appropriate sample preparation.
    - Total and dissolved metals (Fe, Mn, Zn, Cu): IC-OES after appropriate sample preparation (acidification for total metals, filtration for dissolved metals).
  - Quality assurance: analyses performed with reference Aquacheck QC standards (LGC Standards); SRP analyses completed within 48 hours to minimize instability.

- Data structure and site information
  - Time data: date in day/month/year format; sampling time given as hour:minute.
  - Flow data: mean daily flow (m3/s) aligned with chemical measurements; some sites have interpolated or upstream gauging data due to data gaps.
  - Site-specific notes:
    - Jubilee River data not available.
    - Hannington Wick, Wallingford, and Sonning flows interpolated based on catchment area using other gauging data along the Thames.
    - Cut, Colne at Staines and River Kennet sites have gauging data upstream of the monitoring site.
  - Site locations and gauging stations are documented in the CEH Thames Initiative Sampling Site Locations document.

- Data quality, limitations, and accessibility
  - Gaps and missing data are present (recorded as blanks).
  - Instrumentation and method changes over time (e.g., DOC/TDN instrumentation shift in 2010–2011) may affect comparability.
  - Some measurements (e.g., metals) are limited to specific time windows (2010–2013 for dissolved/total metals).
  - Flows at several sites required interpolation due to unavailable nearest gauging stations.
  - Data provenance: collected under the UK Centre for Ecology & Hydrology Thames Initiative; detailed methodology and site information provided, with references for analytical methods.

- References and supporting information
  - References to analytical methods and standard protocols (e.g., Eisenreich et al. 1975; Leeks et al. 1997; Marker et al. 1980; Mullin & Riley 1955; Murphy & Riley 1962; Neal et al. 2000).
  - Supporting Information: Weekly physical and chemical monitoring data for the River Thames and its tributaries (2009–2017) with methodological details.

- Implications for data management and strategy (for Data Leaders)
  - Comprehensive, multi-parameter water quality and flow dataset suitable for long-term trend analysis and cross-site comparisons.
  - Requires careful metadata governance to track method changes, site-specific data gaps, and interpolation steps for flows.
  - Opportunity to harmonize with other datasets through standardized units, consistent time stamps, and documented QA/QC procedures.
  - Useful for gap analysis, data quality assessments, and informing data product development for governance and policy-facing outputs.