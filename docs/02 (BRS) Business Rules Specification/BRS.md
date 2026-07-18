---
Document Title: Business Rules Specification

Document ID: IMS-BRS-001

Version: 1.0

Status: Draft

Project Name: Inventory Management System

Author: Steven Ayman Salah

Reviewer: TBD

Approved By: Client

Created Date: 2026-07-05

Last Updated: 2026-07-10

Classification: Internal Use
---

# Revision History

| Version | Date | Author | Description |
|----------|------|--------|-------------|
| 1.0 | 2026-07-05 | Steven Labib | Initial Draft |

---

# Table of Contents

1. Introduction
2. Product Rules
3. Category Rules
4. Unit Rules
5. Warehouse Rules
6. Customer Rules
7. Inventory Rules
8. Sales Rules
9. Payment Rules
10. Reporting Rules
11. General System Rules

---

# 1. Introduction

## 1.1 Purpose

This document defines the approved business rules for Version 1.0 of the Inventory Management System (IMS).

These rules describe the business policies, operational constraints, and decision logic that govern how the business operates. The system shall enforce these rules to ensure consistent business processes, accurate inventory management, and reliable sales and customer operations.

This document serves as the primary reference for business logic throughout the analysis, design, development, testing, and maintenance phases of the project.

---

## 1.2 Scope

This document applies to all business processes included in Version 1.0 of the Inventory Management System (IMS), including product management, warehouse management, customer management, inventory operations, sales, customer payments, reporting, and system administration.

---

## 1.3 References

This document is based on the following approved project documentation:

- Project Charter
- Product Requirements Document (PRD)

# 2. Product Rules

The following business rules govern product management within the Inventory Management System (IMS).

| Rule ID | Business Rule | Rationale | Related Modules |
|----------|---------------|-----------|-----------------|
| BR-001 | Each product shall have a unique name. | Prevent duplicate products and reduce user confusion. | Product Management |
| BR-002 | Each product shall belong to exactly one warehouse at any given time. | Simplify inventory management and stock tracking. | Product Management, Warehouse Management |
| BR-003 | Each product shall use exactly one measurement unit. | Ensure consistent quantity calculations and inventory transactions. | Product Management, Unit Management |
| BR-004 | The measurement unit assigned to a product shall determine whether fractional quantities are allowed. | Ensure quantities follow the rules of their measurement units. | Product Management, Unit Management, Sales Management |
| BR-005 | Product purchase prices may change over time and shall be updated whenever new stock is received. | Reflect changes in supplier pricing. | Product Management, Inventory Management |
| BR-006 | Selling prices shall not be stored as fixed product values and shall be entered manually when creating each sales invoice. | Allow flexible pricing for different customers and sales situations. | Sales Management |
| BR-007 | Products that require additional attributes (such as carpets) may store Color and Pattern/Model information. | Support products with multiple variations while avoiding unnecessary data for other product types. | Product Management |
| BR-008 | Carpet quantities shall be measured in meters and may include fractional values. | Support selling carpets by length (e.g., 1.5 meters). | Product Management, Sales Management |
| BR-009 | Carpet inventory shall be tracked separately for each Color and Pattern/Model combination. | Maintain accurate stock quantities for each carpet variation. | Product Management, Inventory Management |
| BR-010 | Window wire products shall be measured and sold by roll only. Fractional quantities are not allowed. | Reflect the client's business process. | Product Management, Sales Management |
| BR-011 | Scooter and sanitary products shall be measured and sold by whole pieces only. Fractional quantities are not allowed. | Ensure inventory accuracy for piece-based products. | Product Management, Sales Management |
| BR-012 | Archived products shall not be available for new inventory or sales transactions. | Preserve historical data while preventing future use. | Product Management, Sales Management, Inventory Management |

# 3. Category Rules

The following business rules govern product categories within the Inventory Management System (IMS).

| Rule ID | Business Rule | Rationale | Related Modules |
|----------|---------------|-----------|-----------------|
| BR-013 | Each product shall belong to exactly one category. | Ensure consistent product classification and reporting. | Product Management, Category Management |
| BR-014 | Category names shall be unique. | Prevent duplicate categories and improve data consistency. | Category Management |
| BR-015 | Archived categories shall not be available for assignment to new products. | Preserve historical records while preventing future use. | Category Management, Product Management |
| BR-016 | A category that is assigned to one or more products shall not be deleted. | Protect data integrity and maintain product references. | Category Management |

