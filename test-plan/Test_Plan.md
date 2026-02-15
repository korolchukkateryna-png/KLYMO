# Test Plan for KLYMO – AI Prompt Generator
## 1️⃣ Overview
This **test plan** defines the detailed testing approach for the **KLYMO web application**, an AI prompt generator. It outlines the scope, objectives, testing approach, and deliverables to ensure the application functions correctly and provides a smooth user experience.
---
## 2️⃣ Objectives
- Verify that all **interactive UI elements** work correctly
- Ensure navigation and workflow function as intended
- Detect JavaScript errors using Developer Tools
- Validate that AI prompt generation works as expected
- Document any issues and unexpected behaviour
---
## 3️⃣ Scope
**In Scope:**
- Functional testing of frontend elements (buttons, forms, menus, links)
- UI behaviour in **Chrome** on Windows 11 Pro
- Checking browser console for errors and warnings
- Exploratory testing for unexpected behaviours
**Out of Scope:**
- Backend logic or API functionality
- Performance, load, or security testing
- Other browsers (optional future testing)
---
## 4️⃣ Testing Approach
- **Type of Testing:** Manual Black Box Testing
- **Techniques:**
- Step-by-step functional testing
- Exploratory testing to discover unexpected issues
- Verification using Developer Tools for console errors
- Using sample prompt inputs from the `test-data` folder
---
## 5️⃣ Test Environment
- **Operating System:** Windows 11 Pro
- **Browser:** Google Chrome (latest version)
- **Network / Location:** Ireland
- **Tools:** Chrome Developer Tools, GitHub for documentation
---
## 6️⃣ Test Data
- Input examples: sample AI prompts stored in `test-data` folder
- Data covers normal inputs and edge cases
---
## 7️⃣ Entry & Exit Criteria
**Entry Criteria:**
- UI is accessible and functional in Chrome
- README.md and folder structure exist
- Sample test data available
**Exit Criteria:**
- All test cases and checklists executed
- All discovered issues documented in `BUG_REPORTS.md`
- Test plan completed and verified
---
## 8️⃣ Deliverables
- `TEST_PLAN.md` – this document
- `TEST_CASES.md` – detailed step-by-step test cases
- `CHECKLIST.md` – quick verification checklist
- `BUG_REPORTS.md` – list of all issues
- Screenshots or supporting evidence in `assets/screenshots`
---
> **Note:**
> This test plan is focused on **manual frontend testing** using Black Box techniques. It provides a structured approach to ensure that the KLYMO web application is functional, reliable, and user-friendly.