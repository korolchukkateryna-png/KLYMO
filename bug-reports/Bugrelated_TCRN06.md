
## Bug ID: BR05

**Title:** Form accepts special characters in the "Name" field and submits successfully

**Type:** Functional / Validation Bug

**Severity:** High

**Priority:** High

## Description
The lead form allows submission when the **Name** field contains only special characters.
The system does not display any validation warning and successfully submits the form, which indicates missing input validation for the name field.

## Precondition
User is on the lead form page.

## Steps to Reproduce
1. Enter `@@@###$$$%%%` in the **"Ваше ім’я" (Name)** field.
2. Fill the **Email** field with valid data.
3. Fill the **Phone number** field with valid data.
4. Click the **"Надіслати"** button.

## Expected Result
A validation error message should appear indicating that the **Name** field contains invalid characters.
The form should **not be submitted** until valid input is provided.

## Actual Result
The form is **submitted successfully** despite the Name field containing only special characters.
No validation error is displayed.