# 4. Unit Rules

The following business rules govern measurement units within the Inventory Management System (IMS).

| Rule ID | Business Rule | Rationale | Related Modules |
|----------|---------------|-----------|-----------------|
| BR-017 | Each measurement unit shall have a unique name. | Prevent duplicate measurement units and maintain consistency. | Unit Management |
| BR-018 | Each measurement unit shall define whether fractional quantities are allowed. | Ensure products follow the correct quantity rules during inventory and sales operations. | Unit Management, Product Management |
| BR-019 | Every product shall be assigned exactly one measurement unit. | Ensure accurate quantity calculations and inventory tracking. | Product Management, Unit Management |
| BR-020 | A measurement unit assigned to one or more products shall not be deleted. | Preserve historical data and maintain data integrity. | Unit Management |
| BR-021 | Archived measurement units shall not be available for assignment to new products. | Preserve historical records while preventing future use. | Unit Management, Product Management |

# 5. Warehouse Rules

The following business rules govern warehouse management within the Inventory Management System (IMS).

| Rule ID | Business Rule | Rationale | Related Modules |
|----------|---------------|-----------|-----------------|
| BR-022 | Each warehouse shall have a unique name. | Prevent duplicate warehouse records and user confusion. | Warehouse Management |
| BR-023 | Each product shall belong to exactly one warehouse at any given time. | Simplify inventory tracking and stock management. | Product Management, Warehouse Management |
| BR-024 | Warehouse transfers shall only be allowed between existing warehouses. | Ensure inventory movements occur only between valid warehouses. | Inventory Management, Warehouse Management |
| BR-025 | A warehouse assigned to one or more products shall not be deleted. | Preserve historical records and maintain referential integrity. | Warehouse Management |
| BR-026 | Archived warehouses shall not be available for assigning new products or receiving new inventory transactions. | Preserve historical data while preventing future use. | Warehouse Management, Product Management, Inventory Management |
| BR-027 | Every inventory transaction shall be associated with a warehouse. | Ensure complete traceability of inventory movements. | Inventory Management |

# 6. Customer Rules

The following business rules govern customer management within the Inventory Management System (IMS).

| Rule ID | Business Rule | Rationale | Related Modules |
|----------|---------------|-----------|-----------------|
| BR-028 | Each customer shall have a unique mobile number. | Prevent duplicate customer records. | Customer Management |
| BR-029 | Customer names are not required to be unique. | Different customers may have the same name. | Customer Management |
| BR-030 | Customer payments shall reduce the customer's total outstanding balance. | Ensure accurate debt tracking. | Customer Management, Customer Payments |
| BR-031 | Every sales invoice created as a credit sale shall increase the customer's outstanding balance. | Maintain accurate customer account balances. | Sales Management, Customer Payments |
| BR-032 | Cash sales shall not create customer debt. | Distinguish cash transactions from credit transactions. | Sales Management |
| BR-033 | A customer with existing sales invoices or payment history shall not be deleted. | Preserve historical business records. | Customer Management |
| BR-034 | Archived customers shall not be available for new sales transactions. | Preserve historical data while preventing future use. | Customer Management, Sales Management |
| BR-035 | Customer payment history shall remain available even if the customer is archived. | Maintain complete financial history. | Customer Payments |

# 7. Inventory Rules

The following business rules govern inventory operations within the Inventory Management System (IMS).

