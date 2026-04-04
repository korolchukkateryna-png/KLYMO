## Bug ID BR07

**Title:**Submit form with SQL injection attempt

**Type:**Security / Input Validation

**Severity:**Critical

**Priority:**High

## Description
The form does not properly validate or sanitize input in the "Ваше ім'я" field.
When a SQL injection payload is entered, the system accepts the input and submits the form successfully instead of rejecting or sanitizing the input.

This behavior may indicate insufficient input validation and could potentially expose the system to SQL injection vulnerabilities.

## Precondition
User is on the lead form page.

## Steps to Reproduce
1. Enter the following SQL injection payload in the **"Ваше ім'я"** field:
`' OR 1=1 --`
2. Fill other fields with valid data.
3. Click **"Надіслати"**.

## Expected Result
The system rejects the malicious input or sanitizes it.
The form should not be submitted, and a validation error message should appear.
No system error should occur.

## Actual Result
The form is submitted successfully with the SQL injection payload in the input field.

## Proof of Concept
Payload used during testing:
`' OR 1=1 --`

The payload was accepted and the form submission was completed successfully.

## Potential Risk / Impact
If the backend does not properly sanitize or parameterize database queries, this vulnerability could allow attackers to manipulate database queries.
Potential consequences include:
- Unauthorized data access
- Data leakage
- Data modification
- Database compromise

## Recommendation
Implement strict input validation and sanitization for all form fields.
Use **parameterized queries or prepared statements** on the backend to prevent SQL injection attacks.
Additionally, consider implementing input filtering to block suspicious SQL patterns.