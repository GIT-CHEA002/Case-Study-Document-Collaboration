## Sequence Diagram — Monthly Drug Cost Report

The Monthly Drug Cost Report Sequence Diagram illustrates the automated process used to generate the monthly drug cost report.

At 17:30 on the last working day of each month, the scheduler triggers the report service. The report service retrieves prescription, drug-cost, and dose-unit information from the appropriate databases. It then aggregates the data and produces the Monthly Drug Cost Report.

The generated report is stored and made available through the healthcare management system.

This diagram provides a dynamic representation of SR-F01, particularly the automated scheduling, data aggregation, and report-generation process.

Related Requirements: SR-F01.
![monthly drug cost report]('./3_Monthly Drug Cost Report.png')