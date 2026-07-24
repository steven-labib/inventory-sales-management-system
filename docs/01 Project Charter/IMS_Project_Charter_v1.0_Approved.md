---
Document Title: Project Charter

Document ID: IMS-PC-001

Version: 0.1

Status: Draft

Project Name: Inventory Management System

Author: Steven Labib

Reviewer: TBD

Approved By: Client

Created Date: 2026-07-03

Last Updated: 2026-07-03

Classification: Internal Use
---

# Revision History

| Version | Date | Author | Description |
|----------|------------|-------------|----------------------|
| 0.1 | 2026-07-03 | Steven Labib | Initial Draft |

---

# Table of Contents

1. Executive Summary
# 1. Executive Summary

The Inventory Management System (IMS) is a web-based application designed to streamline and digitize inventory and sales operations for businesses managing products across one or more warehouses.

The system provides a centralized platform for managing products, warehouses, inventory transactions, customers, sales invoices, and customer payments while ensuring data accuracy, operational efficiency, and real-time inventory visibility.

The primary objective of the project is to replace manual inventory management processes with a secure, scalable, responsive, and user-friendly solution that minimizes human errors, improves inventory tracking, and supports business growth.

The first release focuses on core inventory management functionalities, including product management, warehouse management, customer management, inventory transactions, sales invoicing, reporting, and dashboard analytics. The system is designed with scalability in mind to support future enhancements such as supplier management, purchase management, barcode integration, role-based access control, and accounting integration.

2. Business Need
# 2. Business Need

The client currently manages inventory and sales operations using manual processes, which increase the risk of data inconsistency, inventory inaccuracies, delayed reporting, and operational inefficiencies.

As the business grows, managing products, warehouses, inventory movements, customers, sales transactions, and customer balances manually becomes increasingly difficult. The lack of a centralized system limits real-time visibility into inventory availability and makes business decision-making slower and more error-prone.

The Inventory Management System (IMS) is proposed to provide a centralized web-based solution that automates inventory and sales operations, improves data accuracy, enhances operational efficiency, and provides reliable reporting capabilities.

The system will enable users to monitor inventory levels, manage products and warehouses, record inventory transactions, generate sales invoices, manage customer payments, track outstanding customer balances, and access business insights through dashboards and reports.

By replacing manual processes with an integrated solution, the business aims to improve productivity, reduce operational costs, and establish a scalable foundation for future business expansion.

3. Problem Statement
# 3. Problem Statement

The client currently relies on manual methods to manage inventory, customer information, sales transactions, and customer payment records. These manual processes create several operational challenges that negatively impact business efficiency and data accuracy.

The absence of a centralized inventory and sales management system makes it difficult to monitor inventory levels, track inventory movements, generate accurate operational reports, and maintain reliable records of sales and customer payment activities.

Additionally, manual processes increase the likelihood of human errors, duplicate records, inventory discrepancies, and delays in accessing critical business information. As the business continues to grow, these challenges become more significant and reduce the ability to make timely and informed business decisions.

To address these challenges, the business requires a centralized, secure, scalable, and responsive web-based system that improves operational efficiency, ensures data integrity, and provides complete visibility into inventory and sales activities.

4. Project Objectives
# 4. Project Objectives

The primary objectives of the Inventory Management System (IMS) project are:

- Develop a centralized web-based inventory and sales management system that replaces manual business operations.

- Improve inventory accuracy by maintaining real-time product quantities and inventory transaction records.

- Simplify the management of products, categories, measurement units, warehouses, customers, sales invoices, and customer payments through an integrated platform.

- Provide complete traceability for inventory activities, including stock additions, warehouse transfers, product returns, damaged products, inventory adjustments, and inventory counting operations.

- Enable users to generate accurate reports and dashboards that support daily operations and business decision-making.

- Reduce operational errors caused by manual record keeping and disconnected processes.

- Provide a secure, responsive, and user-friendly web application that is accessible through modern desktop and mobile web browsers.

- Deliver a responsive Arabic (RTL) user interface that provides a consistent user experience across desktop and mobile devices.

- Design the system using a scalable architecture that supports future enhancements such as supplier management, purchase management, barcode integration, role-based access control, and accounting integration.

