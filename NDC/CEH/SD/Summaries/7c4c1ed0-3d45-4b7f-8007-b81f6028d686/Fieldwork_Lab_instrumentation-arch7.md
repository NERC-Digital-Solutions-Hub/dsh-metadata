# Soil pools and properties

- The document details collection, processing, and analysis of soil samples to quantify physical, chemical, microbial, and isotopic properties, with a focus on enabling interpretation of soil C and N dynamics across a chronosequence.

## Data collected and variables

- Physical and mineral soil properties
  - Gravimetric soil moisture
  - Organic matter content (loss on ignition)
  - pH
  - Bulk density (from a separate sample collected with a hand-corer)
  - Grain size distribution (determined by laser scattering)

- Derived soil property
  - Total soil water content (gravimetric moisture × estimated total soil mass per site)

- Inorganic nitrogen species (from 2 M KCl extracts)
  - NH4+ (ammonium)
  - NO2- (nitrite)
  - NO3- (nitrate)
  - Extracted concentrations analyzed colorimetrically; detection limit ~0.05 μg mL-1; accuracy ≥90%; CV <1%

- Microbial N cycling potentials
  - Nitrification potential (proxy via nitrite oxidation; 30-hour incubation with NaNO2)
  - Denitrification potential (total denitrification and partial denitrification with and without acetylene; headspace N2O measured by GC)
  - Net N mineralization and net nitrification (NH4+ and NO3- accumulation over 24-day incubation)

- Isotopic analyses
  - Total C and N; δ13C and δ15N in soil and plant leaves
  - Isotope measurements by elemental analyzer coupled to an isotope-ratio mass spectrometer
  - Enrichment factor comparing foliar and soil signatures (εf-s for δ13C and δ15N)

- Chronosequence considerations
  - Isotopic signatures measured along a chronosequence to assess sources and openness of the N cycle

## Methods and processing (key steps)

- Sample handling
  - Processing within four days of collection; field moist soils sieved to 2 mm
  - Separate samples used for bulk density measurement after drying
- Soil texture and composition
  - Grain size determined via laser scattering (Mie principle)
  - Organic matter removal from certain subsamples using 0.1 M NaClO with heat and repeated centrifugation
- Nutrient and ion analyses
  - Extraction in 2 M KCl; colorimetric determinations for NH4+, NO2-, NO3-
- Microbial assays
  - Incubations under controlled aerobic/anaerobic conditions; adjustments for substrate and headspace conditions
  - Gas analyses for N2O via gas chromatography with ECD
- Isotopic measurements
  - δ13C and δ15N measured in soil and leaves; CVs ~0.2‰ (δ13C) and ~0.3‰ (δ15N)

## GIS-relevant implications and data products

- Potential map layers and datasets
  - Point or small-area layers for soil moisture, organic matter, pH, bulk density, and grain size distribution
  - N-species concentrations (NH4+, NO2-, NO3-) by site
  - Nitrification potential and denitrification potential layers
  - Net mineralization and net nitrification rates
  - N2O production potential from denitrification experiments
  - Isotopic layers: δ13C and δ15N values for soils and plant leaves, plus enrichment factors (εf-s)
  - Derived soil water content maps (from gravimetric moisture × total soil mass)
- Temporal dimension
  - Chronosequence-based isotopic and nutrient dynamics enabling temporal comparisons
- Metadata and provenance
  - Sampling dates, site coordinates, methods used, detection limits, and analytical precision (LOD, CV)

## Data quality, standards, and integration considerations

- Quality metrics
  - Detection limits, accuracy thresholds, and coefficients of variation for each assay
  - Standardization across laboratories and instruments
- Data integration challenges
  - Data generated across multiple analyses, potentially different labs (field lab, University of Birmingham, Paris)
  - Need for consistent units, depth/volume definitions, and metadata
- Potential GIS challenges
  - Data held in multiple locations; varying data resolutions; need for harmonized schemas and robust data cleaning

## Practical GIS workflow suggestions

- Build a georeferenced database linking site coordinates to all measured variables
- Create standardized units and formats (e.g., mg/kg dry soil or μg/g for nutrients; ng N2O per incubation; δ notation in ‰)
- Use derived layers where appropriate (e.g., derived soil water content, enrichment factors)
- Annotate with sampling and processing metadata to support reproducibility and quality assessment
- Provide uncertainty ranges (e.g., detection limits, CVs) in GIS popups or metadata

## Challenges and considerations for GIS specialists

- Data fragmentation across sites and labs
- Achieving appropriate spatial and temporal resolution for meaningful mapping
- Cleaning and transforming diverse datasets into GIS-ready formats
- Ensuring sufficient skills and resources to implement and maintain complex data pipelines

## End notes

- The document emphasizes robust laboratory methods to quantify soil physical, chemical, microbial, and isotopic properties with an emphasis on C and N cycling, enabling their integration into GIS as multi-parameter spatial datasets for analysis across a chronosequence.