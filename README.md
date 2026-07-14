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
