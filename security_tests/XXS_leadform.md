## TC302

**Title:** Verify protection against script injection (XSS)

**Precondition:**
User opens the "Залиште заявку" lead form.

**Test Steps:**

1. Open the website homepage.
2. Click the "Автоматизувати" button.
3. In the **Name** field enter:

<script>alert('test')</script>

4. Enter valid Email and Phone values.
5. Click **"Надіслати"**.

**Expected Result:**
The system should sanitize the input and prevent execution of any script.
The script must not execute in the browser.

**Priority:** High
