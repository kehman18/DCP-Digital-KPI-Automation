WORKFLOW ONE
Form submission → KPI calculation → validation → exception alert

WORKFLOW TWO
Daily schedule → daily management summary

WORKFLOW THREE
Manager requests date → retrieve and return historical report

WORKFLOW ONE → AUTOMATION WORKFLOW FOR THE EXCEPTION CASES

Operator submits Daily Production Form
↓
Response enters Google Sheets
↓
Google Sheets Trigger starts n8n
↓
n8n reads the new row
↓
Checks mandatory values
↓
Calculates Production Achievement and Variance
↓
Looks for related downtime record
↓
Calculates Availability
↓
Checks validation and exception rules
↓
Assigns Severity
↓
Identifies Responsible Team
↓
Creates stakeholder alert
↓
Sends email or Teams message
↓
Records alert as Sent

WORKFLOW TWO → DAILY MANAGEMENT SUMMARY

Operator submits Daily Production Form
↓
Response enters Google Sheets
↓
Google Sheets Trigger starts n8n
↓
n8n reads the new row
↓
Returns Daily Management Summary
↓
Through the Chosen Media Channel

STANDARD ALERT FORMAT
Alert ID
Date and Time
Plant
Production Line
Equipment or Process Stage
KPI
Acceptable Threshold
Actual Result
Variance
Availability
Downtime Hours
Severity
Possible Cause
Responsible Area
Recommended Action
Response Deadline
Alert Status

Plant Manager report
PLANT PERFORMANCE EXCEPTION

Plant: Obajana
Production Line: Line 2
Reporting Date: 14 July 2026

Production Achievement: 70.00%
Acceptable Threshold: 95.00%
Expected Cement Output: 5,000 tons
Actual Cement Output: 3,500 tons
Production Variance: -1,500 tons

Availability: 78.00%
Acceptable Availability: 85.00%
Downtime: 5.28 hours

Severity: Very Critical
Primary Exception: Production below target
Possible Cause: Bag shortage and packing plant stoppage
Responsible Area: Warehouse
Recommended Action: Confirm bag inventory, replenish packing materials, and restore packing operations
Escalation Status: Escalated to Warehouse and Operations
Resolution Status: Open

Production and Operations Team report

PRODUCTION EXCEPTION

Plant: Obajana
Production Line: Line 2
Process Stage: Cement Production

Production Achievement: 70.00%
Acceptable Threshold: 95.00%
Cement Target: 5,000 tons
Cement Actual: 3,500 tons
Production Variance: -1,500 tons

Clinker Target: 4,100 tons
Clinker Actual: 3,900 tons
Packing Actual: 3,200 tons

Availability: 78.00%
Downtime: 5.28 hours
Severity: Very Critical

Possible Cause: Packing plant interruption
Supporting Cause: Bag shortage
Responsible Area: Warehouse
Recommended Action: Coordinate material replenishment and recover lost production time

Mechanical Maintenance Team report

MECHANICAL DOWNTIME EXCEPTION

Plant: Ibese
Production Line: Line 3
Equipment: Cement Mill
Equipment ID: IBS-L3-CML

Planned Runtime: 24.00 hours
Actual Runtime: 17.50 hours
Downtime: 6.50 hours
Availability: 72.92%
Acceptable Availability: 85.00%

Downtime Type: Unplanned
Downtime Reason: Bearing failure
Output Impact: 1,420 tons

Severity: Very Critical
Responsible Area: Mechanical
Recommended Action: Inspect bearing assembly, raise corrective work order, replace defective component and confirm restart
Required Response: Immediate
Resolution Status: Open

Electrical Team report

ELECTRICAL EXCEPTION

Plant: Obajana
Production Line: Line 1
Equipment: Cement Mill
Equipment ID: OBJ-L1-CML

Planned Runtime: 23.00 hours
Actual Runtime: 18.00 hours
Downtime: 5.00 hours
Availability: 78.26%
Acceptable Availability: 85.00%

Downtime Type: Unplanned
Downtime Reason: Motor overload
Output Impact: 1,130 tons

Severity: Critical
Responsible Area: Electrical
Recommended Action: Inspect motor load, electrical protection, cabling and reset conditions before restart
Required Response: Within 30 minutes
Resolution Status: Open

Utilities Team report

UTILITIES EXCEPTION

Plant: Gboko
Production Line: Line 2
Equipment: Power System

Planned Runtime: 24.00 hours
Actual Runtime: 18.85 hours
Downtime: 5.15 hours
Availability: 78.54%

Downtime Reason: Generator switchover delay
Production Impact: 1,528 tons

Severity: Critical
Responsible Area: Utilities
Recommended Action: Review generator readiness, switchover procedure and standby power response time
Escalation Level: Plant Manager
Resolution Status: Open

Warehouse report

WAREHOUSE MATERIAL EXCEPTION

Plant: Obajana
Production Line: Line 3
Process Stage: Packing
Equipment: Packing Plant

Cement Produced: 6,421 tons
Cement Packed: 5,160 tons
Packing Gap: -1,261 tons
Packing Achievement: 80.36%

Downtime: 2.63 hours
Downtime Reason: Bag shortage
Output Impact: 279 tons

Severity: High
Responsible Area: Warehouse
Recommended Action: Confirm available bag inventory, initiate emergency replenishment and review reorder level
Escalation Status: Warehouse Manager notified
Resolution Status: Open

Packing and Logistics Team report

PROCESS PERFORMANCE EXCEPTION

Plant: Gboko
Production Line: Line 1
Process Stage: Kiln

Clinker Target: 5,500 tons
Clinker Actual: 4,420 tons
Clinker Variance: -1,080 tons
Clinker Achievement: 80.36%

Availability: 83.00%
Downtime: 4.08 hours
Severity: High

Possible Cause: Unstable kiln operation or feed interruption
Responsible Area: Process
Recommended Action: Review operating parameters, kiln feed consistency and the associated downtime record
Resolution Status: Under Review

Data Quality and Reporting Team report

DATA QUALITY EXCEPTION

Plant: Obajana
Production Line: Line 2
KPI Category: Production
KPI Name: Clinker_Actual_Tons

Reported Value: 4,769 tons
Expected Minimum: 5,281 tons
Expected Maximum: 6,161 tons

Validation Result: Warning
Data Quality Score: 75%
Issue Type: Below Range Warning
Data Quality Dimension: Accuracy

Severity: Medium
Responsible Area: Data Reporting
Recommended Action: Reconcile the kiln production log with clinker stock movement before approving the daily report
Audit Status: Requires Review
Publication Status: Hold Until Validated
