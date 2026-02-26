# Natural enemies of crop pests in oilseed rape fields in relation to local plant diversity and landscape characteristics

## Overview
- Field study conducted in 2013 and 2014 in the Wessex region of southern England, focusing on winter-sown oilseed rape (Brassica napus) and how local plant diversity and landscape context relate to natural enemies of crop pests.
- Data collected via three complementary sampling methods:
  - Suction sampling for canopy parasitoids (Hymenoptera: Parasitica).
  - Pitfall trapping for ground-dwelling natural enemies (Carabidae, Staphylinidae, etc.) and spiders.
  - Water traps for monitoring pest larvae prevalence.
- Local habitat and landscape characteristics mapped using GIS, including field margins, hedges, grassland types, and semi-natural habitats within radii of 0.5 to 3 km around sampling points.
- Dataset designed to be used alongside other Wessex BESS WP4 datasets to enable integrated analyses.

## Dataset components and data structure
- NERCPestNatEnSpeciesList.csv
  - Taxonomic details: Order, Family, Genus, Species; SpeciesCode as a linking key.
  - CollMeth indicating collection method (Pitfall or Suction).
  - Gender field (M/F) recorded only for Hymenoptera; not consistently recorded for other groups.
- NERCPitfall.csv
  - Pitfall trap data with Unique SampleCode per sample, SurveyDate, SampleNo, PointCode.
  - Columns 5–312: counts for individual species; links to NERCPestNatEnSpeciesList.csv via SpeciesCode.
  - Known issues: several pitfalls knocked over; some data missing.
- NERCSuctionSample.csv
  - Suction sampling data with PointCode linking to landscape survey data.
  - Columns 2–33: counts for species observed in suction samples; links to NERCPestNatEnSpeciesList.csv via SpeciesCode.
  - Known issues: field 3.1 transects affected by crop conditions; some data gaps.
- NERCWaterTrap.csv
  - Water-trap data for pest larvae; includes SampleCode, PointCode, SurveyDate, SampleNo, and counts for Meligethes, Dasineura, Ceutorhynchus.
  - Includes derived counts for parasitized larvae and ectoparasites (e.g., MelWTerHet, DasWEcto, CeuWPara).
- NERCNatEnLandscapeSurvey.csv
  - Landscape-scale data per survey point: TransectID, FarmID, FieldID, Year, and a suite of habitat and crop metrics.
  - Local habitat measures: InCropSppRich, MarginPlantSppRich, IPSpeciesCount, AvgPercentCoverIP, field edge and margin dimensions, hedge metrics, and field edge margins.
  - Landscape context metrics across multiple radii (0.5–3 km) for:
    - Intensive grassland (IG…)
    - Restored grassland (Res…)
    - Species-rich grassland (SppRich…)
    - Arable land (TotAra…)
    - Semi-natural habitat (SN…)
    - Derived interaction metrics (IGArea, IGDist, ResArea/Dist, SppRichArea/Dist, etc.)

## Data collection methods and timing
- Field sampling across 12 fields per year, with transects located to capture hedged and hedgeless edges.
- Plant diversity assessed with five 1 m² quadrats near transects; crop plant diversity measured with sampling points inside the crop.
- Sampling windows:
  - Suction sampling: late June–mid July 2013; late May–mid June 2014.
  - Pitfall traps: two 4-day periods in 2013 and 2014.
  - Water traps for pest larvae assessed concurrently with canopy sampling.
- Taxonomic identification references used for key groups (e.g., Ferguson 2010; Joy 1932; Lott 2009/2011; Luff 2007; Rodwell 1992; Stace 1997).

## Metadata, standards, and linking
- Key linking field across datasets: SpeciesCode (found in NERCPestNatEnSpeciesList.csv) to join to NERCPitfall.csv and NERCSuctionSample.csv.
- Data dictionaries and file-level metadata provided, including field definitions, units, and collection methods.
- Taxonomic and methodological standards referenced for identification and data recording.
- GIS-derived landscape variables produced from CEH Land Cover Map 2007, PHI, and local NVC surveys; field-verification within a 1 km buffer.

## Data quality and provenance
- Protocols for field and lab data collection established; data entry conducted in MS Access with validation checks.
- Data quality assurance performed by trained personnel (R. Shaw) with ongoing protocol adherence.
- Documented data quality notes:
  - Gender data missing for most non-Hymenoptera groups.
  - Some traps and transects missing or damaged (e.g., field 3.1 transects).
  - Missing data reported for several pitfall and water-trap records.
- Ethics approval obtained: CLES Penryn Research Ethics Committee (application 2014/622).

## Ethics, rights, and usage
- Dataset is part of the Wessex BESS project and is intended for integration with other WP4 datasets.
- Data handling follows approved ethics protocol; explicit licensing or reuse terms are not stated in the document and should be confirmed for redistribution or downstream use.

## Governance and data stewardship considerations
- Data stewardship actions to support reuse:
  - Maintain and publish the linking key (SpeciesCode) across NERCPestNatEnSpeciesList.csv, NERCPitfall.csv, and NERCSuctionSample.csv.
  - Preserve metadata detailing collection methods, dates, transect design, and GIS-derived variables.
  - Track data quality issues (missing data, damaged transects) and document remediation steps or caveats in analyses.
  - Ensure clear versioning and provenance for all five CSV files; record updates and corrections.
  - Consider licensing terms and data access controls if datasets are to be shared beyond the originating project.
- Interoperability considerations:
  - Some fields are to be treated as categorical (e.g., SampleNo) or require standardization of units and classifications.
  - Taxonomic authorities and species naming conventions should be maintained to avoid drift in linking keys.

## Practical notes for data users
- The dataset enables analyses linking natural enemy assemblages and pest larvae with local plant diversity and landscape structure at multiple spatial scales.
- Cross-dataset analyses depend on robust linking via SpeciesCode and PointCode/SampleCode; careful handling of missing data is required.
- The presence of detailed landscape metrics (IG, Res, SppRich, TotAra, SN, etc.) across 0.5–3 km buffers supports multi-scale ecological investigations in arable landscapes.

## References
- Ferguson, A., et al. (2010). Key Parasitoids of the Pests of Oilseed Rape in Europe: A Guide to Their Identification. In Biocontrol-Based Integrated Management of Oilseed Rape Pests.
- Joy, N. H. (1932). A practical handbook of British beetles.
- Lott, D.A. (2009, 2011). The Staphylinidae of Britain and Ireland; The Staphylinidae in Britain and Ireland (further parts).
- Luff, M.L. (2007). The Carabidae of Britain and Ireland.
- Morton, D., et al. (2011). Final Report for LCM2007 - the new UK Land Cover Map.
- Roberts, M. J. (1993). The spiders of Great Britain and Ireland.
- Rodwell, J. S. (1992). British Plant Communities; Stace, C. (1997). New flora of the British Isles.
- Toynton, P., & Ash, D. (2002). Salisbury Plain grassland study.
- Walker, K., & Pywell, R. F. (2000). Grassland communities on Salisbury Plain Training Area.