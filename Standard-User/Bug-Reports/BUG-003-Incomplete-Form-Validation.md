# BUG-003 — Incomplete Checkout Form Validation

## 📝 Summary

When multiple required fields on the Checkout: Your Information page are left empty, the application displays an error only for the first missing field encountered. The user must submit the form repeatedly to identify and correct each remaining required field.

## 🔗 Related Test Case(s)

- `TC_024` — Checkout validation behavior when multiple required fields are empty

## 🔁 Steps to Reproduce

1. Log in to `saucedemo.com` using the `standard_user` account.
2. Add any product to the cart.
3. Open the Cart page.
4. Click "Checkout".
5. Leave the First Name field empty.
6. Leave the Last Name field empty.
7. Enter a valid Zip/Postal Code.
8. Click "Continue".
9. Observe the validation message.
10. Enter a valid First Name.
11. Click "Continue" again.
12. Observe the next validation message.

## ✅ Expected Result

The application should identify all missing required fields during the form submission and provide clear validation feedback for each missing field. For example, when both First Name and Last Name are empty, the user should be informed that both fields require attention.

## ❌ Actual Result

The application validates the required fields sequentially from top to bottom. When First Name and Last Name are both empty, only the First Name validation message is displayed. After correcting the First Name and submitting the form again, the application then displays the Last Name validation message. The user therefore needs multiple submission attempts to discover all missing required information.

## 🚦 Priority, Severity & Status

| Priority | Severity | Status |
|---|---|---|
| 🟢 Low | Low | Open |

## 🖥️ Environment

- **OS:** Windows 11
- **Browser:** Chrome
- **Platform:** SauceDemo Web Application
- **Account:** `standard_user`
- **Page:** Checkout: Your Information

## 📎 Attachments

- https://github.com/DeemaSalah/QA-Portfolio-Saucedemo/blob/main/Standard-User/Bug-Reports/Attachments/BUG-003(Scenario_A).png

- https://github.com/DeemaSalah/QA-Portfolio-Saucedemo/blob/main/Standard-User/Bug-Reports/Attachments/BUG-003(Scenario_B).png 

## 🏷️ Labels

`Checkout` `Form Validation` `UX` `Usability` `Functional`

## 🧩 Version Info

- **Affected version:** Current publicly available SauceDemo build
- **Fix version:** None

## 📅 Report Details

- **Reported On:** September 10, 2026
- **Reported By:** Deema Salah 
