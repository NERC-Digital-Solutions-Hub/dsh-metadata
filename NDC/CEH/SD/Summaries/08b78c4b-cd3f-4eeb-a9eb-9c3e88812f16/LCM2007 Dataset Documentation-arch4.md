# Land Cover Map 2007 Dataset Documentation

- A parcel-based UK land cover dataset (LCM2007) providing 23 classes tied to UK Broad Habitats, built from 20–30 m satellite imagery.
- Replaces LCM2000 with improved spatial framework using OSMM/generalised cartography and image segmentation; maps land cover (not strictly land use).
- Products include vector data and raster datasets (25 m and 1 km), with GB and Northern Ireland (NI) data distinguished and projected separately.

## Key data products and structure

- Vector data set
  - About 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - 10 attributes per polygon, including Parcel_ID, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE (class for display), Knowledge-Based Enhancements (KBE), ProbList, CorePixels, Construct, TotPixels.
  - Unique Parcel_ID per polygon, enabling unambiguous communication; recommended to retain this field.
  - Broad Habitat sub-classes (BHSub) provide additional tonal/class information but are not as robust as the main LCM2007 classes; recommended validation if used.
- Raster data sets
  - 25 m and 1 km products derived from the vector data.
  - GB and NI provided in separate projections; 1 km rasters provide dominant class and percentage cover (for 23 classes and for 1 km Aggregate classes).
  - Data volumes are large (e.g., GB vector ~4.13 GB in 100 km × 100 km shapefile; GB 25 m raster ~1.36 GB).

## LCM2007 classifications and mapping

- 23 LCM2007 classes based on Broad Habitats; some Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
- The dataset is thematically validated at 23-class level; Appendix 2 describes the cross-walk between Broad Habitats, LCM2007 classes, and their sub-classes.
- 1 km rasters aggregate the 25 m results into:
  - Dominant cover at 1 km (class and aggregate class)
  - Percentage cover at 1 km (class and aggregate class)

## Data quality and validation

- Ground reference validation: 9,127 polygons analyzed; average accuracy ~83%.
- Local discrepancies may occur; accuracy figures are averages across polygons and do not guarantee uniform accuracy across all areas or classes.
- Quality assurance (QA) is strongest at the 23 LCM2007 class level; Broad Habitat sub-classes have lower assurance and should be validated by users if used.

## Data access and licensing

- Data access:
  - 1 km raster data sets available via the CEH Information Gateway.
  - Full vector product and the 25 m raster product available under licence on request from CEH.
- Access process:
  - Complete online application at CEH data portal or contact spatialdata@ceh.ac.uk.
  - Licence fees may apply depending on use and application.

## Technical specifications

- Map projections
  - Great Britain: British National Grid (OSGB36), Transverse Mercator.
  - Northern Ireland: Irish National Grid; NI data moving toward ITM (Ireland Transverse Mercator).
- File sizes and formats
  - Vector data: large due to ~10 million polygons; size varies by format (e.g., 100 km × 100 km shapefile GB ~4.13 GB; NI ~433 MB).
  - Raster data: 25 m and 1 km products; formats include GeoTIFF; GB NI projections differ as noted.
- Minimum mapping unit and generalisation
  - Minimum mappable area > 0.5 ha; parcels < 0.5 ha and lines < 20 m are dissolved into surrounding landscape during production.

## Use guidance for data systems and workflows

- LCM2007 is suitable for broad-scale land cover analyses and for aligning with policy-relevant Broad Habitats.
- The 23-class product is recommended for high-quality thematic analyses; 1 km aggregates offer a lighter-weight option for national-scale modeling.
- Because data volumes are large (especially vector), choose raster products when processing constraints exist or when metadata overhead is a concern.
- Use Parcel_ID and extensive polygon metadata to track provenance, processing history (KBE), and spectral class probabilities (ProbList) for model validation and interpretation.
- Be mindful that Broad Habitat sub-classes are auxiliary and not covered by the primary QA; validate if used for decision-making.

## Practical notes and limitations

- LCM2007 maps land cover, not guaranteed land use; spectral signatures may misrepresent actual land use in some cases.
- Some grassland classes (Neutral/Calcareous Grassland) can be misclassified as Improved Grassland; users should consult Morton et al. 2011 for detailed guidance.
- Montane and inland rock delineations rely on altitude or soil data where appropriate, which may affect classification validity for certain analyses.
- Small patches and features below the minimum mapping unit may be underrepresented; users needing fine-grained details should consider 25 m vector/raster outputs or supplementary data sources.

## Appendices and mapping references

- Appendix 1: LCM2007 class descriptions and brief definitions (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, etc.).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode crosswalks).
- Appendix 3: Colour mapping recipes used in the Final Report (Morton et al., 2011) for visualization.

## Additional references

- Morton, D. et al. 2011. Final Report for LCM2007 – the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson, D.L. 2000. Guidance on interpretation of Biodiversity Broad Habitat Classification. JNCC Report 307.