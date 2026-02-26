# UAV RGB images dataset from core protected areas of the UNESCO Rhön Biosphere Reserve

## Overview
- UAV-derived RGB imagery for European beech (Fagus sylvatica) forest within core protected areas of the UNESCO Rhön Biosphere Reserve.
- Collected in September 2020 using a DJI Phantom 4 RTK.
- Dataset comprises eight GeoTiff files (two per site: Ortho RGB mosaics and corresponding DEMs) provided via the NERC Field Spectroscopy Facility (FSF).

## Data Collection (Methods)
- Sites and dates:
  - Site 1a: 09 Sept 2020, 17:35–18:12, cloudy with slight intensity changes.
  - Site 1b: 09 Sept 2020, 10:15–11:05, clear sky, light wind.
  - Site 1c: 09 Sept 2020, 12:46–13:30, clear sky, strong winds.
  - Site 2: 10 Sept 2020, 11:05–12:35, changeable sky (cloudy/sunny), wind data not provided.
- Sensor: DJI Phantom 4 RTK.
- Core protected areas within the Rhön Biosphere Reserve.

## Data Structure, Nature and Units
- Files (GeoTIFF, 8-bit for imagery):
  - 20200909_Site1a_RGB_DEM.tif
  - 20200909_Site1a_RGB_Ortho.tif
  - 20200909_Site1b_RGB_DEM.tif
  - 20200909_Site1b_RGB_Ortho.tif
  - 20200909_Site1c_RGB_DEM.tif
  - 20200909_Site1c_RGB_Ortho.tif
  - 20200910_Site2_RGB_DEM.tif
  - 20200910_Site2_RGB_Ortho.tif
- Each site includes:
  - Ortho mosaic (RGB) with approximately 3 cm pixel size (0.03 m).
  - DEM (Digital Elevation Model) with pixel size ~10 cm (0.10 m).
- Coordinate Reference System: WGS 84 / UTM zone 32N (meters).
- Data provenance: mosaicked images provided by the NERC Field Spectroscopy Facility (FSF).

## Quality Control and Provenance
- Quality Assurance conducted by NERC FSF prior to mosaic creation.
- For details or requests for the underlying data, contact fsf@nerc.ac.uk.

## Data Access and Use
- The eight GeoTIFF mosaics are available as the published dataset.
- Underlying data not included in this release; requests should be directed to the FSF contact above.

## Governance and Stewardship Considerations for Data Stewards
- Ensure metadata capture includes: site identifiers (1a, 1b, 1c, 2), date/time windows, sensor model, processing steps, CRS, pixel resolutions, and QA status.
- Maintain clear data lineage: source imagery, processing to ortho and DEM, and QA approvals.
- Clarify data sharing terms and access points (FSF contact) for any requests to underlying data.
- Verify consistency across formats (GeoTIFF) and ensure alignment with other datasets in the catalogue (CRS, resolution, extents).

## Potential Limitations and Risks
- Some time windows lack wind information; environmental conditions vary by site.
- Sky conditions ranged from cloudy to clear, which may affect remote sensing analyses.
- Large data volumes and multiple formats across sites may pose interoperability and transfer challenges if expanding beyond the provided two-file-per-site structure.