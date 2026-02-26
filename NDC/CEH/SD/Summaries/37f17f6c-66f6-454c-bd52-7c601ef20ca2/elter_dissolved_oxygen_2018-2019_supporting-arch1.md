# Elter_dissolved_oxygen_2018-2019.txt

## Overview
- Daily average dissolved oxygen concentration (DO_conc, μg L -1) measured at Elterwater Inner basin's deepest point (Lat: 54.4287°, Long: -3.0350°) from May 2018 to December 2019.
- Measurements taken at 3 m and 5 m depth from the surface, with data collected every 15 minutes.
- Sensor type: PME miniDOT oxygen sensors (Precision Measurement Engineering, USA) using a fluorescence method.
- Sensors feature anti-fouling wipers to reduce biofilm buildup. Accuracy is stated as 0.3 mg L -1.

## Data structure
- Columns: Date (yyyy-mm-dd), Depth (m), DO_conc (μg L -1).

## Data collection details
- Raw data: 15-minute intervals.
- Processed data: daily averages of the raw 15-minute measurements.

## Data processing and QC
- Some small gaps in raw QCed data were linearly interpolated (gap < 3 hours).

## Potential uses
- Time-series analyses of DO fluctuations at shallow depths within the deepest point of the basin.
- Comparative analysis between 3 m and 5 m depth to assess vertical DO gradients.
- Diurnal, seasonal, and trend analyses over May 2018–December 2019.
- Inputs for ecological or hydrological models focusing on water quality in the Elterwater basin.

## Quality considerations and caveats
- DO_conc values are reported in μg L -1, with sensor accuracy noted as 0.3 mg L -1 (unit discrepancy to be mindful of during analyses).
- Interpolation introduces estimated values for small gaps (up to 3 hours); longer gaps remain unfilled.
- Data represent a single location (deepest point) and may not reflect broader basin conditions.