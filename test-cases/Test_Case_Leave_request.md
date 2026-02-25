# Test Cases: Leave your request

## Positive Test Cases

### TCR01
**Title:** Submit form with valid data
**Precondition:** User is on the «Залиште заявку» form page
**Test Steps:**
1. Enter valid name in «Ваше ім'я» field
2. Enter valid email in «e-mail» field
3. Enter valid phone number in «Телефон» field
4. Click «Надіслати» button

**Expected Result:** Form submits successfully, success message appears, form resets

**Priority:** High

### TCR02
Title: Submit form with minimal valid input length
Precondition: User is on the «Залиште заявку» form page
Test Steps:
1. Enter minimal allowed length name (e.g., 2 characters) in «Ваше ім'я»
2. Enter valid email
3. Enter minimal valid phone number
4. Click «Надіслати»
Expected Result: Form submits successfully, success message appears
Priority: High

### TCR03
Title: Submit form with maximum allowed input length
Precondition: User is on the form page
Test Steps:
1. Enter maximum allowed characters in «Ваше ім'я»
2. Enter long but valid email address
3. Enter maximum allowed phone length
4. Click «Надіслати»
Expected Result: Form submits successfully without UI breaking
Priority: Medium

### TCR04
Title: Name field accepts hyphenated and double names
Precondition: User is on the form page
Test Steps:
1. Enter name with hyphen (e.g., Anna-Maria)
2. Enter valid email
3. Enter valid phone number
4. Click «Надіслати»
Expected Result: Form submits successfully
Priority: Medium

### TCR05
Title: Email field accepts subdomain email
Precondition: User is on the form page
Test Steps:
1. Enter email with subdomain (e.g., user@mail.company.com)
2. Fill other fields with valid data
3. Click «Надіслати»
Expected Result: Form submits successfully
Priority: Medium

### TCR06
Title: Phone field accepts number with country code and spaces
Precondition: User is on the form page
Test Steps:
1. Enter phone number with country code and spaces (e.g., +380 99 123 45 67)
2. Fill other fields with valid data
3. Click «Надіслати»
Expected Result: Form submits successfully
Priority: Medium

### TCR07
Title: Form submission via Enter key
Precondition: User filled all fields with valid data
Test Steps:
1. Focus on last field («Телефон»)
2. Press Enter key
Expected Result: Form submits successfully
Priority: Medium

### TCR08
Title: Successful submission does not duplicate request on page refresh
Precondition: Form was successfully submitted
Test Steps:
1. Submit form with valid data
2. Refresh the page
Expected Result: Form is not resubmitted automatically, no duplicate request created
Priority: High

### TCR09
**Title:** Cross-browser check
**Precondition:** User is on the form page
**Test Steps:**
1. Open form in Chrome, Edge, and Firefox
2. Perform basic submission with valid data
**Expected Result:** Form works correctly across browsers, success message appears
**Priority:** Medium




## Negative Test Cases

### TCRN01
**Title:** Leave all fields empty and submit
**Precondition:** User is on the form page
**Test Steps:**
1. Leave «Ваше ім'я» empty
2. Leave «e-mail» empty
3. Leave «Телефон» empty
4. Click «Надіслати»
**Expected Result:** Validation messages appear for all fields, form does not submit
**Priority:** High

### TCRN02
**Title:** Enter only whitespace in all fields
**Precondition:** User is on the form page
**Test Steps:**
1. Type spaces only in «Ваше ім'я»
2. Type spaces only in «e-mail»
3. Type spaces only in «Телефон»
4. Click «Надіслати»
**Expected Result:** Validation messages appear, fields are treated as empty, form does not submit
**Priority:** High

### TCRN03
**Title:** Enter invalid email format
**Precondition:** User is on the form page
**Test Steps:**
1. Enter invalid email (e.g., "example.com", "abc@")
2. Fill other fields with valid data
3. Click «Надіслати»
**Expected Result:** Validation message appears for email, form does not submit
**Priority:** High

### TCRN04
**Title:** Enter invalid phone number
**Precondition:** User is on the form page
**Test Steps:**
1. Enter letters or symbols in «Телефон» field
2. Fill other fields with valid data
3. Click «Надіслати»
**Expected Result:** Validation message appears for phone, form does not submit
**Priority:** High


### TCRN05
Title: Submit form with extremely long name input
Precondition: User is on the form page
Test Steps:
1. Enter 20+ characters into «Ваше ім'я»
2. Enter valid email
3. Enter valid phone
4. Click «Надіслати»
Expected Result:
Form does not break UI, input is limited or validation message appears
Priority: High



### TCRN06
Title: Submit form with special characters in name field
Precondition: User is on the form page
Test Steps:
1. Enter "@@@###$$$%%%" in «Ваше ім'я»
2. Fill other fields with valid data
3. Click «Надіслати»
Expected Result:
Validation error appears, form is not submitted
Priority: High



### TCRN07
Title: Submit form with script injection attempt (XSS)
Precondition: User is on the form page
Test Steps:
1. Enter `<script>alert('test')</script>` in «Ваше ім'я»
2. Fill other fields with valid data
3. Click «Надіслати»
Expected Result:
Script is not executed, input is sanitized, form is not submitted
Priority: High



### TCRN08
Title: Submit form with SQL injection attempt
Precondition: User is on the form page
Test Steps:
1. Enter `' OR 1=1 --` in «Ваше ім'я»
2. Fill other fields with valid data
3. Click «Надіслати»
Expected Result:
Form rejects input or sanitizes it, no system error occurs
Priority: High



### TCRN09
Title: Submit form with invalid email edge cases
Precondition: User is on the form page
Test Steps:
1. Enter "test@.com"
2. Enter valid name and phone
3. Click «Надіслати»
Expected Result:
Validation message appears, form is not submitted
Priority: High



### TCRN10
Title: Submit form with phone containing letters
Precondition: User is on the form page
Test Steps:
1. Enter "ABCDEF123" in «Телефон»
2. Fill other fields with valid data
3. Click «Надіслати»
Expected Result:
Validation error appears, form is not submitted
Priority: High



### TCRN11
Title: Rapid multiple clicks on submit button
Precondition: All fields contain valid data
Test Steps:
1. Click «Надіслати» 5–10 times very quickly
Expected Result:
Only one request is sent, no duplicate submissions
Priority: High



### TCRN12
Title: Network interruption during submission
Precondition: All fields contain valid data
Test Steps:
1. Turn off internet connection
2. Click «Надіслати»
Expected Result:
User sees error message, system does not crash
Priority: Medium
