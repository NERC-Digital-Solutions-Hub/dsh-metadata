# Bulk density, carbon and nitrogen content in soil profiles from permafrost in subarctic Canada

- A study describing soil cores collected in 2013 and 2014 from subarctic Canada to compare peatland plateaus, thawing features, and unburnt vs burnt black spruce forests across multiple sites.
- Focuses on measuring bulk density and carbon and nitrogen content in soil profiles, with attention to depth, horizon type, and thaw state.

## Sampling design and sites

- Sites include a mix of peatland plateaus, thaw features, and forest types (e.g., unburnt/burnt black spruce, white spruce, birch, and various Teslin and White Truck locations).
- Five soil cores were collected per site in most locations (3–5 cores per site vary by site).
- Depth targets generally aimed for up to 1 meter, but actual depths varied due to rock or other limitations.
- Frozen-ground sites used a combination of tin foil sampling for upper layers and powerhead coring to access deeper frozen sections; non-frozen sites used tin foil for the upper layer and a Russian corer for deeper samples.
- Cores were labeled (e.g., TPP1–TPP5) and correspond to soil core data; however, the same core IDs for soil profiles do not spatially match the flux data (CO2 and CH4) in other datasets.

## Methods and processing

- In-field sampling distinctions: different instrumentation for sites with frozen ground vs. unfrozen ground.
- Sample handling: cores wrapped and stored frozen in Canada, then shipped to the UK for analysis.
- Laboratory processing:
  - Cores cut to capture the upper 1 cm at the top for lead dating; deeper intervals typically 10 cm, chosen by horizon type (organic vs mineral) based on visual uniformity.
  - Samples freeze-dried, weighed to determine bulk density, and ground for carbon and nitrogen analyses.
  - Carbon and nitrogen contents measured with a C and N analyser; standards and calibrations applied to convert measurements to percentage based on dry mass.
- Units:
  - Bulk density expressed as grams of dry soil per cubic centimeter of wet soil.
  - Carbon and nitrogen contents expressed as percentages of dry mass.
- Data documentation:
  - A Remarks column notes potential over- or underestimation of bulk density due to roots or incomplete soil recovery, vegetation changes (Postthaw vs Pre-thaw peat), and presence of the White River Ash tephra layer in some cores.
  - Some datasets mention vegetation transitions associated with thawing and the Tephra layer context.

## Data structure and caveats

- The dataset includes site-level metadata, core-level measurements, and horizon-based segment data (approximately 1 cm for the top; ~10 cm for deeper sections).
- The "Remarks" field provides context on sampling issues, vegetation changes, and tephra presence that could affect interpretation.
- Important caveat: soil-profile data and flux data (CO2 and CH4) use the same core IDs but originate from different locations; GPS coordinates in the data files should be consulted to align datasets correctly.
- Sampling depth and core recovery varied by site, and field methods differed between frozen and unfrozen sites, which may influence comparability across sites.

## Key considerations for analyses

- When exploring relationships between bulk density, carbon content, and nitrogen content, segment the data by thaw state (pre-thaw vs post-thaw peat) and horizon type (organic vs mineral).
- Exercise caution when combining soil-profile data with flux data due to potential spatial misalignment between core IDs and physical locations.
- Account for potential measurement biases noted in Remarks (root interference, sampling recovery issues) and tephra layer effects where applicable.
- Consider age context from lead dating in the upper 1 cm to anchor temporal analyses of soil changes.

## Use cases and applications

- Identify correlations between soil physical properties (bulk density) and chemical properties (C and N contents) across depth and thaw states.
- Compare soil carbon and nitrogen pools between peatland plateaus, thaw features, and forest types (burnt vs unburnt; spruce vs birch).
- Analyze vegetation transitions and disturbance signals (e.g., post-thaw peat characteristics, tephra layers) in relation to soil nutrient contents and density.
- Integrate with flux datasets (while carefully ensuring spatial alignment) to study links between soil properties and gaseous fluxes in permafrost environments.