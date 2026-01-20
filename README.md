# WOP Statutory Challan Xtract

A lightweight, **100% client-side** toolset to extract key fields from statutory challans/receipts and export **Excel-ready** summaries.  
No server processing. No data storage. Everything runs in your browser.

✅ Especially useful during **audits** for quick **reconciliations**, cross-checking, and documentation.

---

## ✅ Supported Extractors

### 1) ESIC Challan Extractor (`esic.html`)
Extracts key challan details from ESIC challan PDFs/HTML and exports a single summary sheet.

**Fields extracted**
- Employer Code  
- Employer Name  
- Contribution Period  
- Challan Number  
- Created Date  
- Submitted Date  
- Transaction No  
- Total Amount (₹)  

**UI highlights**
- Multi-file upload  
- Summary pills: **Total Records** and **Total Amount (₹)**  
- Export to Excel  

---

### 2) EPF Combined Challan Extractor (`epf_combined.html`)
Extracts tabular rows from EPF Combined Challan of A/C **01, 02, 10, 21 & 22** and totals.

**Output structure**
- One PDF typically produces **3 rows** (Administration Charges, Employer Share, Employee Share)
- Columns:
  - Name  
  - Month / Year  
  - Particulars  
  - A/C.01, A/C.02, A/C.10, A/C.21, A/C.22  
  - Total  
  - Date of Generation  
  - File Name  

**UI highlights**
- Multi-file upload  
- Summary pills: **Total Records** and **Total Amount (₹)** (sum of “Total” column)  
- Export to Excel *(Calibri 11 supported when using xlsx-js-style)*  
- Debug text viewer *(optional)* for troubleshooting PDF parsing  

---

### 3) EPF Payment Receipt Extractor (`epf_payment_receipt.html`)
Extracts payment receipt-level details such as TRRN, wage month, amounts, bank and payment dates.

**Fields extracted**
- TRRN No  
- Challan Status  
- Challan Generated On  
- Establishment ID  
- Establishment Name  
- Challan Type  
- Total Members  
- Wage Month  
- Total Amount  
- Account-1 Amount  
- Account-2 Amount  
- Account-10 Amount  
- Account-21 Amount  
- Account-22 Amount  
- Payment Confirmation Bank  
- CRN  
- Payment Date  
- Payment Confirmation Date  
- File Name  

**UI highlights**
- Multi-file upload  
- Export to Excel  

> Note: Amounts are extracted using text-position line reconstruction (PDF.js).  
> If a particular PDF layout differs, a few labels may require regex tuning.

---

### 4) Income Tax Payment Challan Extractor (`income_tax_challan.html`)
Extracts fields from the Income Tax Department challan receipt and tax breakup.

**Important notes**
- **ITNS No is NOT included** (removed as requested).  
- Tax breakup may include **“Others (F)”** in some receipts.  
  - If present: capture it  
  - If not present: keep blank  
- Total/amounts are parsed from the **“Tax Breakup Details (Amount in ₹)”** section.

**Expected Tax Breakup columns**
- Tax (A)  
- Surcharge (B)  
- Cess (C)  
- Interest (D)  
- Penalty (E)  
- Others (F) *(optional)*  
- Total (A+B+C+D+E+F)

**UI highlights**
- Multi-file upload  
- Summary pills: **Total Records** and **Total Amount (₹)** (grand total across files)  
- Export to Excel  

---

## 🧭 Project Structure (Recommended)

Place all HTML files in the same folder (repo root or `/docs` if using GitHub Pages):

