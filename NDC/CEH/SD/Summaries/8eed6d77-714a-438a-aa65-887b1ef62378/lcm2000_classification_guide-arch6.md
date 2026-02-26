# LCM2000: Calibration and Assessment of Broad Habitat Classification against CSLCM Field Survey

- Purpose: Assess and calibrate the LCM2000 thematic classification (broad habitats and target classes) against CSLCM CS2000 field survey (FS) data to enable generation of BH cover statistics from comprehensive LCM2000 coverage.
- Context: Built to support biodiversity planning in the UK by aligning satellite-derived broad habitats with finer-field observations, recognizing that FS is not ground truth and differences arise from resolution, timing, and classification schemes.

## Data sources and context

- LCM2000: Satellite-derived land cover map for Great Britain with 1 km resolution, mapping Broad Habitats (BHs), Target classes, and Variants; mainly 1998–2001 imagery.
- CS2000 FS: Field survey data from 569 one-kilometre squares (GB), plus separate NI data (not yet digitised); higher detail than LCM2000.
- External/contextual data: peat depth (from British Geological Survey), soil acidity maps, and local knowledge used to refine BH definitions (e.g., bog, heath, fen, montane distinctions).
- Limitations acknowledged: FS is not ground truth; there are mismatches due to resolution differences (25 m pixels in FS vs 1 km/parcel-level in LCM2000), timing differences, and definitional differences between BH targets, Subclasses, and Variants.

## Methods and calibration approach

- GIS workflow: ARC/Info-based mapping; 569 FS squares matched to equivalent LCM2000 map sections; creation of correspondence matrices for pixel, segment, and parcel levels.
- Comparison levels:
  - Per-pixel: direct overlay differences.
  - Per-segment: LCM2000 segment labels vs FS dominant class.
  - Per-parcel: FS parcels mapped to LCM2000-derived labels.
- Thematic levels analyzed:
  - BH level (excluding Boundaries/linear features and Rivers/streams)
  - Target class level
  - Aggregate class level (simplified 10-class equivalents)
- Confidence estimation: bootstrapping to derive 95% confidence limits for correspondence measures.
- MMU and timing: LCM2000 uses >0.5 ha MMU; FS parcels down to 0.04 ha; timing differences (FS mainly 1998 vs LCM2000 imagery 1998–2001) affecting results.

## Key results: overall correspondence and accuracy

- Per-pixel correspondence (GB): 54% (95% CI 53–56%)
  - England & Wales: 60% (95% CI 58–62%)
  - Scotland: 44% (95% CI 40–47%)
- Per-segment correspondence (GB): 58% (95% CI 57–60%)
  - England & Wales: 64% (95% CI 62–66%)
  - Scotland: 47% (95% CI 43–50%)
- Per-parcel correspondence (GB): 62% (95% CI 60–64%)
  - England & Wales: 69% (95% CI 67–72%)
  - Scotland: 48% (95% CI 44–52%)
- Target class level (weighted, parcel-based): ~65% GB; ~73% England & Wales; ~51% Scotland
- Observations: Higher agreement at Target class level than at BH level due to structural/label differences and aggregation effects.

## Class-level findings and interpretive notes

- Woodland and Arable:
  - Broadleaved/mixed woodland and coniferous woodland show similar total cover but lower direct agreement due to small woodlands being below LCM2000’s 0.5 ha minimum and misalignment of boundaries.
  - Arable and horticultural land sizes are similar; misclassifications between arable and grassland or built-up areas contribute to errors.
- Grasslands:
  - Improved grassland is generally well-classified on LCM2000, but distinguishing neutral/calcareous/acid grasslands is difficult spectrally; field context often reveals differences.
  - Rough grasslands are a major source of mismatch, with FS often recording as Improved grassland while LCM2000 maps rough grass as Neutral grassland.
  - About 20% of FS “improved” grassland is mapped by LCM2000 as semi-natural; spectral masking (soil/acid sensitivity) complicates distinctions.
