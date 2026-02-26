# Measurements of microarthropod community structure and diversity from an upland grassland experimental site [NERC Soil Biodiversity Programme]

## Overview
- Context: NERC Soil Biodiversity Thematic Programme (started 1999) conducted at Sourhope, Scotland, to understand soil biodiversity and the functional roles of soil biota; 24 projects studied soil structure, processes (C and N cycles), and microfauna/mesofauna.
- Primary data focus: Microarthropod community structure and diversity, with accompanying soil and plant measurements to relate below-ground diversity to soil fertility manipulations.
- Data producers: Researchers from multiple institutions, including the NERC programme team and the Lancaster University Soil Ecology Group.

## Data Coverage and Scope
- Measured components:
  - Microarthropods: abundance and species composition (mites, Collembola) from soil cores.
  - Soil/root context: microbial biomass carbon, soil respiration, soil pH (measured in water), loss on ignition (organic matter), dry root biomass, total soil and root carbon and nitrogen, soil moisture.
  - Above-ground productivity: annual above-ground biomass (net primary productivity, ANPP) estimates.
- Experimental treatments: five replicate blocks with plots assigned to Control, Nitrogen (N) fertiliser, Lime (CaCO3), and Nitrogen + Lime; N and Lime applied in 1999 and 2000.
- Data timeliness: Sampling occurred over four core sampling occasions (Nov 1999, Feb 2000, May 2000, Aug 2000), with Aug 2000 including additional paired cores for some measurements.
- Data structure: Four CSV datasets (see Data Files and Variables) with detailed metadata describing sampling units, plots, treatments, and depths.

## Site Description and Experimental Design
- Location: Sourhope Field Experiment site, Cheviot Hills, south-east Scotland (55°28'30''N, 2°14'W), ~350 m altitude.
- Climate/soil: Semi-improved upland grassland; humic brown Sourhope soil; annual rainfall ~1117 mm; typical plant species include Agrostis capillaris, Festuca ovina, Poa pratensis, Anthoxanthum odoratum.
- Design: Five blocks downslope; each block contains six plots (12 m x 20 m) with randomized treatments.
- Sampling regime: Soil cores collected to 10 cm depth; N and lime treatments applied at specified times; site mowed five times per growing season with cut biomass removed.
- Core processing: Berlese-Tullgren extraction for microarthropods; samples stored in ethanol with glycerol; identification and counting of mites and Collembola; diversity indices calculated (Shannon-Wiener H, evenness J, cumulative richness R); biomass estimates derived from published conversion factors.

## Data Files and Variables (Datasets 1040–1043)
- Dataset 1040: Plant species data (P2133_FIELD_BOTANICAL_PERCENT.csv)
  - Variables include Sampling Unit ID (SUID), Sampling Date, Block/Main Plot/Sub Plot, Cell coordinates, Treatment, Sample Type, Surface Area, and Plant Species.
  - Purpose: Plant community context associated with each soil core.
- Dataset 1041: Field microarthropod population density data (P2133_FIELD_MPOD_NUMBERS.csv)
  - Variables include SUID, sampling date, block/main plot/sub-plot, cell coordinates, treatment, sample type, surface area, and counts for mites and Collembola per core (5 cm depth).
- Dataset 1042: Field microarthropod species abundance data (P2133_FIELD_MPOD_SPECIES.csv)
  - Variables include SUID, sampling date, block/main plot/sub-plot, cell coordinates, treatment, sample type, surface area, species name, and counts.
- Dataset 1043: Field soils data (P2133_FIELD_SOILS.csv)
  - Variables include SUID, sampling date, block/main plot/sub-plot, cell coordinates, treatment, sample type, surface area, and measurements such as microbial biomass carbon, respiration, pH, LOI, root biomass, soil/root carbon and nitrogen, soil moisture, and related metadata.
- Common methodological details:
  - Depth: cores to 5 cm or 10 cm depending on dataset.
  - Analytical methods: microbial biomass via fumigation-extraction (Vance et al. 1987), respiration via headspace CO2 measurement, carbon/nitrogen via automated analyzers, LOI at 460°C, pH by wet method, root and soil C/N by dry combustion, moisture by standard gravimetric methods.
  - Units and data quality: detailed field and unit descriptions provided; data include range checks and formatting checks as part of quality control.

## Data Processing and Analysis Methods
- Diversity and structure: Calculated for microarthropods as a group (mites + Collembola) and for subgroups; indices include Shannon-Wiener H, evenness J, and cumulative richness R.
- Functional diversity: Indices computed separately for predatory vs. non-predatory mites.
- Biomass: Microarthropod biomass estimated from published conversion factors.
- Soil/root chemistry: Total C and N for soil and roots measured; soil microbial biomass C derived from fumigation-extraction; microbial activity via basal respiration.
- Plant productivity: ANPP estimated from multiple quadrats across mowing dates to infer above-ground productivity.

## Quality Assurance and Data Governance
- Quality control: Numeric range checks, data format checks, and logical integrity checks implemented.
- Uncertainty and liability: Data are QA'd but not warranted for accuracy; user bears risks; no liability accepted by NERC Soil Biodiversity Programme for outcomes from data use.
- Documentation and provenance: References to field data handbook and related literature provided (e.g., Scott et al. 2003; Begon et al.; Hopkin; Jenkinson; Krantz; Luxton; Petersen).
- Data discovery and reuse: Datasets are catalogued (with project code P2133) and linked to related publications; metadata describes sampling regimes, plots, treatments, and analytical methods to support discovery and reuse.

## Access, Use, and Stewardship Considerations
- Stewardship focus: High level of metadata detail supports data discoverability, interoperability, and reuse, aligning with data governance practices (clear sampling units, plot design, treatments, depth, and methodological notes).
- Data preservation: Data are stored with a standardized structure across datasets and include a data handbook and external references; potential for integration with data portals and cross-study analyses.
- Recommendations for data stewards:
  - Maintain consistent metadata schemas across datasets and ensure explicit unit definitions and depth conventions.
  - Preserve project-specific identifiers (SUID, block/main plot/sub-plot, cell) to enable cross-dataset joins.
  - Provide clear provenance and linking to related publications and data handbooks (e.g., Sourhope Field Data Handbook).
  - Monitor for updates or new sampling rounds and version datasets accordingly.
  - Ensure licensing and access terms are explicit when publishing to data portals; include disclaimers and data-use guidance.

## References
- Allen, S.E. 1989; Begon, Harper, Townsend 1996; Buckland, Bardgett, etc. 2005; Hopkin 2000; Jenkinson & Powlson 1976; Jenkinson 1987; Krantz 1978; Luxton 1975; Petersen 1975; Vance, Brookes, Jenkinson 1987; Sourhope Field Data Handbook (2003); Applied Soil Ecology papers (2003, 2006).