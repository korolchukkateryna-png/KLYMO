## Observation ID QAO04

**Title:** Unclear error message during network interruption on form submission

**Type:** UX / Content Improvement

**Severity:** Low

**Priority:** Medium

## Description
When the user submits the form without an active internet connection, the system displays a generic error message:
"Помилка відправки. Спробуйте ще раз."

While technically correct, the message does not clearly indicate the actual cause of the issue (no internet connection), which may confuse users.

## Steps Observed
1. Fill all form fields with valid data.
2. Turn off the internet connection.
3. Click "Надіслати".

## Expected Behavior
The system should display a clear and informative error message indicating the problem.
For example:
"Немає інтернет-з’єднання. Будь ласка, перевірте підключення та спробуйте ще раз."

## Actual Behavior
The system displays a generic error message:
"Помилка відправки. Спробуйте ще раз."

The message does not explain the real reason for the failure.

## Recommendation
- Improve error message clarity by specifying the cause (network issue)
- Provide user-friendly guidance (e.g., check internet connection)
- Optionally detect offline state and show a dedicated message