5. Scope
# 5. Project Scope

The first release (Version 1.0) of the Inventory Management System (IMS) will provide the core functionalities required to manage inventory, warehouses, products, customers, sales operations, and inventory movements for a single organization.

The system is intended to replace manual inventory management processes with a centralized web-based application that supports Arabic (RTL) and provides accurate inventory tracking, customer management, sales invoicing, reporting, and business monitoring.

The following modules are included in the scope of Version 1.0.

## 5.1 Authentication

The system shall provide secure authentication for authorized users.

### Features

- Secure user login
- User logout
- Password authentication
- Change password
- Session management

---

## 5.2 Dashboard

The dashboard shall provide a real-time overview of business operations.

### Features

- Inventory Summary
- Total Products
- Total Customers
- Sales Summary
- Outstanding Customer Balances
- Low Stock Alerts
- Recent Inventory Transactions
- Business Statistics

---

## 5.3 Product Management

The system shall allow users to manage inventory products.

### Features

- Create Product
- Update Product Information
- Archive Product
- Search Products
- Assign Product Category
- Assign Warehouse
- Manage Optional Product Attributes such as Color and Pattern/Model for products that require these attributes (e.g., carpets).
- Define Purchase Price
- Define Measurement Unit
- Define Minimum Stock Level
- View Current Stock Quantity
- Assign Measurement Unit

---

## 5.4 Category Management

The system shall organize products into categories.

### Features

- Create Category
- Update Category
- Archive Category
- Search Categories

---

## 5.5 Unit Management

The system shall manage measurement units used by products.

### Features

- Create Unit
- Update Unit
- Archive Unit
- Configure Whether Fractional Quantities Are Allowed

---

## 5.6 Warehouse Management

The system shall manage warehouse information.

### Features

- Create Warehouse
- Update Warehouse
- Archive Warehouse
- Store Warehouse Address
- Store Warehouse Phone Number
- View Warehouse Inventory
---

## 5.7 Customer Management

The system shall maintain customer information and account balances.

### Features

- Create Customer
- Update Customer Information
- Archive Customer
- Search by Customer Name
- Search by Mobile Number
- View Purchase History
- View Outstanding Balance
- Store Customer Notes


---


## 5.8 Inventory Management

The system shall record all inventory movements.

### Features

- Opening Balance
- Manual Stock Entry
- Warehouse Transfers
- Product Returns
- Damaged Products
- Inventory Adjustments
- Inventory Count (Stock Count)

---

## 5.9 Sales Management

The system shall support customer sales operations.

### Features

- Create Sales Invoice
- Update Sales Invoice
- View Sales Invoice
- Cancel Sales Invoice
- Print Sales Invoices in a printer-friendly format
- Reprint Modified Invoice
- Automatic Invoice Number Generation
- Cash Sales
- Credit Sales
- Customer Invoice History
- Manual Selling Price Entry

---

## 5.10 Customer Payments

The system shall manage customer debt payments.

### Features

- Record Customer Payments
- View Payment History
- Automatically Update Outstanding Customer Balance
- Print Payment Receipt

---

## 5.11 Reporting

The system shall generate business reports.

### Reports

- Inventory Report
- Warehouse Inventory Report
- Sales Report
- Customer Report
- Customer Outstanding Balance Report
- Inventory Movement Report
- Damaged Products Report
- Inventory Count Report
- Low Stock Report

### Export Formats
- PDF
- Excel

---

## 5.12 Audit Trail

The system shall maintain an audit history for critical business operations.

### Audit Events

- Product Changes
- Customer Changes
- Customer Payment Recording
- Warehouse Changes
- Sales Invoice Creation
- Sales Invoice Modification
- Sales Invoice Cancellation
- Inventory Movement History
- User Login
- User Logout
---

## 5.13 System Settings

The system shall provide basic configuration settings.

### Features

- Company Name
- Company Logo
- Company Address
- Company Phone Number
- Invoice Header Information


6. Out of Scope

# 6. Out of Scope

The following features and capabilities are explicitly excluded from Version 1.0 of the Inventory Management System (IMS).

