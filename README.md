# WOP Statutory Challan Xtract

A lightweight, **100% client-side** toolset to extract key fields from statutory challans/receipts and export **Excel-ready** summaries.  
No server processing. No data storage. Everything runs in your browser.

✅ Especially useful during **audits** for quick **reconciliations**, cross-checking, and documentation.

---

## ✅ Purpose of Each Extractor (What it’s for)

### 1) ESIC Challan Extractor (`esic.html`)
**Purpose**
- Build a **summary register** of ESIC challans in minutes.
- Useful for:
  - Monthly ESIC payment reconciliation
  - Audit working papers
 
**File Preview**
<img width="1136" height="691" alt="Screenshot 2026-01-20 060855" src="https://github.com/user-attachments/assets/32920109-0ce1-4c28-8abb-fb6863b19433" />


---

### 2) EPF Combined Challan Extractor (`epf_combined.html`)
**Purpose**
- Extract the EPF **combined challan breakup** for A/C **01, 02, 10, 21 & 22**.
- Useful for:
  - Statutory payment reconciliation
  - Cross-checking totals by contribution heads
  - Power Query Excel has also created for this to check the disclosures are made properly. Kindly email, if intereseted 

>  One PDF usually generates **3 rows**:
> Administration Charges, Employer Share, Employee Share

**File Preview**
<img width="870" height="130" alt="Screenshot 2026-01-20 060800" src="https://github.com/user-attachments/assets/53cd8965-797b-459b-9839-9ef3f32659fa" />

---

### 3) EPF Payment Receipt Extractor (`epf_payment_receipt.html`)
**Purpose**
- Create a **payment confirmation register** from EPF receipts (TRRN, bank, CRN, dates, amounts).
- Useful for:
  - Audit evidence of payment confirmation
  - Tax Audits
  - Payment date/confirmation date tracking

**File Preview**
<img width="1111" height="269" alt="Screenshot 2026-01-20 060750" src="https://github.com/user-attachments/assets/c0e76951-be2f-4dee-a7ac-b31876078b06" />

---

### 4) Income Tax Payment Challan Extractor (`income_tax_challan.html`)
**Purpose**
- Extract challan receipt fields + tax breakup into Excel.
- Useful for:
  - TDS Challan reconciliation, Grouping verification, Tax Payment summary and purpose of payments
  - Tax Audits
  - Breakup reconciliation (Tax/Surcharge/Cess/Interest/Penalty/Others)

**File Preview**
<img width="703" height="111" alt="Screenshot 2026-01-20 060719" src="https://github.com/user-attachments/assets/3cd298b9-5cde-45cf-9d48-fe8b9a8312a2" />

---

## ⚠️ Cautions & User Responsibilities (Important)

Because this tool is **client-side** and relies on **PDF text extraction**, users must verify accuracy before using it for compliance/audit submission.

### 1) Always validate key fields (Preview files are attached this tools works only for those files)
After export, **cross-check at least these** against the original PDF:
- Challan / Transaction / TRRN / CRN numbers  
- Total Amount (₹)  
- Dates (Generated / Submitted / Payment / Confirmation)  
- Month / Period  

### 2) PDFs may vary by layout
Some challans are scanned, image-based, or have different formatting.
- If a PDF is **scanned image** (no selectable text), extraction may return blank or partial data.
- If government portal layouts change, some labels/regex may need updates.

👉 In such cases, treat export as a **draft** and manually correct amounts.

### 4) Do not treat output as a legal proof by itself
The Excel output is only a **working summary**.
For audits/statutory compliance, always keep:
- Original PDF challans/receipts (as source evidence)
- Exported Excel (as working paper)

### 5) Data privacy caution (user-side)
No server upload happens, but user must still ensure:
- Use only trusted devices/browsers.
- Avoid using in shared/public systems.
- Do not leave exported files on unsecured machines.

---

## 🧾 Output & Audit Use
This tool is intended to support:
- Faster reconciliation
- Audit working paper preparation
- Consolidated registers for statutory payments

Final responsibility for correctness remains with the user.
