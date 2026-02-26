# Benthic organic matter of Welsh upland rivers in response to organic matter addition

- Objective
  - Examine how addition of leaf litter affects benthic organic matter (BOM) stocks in Welsh upland rivers using a BACI (before-after-control-impact) design.
  - Compare upstream reference zones with downstream experimental zones to identify treatment effects over time.

- Experimental design
  - Each stream divided into upstream reference (control) and downstream experimental (treatment) zones.
  - Equal lengths and similar habitat structure; 20–50 m gap between zones to ensure independence.
  - Time periods:
    - Before period (T1): Nov 2012–Jan 2013, no manipulation; both zones treated identically.
    - After period (T2): Jan–Mar 2013; experimental zone received leaf litter additions.
  - Leaf litter treatment
    - 1 tonne bags containing oak, birch, and alder leaves proportionally added to simulate natural senescence.
    - Leaf packs distributed to maintain a minimum wet weight of 1.7 kg m^-2 in the experimental zone.
    - Randomly fixed within the channel; slow degradation maintained litter throughout the period.
    - Additional 630 kg (wet weight) of leaf litter added on 12 Feb 2013 and 5 Mar 2013 after two large storm-flow events.

- Treatments and materials
  - Leaf litter sources: deciduous leaves (oak, birch, alder).
  - Deployment method: 1 t bags plus proportional vegetable nets to maintain target wet weight.
  - Field equipment: metal poles to anchor leaf packs; storm-event supplementation.

- Sampling regime
  - Six random BOM samples per reach, collected on five occasions: January, February, March, April, and May 2013.
  - Sampling method: Surber net (0.1 m^2 area, 330 µm mesh, 10 cm depth).
  - Preservation and processing: on-site preservation in 70% IMS; lab processing separated macroinvertebrates from debris; BOM dried to constant weight and weighed to 0.01 g.
  - Inorganic correction: ash-free conversion by combusting a subset of samples at 550°C for 5 h.

- Analytical methods and units
  - BOM stocks weighted to nearest 0.01 g.
  - Units reported: grams of coarse particulate organic matter (CPOM) and fine particulate organic matter (FPOM).

- Data structure and content
  - Data stored as flat CSV files with 10 columns per BOM sample:
    - site_code, landuse, region, time (Before/After manipulation), month, reach (Experimental or Control), replicate, surber_area, cpom, fpom.

- Supporting data
  - Site description file (DURESS_CU_site_description.csv) providing meta-data per site:
    - Site_code, Name, Eastings/Northings, Grid, Latitude/Longitude, Elevation, Survey/Catchment context.

- Quality and limitations
  - Quality control notes indicate no explicit QC steps beyond standard laboratory processing.
  - Potential data challenges for analysts include reliance on BACI design assumptions, need to account for seasonal variability across months, and integration of data across multiple streams with potentially differing baseline conditions.