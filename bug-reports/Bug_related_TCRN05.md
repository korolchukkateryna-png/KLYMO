**Bug ID:** BR03

**Title:** Server returns HTTP 500 error when extremely long input is entered in the Name field

**Type:** Functional / Backend Validation

**Severity:** High

**Priority:** High


## Description
When a user enters an extremely long value in the **Name** field and submits the lead form, the request fails and the server returns **HTTP 500 (Internal Server Error)**.

The application should validate the maximum allowed input length and prevent submission instead of causing a server-side error.


## Steps to Reproduce

1. Open the website homepage.
2. Click **"Автоматизувати"** to open the lead form **"Залиште заявку"**.
3. Enter an **extremely long string** (e.g., 500+ characters) in the **Name** field.
4. Enter a **valid email address**.
5. Enter a **valid phone number**.
6. Click **"Надіслати"**.
7. Open **Chrome DevTools → Network** and check the request status.


## Expected Result
The system should validate the input length in the **Name** field and display a validation message if the allowed character limit is exceeded.
The request should not cause a server error.


## Actual Result
The form submission fails and the user sees the message **"Помилка відправки"**.
In **Chrome DevTools → Network**, the request returns **HTTP 500 (Internal Server Error)**.
