# Collection method

- Objective and scope: RGB aerial imagery collected for dune area monitoring using an unmanned aerial vehicle (UAV) to support environmental observation and policy-relevant analysis.
- Platform and flight: DJI Mavic Pro 2 UAV, 6-minute flight on 5 February 2020.
- Flight planning and resolution: Planned with Pix4DCapture; ground pixel resolution of 0.01 m (1 cm) per pixel.
- Image overlap: Lateral and longitudinal overlap set to 80% to ensure complete coverage for photogrammetry.
- Ground control: Eight Ground Control Points (GCPs) distributed across the dune (approximately 5.8 GCPs per 100 photos); GCP locations surveyed using a Trimble R8 differential GPS.
- Processing workflow: Orthorectification and mosaicking performed with Pix4Dmapper using a fully automated Structure-from-Motion (SFM) photogrammetry workflow.
- Data quality control: Manual identification of surveyed GCPs in imagery; comparison of GCP coordinates to orthomosaic coordinates yielded a root mean square error (RMSE) of 0.003 m in X, Y, and Z, indicating high relative accuracy.
- Data outputs and structure: Aerial imagery stored as GeoTIFFs; RGB pixel values at 0.01 m resolution.
- Coordinate reference system: WGS84 30N (EPSG:32630; Authority ID: ESPG:32630).