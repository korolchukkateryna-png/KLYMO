# Test Cases Leave Your Request – Positive Cases

| Test Case ID | Title | Coverage Status |
|--------------|-------|--------------------------|
| TCR01 | Submit form with valid data |✅ |
| TCR02 | Submit form with minimal valid input length |❌ phone number field accepts less than required symbols,no validation warning shown |
| TCR03 | Submit form with maximum allowed input length |✅ |
| TCR04 | Name field accepts hyphenated and double names|✅ |
| TCR05 | Email field accepts subdomain email | ✅|
| TCR06 | Phone field accepts number with country code and spaces | ✅ |
| TCR07 | Form submission via Enter key | ✅|
| TCR08 | Successful submission does not duplicate request on page refresh |✅ |
| TCR09 | Cross-browser check |✅ |


# Test Cases Leave Your Request – Negative Cases

| Test Case ID | Title | Coverage Status |
|--------------|-------|--------------------------|
| TCRN01 | Submit form with empty fields | ✅|
| TCRN02 | Enter only whitespace in all fields | ✅|
| TCRN03 | Enter invalid email format |✅ |
| TCRN04 | Enter invalid phone number |✅ |
| TCRN05 | Submit form with extremely long name input |❌ had no limited or validation message |
| TCRN06 | Submit form with special characters in name field |❌ the form is submit successfully |
| TCRN07 | Submit form with script injection attempt (XSS) |❌ the form is submit successfully |
| TCRN08 | Submit form with SQL injection attempt |❌ the form is submit successfully |
| TCRN09 | Submit form with invalid email edge cases |✅ |
| TCRN10 | Submit form with phone containing letters |❌ the form is submit successfully |
| TCRN11 | Rapid multiple clicks on submit button |✅ |
| TCRN12 | Network interruption during submission |✅this case got improvment |

