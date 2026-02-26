# XTekCT

## Overview
- Configuration file for Skate 1 CT imaging (XTekCT), detailing acquisition, geometry, detector, processing, and X-ray settings.

## Geometry and Acquisition
- Projections: 1080
- Initial angle: 132.173 degrees
- Angular step: 0.333314456403047 degrees
- Region: Start (0,0); RegionPixels (2000,2000)
- Voxel grid: 2000 x 2000 x 2000
- Voxel size: 0.125079053120795 mm in X, Y, and Z
- Source-to-object distance: 733.918815612793
- Source-to-detector distance: 1173.528
- Centre of rotation: Top 0.0, Bottom 0.0; AutomaticCentreOfRotation = true
- White level: 60000.0
- Scattering: 0.0
- Coefficient terms: X2=0.25, X1=0.75 (X4, X3, X0 = 0)

## Detector and Pixels
- Detector resolution: 2000 x 2000 pixels
- Detector pixel size: 0.2 x 0.2 mm
- Detector offset: (0.0, 0.0)

## Processing and Scaling
- Scale: 1.32
- Normalisation: 1.0
- InterpolationType: 1
- MedianFilterKernelSize: 1
- OutputUnits: /m
- Units: mm
- TIFFScaling: 1
- LowPercentile: 0.2; HighPercentile: 99.8
- AutoScalingType: 0
- ImportConversion: 0

## Shuttling and CT Pro settings
- Shuttling: False
- CTPro: FilterPreset=0; Filter_ThicknessMM=0.000; Filter_Material=None

## X-ray settings
- X-rays: kV=120; μA=145

## Notes for Monitoring Frameworks (relevance)
- The file provides a complete, reproducible set of acquisition and reconstruction parameters, aiding traceability of environmental health measurements if used for monitoring.
- Key metadata include geometry, projection count, angles, detector specs, and driving energy/current.
- Potential governance considerations: ensure explicit units, materials in CTPro, and provenance/versioning of parameter files; assess data-sharing implications of raw/processed data and their metadata.