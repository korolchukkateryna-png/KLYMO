
**Bug ID:** BR04

**Title:** Server returns HTTP 500 when special characters are entered in the Name field

**Type:** Functional / Input Validation

**Severity:** High

**Priority:** High


## Description
When special characters are entered in the **Name** field of the lead form, the request fails and the server returns **HTTP 500 (Internal Server Error)**.

The application should validate user input and reject unsupported characters instead of triggering a server-side error.


## Steps to Reproduce

1. Open the website homepage.
2. Click **"Автоматизувати"** to open the lead form **"Залиште заявку"**.
3. Enter special characters in the **Name** field (for example: `^`, `%`, `@`).
4. Enter a **valid email address**.
5. Enter a **valid phone number**.
6. Click **"Надіслати"**.
7. Open **Chrome DevTools → Network** and observe the request status.


## Expected Result
The system should validate the input and either:
- restrict special characters in the **Name** field, or
- display a validation message indicating invalid input.

The form submission should not cause a server error.


## Actual Result
The form submission fails and the user sees the message **"Помилка відправки"**.

In **Chrome DevTools → Network**, the request returns **HTTP 500 (Internal Server Error)**