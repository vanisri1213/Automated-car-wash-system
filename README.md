
 Automated Car Catalog System for Enhanced Showroom Management

1. Project Overview

The Automated Car Catalog System is a custom ServiceNow application designed for car dealerships to manage catalogs, categories, users, workflows, and notifications.
It automates the process of catalog creation, car fulfillment, approvals, and notifications, reducing manual errors and improving efficiency.

2. Problem Statement

Traditional car dealerships rely on manual processes to handle customer requests, assign tasks, and manage catalogs. This causes:

* Delays in approvals
* Errors in task fulfillment
* Poor tracking of requests

This project solves these challenges using ServiceNow Catalogs, Workflows, and Automation.
3. Objectives

* Automate catalog and car model creation
* Define roles, groups, and access controls
* Enable workflow-based approvals for customer requests
* Provide notifications for approvals, rejections, and booking status

4. Modules and Implementation

Catalog and Categories

* Catalog: Mahendra
* Categories:

  1. Sudden → Polo
  2. XUV → Thar
  3. Sports → XUV700

Catalog Items

* Volkswagen Polo → Compact Hatchback (Price: 70, Recurring: 90)
* Mahindra Thar → Off-road SUV (Price: 150, Recurring: 170)
* Mahindra XUV700 → Premium SUV (Price: 200, Recurring: 211)

5. Roles, Groups and Users

* Role: emp1
* Group: Showroom

  * Manager: Abraham Lincoln
  * Members: Salesperson1, Salesperson2, Salesperson3
* User: Salesperson (emp1 role)
6. Custom Table

* Cars Fulfillment

  * Extended from: Task table
  * Used for workflow task creation
  * Fields: Car Status, Priority, State
7. Workflow Design

Workflow Name: Test (linked to Mahendra Catalog)

Steps:

1. Begin
2. Approval (User = Salesperson)
3. Approval (User = Supervisor)
4. Create Task: Car Company (Table = Cars Fulfillment, State = Closed Complete, Car Status = Ready to Pickup)
5. Create Task: Car Production (Table = Cars Fulfillment, State = Closed Incomplete, Car Status = Deployment Failed)
6. Notification: Booking Notification (to Abraham Lincoln and Showroom group, HTML message)
7. Notification: Car Reject (to Abraham Lincoln and Showroom group, rejection message)
8. End

8. Notifications

Booking Notification (HTML formatted)

* Sent to: Abraham Lincoln and Showroom group
* Subject: Car Showroom
* Message: Dynamic details like \${requested\_for} and \${approval} embedded in styled HTML

Car Reject Notification

* Sent to: Abraham Lincoln and Showroom group
* Subject: Car Showroom
* Message: Car booking approval is rejected

9. Benefits

* Streamlined catalog management
* Automated approval workflow for requests
* Clear task assignment with fulfillment tracking
* Notifications keep managers and staff updated

10. Future Enhancements

* Integration with customer self-service portal for direct bookings
* Add payment gateway integration
* Real-time dashboard analytics for car sales
* AI-based recommendation system for customers

11. Tools and Technologies

* Platform: ServiceNow PDI
* Modules Used: Catalogs, Categories, Roles, Groups, Tables, Workflow Editor, Notifications
* Language: JavaScript (for scripts and validations)

12. Conclusion

The Automated Car Catalog System demonstrates a real-world business use case of ServiceNow beyond ITSM.
By leveraging catalogs, custom workflows, and notifications, the project provides a scalable solution for car showrooms, boosting customer satisfaction and operational efficiency.

Do you also want me to prepare a **step-by-step execution guide** (like a mini-user manual) along with this documentation so you can show both project explanation and how it runs in ServiceNow?
