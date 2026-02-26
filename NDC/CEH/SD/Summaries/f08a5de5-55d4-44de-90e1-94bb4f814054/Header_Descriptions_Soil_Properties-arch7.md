# Header Descriptions for Datasets OH_Soil_Properties and NH4_NO3_OH_Soil Properties

## Overview
- The document provides attribute headers and descriptions for two soil property datasets to support GIS-based data products.
- Fields include site and sample identifiers, temporal context (age), physical/chemical properties, and microbial indicators, with explicit units where provided.

## OH_Soil_Properties – Attribute Descriptions
- Identifier: Sample Identification for measurement of each plot/gas chamber ring at each sampling time.
- Site: Site name.
- Sample: Sample number at that site.
- Age: Site age since last wildfire (years).
- Depth: Depth of soil organic horizon (cm).
- BD: Bulk density, soil organic horizon (g cm-3).
- CN: Ratio of total carbon to total nitrogen, soil organic horizon.
- pH: pH, soil organic horizon.
- LOI: Loss on ignition, soil organic horizon (% soil organic matter).
- P: Total phosphorous, soil organic horizon (mg g -1 soil dry weight).
- totPlfa: Total phospholipid fatty acid content, soil organic horizon (nmol g -1 dry weight).
- totFung: Total fungal phospholipid fatty acid content, soil organic horizon (nmol g -1 dry weight).
- totBact: Total bacterial phospholipid fatty acid content, soil organic horizon (nmol g -1 dry weight).
- fungBact: Ratio of fungal to bacterial phospholipid fatty acid content.

## NH4_NO3_OH_Soil Properties – Attribute Descriptions
- Identifier: Sample Identification for measurement of each plot/gas chamber ring at each sampling time.
- Site: Site name.
- Sample: Sample number at that site.
- Age: Site age since last wildfire (years).
- NO3.ppm: NO3- concentration, soil organic horizon (parts per million).
- NH4.ppm: NH4+ concentration, soil organic horizon (parts per million).
- mgNO3.N: NO3- concentration, soil organic horizon (mg kg -1 soil dry weight).
- mgNH4.N: NH4+ concentration, soil organic horizon (mg kg -1 soil dry weight).

## GIS Use and Analysis Guidance
- Use as attribute tables for map layers; join by Site and Sample for integrated analyses.
- Leverage Age, Depth, and LOI for stratified or temporal analyses of soil properties.
- Utilize CN, pH, P, and LOI to create thematic maps of soil chemistry and fertility.
- Apply totPlfa, totFung, totBact, and fungBact to explore microbial community structure and its spatial patterns.
- Use NO3.ppm, NH4.ppm, mgNO3.N, and mgNH4.N to map inorganic nitrogen forms and concentrations across sites.

## Data Quality and Standards Considerations
- The headers provide clearly labeled, units-specified attributes to support consistent data integration across datasets.
- Standardized field descriptions facilitate quality assurance, data cleaning, and GIS-ready transformation for robust map-based visualizations.