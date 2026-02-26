# Experimental Design/Sampling Regime

- Objective and scope
  - Longitudinal monitoring of earthworms and soil properties across seven fields undergoing conversion transects, with baseline sampling in April 2015 and follow-up sampling through 2017 to assess environmental health indicators relevant to policy evaluation.
  - Temporal sampling to capture seasonal and inter-annual variation, including winter 2015, summer 2016, and autumn 2016.

- Fields and spatial design
  - Seven fields: BSSE (Big Substation East), BSSW (Big Substation West), Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
  - Sampling conducted before and after conversion transects were established.
  - At each sampling occasion, earthworm and soil measurements were taken from 8 locations per field: under the hedgerow and the field-margin boundary, plus sampling within the transects at 2, 4, 8, 16, 32, and 64 meters from the hedge.

- Temporal coverage
  - Core transect sampling in April 2015 (baseline), April 2016, and April 2017.
  - Additional temporal sampling: December 2015 (winter), July 2016 (summer), and October 2016 (autumn).

- Collection methods and instrumentation
  - Earthworms
    - Soil block extraction (18 x 18 x 15 cm) at each distance.
    - Stimulated deeper-dwelling species with dilute allyl isothiocyanate (1.5 L of 0.1 g L-1).
    - 30-minute exposure period; earthworms stored in 80% ethanol.
    - Adults with clitellum identified to species; juveniles grouped into functional groups: epigeic, endogeic, anecic.
    - Biomass recorded from December 2015 onward.
  - Soil measurements
    - Soil moisture (three locations around each pit) and temperature at 5 cm and 10 cm depths.
    - Soil bulk density at 5 cm and 10 cm using density rings; bulk density derived from oven-dried weight.
    - Soil samples returned to pits with position recorded to avoid re-sampling.

- Data structure and recording
  - Multiple data files capturing earthworm and soil data across timepoints:
    - April2015_earthworm_Soil data.csv
    - Dec2015_Earthworm_Soil data.csv
    - April2016_Earthworm_Soil data.csv
    - April2017_Earthworm_Soil data.csv
    - July2016_Earthworm_Soil data.csv
    - Oct2016_Earthworm_Soil data.csv
  - Key column structure (examples)
    - Date, SBH_code (field and distance code), field/strip codes (X, Y, ZZ), field name, strip type (CAL, UAL, Ctrl, NTL-A, CTL-A), distance from hedge, location (Hedge, Margin, 2m, 4m, 8m, 16m, 32m, 64m), soil temperature and moisture readings, bulk density.
    - April 2015 data note: all samples were from control land use as treatment strips were not yet created.
  - Dec2015_Earthworm_Soil data.csv expands to 10 columns, including Field_name, Strip, Distance, Field/Strip codes, and detailed soil variables (e.g., Soil_temp_5cm_1, moisture_5cm_depth_1, etc.) and a 10-column codebook describing the sampling sites.
  - The 2015–2017 (and later) datasets include 31 columns for earthworm count/biomass data, covering a comprehensive list of species and their functional groups.
  - Coding scheme
    - Field codes: BSSE, BSSW, Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
    - Strip codes: CAL (connected arable ley strip), UAL (unconnected arable strip with earthworm barrier), Ctrl (control land use: arable in arable, pasture in pasture), NTL-A (no-till strip in pasture), CTL-A (conventional tillage strip in pasture).
    - Distance codes: Hedge (H), Margin (M), 2m, 4m, 8m, 16m, 32m, 64m from hedge.

- Earthworm taxa and data granularity
  - Functional groups: Endogeic, Epigeic, Anecic.
  - Species examples include Allolobophora chlorotica; Allolobophoridella eiseni; Aporrectodea caliginosa; Aporrectodea longa; Aporrectodea rosea; Dendrodrilus rubidus; Eisenia fetida; Lumbricus terrestris; among many others.
  - Data include both abundance (count) and biomass measures for specified samples and species across time and space.

- Miscellaneous and references
  - Earthworm functional groups: Endogeic (soil-living, horizontal burrowing), Epigeic (litter-living), Anecic (soil-living, deep vertical burrows).
  - References: Sims & Gerard (1999); Zaborski (2003); Pelosi et al. (2008).

- Relevance for monitoring and policy evaluation
  - Provides a structured, multi-temporal, spatially explicit monitoring framework for soil biota and soil physical-chemical properties.
  - Captures species-level and functional-group responses to land-use changes across hedgerow margins and field interiors.
  - Standardized data collection and comprehensive metadata facilitate evaluation of policy-driven habitat and soil health outcomes, and support data sharing and governance considerations through explicit field, strip, and location coding.
  - Data gaps are explicitly labeled (blank cells indicate no data), and baseline-only sampling notes (April 2015) document treatment-naïve conditions before interventions.