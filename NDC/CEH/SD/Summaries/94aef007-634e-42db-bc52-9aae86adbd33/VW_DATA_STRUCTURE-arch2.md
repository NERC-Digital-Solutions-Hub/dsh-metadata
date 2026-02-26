# Explanatory Information: Species codes and Quality Codes

## Explanatory Information: Species codes

- Purpose
  - Provide mappings between ECN's internal species coding (e.g., Vas_, Bry_) and Latin names, with cross-references to the Biological Records Centre (BRC) concepts.
  - Support consistency across life stages and contexts (e.g., sapling, canopy, seedling) and enable interoperability with other datasets.

- Structure and examples
  - Entries pair a numeric code with a Latin name and show cross-relations to other coding schemes (e.g., 1335, Tilia platyphyllos (c) = Tilia x vulgaris (c); 2638, Tilia platyphyllos = Tilia cordata x platyphyllos).
  - Many rows map the same taxon to multiple codes or related taxa (e.g., cross-references to Torilis japonica, Tortella tortuosa, Trifolium pratense, Ulex europaeus, Ulmus glabra, etc.).
  - Some codes denote life-stage or context-specific coding (e.g., sapling, seedling, canopy, shrub) and include “seedling/sp.” or species aggregations.

- Coverage and taxonomy
  - The list demonstrates extensive coverage across taxa and life-stages, reflecting ECN’s use of the VESPAN species coding list with cross-references to BRC and other taxonomic concepts.
  - Includes cross-references that support consistency in analysis and interoperability across datasets and platforms.

- Practical usage
  - Enables consistent identification of taxa across sites and time, and supports longitudinal environmental health analyses.
  - Analysts should use the cross-references and life-stage distinctions to harmonize datasets and ensure correct species interpretation.

## Explanatory Information: Quality Codes

- Purpose
  - Provide a standardized set of codes to describe data quality issues, sampling problems, and anomalous conditions affecting data collection, processing, or interpretation.

- Categories and examples
  - Data availability and sampling in the field or lab (e.g., 100 No information available; 101 No sample/reading taken; 102 Sample lost; 103 Partial loss; 104 Sample frozen).
  - Sampling conditions and interference (e.g., 105 Snow in funnel; 106 Snow during sampling; 107 Insects in sample; 119 Construction work in vicinity; 121 Change of land use in vicinity).
  - Field and handling issues (e.g., 123 Clip open; 124 Tubing damaged; 131 Trampling during sampling; 133 Evidence of disease in plot; 134 Significant disturbance).
  - Habitat or management effects (e.g., 145 Coppicing; 146 Thinning; 147 Clear Felling; 149 Wind-throw).
  - Hydrology and climate-related factors (e.g., 169 High river flow; 170 Pond frozen; 180 Trace rainfall; 182 Snow during sampling; 183-187 meteorological/measurement conditions).
  - Non-standard sampling and data handling (e.g., 222 Non-standard sampling date; 223 Non-standard sampling time; 224 Data edited - HYDROLOG code 2; 237-241 taxon identification confidence).
  - Laboratory-related issues (e.g., 501 Laboratory: No sample; 502 Laboratory: Sample lost; 503 Partial loss; 506 Equipment failure; 513 Calculated PPART issues).
  - Confidence in taxon identification (239 High confidence; 240 Medium confidence; 241 Low confidence).

- Unusual events
  - 999 Unusual event - see the quality text, with accompanying text in ECN_VW_qtext.csv to describe specifics.

- Quality text and context
  - For many entries, a separate quality text field provides additional explanations (e.g., descriptive notes for complex or multi-factor events). A dedicated ECN_VW_qtext.csv file stores these narratives.

- Practical usage
  - Use quality codes to interpret outputs, flag data in analyses, and understand limitations due to field/lab conditions.
  - When integrating with other datasets, reference the quality codes and accompanying text to assess data reliability and context.
  - The taxonomy-related codes (239-241) help gauge confidence in species-level identifications and guide downstream analyses.