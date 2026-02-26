# Broad Habitat Area Estimates by Land Class for Great Britain

- National estimates of Broad Habitat stock (Habitats 1-17) for 2007 using the 2007 ITE Land Classification.
- Freshwater habitats were analyzed with a different statistical model than other habitats.
- Data are provided with both tabular and raster formats and accompanied by extensive references and usage notes.

## Data Sets and Formats

- CS007_Broad_Habitat_Stock.csv
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total Area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
      - Note: Negative values may occur due to the statistical model; treat as 0.
    - LOWER_ESTIMATE: Lower 95% CI (000s ha)
    - UPPER_ESTIMATE: Upper 95% CI (000s ha)
- CS2007_Stock.tif
  - Raster dataset with 1 km pixel resolution; each 1 km pixel contains a mean percentage estimate of habitat within that square.
  - Each band corresponds to a Broad Habitat class (mapping described in the data notes).
  - Band mapping example: various Broad Habitat/land class combinations determine band assignment (e.g., Band 2 corresponds to Broad Habitat 2 for some land-class combinations; exact band-to-habitat mapping is detailed in the source notes).
  - Spatial details: 1 km pixels, British National Grid (OSGB1936), Transverse Mercator projection.

## Metadata, Provenance, and Rights

- Source: Countryside Survey data, owned by NERC - Centre for Ecology & Hydrology (CEH).
- Copyright: Countryside Survey © NERC-CEH. All rights reserved.
- Acknowledgement requirements: All use of CS data must include a clear acknowledgment that credits NERC-CEH Countryside Survey data.
- References and methodologies: Includes links and citations to CS technical reports, land classification references (ITE Merlewood), and habitat classification guidance (BAP Broad Habitats).

## Data Quality, Limitations, and Notes

- MEAN_ESTIMATE values are in thousands of hectares; interpret cautiously, especially when negative values occur (treated as 0).
- Freshwater habitats were modeled separately from other habitats; cross-compatibility with other habitat models may require careful methodological alignment.
- The dataset provides both national estimates and per-1 km raster estimates, enabling different scales of analysis but requiring consistent aggregation for comparable outputs.
- Documentation and methodologies are linked to several publications (e.g., CS UK Results 2007, Technical Reports on statistical methods, Land Classification references).

## Access, Use and Attribution

- Usage must acknowledge Countryside Survey data and CEH/NERC ownership.
- Primary publications and CS website provide methodological context and validation details (e.g., CS UK Results from 2007, statistical reports, land-class descriptions).
- The data support analyses of Broad Habitat extents across Great Britain and can be leveraged for mapping and governance, with appropriate metadata and provenance maintained.

## Governance and Stewardship Considerations

- Data Steward responsibilities align with ensuring standards for:
  - Metadata completeness (year, land class, habitat codes/names, area units, estimates, confidence intervals).
  - Provenance tracking (survey year, classification method, modeling approach for freshwater habitats).
  - Clear data lineage and repeatability (linking CSV and raster datasets to the same survey and classification framework).
  - Correct handling of anomalous values (negative MEAN_ESTIMATE should be treated as zero).
  - Proper attribution and licensing across all uses and redistribution.
- Data update considerations:
  - If newer survey waves are released, align metadata fields and maintain consistency with the 2007 ITE Land Classification reference.
  - Ensure interoperability with other Countryside Survey datasets and with global biodiversity/habitat metadata standards.

## References

- Countryside Survey website and reports (methodologies and UK results 2007)
- Carey et al., 2008 (CS UK Results 2007)
- Scott, 2007 (Statistical/Technical reports on national estimates)
- Bunce et al., 1996 (ITE Merlewood Land Classification)
- Jackson, 2000 (Biodiversity Broad Habitat Classification guidance)
- Countryside Survey Field Mapping Handbook (Technical Report No. 1/07)