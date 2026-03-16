- The request is blocked by the server due to too many submissions.

---

## Expected Result
Rate limiting should remain active for security purposes, but the **user-facing message should clearly explain the issue**, for example:

- "Too many requests. Please try again later."
- "You have submitted the form too many times. Please wait a few minutes before trying again."

This would improve **user experience and transparency**.

---

## Notes
- The behaviour appears to be **intentional server-side spam protection**, not a functional bug.
- However, the **error message UX can be improved**.
- This observation was discovered during **manual form validation testing**.

---

## Severity
Low (Security feature working correctly)

## Priority
Low / UX Improvement

---

## Related Testing
Security / Abuse Prevention Testing
