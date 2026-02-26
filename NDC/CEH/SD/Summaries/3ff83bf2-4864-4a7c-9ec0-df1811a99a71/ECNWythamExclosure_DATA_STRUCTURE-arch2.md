# ECNWythamExclosures vegetation data

## Explanatory Information: Species codes
- Provides crosswalks linking numeric species codes to exact species names, including multiple mappings per code.
- Examples of mappings:
  - 1209: Schistidium strictum = Scirpus cernuus
  - 1210: Schistidium strictum = Scirpus cespitosus
  - 1214: Schistidium strictum = Scirpus setaceus
  - 1220: Schistidium strictum = Scrophularia nodosa
  - 1224: Schistidium strictum = Scutellaria minor
  - 1225: Schistidium strictum = Sedum acre
  - 1237: Schistidium strictum = Senecio erucifolius
  - 1252–1254: Sedum/Silene mappings (e.g., Sedum acre, Silene dioica)
  - 1259: Schistidium strictum = Silene vulgaris
  - 1268, 1270, 1271 etc.: mappings to Solanum dulcamara, Solidago virgaurea, Sonchus spp., Sorbus spp.
  - 3233: Sequoia sempervirens
  - 4396: Scleropodium sp. or Scleropodium
  - 6029–603? and many others: Ulmus procera, and extensive crosswalks to Bry_315 and Vas_ codes
- Includes numerous entries where Schistidium strictum is mapped to multiple plant taxa, often with crosswalks to Bry_315 and Vas_ codes.
- Also includes mappings to higher-level or ambiguous taxa (e.g., Senecio sp., Viola sp.) and to vascular plant codes with crosswalks to standard coded vocabularies (e.g., Bry_315, Vas_x).
- Overall purpose: enable consistent interpretation of species codes across the ECN vegetation datasets, linking short numeric codes to Latin names and established crosswalks.

## Explanatory Information: Quality Codes
- Defines a comprehensive set of quality flags describing data availability, sampling conditions, and potential disturbances.
- Examples of categories and notes:
  - 100–105: No information available, no sample/reading taken, sample lost, partial loss, or freezing at collection.
  - 106–119: Snow in sampling period or in funnel; debris or inconclusive sample issues; environmental/nearby disturbances noted (e.g., bonfires, burning, construction).
  - 120–125: Various in-vicinity conditions or procedural flags (e.g., changes in land use, equipment changes, clipping/opening).
  - 126–179: Field-level disturbances (e.g., non-standard sampling dates/times, trampling, fencing, grazing, mowing, watering, or sampling site obstructions).
  - 180–206: Hydrological or site-level issues (e.g., water level, flow observations, sample preservation, supplementary samples).
  - 207–238: Species- or site-specific notes (e.g., dead taxa, unidentified seedlings, confidence levels in taxon identification).
  - 500s: Laboratory/measurement-related flags (e.g., no sample for lab, contamination, measurement not made due to equipment failure).
  - 513, 999: Specific laboratory-related caveats; 999 indicates an unusual event (detailed in the quality text).
- 999: Unusual event - see the quality text for details.
- These codes, often accompanied by descriptive text in separate quality text files, enable analysts to account for data quality and disturbances when interpreting vegetation data.