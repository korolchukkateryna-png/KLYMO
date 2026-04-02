## Bug ID: BR04

### Title
No message about limit or validation 

### Type
Validation(Functional_

### Severity
Medium

### Priority
High

### Description
The "name" field is accept any numbers of characters 

### Precondition
User opens the lead form.

### Steps to Reproduce
1. Enter 20+ characters into «Ваше ім'я»
2. Enter valid email.
3. Enter valid phone
4. Click «Надіслати»


### Expected Result
Expected Result: Form does not break UI, input is limited or validation message appears

### Actual Result
The form is submitted successfully without any warning.