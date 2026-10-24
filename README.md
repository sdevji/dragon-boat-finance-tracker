# Dragon Boat Finance Tracker

Tracks the team's money in one place: member fees and installments, drop-ins, expenses with receipt photos, reimbursements, budgets and net balance.

**Open it here:** https://sdevji.github.io/dragon-boat-finance-tracker/

It's a single web page (`index.html`) that needs no install and no account. Chrome or Edge is recommended. It works on a phone too.

## Getting started

1. Open the link above and bookmark it. On a phone, use **Add to Home Screen**.
2. To use it offline instead, download `index.html` from this repository and double-click it. Keep the file in one folder after that.
3. The dashboard walks you through setup:
   1. Set the starting float.
   2. Add fee plans.
   3. Import or add members.
   4. Set budgets.

To look around first, choose **Load sample data** on the dashboard. You can erase it later in **Settings**.

## Bringing over the 25-26 Finances workbook

Go to **Import / Export**. You can use the Excel file directly:

1. **Before importing members, set up your fee plans** under **Settings → Fee plans**:
   - Full season, $800: $325 by Dec 7, $260 by Jan 11, $215 by Mar 1
   - Students / new grads, $650: $225 + $225 + $200
   
   During import, anyone whose fee matches a plan is put on it automatically.
2. Drop in the `.xlsx` file, from Excel or from Google Sheets (**File → Download → Microsoft Excel**). Then pick a tab:
   - **Fee Collection:** one member per row. Payment 1, Payment 2 and Payment 3 each become a separate payment. Names with no fee and no payments come in unticked.
   - **Payments:** the expense tables. The "Regattas" table becomes its own category, "Coaching" is offered as a new category, and the totals rows and the bank-balance log underneath are left out.
   - **Drop-ins:** choose **Fee Collection** again and set "Column headings are on row" to **64**, where the drop-in list starts. It's recognised as drop-ins ($700 paid).
3. Check the preview, untick anything you don't want, and click **Import**.

The workbook has no payment dates. You choose one date to record them all under, and you can edit any payment afterwards.

## Bank e-Transfers and other names

People's e-Transfers often arrive under their legal name rather than the name they go by. To handle that:

1. Open a member (pencil icon) and add their other names under **Other names**, one per line, e.g. `SMITH, JOHN ROBERT`. Order, capitals and punctuation don't matter.
2. In online banking, copy the rows from your e-Transfer list and paste them into **Import / Export**. No headings are needed; the date, name and amount columns are worked out automatically.
3. Each payment is matched to a member by any of their names, or to a drop-in. Anything it can't place shows **Don't import**. Use the **Who is it?** picker to choose a member, and that name is remembered for next time.
4. Payments that are already in the tracker are spotted and left out.

## Where your data lives (please read)

Everything saves automatically inside the browser on this device. Nothing is uploaded. That keeps it private, but it also means:

- **Use the same browser every time.** Data saved in Chrome won't show up in Edge, and the other way round.
- **Keep the file in the same folder,** or keep using the same web link.
- **Clearing browsing data or cookies will erase it.** So will using a private or incognito window.
- **Download a backup regularly.** Go to **Import / Export → Download backup**. You get one `.json` file holding everything, receipt photos included. Keep it in OneDrive or Google Drive, or email it to yourself. The dashboard reminds you if your last backup is more than 2 weeks old.

To move to another computer or browser, open the tracker there. Then go to **Import / Export → Restore from backup**.

A restore replaces everything on that computer. Before it does, the tracker compares the backup with what's on the computer:
- If the computer has changes that aren't in the backup, it lists them, warns that they'd be lost, and offers to back up the computer first.
- If nothing would be lost, it says so.

If you use two computers, restore the latest backup when you sit down, and download a fresh one when you're done.

## What's in it

| Section | What it does |
|---|---|
| **Dashboard** | Shows net balance (float + fees collected + drop-ins − expenses), cash on hand, fee-collection progress, key totals including the overdue amount and drop-in income, spending by category against budget, and recent activity. |
| **Members & Fees** | Each person's fee, fee plan, amount paid, balance, next installment due and status (Paid, Partial, Unpaid or Overdue), plus any other names they go by. Click a row to see their payment history and installment schedule. Record payments with date, method (Cash, e-Transfer, Credit, Cheque, Bank Transfer) and notes. Search by any of their names, filter and sort. |
| **Drop-ins** | People who come to a practice or event without being full members. Record one person or a whole list at once (e.g. Discovery Day), with the first visit free if you like. See it by person or as a visit log, mark visits paid, and turn a regular into a member in one click. |
| **Expenses** | Itemized ledger with quantity × unit price, category, payment method, who paid, reimbursement status and **receipt photos**. Filter by category, reimbursement or missing receipts. |
| **Budget** | A spending target per category. Add, rename or remove categories, such as Coaching, Regattas or Socials. Bars turn amber at 80% and red once a category is over. |
| **Import / Export** | Imports members, drop-ins, payments (such as a bank e-Transfer list) and expenses from .xlsx files, CSV files or pasted cells, with column matching and a row-by-row preview. Exports CSVs. Also holds backup and restore. |
| **Settings** | Team name, currency, **fee plans**, default fee and due date, drop-in rate and free first visit, budget warning level, light/dark mode, sample data and the erase-everything option. |

### Fee plans and statuses

A fee plan is a standard fee and its installment schedule.

- **Custom amounts:** anyone can still have their own amount, for a youth rate, a recruitment bonus or a part season. If a member's fee differs from their plan's total, the last installment is adjusted to match.
- **Status:** **Overdue** means a due date has passed and the member hasn't paid enough to cover it. **Partial** means they're on track but not finished.
- **Members not on a plan** use one due date: their own, or the team date in Settings.

### Receipt photos

Open an expense and use **Add photo**, drag photos in, or paste a screenshot. Photos are resized to about 1600 px (roughly 150–250 KB each), which keeps receipts readable. They're stored in the browser and included in backups. Click a thumbnail in the ledger to view, open full size or download.

### The dragon 🐉

A small dragon peeks up from the bottom-left corner:
- It reacts when you record things, and now and then reminds you about overdue fees or a backup.
- Click it for a dragon boat fun fact.
- Turn it off under **Settings → Mascot**.

### Mistakes

Deleting a member, payment, drop-in, expense, category or plan, or running an import, pops up an **Undo** button for a few seconds.
