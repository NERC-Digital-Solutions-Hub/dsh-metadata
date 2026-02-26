# Hydroscape chlorophyll abs data

## Purpose and scope
- A standardised dataset documenting chlorophyll absorbance from phytoplankton and periphyton across multiple lakes, tarns, and Broad waters.
- Supports monitoring environmental health and policy performance over time by providing consistent, comparable measurements.

## Data collection methods
- Phytoplankton samples collected as surface dip water samples at the deepest point of each lake or waterbody (e.g., Bassenthwaite Lake, Derwentwater, Grasmere, Esthwaite Water, Wroxham Broad, etc.).
- Sampling used a long-handled pole to access deep points; additional river samples collected from banks.
- Periphyton samples (PERI) obtained from nutrient-diffusing periphytometers deployed in streams for two weeks; filters retrieved and frozen post-deployment.
- Water samples for PHYT bioassays kept cool and dark; incubation started within hours of sampling (with a subset of Norfolk samples started later).
- All samples filtered through an initial filter to remove grazers and debris; aliquots prepared for nutrient-enrichment treatments.

## Bioassay and measurement details
- Treatments for PHYT and PERI include controls and nutrient amendments: phosphorus, nitrogen (nitrate, ammonium), silica, and combinations (e.g., N+P).
- Incubations conducted for several days at approximately 20°C.
- Post-incubation, contents resuspended, filtered onto GF/C filters, and frozen for analysis.
- Chlorophyll a quantified by absorbance measured at multiple wavelengths: 632 nm, 652 nm, 665 nm, 696 nm, and 750 nm.
- Dilution factors recorded to indicate sample dilution.

## Data processing and quality control
- Three replicates per treatment to ensure reliability.
- Baseline wavelength scans performed on the spectrophotometer with methanol as reference; instrument auto-zero and blanks applied to correct absorbance values.
- Data include a Known_issues flag to flag any data quality concerns.

## Data structure and metadata
- Core fields (16 columns) include:
  - System, Site, Algae (PHYT or PERI), Deployment (seasonal order 1–4; 0 for a trial deployment in Esthwaite Water)
  - DateStart, DateStop
  - Vol_or_Area, DataFlag (quality indicator; 1 = issues present, 0 = no issues)
  - DOSE (nutrient treatment code; 0 = initial, 1 = control, 2 = P, 3 = Nitrate, 4 = N+P, 5 = Ammonium, 6 = Silica)
  - REPLICATION (A–C, with Esthwaite deployment 0 using A–D)
  - 632nm, 652nm, 665nm, 696nm, 750nm (absorbance readings)
  - Dilution_factor (1 = no dilution, 2 = 50% dilution)
- A separate table provides site names with precise Eastings and Northings coordinates for each location.

## Site locations
- Extensive list of sites and coordinates, including Bassenthwaite_Lake, Bishop_Loch, Castle_Semple_Loch, Church_Bend, Codale_Tarn, Decoy_Broad, Derwentwater, Esthwaite_Water, Grasmere, Loch_Libo, Ranworth_Broad, Rydal_Water, Strathclyde_Loch, Swan_Bend, Wroxham_Broad, Woodend_Loch, and others.

## Relevance to environment monitoring
- Delivers a uniform, auditable dataset enabling time-series analyses of algal responses to nutrient conditions across multiple water bodies.
- Supports cross-site comparisons and policy evaluation using standardized measurements and QA procedures.
- Data storage and accessibility align with the aim to store datasets and provide access through appropriate portals.

## Challenges and opportunities
- Increasing the value of datasets by integrating with other environmental data sources for broader context.
- Enhancing access to underlying data to improve transparency and secondary analyses by stakeholders.