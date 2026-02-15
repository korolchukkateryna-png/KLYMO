# Test Strategy for KLYMO – AI Prompt Generator
## 1️⃣ Overview
This **test strategy** defines the approach for testing the **KLYMO web application**, an AI prompt generator. The testing focuses solely on the **user interface (UI)**, using **Black Box Testing** techniques. The purpose is to ensure that all visible features work correctly and that the website provides a smooth, error-free user experience.
---
## 2️⃣ Scope
**In Scope:**
- Frontend functionality: buttons, navigation, forms, and interactive elements
- UI behaviour and layout consistency in **Chrome** on Windows 11 Pro
- Error messages, pop-ups, and validation
- Browser console logs via Developer Tools (checking for JavaScript errors)
**Out of Scope:**
- Backend functionality and APIs
- Database interactions
- Performance, security, or stress testing
---
## 3️⃣ Testing Approach
- **Type of Testing:** Black Box / Functional Testing
- **Techniques:**
- Manual testing of all interactive elements
- Exploratory testing for unexpected behaviours
- Developer Tools inspection for console errors and warnings
- Optional cross-browser testing (currently only Chrome is used)
---
## 4️⃣ Test Environment
| Item | Details |
|------------|---------------------------------|
| Operating System | Windows 11 Pro |
| Browser | Google Chrome (latest) |
| Location / Network | Ireland |
| Tools | Chrome Developer Tools, GitHub |
---
## 5️⃣ Test Data
- Input data consists of example prompts for AI generation
- Sample test inputs will be stored in the `test-data` folder
---
## 6️⃣ Entry & Exit Criteria
**Entry Criteria:**
- UI is accessible in Chrome
- README and folder structure for QA portfolio are in place
**Exit Criteria:**
- All defined test cases and checklists have been executed
- All bugs found are documented in the Bug Reports folder
---
## 7️⃣ Deliverables
- `TEST_STRATEGY.md` – this document
- `TEST_PLAN.md` – detailed test plan
- `TEST_CASES.md` – step-by-step test cases
- `CHECKLIST.md` – quick test checklist
- `BUG_REPORTS.md` – all found issues
- Screenshots or videos in `assets/screenshots` (if needed)
---
> **Note:**
> This strategy focuses on **manual Black Box testing** for the frontend only. Even without access to backend APIs, it ensures the **stability, usability, and functionality** of the KLYMO web application.

