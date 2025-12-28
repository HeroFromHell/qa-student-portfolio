# Test Cases — Expand Testing Practice Site
**Target:** https://practice.expandtesting.com/  
**Scope:** /login, /register, Forgot Password Form  
**Test Period:** Fall 2025  
**Environment:** macOS Tahoe 26.1 | Chrome v131.x | MacBook Pro 14" | 3024×1964

## Legend
- Priority: P1 (High) / P2 (Medium) / P3 (Low)

---

## Login (/login)

**TC-L01 (P1) — Valid login**
- Steps:
  1. Open /login
  2. Enter valid username and password
  3. Click **Login**
- Expected: User is redirected to the secure area and sees a success message.

**TC-L02 (P1) — Valid username + invalid password**
- Steps:
  1. Open /login
  2. Enter valid username and an invalid password
  3. Click **Login**
- Expected: Login is blocked and an error message is displayed.

**TC-L03 (P1) — Invalid username + valid password**
- Steps:
  1. Open /login
  2. Enter an invalid username and a valid password
  3. Click **Login**
- Expected: Login is blocked and an error message is displayed.

**TC-L04 (P1) — Empty username**
- Steps:
  1. Open /login
  2. Leave username empty, enter any password
  3. Click **Login**
- Expected: Login is blocked and a required-field message is shown.

**TC-L05 (P1) — Empty password**
- Steps:
  1. Open /login
  2. Enter any username, leave password empty
  3. Click **Login**
- Expected: Login is blocked and a required-field message is shown.

**TC-L06 (P2) — Leading/trailing spaces in credentials**
- Steps:
  1. Open /login
  2. Enter username/password with leading or trailing spaces (e.g., " practice ")
  3. Click **Login**
- Expected: App handles spaces consistently (either trims or rejects). Record actual behavior.

**TC-L07 (P2) — Multiple failed attempts**
- Steps:
  1. Open /login
  2. Attempt login with invalid credentials 3 times
- Expected: Page remains stable; messaging is consistent; no UI break.

**TC-L08 (P2) — Password field masking**
- Steps:
  1. Open /login
  2. Type into the password field
- Expected: Password characters are masked (e.g., dots/bullets).

**TC-L09 (P2) — Keyboard navigation**
- Steps:
  1. Open /login
  2. Use **Tab** to move through inputs and buttons
  3. Press **Enter** on the Login button (or while focused on it)
- Expected: Focus indicator is visible; navigation order is logical; Enter triggers login.

**TC-L10 (P3) — Refresh behavior**
- Steps:
  1. Open /login
  2. Enter values into fields (do not submit)
  3. Refresh the page
- Expected: Page reloads cleanly. Record whether fields reset or persist.

---

## Register (/register)

**TC-R01 (P1) — Successful registration**
- Steps:
  1. Open /register
  2. Enter a valid username, password, and confirm password
  3. Click **Register**
- Expected: Registration succeeds and a success message is displayed (and/or user is directed to login).

**TC-R02 (P1) — All fields empty**
- Steps:
  1. Open /register
  2. Leave all fields empty
  3. Click **Register**
- Expected: Registration is blocked and a required-field message is displayed.

**TC-R03 (P1) — Empty username**
- Steps:
  1. Open /register
  2. Leave username empty; fill password + confirm password
  3. Click **Register**
- Expected: Registration is blocked and a required-field message is displayed.

**TC-R04 (P1) — Empty password**
- Steps:
  1. Open /register
  2. Fill username; leave password empty; fill confirm password
  3. Click **Register**
- Expected: Registration is blocked and a required-field message is displayed.

**TC-R05 (P1) — Empty confirm password**
- Steps:
  1. Open /register
  2. Fill username + password; leave confirm password empty
  3. Click **Register**
- Expected: Registration is blocked and a required-field message is displayed.

**TC-R06 (P1) — Password mismatch**
- Steps:
  1. Open /register
  2. Fill username
  3. Enter password and a different confirm password
  4. Click **Register**
- Expected: Registration is blocked and a “passwords do not match” message is displayed.

---

## Forgot Password Form

**TC-F01 (P1) — Empty email**
- Steps:
  1. Open the Forgot Password Form page
  2. Leave email empty
  3. Submit the form
- Expected: Submission is blocked and a required-field message is displayed.

**TC-F02 (P1) — Invalid email format**
- Steps:
  1. Open the Forgot Password Form page
  2. Enter an invalid email (e.g., "abc@")
  3. Submit the form
- Expected: Submission is blocked and a validation message is displayed.

**TC-F03 (P2) — Valid email submission**
- Steps:
  1. Open the Forgot Password Form page
  2. Enter a valid email format (e.g., "test@example.com")
  3. Submit the form
- Expected: A confirmation message is shown (e.g., email sent / next steps).

**TC-F04 (P2) — Repeat submission**
- Steps:
  1. Submit the Forgot Password Form with a valid email
  2. Submit again with the same email
- Expected: Page remains stable; confirmation messaging is consistent.

