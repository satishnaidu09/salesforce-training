

# 1. Introduction to Salesforce

Salesforce is a cloud-based Customer Relationship Management (CRM) platform used by organizations to manage customer information, business processes, sales, services, and automation. Salesforce allows companies and educational institutions to store and manage large amounts of data efficiently.

To automate processes and retrieve information from the database, Salesforce provides powerful tools such as:

* **SOQL (Salesforce Object Query Language)**
* **Apex Triggers**

These tools help organizations automate operations, improve productivity, reduce manual work, and maintain accurate records.

---

# 2. What is SOQL?

## Definition

**SOQL (Salesforce Object Query Language)** is a query language used in Salesforce to retrieve records from Salesforce objects. It works similarly to SQL (Structured Query Language) used in traditional databases.

SOQL is specially designed for Salesforce and is used to fetch data from standard objects like:

* Account
* Contact
* Opportunity

and custom objects like:

* Student__c
* Course__c
* Admission__c

SOQL allows users to search, filter, and display records based on specific conditions.

---

# 3. Importance of SOQL

SOQL is very important in Salesforce because it helps users:

* Retrieve required records quickly
* Filter data based on conditions
* Generate reports and dashboards
* Display records inside applications
* Perform automation tasks
* Connect business logic with database records

Without SOQL, it would be difficult to access and manage data stored inside Salesforce.

---

# 4. Basic Structure of SOQL Query

The basic syntax of SOQL is:

```sql id="7iv0rk"
SELECT FieldName
FROM ObjectName
WHERE Condition
```

### Explanation

* **SELECT** → Used to choose fields
* **FROM** → Specifies the object name
* **WHERE** → Applies conditions

---

# 5. SOQL Query Examples

## Example 1: Show All Students

```sql id="9t5x0v"
SELECT Name
FROM Student__c
```

### Explanation

This query retrieves the names of all students stored in the Student object.

---

## Example 2: Students in Computer Science Course

```sql id="g4ux2v"
SELECT Name, Course__c
FROM Student__c
WHERE Course__c = 'Computer Science'
```

### Explanation

This query displays students who applied for the Computer Science course.

---

## Example 3: Approved Admissions

```sql id="3m31d7"
SELECT Name, Admission_Status__c
FROM Student__c
WHERE Admission_Status__c = 'Approved'
```

### Explanation

This query retrieves students whose admission status is approved.

---

## Example 4: Students with Pending Fees

```sql id="l9y7dh"
SELECT Name, Fee_Status__c
FROM Student__c
WHERE Fee_Status__c = 'Pending'
```

### Explanation

This query displays students who have not completed fee payment.

---

## Example 5: Students with High Marks

```sql id="w5kr88"
SELECT Name, Marks__c
FROM Student__c
WHERE Marks__c > 80
```

### Explanation

This query shows students who scored more than 80 marks.

---

# 6. What is an Apex Trigger?

## Definition

An **Apex Trigger** is a block of Apex code that executes automatically when specific events occur on Salesforce records.

Triggers help automate business operations whenever records are:

* Created
* Updated
* Deleted
* Restored

Apex Triggers are mainly used when business requirements cannot be achieved using only declarative tools like Flow or Process Builder.

---

# 7. Why Are Triggers Important?

Triggers are important because they help organizations:

* Automate repetitive tasks
* Maintain data consistency
* Validate information
* Send notifications automatically
* Update related records
* Reduce manual work
* Improve system efficiency

Triggers allow Salesforce applications to react automatically whenever data changes occur.

---

# 8. Trigger Events in Salesforce

Salesforce supports different trigger events:

| Trigger Event  | Description                          |
| -------------- | ------------------------------------ |
| before insert  | Runs before a new record is saved    |
| after insert   | Runs after a new record is saved     |
| before update  | Runs before updating a record        |
| after update   | Runs after updating a record         |
| before delete  | Runs before deleting a record        |
| after delete   | Runs after deleting a record         |
| after undelete | Runs after restoring deleted records |

