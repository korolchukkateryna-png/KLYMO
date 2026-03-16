# AI Resume Generator Test Cases

## Positive

### TC-RG-01
**Title:** Generate resume with default options

**Precondition:** User is on AI Resume Generator page

**Steps:**
1. Select role: Менеджер
2. Select experience: Початковец
3. Select format: Класичний
4. Select AI model: DeepSeek V3
5. Click **Згенерувати**

**Expected Result:** Prompt is generated correctly, reflects selected options, output visible

### TC-RG-02
**Title:** Generate resume with custom role & format

**Precondition:** User is on AI Resume Generator page

**Steps:**
1. Enter custom role: Аналітик
2. Select experience: Середній
3. Select format: Креативний
4. Select AI model: Gemini 2.5 Pro
5. Click **Згенерувати**

**Expected Result:** Output contains correct custom role, format, and experience context

### TC-RG-03
**Title:** Generate resume after using **Нова генерація**

**Precondition:** User has already generated one prompt

**Steps:**
1. Click **Нова генерація**
2. Select new options (role / experience / format / AI model)
3. Click **Згенерувати**

**Expected Result:** Output updates according to new selections; remaining generations counter decreases

### TC-RG-04
**Title:** Buttons functionality

**Precondition:** Generated prompt is visible

**Steps:**
1. Click **Оцінити промпт**
2. Click **Навчитись промптам**
3. Click **Нова генерація**

**Expected Result:** Each button works correctly; modals open; prompts updated; no crashes

---

## Negative

### TC-RG-N01
**Title:** Attempt generation with empty required fields

**Precondition:** User is on AI Resume Generator page

**Steps:**
1. Leave role or experience unselected
2. Click **Згенерувати**

**Expected Result:** Warning appears; generation blocked

### TC-RG-N02
**Title:** Input unsupported characters in role/format fields

**Precondition:** User is on AI Resume Generator page

**Steps:**
1. Enter emojis, control codes, or special symbols in role/format fields
2. Click **Згенерувати**

**Expected Result:** Input sanitized or error shown; system does not crash

### TC-RG-N03
**Title:** Exceed remaining generations

**Precondition:** Remaining generations = 0

**Steps:**
1. Click **Згенерувати**

**Expected Result:** User notified about generation limit; prompt not generated

### TC-RG-N04
**Title:** Rapid consecutive generation

**Precondition:** User is on AI Resume Generator page

**Steps:**
1. Click **Згенерувати** multiple times rapidly

**Expected Result:** System handles requests gracefully; output generated correctly for first click

### TC-RG-N05
**Title:** API / network failure

**Precondition:** Simulate offline or API failure

**Steps:**
1. Attempt to generate prompt

**Expected Result:** User-friendly error message appears; system does not crash