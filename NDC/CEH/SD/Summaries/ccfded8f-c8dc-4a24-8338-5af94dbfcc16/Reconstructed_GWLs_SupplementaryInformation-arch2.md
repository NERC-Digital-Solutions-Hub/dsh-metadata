# Historic reconstructions of monthly groundwater levels for 54 boreholes in the UK (1981-2015)

## Project context and aim
- Historic Droughts project (2014–2018; £1.5m) funded by UK Research Councils to develop cross-disciplinary understanding of past UK droughts and improve future drought management tools.
- Aims to understand links between hydrometeorological and social systems during droughts, informing water resource management and policy.
- Dataset is part of the Historic Droughts Inventory, a knowledge base of past drought characteristics, impacts, and responses.

## What the dataset contains
- Reconstructed groundwater levels relative to Ordnance Datum (maOD) for 54 observation boreholes across the UK.
- Time period covered: 1891–2015, with 90th and 10th percentile confidence bounds estimated for each date.
- Borehole sites distributed across Principal Aquifers (primarily Chalk; others include Carboniferous Limestone, Middle Jurassic, etc.).
- The dataset is one component of groundwater-related data in the Inventory, alongside the Standardised Groundwater level Index (SGI).

## Data provenance, sources, and methods
- Groundwater level data sourced from the National Groundwater Level Archive (NGLA); raw data irregular and typically monthly or sub-monthly, interpolated to monthly.
- Precipitation data drawn from an extended UKCP09 dataset (5x5 km cell corresponding to each borehole).
- Potential evapotranspiration (PET) estimated from temperature via a McGuinness–Bordne-based method.
- Groundwater levels reconstructed using BGS AquiMod model; calibration via Monte Carlo simulations generating ~1,000,000 parameter sets based on aquifer properties.
- Uncertainty quantified with Generalised Likelihood Uncertainty Estimation (GLUE); parameter sets are “behavioural” if Nash–Sutcliffe Efficiency > 0.5.
- Outputs include monthly GWL time series with 10% and 90% confidence bounds.

## Data format and access
- Data delivered as separate CSV files for each site with headers: Date (YYYY-MM-DD), GWL (maOD), Cl90_GWL, Cl10_GWL.
- File naming follows a structured convention linking to the Historic Droughts project and model run (example: HistoricDroughts_BGSAquiMod_Output_Feb2018_GWL_Rockleyver1).
- Additional file: Metadata_forGWLandSGI_reconstructions.csv, listing sites and metadata (Site_name, coordinates, WellMaster ID, aquifer, MORECS_ID, etc.).
- Metadata includes easting/northing, aquifer name, and site identifiers for cross-referencing with other datasets and databases.

## Motivation and potential uses
- Enables exploration of long-term drought history and major drought events prior to the 1960s/1970s records.
- Provides reference events for water utilities’ Drought Management Plans (as per DEFRA guidance).
- Supports cross-disciplinary analyses linking hydro-meteorological conditions with regulatory and societal responses.

## Relevance to environmental monitoring and data governance
- Demonstrates standardized, transparent methods for reconstructing historical hydrological series with quantified uncertainty.
- Examples of reproducible data processing: monthly time-step interpolation, model calibration, and GLUE-based uncertainty bounds.
- Dataset format and accompanying metadata enhance interoperability and reuse, aligning with the archetype’s emphasis on verified data, standardised outputs, and accessible datasets.

## Acknowledgements and references
- Funded by the Natural Environment Research Council (NERC grant NE/L010151/1).
- Related methodological and data references include AquiMod (Jackson et al., 2016), GLUE (Beven & Freer, 2001), and UKCP09-based climate inputs.