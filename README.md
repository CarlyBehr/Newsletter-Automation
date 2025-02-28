<img width="914" alt="Screenshot 2025-02-11 at 12 12 06 PM" src="https://github.com/user-attachments/assets/e4cdef30-eea9-4add-a8af-b143c4a1789f" />

Overview
The Newsletter Automation System is a Google Apps Script-based solution that automates the process of sending personalized emails to multiple recipients using data from a Google Spreadsheet. The system is designed to run automatically on a weekly schedule, managing email distribution while maintaining a record of sent messages.
System Components
Google Spreadsheet Structure
The system uses a Google Spreadsheet as its data source with the following columns:

Column A: Recipient email addresses
Column B: Email subject lines
Column C: Email message content
Column D: Sent status tracking

Automation Script
The core automation script handles:

Reading data from the spreadsheet
Validating email addresses
Sending emails via Gmail
Tracking delivery status
Error handling and logging

Key Features
Email Processing

Processes each row in the spreadsheet sequentially
Only sends emails to rows where the "Sent" status is blank
Updates the "Sent" column with a timestamp after successful delivery
Includes error handling for invalid email addresses and failed sends

Data Validation

Validates email addresses using regex pattern matching
Skips empty rows automatically
Checks for required fields before sending

Error Handling

Captures and logs all errors during execution
Updates spreadsheet with error messages for failed sends
Prevents duplicate sends through status tracking

Rate Limiting

Implements a 1-second delay between emails to respect Gmail quotas
Helps prevent throttling and ensures reliable delivery

Automated Schedule

Runs automatically every Monday at 9:00 AM
No manual intervention required after initial setup
Can be manually triggered if needed

Usage Guidelines
Adding New Recipients

Add new rows to the spreadsheet
Fill in recipient email, subject, and message
Leave the "Sent" column blank
The system will process new rows in the next scheduled run

Monitoring

Check the "Sent" column for delivery status
Review any rows marked with "Error" for troubleshooting
Access the Apps Script logs for detailed error information

Maintenance

Regularly archive sent emails by creating a new sheet
Monitor Gmail quota usage
Review and update email templates as needed

Technical Limitations

Subject to Gmail's daily sending limits
Maximum 100 recipients per batch
Message size limited to Gmail's restrictions
Requires Google Workspace or Gmail account permissions

Support and Troubleshooting
For issues, check:

Spreadsheet permissions
Gmail access and quotas
Apps Script execution logs
"Sent" column status messages

Security Considerations

Runs with user's Gmail permissions
Access restricted to authorized spreadsheet users
Email data stored in Google Sheets with Google's security# Newsletter-Automation
