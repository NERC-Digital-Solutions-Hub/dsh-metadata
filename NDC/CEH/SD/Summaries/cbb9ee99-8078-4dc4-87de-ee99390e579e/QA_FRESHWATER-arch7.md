# Quality Assurance Report: surveying condition of headwater streams and ponds

- The freshwater module of Countryside Survey 2007 (CS2007) aimed to provide high-quality information on changes in the physical and biological condition of small streams and ponds across Great Britain, including distribution of components of biological diversity.
- A rigorous quality assurance (QA) process was conducted to quantify uncertainty in field data collection, focusing on inter-surveyor variation and repeatability, to baseline future surveys and inform improvements.

## Objective and scope

- Validate that CS2007 freshwater fieldwork was conducted to high standards by experienced, trained surveyors and laboratories.
- Quantify uncertainty and inter-surveyor differences across key freshwater components:
  - Aquatic plants (streams)
  - River Habitat Survey (RHS)
  - Aquatic macroinvertebrates (analysis proceeding; report due late 2009)
  - Hydrochemistry
  - Aquatic plants in ponds (wetland plants)
- Use QA results as a baseline for future CS freshwater surveys and to refine field protocols and training.

## Field survey design and QA approach

- Random-stratified sub-sample of 31 squares re-surveyed by an experienced CEH freshwater biologist to assess error/variation.
- Coverage:
  - Streams: re-sampled in all 31 squares (8% re-survey effort)
  - Ponds: 18 of the 31 squares contained a pond and were re-surveyed (7% re-survey effort)
  - Aquatic plant surveys: 30 of 31 QA stream sites re-surveyed (one site dry)
  - RHS: 31 stream sites re-surveyed at the same 500 m reach as CS2000
  - Macroinvertebrates: samples taken for QA, processed by CEH River Communities Group (results pending)
  - Hydrochemistry: sampling at QA streams and ponds aligned with plant/RHS efforts
- Data capture tools: IRIS on Tablet PC (plants), RAPID on Tablet PC (RHS), standard protocols for macroinvertebrates and hydrochemistry.
- Pond and stream plant data validated taxonomically and compared against main CS2007 surveys.

## Key QA findings by component

- Aquatic plants (streams)
  - 30/31 streams re-surveyed; one site dry.
  - QA tended to record more taxa than the main CS2007 survey: average difference ≈ 1.9 taxa (±0.87 95% CL) with QA higher.
  - Mean agreement of species lists between CS2007 and QACS2007 was only 31%; 100% agreement occurred only where only a single species was found in both surveys.
  - Most discrepancies occurred with rare taxa (cover <1%), suggesting thorough searching is crucial. Over 60% of errors involved taxa overlooked by the main survey; 15% involved misidentifications.
  - Commonly missed taxa included certain bryophytes, algae, and grass-like species (e.g., Pelia sp., Rhynchostegium riparioides, Agrostis stolonifera, Cladophora, Vaucheria).
  - Resulting MTR scores: QA surveys tended to score 5.6 (±10.6 95% CL) higher than main surveys, though this was not statistically significant.
  - Overall, substantial variability remains in repeating aquatic plant surveys; even on the same day, 57% agreement was observed for a stream site.
- River Habitat Survey (RHS)
  - 70% of sites showed no difference in bridge/culvert counts between CS2007 and QA surveys.
  - Some discrepancies ±1 to ±2 in bridges/culverts likely due to slight relocation of the 500 m reach.
  - Habitat Quality Assessment (HQA) values varied; QA generally reported different classifications of bank-face and bank-top vegetation, especially in upland moorland where different vegetation interpretations occurred (e.g., “Simple” vs “Uniform”).
  - Across 31 squares, a significant bias existed: main CS results tended to yield higher HQA scores by about 6.9 units (P < 0.001).
  - No QA data for CS2000; precautionary assumption that CS2000 and CS2007 share similar bias; hence CS2007 RHS data can be analyzed with caution and without formal correction, recognizing data quality issues.
