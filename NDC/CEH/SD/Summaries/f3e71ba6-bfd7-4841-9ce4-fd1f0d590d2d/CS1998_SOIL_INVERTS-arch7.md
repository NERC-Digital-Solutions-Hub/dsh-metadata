# Soil invertebrate data 1998 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey (GB) for soil invertebrates (mesofauna) in 1998.
- Samples collected from soil cores at 0–8 cm depth, across up to 256 one-kilometre squares.
- Provides counts for numerous taxa, plus derived ecological metrics and location metadata.
- All CS data use must be acknowledged; data copyrighted by NERC CEH.

## Data content and structure
- Core data are in CS1998_SOIL_INVERTS.csv.
- Spatial and sampling framework:
  - SQUARE: 1 km square sampling site code (text)
  - PLOT: Plot within each square (one of 5 plots) (text)
  - YEAR: Survey year (number)
- Taxon counts (example, many taxa listed):
  - ACTO, ARAN, CHTO, CHGE, CHLI, COLA, COAD, COEN, CONE, COPU, COSM, COPE, DIPP, DIPL, DILA, DIAD, GAST, HEMI, HYME, ISOP, LEAD, LELA, NEMA, NEMM, OLIG, OPIL, PAUR, PROT, PSEU, PSOC, PULM, SYMP, THYP, THYN, TOTAL_CATCH
- Summary metrics (per core):
  - COLL_TOTAL, AC_COLL_TOTAL, MC_RATIO
  - TOTAL_TAXA (taxa richness), SHANNON (diversity index)
  - LC07, LC07_NUM (ITE Land Classification 2007)
  - COUNTRY, COUNTY07, EZ_DESC_07
- Additional metadata:
  - TOTAL_CATCH, TOTAL_TAXA, SHANNON, and various taxon-specific counts
  - Text and numeric fields to support GIS joins and mapping

## Sampling, laboratory methods, and processing
- Field collection:
  - Soil cores collected and processed using a dry Tullgren extraction method.
  - Extraction period: 5 days; heat source and 70% ethanol preservative.
  - Fauna identified to major taxa (level 1); Collembola and mites identified to morphotype level.
- Laboratory protocols:
  - Standard methods documented in CS2000 Field Handbook.
  - Detailed sample coding, processing dates, and keys used are recorded.

## Quality control and data management
- Adherence to established biolytical protocols; project log books maintained.
- Quality control:
  - One in twenty samples rotated between staff to compare identifications.
  - Selected samples additionally checked by taxonomic specialists for validation.
- Documentation:
  - Complete sample metadata in dedicated notebooks (species list, counts, processing date, sample code).
  - Data entered weekly into databases, then copied to CD-ROMs and stored securely (fireproof cabinet or off-site).

## Spatial and temporal scope
- Temporal coverage: Survey year 1998.
- Spatial coverage: Great Britain; up to 256 1 km squares; 0–8 cm soil depth.
- Data suitable for GIS applications at 1 km resolution, with associated land-class and geographic descriptors.

## GIS applications and considerations
- Suitable for map-based visualizations of:
  - Taxon counts and totals by square/plot
  - Taxa richness (TOTAL_TAXA) and Shannon diversity
  - Derived metrics (MC_RATIO, AC_COLL_TOTAL, COLL_TOTAL)
  - Landscape context via LC07 (ITE Land Class 2007) and EZ_DESC_07
  - Location context via COUNTRY, COUNTY07
- Considerations:
  - Data are from 1998; may require temporal alignment with other datasets.
  - 1 km resolution; depth limited to 0–8 cm; some taxa identified only to major taxa or morphotype.
  - Data standardization and consistent attribution are important when combining with other sources.

## Data usage, rights, and citations
- Acknowledgement requirement:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Data/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Usage references and related publications are available through the Countryside Survey resources (e.g., MASQ, ITE Land Classification GB 2007, and Countryside Survey UK results).

## References and related resources
- Countryside Survey project general overview and methodologies.
- Key methodological and classification references:
  - MASQ: Monitoring and Assessing Soil Quality in Great Britain
  - ITE Land Classification of Great Britain (1996, 1981, 2007)
  - Countryside Survey: UK Results from 2007
- Field and data handling handbooks (CS2000 Field Handbook; laboratory QC procedures).
- Data centre and access links:
  - Countryside Survey website and CEH data centre entries
  - NERC Environmental Information Data Centre entries for land classification datasets