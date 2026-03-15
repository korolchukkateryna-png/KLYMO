## TC303

**Title:** Verify protection against SQL injection attempts

**Precondition:**
User opens the lead form.

**Test Steps:**

1. Open the lead form.
2. In the **Name** field enter:

' OR 1=1 --

3. Enter valid Email and Phone values.
4. Click **"Надіслати"**.

**Expected Result:**
The system should treat the input as plain text and safely process the request.
No database errors or unexpected behavior should occur.

**Priority:** High