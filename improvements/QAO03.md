**Observation ID:** QAO03

**Title:** Lead form temporarily blocked due to rate-limiting (HTTP 429)

**Type:** System limitation / UX observation

**Severity:** Medium

**Priority:** Medium


## Description
After multiple submissions (approximately 15-20) over time, the server responds with **HTTP 429 (Too Many Requests)** for all lead form attempts, including valid data.

This is a **rate-limiting mechanism** designed to prevent spam, but it impacts testing and may confuse end users.


## Steps Observed

1. Open website in Chrome (normal or Incognito mode).
2. Click **"Автоматизувати"** to open the lead form.
3. Enter valid data in all fields.
4. Click **"Надіслати"**.
5. Repeat submission several times (~15-20).
6. Observe **HTTP 429 Too Many Requests** in DevTools → Network.


## Expected Behavior
- Form submissions should be limited, but users should receive a **clear message**:
`"Too many requests, please try again in X minutes."`
- UX should prevent confusion when testing or during real use.


## Actual Behavior
- Form submission blocked for all data.
- DevTools shows **HTTP 429**.
- No user-friendly message; only generic failure.


## Recommendation
- Document as **QA Observation**.
- Avoid consecutive submissions during testing to prevent triggering rate-limiting.
- Consider displaying a **friendly warning** for users when rate-limiting occurs.