| Rule ID | Business Rule | Rationale | Related Modules |
|----------|---------------|-----------|-----------------|
| BR-036 | Every inventory transaction shall be associated with exactly one product. | Ensure accurate inventory tracking. | Inventory Management |
| BR-037 | Every inventory transaction shall be associated with exactly one warehouse. | Maintain inventory traceability by warehouse. | Inventory Management, Warehouse Management |
| BR-038 | Inventory quantities shall never become negative. | Prevent selling or transferring stock that is not available. | Inventory Management, Sales Management |
| BR-039 | Every inventory transaction shall be recorded in the inventory history. | Maintain complete inventory traceability. | Inventory Management, Audit Trail |
| BR-040 | Opening Balance shall be recorded only once for each product when it is first introduced into a warehouse. | Establish the initial stock quantity for inventory tracking. | Inventory Management |
| BR-041 | Stock In transactions shall increase the available inventory quantity. | Maintain accurate inventory levels. | Inventory Management |
| BR-042 | Stock Out transactions shall decrease the available inventory quantity. | Maintain accurate inventory levels. | Inventory Management |
| BR-043 | Warehouse Transfer transactions shall decrease inventory from the source warehouse and increase inventory in the destination warehouse within the same transaction. | Ensure inventory consistency during transfers. | Inventory Management, Warehouse Management |
| BR-044 | Inventory Adjustment transactions shall require a recorded reason. | Maintain accountability for inventory changes. | Inventory Management |
| BR-045 | Inventory Count (Stock Count) may adjust the recorded inventory quantity to match the physical inventory count. | Ensure inventory accuracy after stock counting. | Inventory Management |
| BR-046 | Damaged quantities shall be recorded separately from available quantities while remaining part of the total inventory quantity. | Preserve accurate inventory visibility by distinguishing sellable stock from damaged stock without losing the total inventory record. | Inventory Management |
| BR-047 | Product Return transactions shall increase the available inventory quantity. | Returning products restores sellable stock when accepted. | Inventory Management, Sales Management |
| BR-048 | Every inventory transaction shall record the transaction date and the user who performed it. | Support auditing and historical tracking. | Inventory Management, Audit Trail |
| BR-049 | Inventory transactions shall not be modified or deleted after they are recorded. Any correction shall be performed through a new inventory adjustment transaction. | Preserve inventory history and ensure full traceability of stock movements. | Inventory Management, Audit Trail |

# 8. Sales Rules

The following business rules govern sales operations within the Inventory Management System (IMS).

| Rule ID | Business Rule | Rationale | Related Modules |
|----------|---------------|-----------|-----------------|
| BR-050 | Every sales invoice shall have a unique system-generated invoice number. | Ensure unique identification and traceability of sales invoices. | Sales Management |
| BR-051 | Every sales invoice shall be associated with exactly one customer. | Maintain accurate customer purchase history and account balances. | Sales Management, Customer Management |
| BR-052 | Selling prices shall be entered manually for each sales invoice. | Allow flexible pricing based on customer agreements and market conditions. | Sales Management |
| BR-053 | The system shall calculate each invoice line total based on the entered selling price and quantity. | Ensure accurate invoice calculations. | Sales Management |
| BR-054 | The system shall calculate the invoice grand total automatically. | Prevent manual calculation errors. | Sales Management |
| BR-055 | Sales invoices may be modified after creation. | Support business corrections when necessary. | Sales Management |
| BR-056 | When a sales invoice is modified, the system shall update inventory quantities and customer balances accordingly. | Maintain data consistency after invoice modifications. | Sales Management, Inventory Management, Customer Payments |
| BR-057 | The system shall retain the complete history of sales invoice modifications. | Ensure traceability and auditability of invoice changes. | Sales Management, Audit Trail |
| BR-058 | A sales invoice shall not be completed if the requested quantity exceeds the available inventory quantity. | Prevent negative inventory quantities. | Sales Management, Inventory Management |
| BR-059 | Cash sales shall not create customer debt. | Distinguish immediate payments from credit sales. | Sales Management |
| BR-060 | Credit sales shall increase the customer's outstanding balance by the invoice amount. | Maintain accurate customer account balances. | Sales Management, Customer Payments |
| BR-061 | Sales invoices shall be printable using a standard A4 printer-friendly layout. | Support the client's daily invoicing process. | Sales Management |
| BR-062 | A sales invoice may contain one or more products. | Allow customers to purchase multiple products within a single invoice. | Sales Management |


# 9. Payment Rules

The following business rules govern customer payment operations within the Inventory Management System (IMS).