---

# 9. Basic Syntax of Apex Trigger

```apex id="72a5x7"
trigger StudentTrigger on Student__c (before insert) {

    for(Student__c stu : Trigger.new){

    }

}
```

---

# 10. Difference Between Before Trigger and After Trigger

| Before Trigger                                | After Trigger                              |
| --------------------------------------------- | ------------------------------------------ |
| Executes before saving records into database  | Executes after records are saved           |
| Used for validation and updating field values | Used for notifications and related records |
| Faster for modifying records                  | Useful when record ID is needed            |
| Can change field values directly              | Cannot directly change same record values  |
| Example: Generate Student ID                  | Example: Send confirmation email           |

---

# 11. Detailed Trigger Use Cases

## 1. Automatic Student ID Generation

### Purpose

Generate a unique Student ID automatically whenever a new student record is created.

### Example Trigger

```apex id="ohc71m"
trigger StudentIDTrigger on Student__c (before insert) {

    for(Student__c stu : Trigger.new){

        stu.Student_ID__c = 'STU-' + System.currentTimeMillis();

    }

}
```

### Explanation

* The trigger runs before inserting records.
* A unique Student ID is automatically assigned.
* Manual entry is avoided.
* Duplicate IDs are prevented.

---

# 12. Seat Count Update Trigger

## Purpose

Reduce available seats automatically after student admission confirmation.

### Example Trigger

```apex id="63n7mk"
trigger SeatUpdateTrigger on Admission__c (after insert) {

    // Logic for reducing seat count

}
```

### Explanation

* When admission is confirmed, available seats decrease automatically.
* Helps maintain accurate seat availability.
* Prevents overbooking.

---

# 13. Admission Status Notification Trigger

## Purpose

Send notifications when admission status changes.

### Example Trigger

```apex id="y8t8b9"
trigger AdmissionNotification on Admission__c (after update) {

    // Logic for notification

}
```

### Explanation

* Students receive updates immediately.
* Improves communication.
* Reduces manual follow-up work.

---

# 14. Fee Payment Reminder Trigger

## Purpose

Automatically remind students about pending fees.

### Example Trigger

```apex id="qz4g7x"
trigger FeeReminderTrigger on Student__c (after update) {

    // Logic for fee reminder

}
```

### Explanation

* Detects pending payments.
* Sends reminder notifications or emails.
* Helps institutions collect fees on time.

---

# 15. Attendance Warning Trigger

## Purpose

Generate warnings when student attendance becomes low.

### Example Trigger

```apex id="8h4g9r"
trigger AttendanceWarning on Attendance__c (after insert, after update) {

    // Logic for attendance warning

}
```

### Explanation

* Monitors attendance percentage automatically.
* Sends warning messages to students.
* Helps improve attendance management.

---

# 16. Real-Life Importance of Apex Triggers

Apex Triggers are widely used in real-world enterprise systems because they allow systems to react automatically to business events.

### Examples

* Banking systems sending transaction alerts
* E-commerce websites updating stock automatically
* Hospitals updating patient records
* Schools managing admissions and attendance
* Companies sending approval notifications

Automation reduces human effort and increases reliability.

---

# 17. Reflection: Why Enterprise Systems React Automatically to Data Changes

Modern organizations handle huge amounts of information every day. Managing these records manually is difficult, time-consuming, and may lead to errors.

Enterprise systems react automatically to data changes because automation provides many benefits.

## Benefits of Automatic Reactions

### 1. Faster Processing

Systems update records instantly without waiting for human action.

### 2. Reduced Errors

Automation minimizes mistakes caused by manual work.

### 3. Improved Efficiency

Employees save time and focus on important tasks.

### 4. Better Communication

Notifications and updates are sent automatically.

### 5. Data Accuracy

Business rules are applied consistently.

### 6. Real-Time Updates

Information remains current across departments.

### 7. Improved Customer Service

Organizations respond faster to customer or student needs.

---
