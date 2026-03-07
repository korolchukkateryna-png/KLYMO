

**ID:** BR01

**Type:** Input Validation

**Title:** Phone number field accepts less than required digits

**Precondition:** User is on the main page.

**STR:**
1. Click on the "Автоматизувати" button.
2. The "Залиште заявку" form appears.
3. Enter minimal characters for Name, Email, and Phone fields (e.g., Name: "Aa", Email: "1@yandex.ru", Phone: "8").
4. Click the "Надислати" button.

**Expected Result:**
Phone number field shows a validation warning; submission is blocked until a valid phone number is entered.

**Actual Result:**
Form is submitted successfully; no warning is shown for the phone number field.

**Severity:** Medium

**Priority:** Medium-High

**Notes:**
Phone number field works incorrectly; no minimum digit validation is enforced. Can lead to invalid data submission.
