# SAP ERP Blueprint & ABAP ALV Report

Enterprise Configuration Project (FI, MM, SD)  
Academic Project | 2024–2025  

---

## Project Overview

This project presents a complete SAP ERP implementation for a fictional organization, GlobalEdge Industries Pvt. Ltd. It integrates core business functions across Financial Accounting (FI), Materials Management (MM), and Sales & Distribution (SD).

In addition, a custom ABAP ALV report is developed to provide a consolidated view of vendor data, stock levels, and sales orders in a single interface.

---

## Problem Statement

The organization faced several operational challenges:

- Lack of a unified enterprise structure  
- Manual reconciliation in financial processes  
- No integration between inventory and finance  
- Sales tracking handled through spreadsheets  
- Absence of consolidated reporting for management  

---

## Solution

A full SAP ERP configuration was implemented with the following:

- Unified enterprise structure across multiple company codes  
- End-to-end integration between FI, MM, and SD modules  
- GST tax configuration aligned with Indian standards  
- Automated three-way matching in procurement  
- Custom ABAP ALV report for real-time consolidated insights  

---

## Key Features

- Cross-module integration enabling automatic financial postings from MM and SD  
- Three-way matching process (Purchase Order, Goods Receipt, Invoice Verification)  
- Custom ALV report (Transaction Code: ZGEBI01) with sorting, filtering, and export functionality  
- Hotspot navigation from report to purchase order display (ME23N)  
- Authorization control based on company code  
- Support for ALV layout variants  

---

## Enterprise Structure

| Component              | Value                          |
|----------------------|--------------------------------|
| Client               | 800                            |
| Company Codes        | GE01 (India), GE02 (Europe)    |
| Controlling Area     | GE00                           |
| Plants               | P001 (Mumbai), P002 (Pune)     |
| Purchasing Org       | PO01                           |
| Sales Organization   | SO01                           |

---

## Modules Covered

### Financial Accounting (FI)
- Company code configuration  
- Chart of accounts setup  
- Fiscal year and posting periods  
- GST tax configuration  
- Bank and reconciliation setup  

### Materials Management (MM)
- Plant and storage location configuration  
- Purchasing organization and groups  
- Inventory and valuation setup  
- Material requirements planning (MRP)  
- Movement types and account determination  

### Sales & Distribution (SD)
- Sales area configuration  
- Pricing procedures  
- Delivery and billing processes  
- Revenue account determination  
- Document flow configuration  

---

## ABAP Development

### Custom Report

- Program Name: ZGEBI_VENDOR_STOCK_SO_RPT  
- Transaction Code: ZGEBI01  

### Technical Details

- Developed using REUSE_ALV_GRID_DISPLAY  
- Data integration from multiple tables:
  - LFA1, EKKO, EKPO (Vendor and Purchase Orders)  
  - MARD (Stock Data)  
  - VBAK, VBAP (Sales Orders)  
- Dynamic field catalog generation  
- Interactive hotspot functionality for navigation  
- Selection screen with filtering options  

---

## Tech Stack

- SAP ECC 6.0 / S/4HANA  
- ABAP (SE38)  
- SPRO (Implementation Guide)  
- SAP Data Dictionary (SE11)  
- ALV Grid (SLIS framework)  

---

## Unique Highlights

- Consolidated reporting across FI, MM, and SD modules  
- Real-time integration eliminating manual processes  
- GST-compliant configuration  
- Multi-company setup within a single SAP client  
- Dynamic ALV structure adaptable to future changes  

---

## Future Enhancements

- Migration to object-oriented ALV (CL_GUI_ALV_GRID)  
- Development of SAP Fiori application using OData services  
- Optimization using Core Data Services (CDS) views  
- Background job scheduling for automated report execution  
- Integration with SAP Analytics Cloud for advanced reporting  

---

## Author

Aditi Prajapati  
Engineering Student  

---

## Usage

1. Configure enterprise structure and modules using SPRO  
2. Develop and activate the ABAP program in SE38  
3. Execute transaction code ZGEBI01  
4. Analyze the ALV report output  
