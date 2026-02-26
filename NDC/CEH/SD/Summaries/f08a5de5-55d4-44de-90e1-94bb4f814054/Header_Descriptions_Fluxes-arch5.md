# Header Descriptions for Dataset "CO2_Flux_Data" and "CH4_N2O_Flux_Data"

## Overview
- Provides field-by-field metadata descriptions for two datasets: CO2_Flux_Data and CH4_N2O_Flux_Data.
- Defines each header’s meaning, units, instruments used, and measurement context to support data discovery, interoperability, and reuse.
- The CH4_N2O_Flux_Data section notes that most headers are the same as CO2_Flux_Data, with three additional flux columns.

## CO2_Flux_Data: Key Headers and Meanings
- Sample Identification
  - Sample, Date, DateNumber, SamplingPeriod: identifiers for sampling events; DateNumber assigns sequential day numbers (1, 2, …) within a sampling period.
  - Site, Age, Plot: site name, site age since last wildfire (years), and plot/chamber number.
- Measurements and Fluxes
  - Biomass: final dry biomass in plot (g).
  - Temperature: air temperature at sampling time (°C); measured with Tinytag data loggers.
  - Par: Photosynthetically Active Radiation (μmol m^-2 s^-1) from Skye Instruments PAR sensor.
  - Respiration: ecosystem respiration (mg CO2-C m^-2 hr^-1) measured with EGM-4 IR gas analyser (dark chamber).
  - NEE: Net Ecosystem Exchange (mg CO2 m^-2 hr^-1); sign convention: positive = net CO2 emitted, negative = net CO2 taken up.
  - Photosynthesis: gross CO2 uptake (mg CO2 m^-2 hr^-1); derived from Respiration and NEE.
- Soil and Soil-Environment Properties
  - BD: bulk density of soil organic horizon (g cm^-3).
  - PercentC, PercentN: percent carbon and nitrogen in soil organic horizon.
  - CN: carbon-to-nitrogen ratio.
  - OrgDepth: depth of the organic horizon (cm).
- Microclimate and Soil Conditions
  - SM1, SM24: soil moisture averaged over 1 hour and 24 hours prior to sampling (m3/m3).
  - LWCount1, LWCount24: leaf wetness count (1 hr and 24 hr prior) on a 445–1400 scale.
  - Soil1cm1, Soil5cm1, Soil1cm24, Soil5cm24: soil temperatures at 1 cm and 5 cm depth (°C) averaged over 1 hour and 24 hours prior, respectively.
  - AirTemp1: air temperature averaged over 1 hour prior (°C).
- Vegetation and Ground Cover
  - P.Schreberi, V.myrtillus, V.vitis-idaea, V.uliginosum, D.flexuosa, Dicranum, P.commune, Lichen, Daisy, Equisetum, Galium, Luzula, Cladonia, E.angustifolium, Vicia, L.borealis, Moss, Shrub: percentage cover by various moss, lichen, shrub, and herb species (note: some lines show formatting inconsistencies in species labeling).
- Notes
  - Numerous habitat and canopy cover descriptors captured as percent cover; enables linking flux measurements to vegetation context.

## CH4_N2O_Flux_Data: Additions and New Headers
- Note: Most headers are the same as in CO2_Flux_Data.
- New headers (three flux metrics per plot)
  - Ch4Flux: CH4 flux from the plot (μg CH4 m^-2 hr^-1).
  - Co2Flux: CO2 flux from the plot (μg CO2 m^-2 hr^-1).
  - N2oFlux: N2O flux from the plot (μg N2O-N m^-2 hr^-1).

## Data Quality, Standards, and Governance Considerations
- Consistent metadata: explicit definitions, units, and instrument details accompany each header to support consistent interpretation across datasets.
- Instrument provenance: mentions of Tinytag data loggers, Skye PAR sensor, and EGM-4 IR gas analyser facilitate traceability and reproducibility.
- Unit standardization: varied units (e.g., mg CO2 m^-2 h^-1, μg CH4 m^-2 h^-1, °C) are specified, aiding cross-dataset comparability if kept consistent.
- Metadata completeness: comprehensive coverage of sample descriptors, environmental conditions, and vegetation context enhances discoverability and reuse.

## Particular Challenges and Recommendations for Data Stewards
- Incomplete user needs: ensure header descriptions align with downstream analysis needs and provide mappings to potential data user queries.
- Data timeliness: coordinate timely data capture and metadata updates to keep datasets current.
- Standards adoption: encourage data creators to follow the defined metadata rigor (consistent naming, units, and instrument details).
- Heterogeneous formats: provide clear guidance on validating and harmonizing fields across CO2 and CH4/N2O datasets.
- Large and complex headers: implement validation rules and controlled vocabularies for species names and site identifiers.
- Interoperability: expand crosswalks or ontologies to link headers to broader data catalogs and metadata schemas.
- Documentation quality: address any formatting inconsistencies (e.g., duplicated or garbled species lines) to prevent ambiguity.