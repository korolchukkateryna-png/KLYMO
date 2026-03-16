**Observation ID:** QAO02

**Title:** Lead form submission triggers HTTP 500 for invalid inputs

**Type:** Functional / Backend

**Severity:** High

**Priority:** High


## Description
When submitting the lead form with edge-case inputs (e.g., extremely long strings or special characters in the **Name** field), the server responds with **HTTP 500 (Internal Server Error)**.

This indicates **lack of proper backend validation**, as the form should either restrict unsupported inputs or return **400/422** errors instead of crashing.


## Steps Observed

1. Open website homepage.
2. Click **"Автоматизувати"** to open the lead form **"Залиште заявку"**.
3. Enter extreme values in **Name** field (long strings or special characters like `^`, `%`, `@`).
4. Enter a **valid email**.
5. Enter a **valid phone number**.
6. Click **"Надіслати"**.
7. Observe **HTTP 500 Internal Server Error** in Chrome DevTools → Network.


## Expected Behavior
- Frontend or backend should validate the input and prevent submission of invalid data.
- The server should not return **500**, but either:
- block the input with a validation message, or
- return **400 Bad Request / 422 Unprocessable Entity**.


## Actual Behavior
- Form submission fails.
- Server responds with **HTTP 500**.
- User sees **"Помилка відправки"** without details.


## Recommendation
- Document as **QA Observation / backend issue**.
- Backend validation should be implemented to handle edge-case inputs.
- This issue is linked with **rate-limiting (429 errors)** when multiple submissions occur.


