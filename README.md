# 🏦 Financial Cheque Management & Printing System
**Enterprise Finance Automation Solution developed for MEDAŞ**

This is a comprehensive **ASP.NET Core MVC** application designed to digitize and automate cheque management processes for **MEDAŞ (Meram Electricity Distribution Inc.)**. It streamlines financial workflows by providing secure tracking, advanced filtering, and a precision-engineered PDF printing module for physical cheque issuance.

---

## 🎯 Project Impact & Objectives

- **Operational Efficiency:** Automated the manual process of cheque issuance, significantly reducing human error in financial documentation.
- **Hardware Integration:** Developed a custom JavaScript-based printing engine to map digital data onto physical cheque templates with millimeter precision.
- **Data Integrity:** Implemented robust validation and formatting for complex financial data (Currency, VKN, Tax IDs).
- **Scalability:** Built to handle multi-currency transactions and large-scale archiving needs.

---

## 🚀 Key Features

- ✅ **Advanced Management:** Full CRUD operations for financial instruments with secure state management.
- ✅ **Precision PDF Printing:** Custom-built module using **jsPDF** to generate PDFs in specific cheque dimensions (200mm x 75mm).
- ✅ **Dynamic Coordinate Mapping:** Fine-tuned coordinate system to align Tax IDs, Dates, and Amounts perfectly with physical bank cheque fields.
- ✅ **Financial Formatting:** Automated currency formatting (thousands/decimal separators) and "Amount in Words" logic.
- ✅ **Data Portability:** Bi-directional Excel integration (Import/Export) for seamless accounting synchronization.
- ✅ **Smart Text Scaling:** Automatic font-size adjustment to ensure long vendor names or amounts fit within physical constraints.

---

## 🏗️ Technical Deep Dive: Cheque Issuance Module



### `printerEdit.js` Engine
A specialized JavaScript module engineered for the precise rendering of financial data:
- **Header Config:** Dynamic placement of VKN, City, and Date.
- **Details Config:** Precise mapping for Numeric Amount, Beneficiary Name, and Currency Fractions.
- **Robust Formatting:** A custom `formatAmount()` function ensures financial accuracy across different currency locales.

---

## 🛠️ Tech Stack

- **Backend:** ASP.NET Core MVC (C#)
- **Database:** MSSQL / Entity Framework Core
- **Client-Side Logic:** JavaScript, jQuery
- **Documentation Engine:** [jsPDF](https://github.com/parallax/jsPDF)
- **UI Framework:** Bootstrap & Custom CSS for financial dashboards

---

## 📈 Professional Outcomes (MEDAŞ Engagement)

- **End-to-End Delivery:** Managed the software lifecycle from financial requirement gathering to on-site production deployment.
- **System Accuracy:** Achieved zero-margin error in printing alignments, ensuring bank compatibility for physical cheques.
- **Compliance:** Built the system according to corporate financial security and audit standards.

---

## 👩‍💻 Developer

**Esra Tosun** *Software Engineer*
