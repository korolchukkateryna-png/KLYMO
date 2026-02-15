# Test Cases for KLYMO – Main Page
---
### Test Case ID: TC01
**Title:** Header Buttons Functionality
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Click "Рішення" button
2. Click "Генератор" button
3. Click "Про нас" button
4. Click "Блог" button
**Expected Result:** Each button navigates to the correct section/page. No errors occur.
**Priority:** High
---
### Test Case ID: TC02
**Title:** Language Switcher
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Click "Українська" button
2. Click "English" button
3. Click "Русский" button
**Expected Result:** Page content changes according to selected language. Layout remains intact.
**Priority:** High
---
### Test Case ID: TC03
**Title:** "Автоматизувати" Button in Header
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Click "Автоматизувати" button in the header
**Expected Result:** User is redirected to the automation section/page without errors.
**Priority:** High
---
### Test Case ID: TC04
**Title:** AI Prompt Input Box
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Type a valid prompt in "Що хочете зробити?" input box
2. Press Enter or click suggested prompt
**Expected Result:** Prompt is accepted; suggestions appear; AI response is generated correctly.
**Priority:** High
---
### Test Case ID: TC05
**Title:** Training Promotion Section
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Scroll to "Хочете створювати промпт як професіонал?" section
2. Click "Дізнатись про навчання" button
**Expected Result:** User is redirected to training details page. No errors occur.
**Priority:** Medium
---
### Test Case ID: TC06
**Title:** Business Automation Section
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Scroll to "Готови ано автоматизувати ваш бізнес" section
2. Click "Автоматизувати" button
**Expected Result:** User is redirected to automation page. No errors occur.
**Priority:** Medium
---
### Test Case ID: TC07
**Title:** Footer Product Links
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Scroll to footer
2. Click each product link: "Продукты", "Клира", "Клим", "Клио"
**Expected Result:** Each link navigates to the correct product page/section.
**Priority:** Medium
---
### Test Case ID: TC08
**Title:** Footer Service Links
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Click each service link: "Послуги", "Интеграция", "Аудит", "Навчання", "Инструменты", "Генератор промптов"
**Expected Result:** Each link navigates to the correct service page/section.
**Priority:** Medium
---
### Test Case ID: TC09
**Title:** Footer Company Links
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Click each company link: "Компания", "Про нас", "Блог", "FAQ", "Контакты"
**Expected Result:** Each link navigates to the correct page.
**Priority:** Medium
---
### Test Case ID: TC10
**Title:** Social Media Links
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Click each social icon: Telegram, Instagram, LinkedIn, YouTube
**Expected Result:** Each icon opens the correct social media page in a new tab.
**Priority:** Low
---
##  Basic Negative Test Cases
### Test Case ID: TC11
**Title:** Invalid Input in Prompt Box
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Type invalid characters (symbols, random characters) in the prompt box
2. Press Enter
**Expected Result:** System either ignores invalid input or shows an error message. No crash occurs.
**Priority:** High
---
### Test Case ID: TC12
**Title:** Clicking Links Before Page Loads Fully
**Pre-conditions:** User has refreshed the page
**Test Steps:**
1. Immediately click header/footer buttons before page fully loads
**Expected Result:** Buttons navigate correctly or show loading feedback. Page does not crash.
**Priority:** Medium
---
### Test Case ID: TC13
**Title:** Rapid Language Switching
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Click language buttons rapidly multiple times
**Expected Result:** Page content remains consistent, no broken text or layout errors occur.
**Priority:** Medium
---
### Test Case ID: TC14
**Title:** Empty or Whitespace Input in Prompt Box
**Pre-conditions:** User is on the main page
**Test Steps:**
1. Click on the "Що хочете зробити?" input box
2. Type only whitespace
3. Press Enter
4. Leave the field completely empty and press Enter
**Expected Result:**
- System does not crash
- User sees a warning message indicating invalid input **or** the input field remains empty
**Priority:** High