- Supplier management
- Purchase management and purchase orders
- Barcode generation and barcode scanning
- QR code integration
- Role-based access control (all users have the same permissions in Version 1.0)
- Multi-language support (the system supports Arabic only)
- Multi-company support
- Accounting system integration
- Payment gateway integration
- SMS notifications
- Email notifications
- Mobile application (Android/iOS)
- Offline mode
- Automatic cloud backup
- Advanced analytics and business intelligence


7. Stakeholders

# 7. Stakeholders

The following stakeholders are involved in the Inventory Management System (IMS) project.

| Stakeholder | Role | Responsibility |
|-------------|------|----------------|
| Client | Project Sponsor | Defines business requirements, reviews deliverables, approves project milestones, performs User Acceptance Testing (UAT), and accepts the final system. |
| End Users | System Users | Use the system for daily inventory, customer, sales, and payment operations, and provide operational feedback during User Acceptance Testing (UAT). |
| Project Developer | System Analyst, Software Engineer, and Technical Lead | Responsible for requirements analysis, system architecture, database design, development, testing, deployment, documentation, maintenance, and technical support. |

8. High-Level Requirements

# 8. High-Level Requirements

The following high-level requirements define the major system capabilities that shall be delivered in Version 1.0 of the Inventory Management System (IMS).

| ID | Requirement |
|----|-------------|
| HR-001 | The system shall provide secure user authentication for authorized users. |
| HR-002 | The system shall provide a dashboard displaying key business information and inventory statistics. |
| HR-003 | The system shall allow users to manage products and their information. |
| HR-004 | The system shall allow users to manage product categories. |
| HR-005 | The system shall allow users to manage warehouses. |
| HR-006 | The system shall allow users to manage customer information and outstanding balances. |
| HR-007 | The system shall support inventory management operations. |
HR-008 | The system shall support sales operations, including sales invoice management.
| HR-009 | The system shall support customer payment management. |
| HR-010 | The system shall maintain inventory transaction history. |
| HR-011 | The system shall generate operational and business reports. |
| HR-012 | The system shall support printing sales invoices in a printer-friendly format. |
| HR-013 | The system shall maintain an audit trail for critical business activities. |
| HR-014 | The system shall provide system configuration settings. |
| HR-015 | The system shall provide a responsive Arabic (RTL) user interface that supports desktop and mobile web browsers. |

9. Assumptions
# 9. Assumptions

The following assumptions are considered valid for the successful implementation and operation of Version 1.0 of the Inventory Management System (IMS).

- The client will provide a stable internet connection for accessing the web application.

- Users have basic computer literacy and are capable of operating a web-based system.

- All business data entered into the system will be accurate and maintained by authorized users.

- Sales invoices shall be printed on standard A4 paper using a standard office printer.

- The organization operates as a single company using one centralized system.

- Product information, inventory quantities, customer information, sales transactions, and customer payments will be entered manually by system users.

- All users will share the same system permissions in Version 1.0.

- The client will provide timely feedback during requirements clarification, User Acceptance Testing (UAT), and final system acceptance.

10. Constraints

# 10. Constraints

The following constraints shall be considered throughout the design, development, testing, and deployment of Version 1.0 of the Inventory Management System (IMS).

- The target deployment environment uses Windows 10.

- The user interface shall be available in Arabic (RTL) only.

- The application shall be web-based and accessed through a modern web browser.

- The application shall provide a responsive user interface that supports desktop and mobile web browsers.

- Sales invoices shall be designed for printing on standard A4 paper.

- All users shall have the same access permissions in Version 1.0.

- Each product shall belong to only one warehouse at any given time.

- Product data, inventory transactions, customer information, and customer payments shall be entered manually by system users.

11. Risks

# 11. Risks

The following risks have been identified for Version 1.0 of the Inventory Management System (IMS).

