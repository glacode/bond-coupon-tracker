# BondCoupon Tracker 📈

A lightweight, privacy-focused **Single Page Application (SPA)** designed to manage bond portfolios and audit coupon payments. 

This tool is specifically built to help investors verify that every expected coupon has been correctly credited to their bank account, with a focus on fixed-income instruments like **BTPs**, Treasury Bonds, and Corporate Bonds.

## ✨ Key Features

* **Portfolio Management**: Track nominal amounts, purchase dates, and maturity schedules.
* **Automated Coupon Calculation**: Built-in formula for semi-annual coupons (optimized for the **12.5% tax rate** used for Government Bonds).
* **Reconciliation Engine**: Automatically flags missing payments by cross-referencing "Expected" vs. "Confirmed" coupons.
* **Time-Travel Filter**: View your open positions at any specific date in the past or future.
* **Privacy by Design**: 
    * **100% Client-Side**: Your financial data never leaves your computer.
    * **No Server/Database**: Uses browser `LocalStorage` for persistence.
    * **Zero Dependencies**: No heavy frameworks—just pure HTML, Tailwind CSS, and Vanilla JavaScript.

## 🚀 Getting Started

Since this is a portable SPA, there is **no installation required**.

1.  **Clone or Download** the repository.
2.  Open `index.html` in any modern web browser (Chrome, Firefox, Safari, Edge).
3.  (Optional) Host it for free via **GitHub Pages** to access it from your mobile device.

## 🛠 How It Works

### 1. Register Your Purchases
Input your bond details. The app uses the following formula to estimate your net semi-annual coupon:

$$NetCoupon = \frac{NominalAmount \times (CouponRate / 100) \times 0.875}{2}$$

### 2. Log Received Payments
Enter the date and amount whenever you receive a coupon credit in your bank account.

### 3. Audit & Reconcile
The **Reconciliation** section automatically generates a list of all expected coupons from your purchase date to the current day. If a payment is not found in the same month/year in your "Confirmed" list, it will be highlighted in **red** as `MISSING`.

## 💾 Data Persistence & Portability

* **LocalStorage**: Your data is automatically saved in your browser's local storage.
* **JSON Export**: Click **Export JSON** to download a backup of your data.
* **JSON Import**: Move your data between different browsers or operating systems (Windows/Linux) by importing your backup file.

> [!WARNING]
> Since data is stored in your browser's local cache, clearing your browsing data may delete your records. **Always keep a JSON backup** of your data!

## ⚖️ License

Distributed under the **MIT License**. This tool is provided "as is" for tracking purposes only. Always cross-reference with your official bank statements and consult a professional for financial advice.

---
*Created with a focus on simplicity and financial transparency.*