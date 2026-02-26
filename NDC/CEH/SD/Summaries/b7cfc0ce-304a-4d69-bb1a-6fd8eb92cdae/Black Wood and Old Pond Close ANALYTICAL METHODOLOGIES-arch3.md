# Rainfall catch

- Overview
  - A multi-component environmental monitoring dataset covering rainfall catch, throughfall catch, stemflow catch, and a broad suite of dissolved constituents in collected waters.
  - Timeframe: 1990-05-23 to 1992-04-06.
  - Laboratories/sites: Wallingford (Rainfall/Throughfall), Field (Stemflow); Wallingford is the primary analytical lab.
  - Aims aligned with environmental health monitoring and policy scrutiny, emphasizing rich metadata, data quality, and governance.

- Data components and scope
  - Rainfall catch, Throughfall catch, Stemflow catch
    - Rainfall catch: units in mls; gravimetric method; LAB: Wallingford; FILTRATION: Unfiltered; PRESERVATION: Non; START/END defined.
    - Throughfall catch: units in mls; gravimetric method; LAB: Wallingford; FILTRATION: Unfiltered; PRESERVATION: Non; START/END defined.
    - Stemflow catch: units in mls; volumetric method; LAB: Field; PRESERVATION: Non; START/END defined.
  - Dissolved constituents (example analytes: Al, B, Ba, Ca, Cl, Cu, F, Fe, Mn, Na, NH4, NO3, Si, SO4, Sr, Zn, K, Mg, SRP, pH, etc.)
    - Each analyte includes: UNITS, LQDC, START/END, LAB, FILTRATION, PRESERVATION, METHOD, plus multiple value fields (many placeholders like ".").
    - Analytical methods represented include ICP-OES, AAS, ion chromatography, automated colorimetry, and radiometer pH measurements.
    - Filtration and preservation practices typical of environmental chemistry (filters such as 47 mm 0.45 µm, GF/C; preservation often via acidification or cooling).

- Methods and analytical approach
  - Field sampling
    - Rainfall, throughfall, and stemflow collected with specified filtration and handling protocols.
    - Filtration schemes include standard membranes and glass fibre filters; preservation strategies include acidification and cooling.
  - Laboratory analyses
    - Metals/metalloids (e.g., Al, Fe, Mn, Cu, Zn, Ca, Na, K, Mg, Ba, Sr) via ICP-OES or equivalent.
    - Major ions and nutrients (NO3, NH4, Cl, SO4, etc.) via ion chromatography or colorimetric methods.
    - pH measured with radiometer pH meter.
    - SRP measured by standard chromatographic techniques.
  - Metadata schema
    - Each analyte is accompanied by START/END dates, LAB, FILTRATION, PRESERVATION, and METHOD; explicit units provided.
    - Many measurement fields are placeholders (".") indicating missing data.
  - QA/QC
    - Documented accuracy assessment for ICP-OES determinations using materials from the Aquacheck LGC Interlaboratory Proficiency Testing Scheme.

- Metadata quality and data governance signals
  - Strengths
    - Rich, analyte-specific metadata enabling reproducibility and QA assessment.
    - Clear, standard sample handling and laboratory methods documented.
  - Gaps and barriers
    - Numerous result fields are placeholders (".") or blank, signaling incomplete reporting.
    - Some metadata values (e.g., LQDC, filtration details) may be missing or inconsistently reported.
  - Data sharing and openness implications
    - Demonstrates the need for sharing underlying data with governance, but incomplete reporting and inconsistent completion hinder immediate reuse.
    - Governance considerations include ensuring consistent preservation, storage, and versioning across sites/labs.

- Practical implications for authors of Monitoring Frameworks
  - Use as a model for integrating analyte-level metadata with measurement results to support policy evaluation.
  - Address data-availability challenges evidenced here:
    - Strive to minimize "." placeholders and ensure complete reporting of all fields.
    - Standardize QA/QC procedures and detection limits (LQDC) across analytes.
    - Harmonize filtration, preservation, and extraction methods to reduce heterogeneity.
  - Governance and openness
    - Develop clear data-sharing protocols balancing openness with data integrity and privacy.
    - Establish source-level data management standards across collection, filtration, preservation, and lab analysis to avoid silos and enable timely access.
  - Data utilization for policy
    - Ensure coverage of broad environmental health indicators (input water, runoff pathways, and dissolved chemistry) to support policy evaluation and scenario analysis.
    - Create dashboards/reports translating multi-parameter data into policy-relevant metrics (e.g., nutrient loading, contaminant trends, dilution effects).

- Enduring takeaways
  - The dataset exemplifies a comprehensive monitoring framework that blends physical hydrology (rainfall, throughfall, stemflow) with extensive chemical characterization.
  - Highlights the necessity of complete metadata, consistent analytical methods, and robust data governance to translate raw monitoring into policy-relevant insights.
  - Actionable improvements for Monitoring Framework authors include filling data gaps, unifying metadata standards, reducing silos, and implementing transparent data governance and sharing practices.