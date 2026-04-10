## Bug ID
BR08

**Title:**Form accepts letters in the phone number field and submits successfully

**Type:**Functional / Validation Bug

**Severity:**High

**Priority:**High

## Description
The phone number field allows input containing alphabetic characters and does not validate the format.
The form is successfully submitted even when invalid phone data is entered, which indicates missing or incorrect validation for the phone field.

## Precondition
User is on the lead form page.

## Steps to Reproduce
1. Enter `ABCDEF123` in the "Phone number" field.
2. Fill other fields with valid data.
3. Click "Надіслати".

## Expected Result
A validation error message should appear indicating that the phone number format is invalid.
The form should **not be submitted** until valid input is provided.

## Actual Result
The form is **submitted successfully** even when the phone number contains letters.
No validation error is displayed.

## Potential Risk / Impact
- Invalid contact data may be stored in the system or CRM
- Users cannot be contacted due to incorrect phone numbers
- Decreased data quality and reliability of collected leads
- Negative impact on business processes (missed leads, communication issues)

## Recommendation
- Implement strict validation for the phone number field (allow only numeric input and valid formats)
- Add both client-side and server-side validation
- Display a clear validation message when invalid input is entered
- Optionally enforce a format (e.g., minimum/maximum length, country code)