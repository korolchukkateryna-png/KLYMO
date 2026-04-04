## Bug ID: BR06

**Title:** Form accepts script injection attempt in the "Name" field (XSS vulnerability)

**Type:** Security Bug (Input Validation / Potential XSS)

**Severity:** High

**Priority:** High

## Description
The lead form accepts a script injection payload in the **Name** field and allows the form to be submitted successfully.
The application does not validate or sanitize the input before submission. This behavior may indicate a potential **Cross-Site Scripting (XSS)** vulnerability if the data is later rendered in the UI or stored and displayed elsewhere.

## Precondition
User is on the lead form page.

## Steps to Reproduce
1. Enter the following payload in the **"Ваше ім’я"** field:
`<script>alert('test')</script>`
2. Enter valid data in the **Email** field.
3. Enter valid data in the **Phone number** field.
4. Click the **"Надіслати"** button.

## Expected Result
- Script tags should be **sanitized or rejected**.
- The form should **display a validation error**.
- The form **should not be submitted**.

## Actual Result
The form is **submitted successfully** with the script payload in the Name field.
No validation or sanitization occurs.

## Proof of Concept (PoC)
Payload used during testing:
<script>alert('test')</script>

## Potential Risk / Impact
If this input is later displayed in the UI without proper escaping, it may lead to **Cross-Site Scripting (XSS)** which could allow attackers to:
- execute arbitrary scripts in the browser
- steal session data
- manipulate page content

## Recommendation
- Implement **server-side input validation** for the Name field.
- Sanitize user input by escaping HTML/script tags.
- Restrict the field to **alphabetic characters and basic punctuation only**.
