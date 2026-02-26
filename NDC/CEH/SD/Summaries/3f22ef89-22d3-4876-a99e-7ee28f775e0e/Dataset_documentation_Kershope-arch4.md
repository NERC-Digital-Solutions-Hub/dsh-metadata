# Solute concentrations in water samples from clearfelled and standing Sitka spruce ( Picea sitchensis ) forest ecosystems, Kershope Forest

## Overview
- Long-term dataset investigating how clearfelling Sitka spruce plantations affects solute concentrations in drainage and related waters at Kershope, England.
- Timeframe: 1981–1987 for drainage water; sampling from 1981–1985 for water samples; experimental setup includes six plots in Block 1, with three felled during 1983.
- Focus on a wide suite of solutes (K, Ca, Mg, Fe, Na, Al, PO4P, NO3N, NH4N, Cl, SO4S) plus pH, suspended solids, and total organic carbon (TOC).

## Geographic and site context
- Location: Kershope Forest, Cumbria, England; upland peat gley soils on former grassland planted with Sitka spruce in 1948.
- Experimental design: Block 1 of an original drainage experiment comprising six plots with varying drain spacing and depths; three plots felled in 1983, three unfelled (controls).
- Plot characteristics: each plot ~2–3 hectares; drainage water collected through a main exit drain and sampled weekly.

## Data collected and sampling pathways
- Primary drainage water data: solute concentrations and discharge from six main drains; samples collected weekly with dedicated sampling pipe and discharge measured at a V-notch weir.
- Additional water pathways sampled per plot include:
  - Soil solution samplers and lysimeters (L and O horizons), moisture-related samples.
  - Rainfall (bulk precipitation), stemflow, throughfall, and needle-tray brash throughfall samples.
  - Knapp throughflow data collected (noted as unreliable).
  - Regular sampling of main exit drains to link surface/groundwater flux with solute concentrations.
- Sampling frequency:
  - Drainage waters: weekly (1981–1987 data window).
  - Soil solution lysimeters and related samplers: fortnightly.
  - Rainfall and throughfall/needle trays: variable schedules, provisioned to yield regular composite samples.

## Analytical methods and quality considerations
- Analyzed at the Chemical Analysis Section, ITE Merlewood (and linked CEH expertise): 
  - pH measured in sub-samples; samples filtered for most analyses.
  - Calcium, magnesium, aluminium, iron by atomic absorption spectrophotometry.
  - Sodium and potassium by flame emission spectrometry.
  - Phosphate (PO4-P) by molybdenum blue; ammonium (NH4-N) by indophenol blue.
  - Chloride, nitrate, and sulfate by various established methods; later years used ion chromatography for some ions.
  - Suspended solids (TSS) and TOC by standard methods.
- Method cross-validation: older and newer methods used concurrently for three months to ensure comparability.

## Datasets and data structure
- Drainsker.csv: main drainage water solute data from six drains; includes discharge (m3 s-1), major ions (K, Ca, Mg, Fe, Na, Al, PO4P, NO3N, NH4N, Cl, SO4S), pH, suspended solids, TOC; includes sample codes and notes where samples were not taken.
- Soilsker.csv: solute data from soil solution samplers and lysimeters across horizons; includes sampling week, sample volumes, and concentrations by ion; coded to sample types (e.g., N1/N2 for needle trays) and horizons.
- Kershope_sampling_points.csv: sampling locations and mapping for points listed in corresponding tables; includes plot/block details, felled status, and coordinates (Easting/Northing) for geospatial reference.
- Kershope_codes (reference table in accompanying documentation) provides mappings for sample codes to sample types (e.g., needle trays, stemflow, rainfall, throughfall, Knapp throughflow, lysimeters).

## Design, governance, and context for data leaders
- Purpose and use: assess nutrient fluxes and soil fertility implications of clearfelling, with pre- and post-felling comparisons and cross-plot contrasts.
- Multi-source data architecture: integrates drainage chemistry, hydrology (discharge), and various water pathways within a single site, enabling holistic evaluation of forest hydrology and nutrient dynamics.
- Metadata and traceability: clear documentation of plots, treatments, sampling schedules, and analytic methods; cross-referenced with relevant publications for methodological context.
- Potential data governance insights:
  - Complex, multi-file dataset with diverse sampling types and coding schemes; requires careful metadata mapping for reuse.
  - Some data streams (e.g., Knapp throughflow) flagged as unreliable, highlighting the need for quality notes and lineage tracking.
  - Longitudinal time series across pre- and post-disturbance periods, offering opportunities for temporal analysis and policy-relevant modeling.

## Notable uses and limitations
- Uses:
  - Compare solute fluxes between felled and unfelled plots.
  - Model ecosystem nutrient dynamics following clearfelling.
  - Inform forest management and environmental policy on nutrient leaching and soil fertility.
- Limitations:
  - Knapp throughflow data deemed unreliable.
  - Methodological changes over time (multiple analytic methods used in parallel) require careful harmonization.
  - Spatial scope limited to six plots within Block 1; generalizability to other sites requires caution.

## References and further reading
- Key publications linked to the dataset:
  - Adamson & Hornung (1990); changes in drainage water solute concentrations after clearfelling.
  - Adamson et al. (1987); solute chemistry changes in drainage waters following clearfelling.
  - Neal et al. (1999); broader context on anion variations and acidity impacts.
  - Pyatt et al. (1985); drainage experiment design at Kershope Forest.
  - Rowland (1983); ammonium-N determination method.
  - Allen (1989); Chemical Analysis of Ecological Materials (method reference).
  - Avery (1980); soil classification context.