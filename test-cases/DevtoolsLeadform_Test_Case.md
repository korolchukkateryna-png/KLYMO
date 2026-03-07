# DevTools Test Cases – Leave a Request Form

---

##  Network Tests

### TC201
**Title:** Submit form with valid data and verify network request
**Precondition:** User is on "Leave a Request" form page, DevTools → Network tab open
**Test Steps:**
1. Fill all fields with valid data
2. Click "Submit"
3. Observe network request in Network tab
**Expected Result:** POST request sent to correct URL with `Content-Type: application/json`; response status 200; confirmation message appears
**Priority:** High

### TC202
**Title:** Verify server response payload after submission
**Precondition:** User is on "Leave a Request" form page
**Test Steps:**
1. Fill all fields with valid data
2. Submit the form
3. Inspect response payload in Network tab
**Expected Result:** Response body contains `{status: "success", message: "Спасибо, мы с вами свяжемся"}`
**Priority:** High

### TC203
**Title:** Form submission under slow network
**Precondition:** DevTools Network throttling set to Slow 3G
**Test Steps:**
1. Fill all fields with valid data
2. Click "Submit"
3. Observe network request and confirmation message
**Expected Result:** Loading indicator shown; POST request completes successfully; confirmation message displayed
**Priority:** Medium

### TC204
**Title:** Prevent duplicate POST on multiple clicks
**Precondition:** DevTools Network tab open
**Test Steps:**
1. Fill form
2. Click Submit multiple times rapidly
**Expected Result:** Only one POST request sent; confirmation message displayed once
**Priority:** High

### TC205
**Title:** Verify response status codes for invalid submissions
**Precondition:** DevTools Network tab open
**Test Steps:**
1. Leave email invalid
2. Submit form
3. Inspect network response
**Expected Result:** Response contains 400 or relevant validation error code
**Priority:** High

### TC206
**Title:** Cancel network request using DevTools
**Precondition:** DevTools Network tab open
**Test Steps:**
1. Start form submission
2. Quickly click "Cancel" icon in Network tab
**Expected Result:** POST request canceled; no confirmation message shown
**Priority:** Low

### TC207
**Title:** Simulate offline mode during submission
**Precondition:** DevTools → Network → Offline mode
**Test Steps:**
1. Fill all fields
2. Submit form
**Expected Result:** Submission fails gracefully; error message displayed; no network request sent
**Priority:** High

---

##  Console Tests

### TC208
**Title:** Check console for errors during form submission
**Precondition:** DevTools → Console tab open
**Test Steps:**
1. Fill all fields with valid data
2. Click "Submit"
3. Observe Console tab for errors or warnings
**Expected Result:** No JS errors or warnings appear
**Priority:** Medium

---

##  DOM / Attributes Tests

### TC209
**Title:** Inspect DOM structure of form fields
**Precondition:** User is on form page
**Test Steps:**
1. Open DevTools → Elements tab
2. Inspect all input fields (`name`, `id`, `required`) and submit button
**Expected Result:** All fields have correct attributes; submit button is enabled and clickable
**Priority:** Medium

### TC210
**Title:** Verify form field attributes via DevTools
**Precondition:** User is on form page
**Test Steps:**
1. Inspect each input field
2. Verify `maxlength`, `type`, `placeholder`, `required` attributes
**Expected Result:** Attributes correct for each field
**Priority:** Medium

---

##  Keyboard / Focus Tests

### TC211
**Title:** Submit form via Enter key in last field
**Precondition:** User is on form page; all fields filled with valid data
**Test Steps:**
1. Focus on the last input field (Phone)
2. Press Enter key
**Expected Result:** Form submits successfully; network POST request sent; confirmation message displayed
**Priority:** Medium

### TC212
**Title:** Navigate form using Tab key
**Precondition:** User is on form page
**Test Steps:**
1. Press Tab key sequentially through all input fields
2. Observe focus on each field
**Expected Result:** Focus moves correctly from Name → Email → Phone → Submit button
**Priority:** Medium

---

##  UI / Hover Tests

### TC213
**Title:** Hover effects on form fields
**Precondition:** User is on form page
**Test Steps:**
1. Hover over each input field
2. Hover over Submit button
**Expected Result:** Visual hover effects (border/highlight) displayed correctly
**Priority:** Low

### TC214
**Title:** Inspect UI updates after submission via DevTools
**Precondition:** DevTools open
**Test Steps:**
1. Submit valid form
2. Observe DOM changes, confirmation message, and button state
**Expected Result:** Confirmation message visible; form fields disabled or cleared; Submit button enabled after success
**Priority:** Medium

---

##  Storage / Other Tests

### TC215
**Title:** Verify local storage/session storage changes after submission
**Precondition:** DevTools → Application tab open
**Test Steps:**
1. Fill form with valid data
2. Submit form
3. Inspect localStorage/sessionStorage
**Expected Result:** Storage updated if applicable; no sensitive data saved incorrectly
**Priority:** Medium

### TC216
**Title:** Form reset after page reload
**Precondition:** Form submitted successfully
**Test Steps:**
1. Reload page
**Expected Result:** All fields cleared; no duplicate POST requests sent automatically
**Priority:** Medium