- Heath, bog, fen, and montane:
  - Dwarf shrub heath vs bog: significant discrepancies due to peat depth criteria and spectral/soil-context masking; peat depth (>0.5 m) used to distinguish bog vs heath, influencing mapping outcomes.
  - Fen, marsh, swamp: FS records more extent than LCM2000; rush pastures create particular challenges in consistent classification.
  - Montane habitats: altitude-based rules in LCM2000 may misrepresent actual montane extent in inaccessible areas.
- Inland bare ground and water:
  - Inland bare ground: LCM2000 tends to classify some urban bare ground as Inland bare ground, leading to mismatches with FS’s urban-focused context.
  - Water (inland): LCM2000 aggregate standing water/canals with relatively small water bodies; FS tends to record more water features due to higher resolution and different delineation criteria.
- Coastal and maritime habitats:
  - Supralittoral and littoral habitats are small and often near resolution limits; differences arise from tidal state and coastline definitions; generally contribute little to overall non-correspondence.
- Built up areas and boundaries:
  - Built up areas and gardens in LCM2000 distinguish suburban/rural development from continuous urban areas, whereas FS treats urban land more continuously; this causes notable classification disagreements.

## Change detection and temporal dynamics

- Real landscape change between 1990 and 2000 is expected to be small relative to study scale; detection is hampered by reliance on satellite data alone.
- A segment-based approach with BH pre-classification reduces some differences but direct 1990 vs 2000 comparison remains challenging.
- Proposed approach: use intelligent, pattern-based change detection that leverages FS change expectations (e.g., from Haines-Young et al. 2000) to distinguish real change from classification error.

## Accuracy interpretation and practical implications

- FS repeatability (88%) sets an upper bound for achievable accuracy; LCM2000 likely attains around 72–85% accuracy at the Target class level, given structural differences and MMU constraints.
- Important caveats:
  - LCM2000 is not a ground truth dataset; differences reflect survey design, timing, and mapping scales.
  - Per-pixel accuracy is inherently lower due to resolution and MMU differences; per-parcel and per-segment comparisons provide more meaningful measures of classification performance.

## Data products, use, and recommendations for data support

- Calibrated outputs:
  - Generate Broad Habitat statistics calibrated against FS to enable robust BH area estimates across GB.
  - Provide Target class and Aggregate class maps with documented accuracy metrics and confidence intervals.
- Data integration:
  - Combine LCM2000 with FS and external data (peat depth, soil pH maps, urban context) to improve classification of complex swards and peat-related habitats.
  - Use Variant-level information where feasible to refine distinctions (e.g., rough vs improved grassland, bog vs heath) for downstream analyses.
- Change detection product development:
  - Develop intelligent change-detection workflows that use prior knowledge of expected changes and calibration results to distinguish real landscape change from classification noise.
- Documentation and transparency:
  - Clearly document class definitions, mappings between LCM2000 variants and BHs, and the rationale for corrections based on contextual data.
  - Provide detailed confusion matrices and country-level summaries to aid data users in interpreting outputs.
- Future work (as indicated):
  - Re-examine LCM2000 bogs and heaths by integrating FS and external datasets; evaluate peatland mapping with updated peatland data sources.
  - Enhance representation of upland areas, montane habitats, and intertidal/coastal BHs with additional data sources and refined criteria.
  - Consider refining the MMU or adopting multi-scale assessments to better capture small but ecologically important features.

## Appendix and supplementary notes

- Appendix I outlines distinguishing features of Broad Habitats relative to LCM2000 mapping and notes key spectrally-based challenges (e.g., distinguishing neutral vs calcareous vs acid grasslands, peat depth criteria for bogs, and limitations in mapping complex mosaics).
- Appendix provides mapping details of LCM2000 class Variants to BHs, including alpha-codes, color representations, and broad habitat associations to assist data users in understanding classification schemes and visual outputs.

Note: The document emphasizes that LCM2000 should be used in conjunction with field data (FS) and external contextual information to produce reliable, usable data products for policy, planning, and biodiversity assessment, rather than relying on LCM2000 alone as ground truth.