- Hydrochemistry
  - Rank correlations between main CS2007 and QA values were high for all parameters:
    - Soluble reactive phosphorus: r = 0.89
    - Total oxidised nitrogen: r = 0.79
    - Alkalinity: r = 0.97
    - pH: r = 0.74
    - Conductivity: r = 0.97
  - Indicates consistent field and laboratory procedures; confidence in measured results.
  - Notable exception: TON values showed some discrepancy in two ponds with a two-month gap between visits.
- Wetland plants (ponds)
  - 16 ponds with both main CS2007 and QA pond surveys; 59% mean taxon agreement; 100% agreement at 5 ponds.
  - No significant overall bias: main survey found 0.6 more taxa on average (not statistically significant).
  - Reasons for discrepancies include misidentifications, boundary definition (winter water level), and seasonal differences.
  - 36 taxa missed across surveys; 29 missed on only one occasion; seven missed at more than one site (notably grasses and rush-like species such as cotton-grasses, deergrass, Juncus, Agrostis).
  - Indicates grass-like taxa are particularly challenging and important for targeted training.
- Discussion on uncertainties and timing
  - Environmental measurements carry inherent uncertainty; QA provides a first indication of variability in freshwater data within CS.
  - Temporal differences (disparities in survey dates) and spatial relocation contribute to variability and complicate attribution to inter-surveyor competence.
  - Two-week timing window between main and QA surveys is recommended to minimize temporal error; many QA surveys occurred weeks after the main survey.
  - The QA exercise highlights the need to improve identification skills for bryophytes and algae, and to emphasize exact return to previous survey stretches, as well as defining lateral survey boundaries more consistently.
  - The freshwater QA report serves as a baseline for future CS freshwater QA and informs training, protocols, and data interpretation.

## Implications for GIS data and map-based products

- Data quality and uncertainty must be explicitly captured in map-based data products (e.g., confidence intervals, QA flags, and notes on potential biases).
- Spatial accuracy and relocation procedures impact the fidelity of map features (e.g., 500 m RHS reach and exact plant survey stretches). Documentation of survey reach definitions and relocation references is essential.
- Taxon-richness and HQA scores contain systematic biases (e.g., higher MTR in QA for streams, higher RHS HQA in main surveys). These biases should be considered when comparing across years or aggregating data spatially.
- Temporal alignment is critical for change detection; avoid or account for time lags between main and QA surveys when building GIS-informed change analyses.
- Data products should include metadata on survey dates, observer identity, and QA status to enable proper uncertainty propagation in GIS analyses and visualisations.

## Recommendations and next steps

- Training and protocols
  - Enhance training for bryophytes, algae, and inconspicuous grasses/rush-like taxa to reduce taxonomic omissions.
  - Improve guidance and consistency on identifying bank vegetation classifications (e.g., Simple vs Uniform) to reduce HQA variability.
  - Emphasize precise relocation to exact survey stretches and clear definitions of lateral survey boundaries.
- Timing and sampling
  - Conduct QA and main surveys within two weeks of each other whenever possible to minimize temporal variation.
  - Where timing cannot be close (due to logistics), document temporal gaps and consider their potential impact on QA interpretation.
- Data handling and reporting
  - Maintain QA as a baseline for all future CS freshwater surveys; use QA findings to refine field protocols and training needs.
  - For GIS products, include QA flags and uncertainty estimates, especially for taxa-richness and HQA-derived indicators.
- Future work
  - Complete macroinvertebrate QA analysis and integrate results into the overall QA framework.
  - Use QA results to inform targeted improvements in the pond and stream surveying protocols, and to tailor data products for policy, client, and public audiences.

## Limitations

- No QA data were available for CS2000, necessitating assumptions of equal bias for CS2000 and CS2007 RHS data.
- Some QA results (notably macroinvertebrates) were pending at the time of this report; overall QA conclusions focus on streams, RHS, hydrochemistry, and pond plants.
- Temporal gaps between main and QA surveys limit the ability to fully partition error sources into spatial, temporal, and inter-surveyor components.