| ID | Risk | Impact | Mitigation |
|----|------|--------|------------|
| R-001 | Changes in business requirements during development may increase the project scope, development effort, and delivery timeline. | High | All new requirements shall be documented, reviewed, and treated as change requests after requirements approval. |
| R-002 | Delayed client feedback or approval may postpone development activities and project milestones. | Medium | Schedule regular review meetings, milestone demonstrations, and obtain timely feedback throughout the project. |
| R-003 | Incorrect or incomplete manual data entry may affect inventory accuracy, customer balances, and reporting quality. | Medium | Implement input validation and provide clear user guidance throughout the system. |
| R-004 | Failure to perform regular database backups may result in data loss. | High | Define periodic database backup procedures and provide backup guidance to the client. |
| R-005 | Compatibility limitations of the client environment or unsupported web browsers may affect the user experience. | Medium | Verify compatibility with Windows 10 and supported modern web browsers during testing. |
| R-006 | The responsive user interface may not perform consistently across different mobile devices and screen sizes. | Medium | Perform responsive testing across common desktop and mobile browsers before deployment. |

12. Success Criteria

# 12. Success Criteria

The Inventory Management System (IMS) project will be considered successful when all of the following criteria are achieved.

- The system is successfully deployed and operational in the client's business environment.

- Users can securely access the system using their authorized accounts.

- All agreed functional requirements are implemented and operate according to the approved project documentation..

- Inventory quantities are accurately maintained through all supported inventory operations.

- Users can create, update, print, and cancel sales invoices successfully.

- Customer balances and payment records are accurately maintained.

- The system generates the required reports with accurate and reliable data.

- The user interface is fully available in Arabic (RTL) and provides a responsive experience on desktop and mobile devices.

- Sales invoices are successfully printed on standard A4 paper.

- The client completes User Acceptance Testing (UAT) and formally approves the delivered system.

- End users are able to perform their daily inventory and sales operations without relying on manual record-keeping.

13. Deliverables

# 13. Deliverables

The following deliverables are included within the scope of Version 1.0 of the Inventory Management System (IMS) project.

| ID | Deliverable | Description |
|----|-------------|-------------|
| D-001 | Project Charter | Defines the project vision, scope, objectives, assumptions, constraints, risks, and success criteria. |
| D-002 | Business Rules Specification (BRS) | Documents all approved business rules governing the system. |
| D-003 | Business Requirements Document (BRD) | Defines the approved business requirements for the system. |
| D-004 | Software Requirements Specification (SRS) | Defines the functional and non-functional system requirements. |
| D-005 | Database Design | Defines the database schema, relationships, and data structures. |
| D-006 | API Specification | Documents the application endpoints and request/response contracts. |
| D-007 | UI/UX Specification | Defines the user interface layouts and navigation flow. |
| D-008 | Deployed Web Application | A fully functional Arabic (RTL) web application deployed and configured for the client's business environment. |
| D-009 | Deployment Guide | Documents the deployment and installation procedures. |
| D-010 | User Manual | Provides Arabic instructions for operating the system. |
| D-011 | Tested Production Release | A tested, production-ready release approved through User Acceptance Testing (UAT). |
| D-12 | System Backup & Restore Guide | Documents the recommended database backup and restore procedures. |

14. Milestones

# 14. Milestones

The project will be executed through the following major milestones.

| ID | Milestone | Description |
|----|-----------|-------------|
| M-001 | Project Initiation | Project kickoff, requirements gathering, and initial planning. |
| M-002 | Documentation Completion | Completion and approval of all project documentation, including the Project Charter, BRS, BRD, and SRS. |
| M-003 | System Design | Completion of the database design, system architecture, API specification, and UI/UX specification. |
| M-004 | Development Phase | Implementation of all approved Version 1.0 features. |
| M-005 | System Testing | Functional testing, integration testing, and bug fixing. |
| M-006 | User Acceptance Testing (UAT) | Client validation and approval of the completed system. |
| M-007 | Production Deployment | Deployment of the system to the client's production environment. |
| M-008 | Project Closure | Final delivery, user training, and project handover. |

---

Next Document

Business Rules Specification (BRS)

Purpose

Defines all approved business rules governing the system.

---

15. Approval

# 15. Approval

The undersigned acknowledge that they have reviewed and approved this Project Charter and agree to the project objectives, scope, and responsibilities described in this document.

| Name | Role | Signature | Date |
|------|------|-----------|------|
| Client | Project Sponsor | | |
| Steven Labib | Project Developer | | |


