# Penllwyn Rain gauge read me document

## Overview
- A maintenance and data quality log for the Penllwyn rain gauge, documenting installation, readings anomalies, equipment upkeep, and time-stamp adjustments from 2006–2007.

## Chronology of data quality issues and events
- 25/01/06: Rain gauge installed.
- 03/10/06: Last reading recorded as 1349 while laptop showed 1441 GMT; ~52 minutes out. Reset performed.
- Feb/07: Data considered dodgy due to significant snow; wind-blown snow likely not recorded properly.
- 30/04/07: Battery, seal, and desiccant on Tinytag replaced.
- 31/10/07: Wind blew the tipping bucket, affecting readings (11:20).
- 30/11/07: Wind blew tipping bucket again (10:36); some water present in the bucket.
- 22/12/07: Around 8 hours of readings with implausibly high values; Tinytag maxing out. Possibly due to cold; bowl weirboxes also had issues.
- 03/11/07: Time stamp issue with overlap from previous download; time adjusted to follow on after last record. Adjustments reflected in the Excel file.

## Data handling and provenance
- Readings come from a Tinytag device; some corrections and adjustments were made post-download.
- Time-related discrepancies and anomalous readings were noted and addressed, with corrections documented in an Excel file to preserve provenance.

## Maintenance and operational actions
- Regular maintenance included battery, seal, and desiccant replacement (30/04/07).
- Time synchronization issues were identified and corrected in the data record (03/11/07), with explicit note that adjustments are reflected in the Excel file.

## Implications for data governance (actionable takeaways for data leaders)
- Ensure robust timestamp synchronization between sensors and data collection systems.
- Implement validation for implausible readings and timestamp overlaps to trigger rapid review.
- Maintain clear data provenance by recording raw vs. corrected values and linking corrections to source logs.
- Document environmental factors (wind, snow, cold) that can bias sensor readings and establish guidelines for when data should be flagged or excluded.
- Schedule and document regular equipment maintenance (batteries, seals, desiccants) to minimize data quality issues.
- Consider improved monitoring during extreme weather (e.g., wind events) or explore redundant sensors to mitigate single-point failures.

## Endnotes
- The log primarily covers 2006–2007, with noted adjustments reflected in the accompanying Excel file.