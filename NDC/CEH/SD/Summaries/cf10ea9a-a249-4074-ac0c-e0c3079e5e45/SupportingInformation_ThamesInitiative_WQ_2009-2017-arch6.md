# Weekly physical and chemical monitoring data for the River Thames and its tributaries (2009-2017)

- Scope and coverage
  - Weekly water quality data from seven sites along the River Thames and sixteen major tributaries.
  - Time period: March 2009 to September 2017.
  - Accompanying daily mean river flow data provided.
  - Missing data are indicated as blanks.

- Parameters measured
  - Nutrients and related measures: total phosphorus (TP), total dissolved phosphorus (TDP), soluble reactive phosphorus (SRP), dissolved reactive silicon (DSi), dissolved and total nitrogen species.
  - Major inorganic constituents: fluoride, chloride, bromide, sulphate; sodium, potassium, calcium, magnesium, boron.
  - Metals (August 2010–February 2013): iron, manganese, zinc, copper (dissolved or total as appropriate).
  - Physical/chemical indicators: water temperature, pH, Gran alkalinity, suspended solids, chlorophyll a.
  - Ammonium, dissolved organic carbon (DOC), and related measures.
  - Units and definitions: dissolved vs total forms; e.g., TP includes dissolved and acid-extractable particulate phosphorus; SRP is filterable reactive phosphorus.

- Sampling and analytical methods
  - Sampling: bulk samples from main flow usually on Monday or Tuesday each week.
  - Field measurements (2013–present): water temperature, pH, conductivity, redox potential measured in the field.
  - Filtration: subsamples filtered in the field through 0.45 μm membranes; samples stored at 4 °C in the dark.
  - Laboratory analyses (selected methods):
    - pH by pH meter with standard buffers (NIST-traceable).
    - Alkalinity by acidimetric titration to pH 4 and 3.
    - Suspended solids by filtration and gravimetric reweighing.
    - Chlorophyll a by filtration, acetone extraction, and spectrophotometry.
    - TP/TDP by digestion with acidified potassium persulphate and spectrophotometry.
    - SRP by filtration and phosphomolybdate colorimetry (modified Murphy & Riley method).
    - DSi by molybdate reaction and colorimetry.
    - Ammonium by indophenol-blue colorimetric method.
    - DOC and TDN by thermal oxidation methods (Thermalox; Elementar system from 2011).
    - Major anions by ion chromatography; major cations by acidification followed by IC-OES.
  - Quality control: analyses conducted alongside reference QC standards (Aquacheck/LC Standards).

- Data structure, formatting, and units
  - Date/time: day/month/year; sampling time: hour:minute.
  - Data fields for each parameter follow established units:
    - Temperature (°C); pH; Gran alkalinity (μeq/L); conductivity (µS/cm); redox (mV).
    - Suspended solids (mg/L); chlorophyll a (μg/L).
    - Phosphorus: SRP, TDP, TP (μg P/L or mg P/L as specified); dissolved/total phosphorus distinctions explained.
    - Nitrogen species: ammonium (mg NH4+/L); dissolved and total nitrogen (mg N/L).
    - Silicic species: dissolved silicon (mg Si/L).
    - Major ions and metals with respective units (e.g., mg/L, μg/L, etc.).
  - Flow data: mean daily flow in cubic metres per second (m³/s).
  - Site-specific details and gauging station associations provided; some sites interpolate flow from upstream data when direct station data are not available.

- Data quality, limitations, and provenance
  - Data gaps due to instrument failures, lost samples, or inaccessible sites.
  - Some metal data (Fe, Mn, Zn, Cu) available only for Aug 2010–Feb 2013.
  - Flows near/along gauging stations; exceptions include Jubilee River data gaps and interpolation for certain Thames sites.
  - Site locations and gauging relationships documented separately (CEH Thames Initiative sampling site locations).

- How the data can be used (data support perspective)
  - Build time-series dashboards combining water quality with flow data for trend analysis and event-based studies.
  - Cross-parameter analyses (nutrients vs. flow, chlorophyll vs. nutrients, metal concentrations vs. pH/alkalinity).
  - Compare across seven Thames sites and tributaries to assess spatial patterns.
  - Data integration with site location metadata for mapping and spatial analyses.
  - Develop self-serve data products and lightweight dashboards for non-expert users, with clear documentation on units and forms (dissolved vs total).

- References and methodological sources
  - Eisenreich et al. (1975); Leeks et al. (1997); Marker et al. (1980); Mullin & Riley (1955); Murphy & Riley (1962); Neal et al. (2000).
  - Supporting Information: Weekly physical and chemical monitoring data for the River Thames and its tributaries (2009–2017).