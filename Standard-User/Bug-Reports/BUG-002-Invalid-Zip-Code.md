# BUG-002 — Invalid Zip Code Accepted During Checkout

## 📝 Summary

The Zip/Postal Code field on the Checkout: Your Information page accepts malformed input, including negative numbers, special characters, and script-like strings. The application does not display validation feedback and allows the user to continue to the next checkout step.

## 🔗 Related Test Case(s)

- `TC_025` — Checkout Zip/Postal Code validation rejects negative numbers, special characters, and malformed inputs

## 🔁 Steps to Reproduce

1. Log in to `saucedemo.com` using the `standard_user` account.
2. Add any product to the cart.
3. Open the Cart page.
4. Click "Checkout".
5. Enter a valid First Name.
6. Enter a valid Last Name.
7. Enter an invalid value such as `-41637` in the Zip/Postal Code field.
8. Click "Continue".
9. Repeat the test using `&&**$%@@` as the Zip/Postal Code.
10. Repeat the test using `<script>alert(1)</script>` as the Zip/Postal Code.
11. Observe the application response.

## ✅ Expected Result

The Zip/Postal Code field should validate the entered value according to the expected postal-code format. Malformed values such as negative numbers, unsupported special characters, or invalid strings should be rejected and an appropriate validation message should be displayed. The user should not be allowed to continue checkout until a valid postal code is entered.

## ❌ Actual Result

The Zip/Postal Code field accepts the tested malformed values without displaying a validation error. The user can click "Continue" and proceed to the Checkout Overview page with the invalid value. No validation message is displayed.

## 🚦 Priority, Severity & Status

| Priority | Severity | Status |
|---|---|---|
| 🟠 Medium | Medium | Open |

## 🖥️ Environment

- **OS:** Windows 11
- **Browser:** Chrome
- **Platform:** SauceDemo Web Application
- **Account:** `standard_user`
- **Page:** Checkout: Your Information

## 📎 Attachments

- https://github.com/DeemaSalah/QA-Portfolio-Saucedemo/blob/main/Standard-User/Bug-Reports/Attachments/BUG-002(Negative%20number-Zip%20Code).mp4

- https://github.com/DeemaSalah/QA-Portfolio-Saucedemo/blob/main/Standard-User/Bug-Reports/Attachments/BUG-002(Special%20Characters-Zip%20Code).mp4

- https://github.com/DeemaSalah/QA-Portfolio-Saucedemo/blob/main/Standard-User/Bug-Reports/Attachments/BUG-002(XSS-Like%20Input-Zip%20Code).mp4

## 🏷️ Labels

`Checkout` `Input Validation` `Zip Code` `Functional` `Security`

## 🧩 Version Info

- **Affected version:** Current publicly available SauceDemo build
- **Fix version:** None

## 📅 Report Details

- **Reported On:** September 10, 2026
- **Reported By:** Deema Salah 
