# Ledgerly

> **"Ledgerly" is a working title.** The product name is not final and may change.

Automated bookkeeping for small businesses. Receipts captured by phone photo, email, and SMS are matched to bank and credit card transactions retrieved through [Plaid](https://plaid.com), then exported to accounting platforms such as QuickBooks, Xero, and Wave.

🌐 **Live site:** https://builderw33.github.io/W33/
📄 **Privacy Policy:** https://builderw33.github.io/W33/privacy.html
📄 **Terms of Service:** https://builderw33.github.io/W33/terms.html

---

## Status

Closed beta · 2026. The product is in active development; details are subject to change.

## How it works

1. **Capture** — Receipts are submitted by phone photo, forwarded email, or SMS.
2. **Extract** — Receipt data (vendor, date, total, tax, line items) is read automatically.
3. **Match** — Bank and credit card transactions, retrieved through Plaid, are matched to receipts.
4. **Export** — Categorized records are exported to QuickBooks, Xero, Wave, or CSV.

## Plaid integration

The product uses Plaid to let users securely connect their bank and credit card accounts. Users enter their credentials directly with Plaid; the application never sees or stores bank login credentials.

| | |
|---|---|
| **Plaid products** | Transactions, Balance |
| **Purpose** | Matching user-submitted receipts to bank transactions and generating accounting exports |
| **Data accessed** | Transaction history and account balances for accounts the user explicitly links |
| **Not accessed** | Identity, Auth, Investments, Liabilities, and other Plaid products |

### Data handling

- **Storage** — Encrypted at rest and in transit; scoped per authenticated user.
- **Retention** — Deleted on account closure or user request.
- **Sharing** — No sale or third-party sharing. Exports go only to destinations the user authorizes.
- **Access tokens** — Plaid access tokens are held in encrypted secret storage.

The full [Privacy Policy](privacy.html) discloses how end-user financial data is collected, used, and protected, and links to the [Plaid End User Privacy Policy](https://plaid.com/legal/#end-user-privacy-policy).

## Repository contents

| File | Purpose |
|---|---|
| `index.html` | Product landing page |
| `privacy.html` | Privacy policy |
| `terms.html` | Terms of service |

This repository hosts the public-facing site for the product, served via GitHub Pages. It does not contain application source code.

## Local preview

The site is plain static HTML — open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Contact

General and privacy inquiries: `hello@w33.biz`
