# Quality Assurance of botanical recording CS2007 Countryside Survey

- Purpose
  - Assess consistency and reliability of botanical recording across plots in the CS2007 survey.
  - Compare 2007 QA with previous QA exercises (1990, 1998) to gauge changes in data quality.
  - Focus on eight plot types and 266 plots across 44 squares.

- Methodology and scope
  - QA sample: one quarter of each of 44 1-km squares; 266 plots across eight plot types.
  - Plot types include: X (200 m2), Y (4 m2), U (unenclosed), R (road verges), H (hedges), S (streamsides), B (boundaries), A (arable margins).
  - Data collection: CS surveyors recorded plots in the field; QA assessors recorded blind using standard sheets, then compared lists and covers. In 2007, a subset was also recorded on a computer tablet to assess tablet-related errors.
  - Plot relocation: assessed relocation efficiency using sketch maps, photos, and metal detector plates.

- Key findings on data quality
  - Plot relocation and plate recovery
    - CS2007: ~86% overall plot relocation success (70% relocated precisely, ~16% adequately repositioned; 14% unsatisfactorily located).
    - Plate relocation by CS2007 assessors: ~36.4% recovered; long-term plate recovery higher when comparing to earlier QA (1990: ~65%, 1998: ~69%), with the same assessors.
    - Photos and sketches were crucial for locating plots when plates were difficult to relocate.
  - Species richness (per plot)
    - CS2007 surveyors: 17.5 species/plot; QA assessors: 21.7 species/plot.
    - CS surveyors recorded about 80% of species present, with the shortfall most pronounced in small U and Y plots; hedges and arable plots had better performance (≈94–96% of QA).
    - Bryophytes and cryptogams were particularly under-recorded (cryptogams only 40.2% of the QA level).
  - Accuracy and mis-matches in species records
    - Total records: CS2007 and QA2007 combined = 6511; correct/common to both lists = 3745; mis-matches = 2766.
    - Major sources of error: overlooked species within plots (48.9% of mis-matches), location/orientation errors (14.5%), mis-identifications (7%), seasonal/management changes also contribute.
    - Relative to previous QA, mis-matches due to location/orientation declined; overlook rate increased.
  - Tablet vs paper recording
    - Tablet test (90 plots): about 2% of entries contained errors; notable omissions (~10% of overlooked species across full QA) and some erroneous records due to incorrect codes or improbable taxa.
    - Tablet errors contributed to some “unknown” or unlikely records and may have led to over-writing other records.
  - Species frequency and abundance
    - Several common species were under-recorded by CS surveyors (e.g., many grasses and bryophytes), while some over-recorded species included Poa trivialis and certain grasses.
    - Cover values tended to be higher in CS surveyor records than QA assessors for many species; many discrepancies in high-cover assignments tied to identification timing or misallocation on tablets.
  - Cryptogams and uplands
    - Cryptogams had a strong impact on upland plot accuracy; omitting cryptogams increases overall agreement/accuracy.
  - Change detection implications (1990–2007)
    - CS surveyors show declines in species richness over time (1990–2007), while QA assessors show less pronounced declines; overall,QA assessments consistently record more species than CS surveyors.
  - Overall agreement and accuracy
    - Percentage agreement (shared species relative to total species lists): 65.6% for CS2007 vs QA2007 (lower than 1998: 73.1%; 1990: 79.3%).
    - With adjustments for seasonal, management, and location changes, accuracy could be higher by approximately 5–6%.

- Data quality metrics and interpretation
  - Efficiency and agreement metrics
    - Percentage agreement and percentage efficiency measured per plot type and landscape category.
    - Variation exists across plot types; arable and hedge plots tended to show higher agreement.
  - Landscape and plot-type effects
    - upland squares showed broader variation and lower agreement, partly due to cryptogam recording difficulties.
    - Arable and hedge plots performed relatively better.
  - Frequency of occurrence analyses
    - Identified species with notable discrepancies in frequency between CS surveyors and QA assessors (e.g., grasses and bryophytes more prone to under-recording by CS surveyors).

- Recommendations for future surveys and GIS data products
  - Plot and plate practices
    - Avoid erecting new plates when the original cannot be found; note non-findings and rely on best available data rather than adding new plots.
  - Cryptogams and grasses
    - Increase training emphasis on identifying cryptogams and vegetative grass forms; cryptogams are critical in upland plots.
  - Data capture and tablet use
    - Default presence/absence or simplified input to reduce tablet-entry errors; improve taxonomy entry with faster, guided selection (e.g., letter-based suggestions for genus/species).
  - Photos, sketches, and plot positioning
    - Emphasize capturing clear photos and including key background features; verify photo placement on plot sketches; verify hedge/streamside plot side and boundary context to prevent orientation errors.
  - Data quality and metadata
    - Document QA results alongside the main dataset to aid users in assessing reliability and potential biases, especially for cryptogams and high-cover assignments.
  - Permanent plots and relocation
    - Where possible, use permanent quadrats to reduce relocation errors and improve comparability across years.
  - Training and assessor selection
    - Consider pairing surveyors with more experienced observers; emphasize standardized procedures to reduce inter-operator variability.

- Implications for GIS and map-based data products
  - Spatial accuracy: relocation and orientation errors can affect plot georeferencing; include QA flags and uncertainty estimates for each plot/record.
  - Attribute accuracy: species lists and cover values show systematic biases (under-recording, over-recording, cryptogams impact); incorporate quality indicators and cryptogam flags.
  - Temporal comparability: when integrating CS2007 with prior years, account for differences in data quality and potential seasonal/management effects.
  - Metadata and provenance: document QA procedures, dataset versions, tablet vs paper data capture, and known limitations to support reliable analyses and reproducibility.

- Reference notes
  - The report covers QA results, methods, tables, and annexes detailing mis-match categories, frequency analyses, percentage agreement/accuracy by plot type and landscape, and tablet error analysis.
  - It situates CS2007 QA in the context of prior QA exercises (1990, 1998) and discusses implications for long-term vegetation monitoring and data utility in GIS applications.