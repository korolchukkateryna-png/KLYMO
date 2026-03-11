***TC301***

**Title:** Verify rate limiting protection on lead form (multiple submissions)

**Precondition:**
User opens the "Залиште заявку" lead form.

**Test Steps:**

1. Open the website homepage.
2. Click the "Автоматизувати" button to open the lead form.
3. Fill in valid data in all fields (Name, Email, Phone).
4. Submit the form.
5. Repeat the submission process multiple times (approximately 15–20 submissions).
6. Observe the response after repeated submissions.
7. Open Chrome DevTools → Network and inspect the request status.

**Expected Result:**
The system should protect the form from excessive submissions using rate limiting.
After multiple submissions, the server may return HTTP 429 (Too Many Requests) to prevent spam or abuse.

**Actual Result:**
After approximately 15 submissions, the server returns HTTP 429 (Too Many Requests).
The form displays a generic error message: "Помилка відправки, спробуйте ще раз".

**Priority:** Low