| Rule ID | Business Rule | Rationale | Related Modules |
|----------|---------------|-----------|-----------------|
| BR-063 | Every customer payment shall be associated with exactly one customer. | Ensure accurate customer account management. | Customer Payments, Customer Management |
| BR-064 | Every payment transaction shall have a unique system-generated payment reference number. | Ensure payment traceability and simplify future reference. | Customer Payments |
| BR-065 | Customer payments shall reduce the customer's outstanding balance. | Maintain accurate customer account balances. | Customer Payments |
| BR-066 | A customer payment shall not result in a negative outstanding balance. | Prevent overpayment from creating invalid account balances. | Customer Payments |
| BR-067 | Every customer payment shall record the payment date, payment amount, and the user who recorded the payment. | Maintain complete payment history and accountability. | Customer Payments, Audit Trail |
| BR-068 | Every customer payment shall remain in the payment history and shall not be deleted after being recorded. Any correction shall be performed through a separate adjustment transaction. | Preserve financial records and maintain auditability. | Customer Payments, Audit Trail |
| BR-069 | The system shall allow printing a payment receipt in a printer-friendly A4 format. | Provide customers with proof of payment and support business operations. | Customer Payments |

# 10. Reporting Rules

The following business rules govern reporting within the Inventory Management System (IMS).

| Rule ID | Business Rule | Rationale | Related Modules |
|----------|---------------|-----------|-----------------|
| BR-070 | Reports shall display data based on the latest approved inventory and sales transactions. | Ensure reports reflect the current business status. | Reporting |
| BR-071 | Reports shall provide accurate and consistent information based on the system data. | Support operational and business decision-making. | Reporting |
| BR-072 | Inventory reports shall include available quantities, damaged quantities, and total quantities. | Provide complete inventory visibility. | Reporting, Inventory Management |
| BR-073 | Customer statements shall display all sales invoices, payments, and the current outstanding balance for the selected customer. | Provide a complete financial history for each customer. | Reporting, Customer Payments |
| BR-074 | Low stock reports shall identify products whose available quantity is less than or equal to their minimum stock level. | Help users replenish inventory before stock shortages occur. | Reporting, Inventory Management |
| BR-075 | Reports shall support printing in a printer-friendly A4 format. | Support operational reporting requirements. | Reporting |
| BR-076 | Reports shall support exporting to PDF and Excel formats. | Allow users to share, archive, and analyze business data. | Reporting |
| BR-077 | Reports shall be generated based on the user's selected search criteria and filters. | Allow users to retrieve relevant business information efficiently. | Reporting |
| BR-078 | Reports shall include only active data by default while allowing historical data to be viewed when requested. | Improve report clarity while preserving historical records. | Reporting |

# 11. General System Rules

The following business rules apply across the entire Inventory Management System (IMS).

| Rule ID | Business Rule | Rationale | Related Modules |
|----------|---------------|-----------|-----------------|
| BR-079 | Every master data entity shall be assigned a unique system-generated code. | Ensure unique identification and simplify system management and reporting. | System |
| BR-080 | The system shall implement logical deletion (Soft Delete) for all master data entities. | Preserve historical records and maintain referential integrity. | System |
| BR-081 | Archived records shall not be available for new business transactions but shall remain accessible for historical reference and reporting. | Preserve historical data while preventing future operational use. | System |
| BR-082 | The system shall maintain an audit trail for all critical business operations. | Ensure accountability and traceability of important system activities. | System, Audit Trail |
| BR-083 | All dates and times shall be recorded automatically by the system. | Ensure consistent and reliable transaction history. | System |
| BR-084 | The system shall record the user responsible for each critical business transaction. | Support auditing and accountability. | System, Audit Trail |
| BR-085 | The system shall support the Arabic language (RTL) throughout the user interface. | Meet the client's operational requirements. | System |
| BR-086 | The system shall provide a responsive user interface that supports desktop, tablet, and mobile devices. | Ensure usability across all supported devices. | System |
| BR-087 | System-generated reference numbers shall not be editable by users. | Preserve data integrity and ensure reliable traceability. | System |
| BR-088 | Required fields shall be validated before saving any business transaction. | Prevent incomplete or invalid data from being stored. | System |
| BR-089 | The system shall display clear validation messages when business rules are violated. | Help users correct errors and improve data quality. | System |
| BR-090 | All business transactions shall be executed atomically to ensure data consistency. | Prevent partial updates that could compromise inventory and financial data. | System |
| BR-091 | The system shall use a consistent numbering format for all system-generated reference numbers. | Improve readability and standardize business documents. | System |

