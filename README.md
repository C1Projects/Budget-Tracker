# Budget Tracker

A personal, encrypted budgeting and expense-tracking app — built to replace a manually-maintained spreadsheet with something faster, more customizable, and genuinely private.

**[ https://c1projects.github.io/Budget-Tracker/budget-tracker-app.html ]**

## What this is

Budget Tracker is a single-page web app for tracking money in and money out across accounts (bank, cash, debit, credit card) on a month-by-month basis. It's designed to be used the way a checkbook register or a monthly budget spreadsheet would be — but with automatic running totals, category breakdowns, and a visual chart of how your balance moves through the month.

It runs entirely in the browser, works on both desktop and mobile, and installs like a lightweight app when added to a phone's home screen.

## Key features

- **Income and expense tracking** — log transactions by date, account, category, and description.
- **Paycheck splitting** — divide incoming pay across spending, savings, and investment allocations in a single entry.
- **Cash-flagging** — income received as cash or through a non-primary account is automatically flagged as a reminder to reconcile it into your main bank account.
- **Editable history** — past transactions can be edited or deleted, not just appended.
- **Month-by-month view** — a starting balance carries into an automatically calculated ending balance, with per-month savings and investment totals (plus a lifetime total view).
- **Balance flow chart** — a running, day-by-day visualization of account balance across the month.
- **Fully customizable categories and accounts** — add or remove dropdown options for accounts and categories from a Settings tab, no code changes required.
- **CSV export** — export any month's transactions, or an all-time summary, for backup or use in a spreadsheet.

## Security and data storage

Unlike a typical spreadsheet or budgeting app, this project treats privacy as a first-class requirement rather than an afterthought:

- **Client-side encryption.** All transaction data is encrypted (AES-GCM, with a key derived via PBKDF2) before it ever leaves the device. The storage layer never sees plaintext.
- **PIN-based daily access.** A 4-digit PIN unlocks the app for everyday use; a separate, stronger passphrase underlies the actual encryption key, so quick daily access doesn't come at the cost of weak encryption.
- **Auto-lock.** The app re-locks itself after a period of inactivity, clearing the decryption key from memory.
- **Self-hosted sync.** Data syncs across devices via a private GitHub repository that only the account owner controls — there's no third-party server involved and no ongoing cost.

## Status

This is an actively evolving personal project. Expect the feature set (and this README) to keep growing — planned additions include automatic screenshot/receipt reading and further UI refinement.

## License

All rights reserved. See `LICENSE` for details — this code is not licensed for reuse without explicit written permission.
