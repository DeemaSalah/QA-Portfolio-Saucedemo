# BUG-001 — Empty Cart Checkout Completion

## 📝 Summary

The checkout flow allows a user to complete an order even when the cart contains no products. The user can proceed through checkout, reach the Overview page with a $0.00 total, and successfully receive the order confirmation.

## 🔗 Related Test Case(s)

- `TC_019` — Checkout is blocked/handled correctly after removing the only item, leaving the cart empty
- `TC_027` — Checkout is blocked/handled correctly when the cart was empty from the start

## 🔁 Steps to Reproduce

1. Log in to `saucedemo.com` using the `standard_user` account.
2. Add any product to the cart.
3. Open the Cart page.
4. Remove the product so the cart becomes empty.
5. Click "Checkout".
6. Enter valid First Name, Last Name, and Zip/Postal Code.
7. Click "Continue".
8. On the Checkout Overview page, click "Finish".
9. Observe the checkout result.

## ✅ Expected Result

The application should prevent the user from completing checkout when the cart contains zero items. The user should either be prevented from entering checkout or shown an appropriate message indicating that at least one product must be added before placing an order.

## ❌ Actual Result

The application allows checkout to continue with an empty cart. The Checkout Overview page displays:

- Item Total: `$0.00`
- Tax: `$0.00`
- Total: `$0.00`

The user can click "Finish" and receives the "Thank you for your order!" confirmation despite no products being purchased.

## 🚦 Priority, Severity & Status

| Priority | Severity | Status |
|---|---|---|
| 🔴 High | High | Open |

## 🖥️ Environment

- **OS:** Windows 11
- **Browser:** Chrome
- **Platform:** SauceDemo Web Application
- **Account:** `standard_user`
- **Page:** Checkout flow

## 📎 Attachments

https://github.com/DeemaSalah/QA-Portfolio-Saucedemo/blob/main/Standard-User/Bug-Reports/Attachments/BUG-001(Empty_Cart).mp4

## 🏷️ Labels

`Checkout` `Cart` `Order Validation` `Functional` `Business Logic`

## 🧩 Version Info

- **Affected version:** Current publicly available SauceDemo build
- **Fix version:** None

## 📅 Report Details

- **Reported On:** September 10, 2026
- **Reported By:** Deema Salah 
