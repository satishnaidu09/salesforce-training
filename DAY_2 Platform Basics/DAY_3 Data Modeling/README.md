# Salesforce Concepts and Data Management

---

# 1. Difference Between App, Object, Record, and Field

Salesforce stores and manages data using different components such as Apps, Objects, Records, and Fields. These components work together to organize business information in a structured manner.

| Term       | Meaning                                                                                | Example                 |
| ---------- | -------------------------------------------------------------------------------------- | ----------------------- |
| **App**    | A collection of related features, tabs, and tools used for a specific business purpose | College Admission App   |
| **Object** | A database table used to store a particular type of information                        | Student Object          |
| **Record** | A single entry or row inside an object                                                 | Rahul’s Student Details |
| **Field**  | Individual pieces of information stored in a record                                    | Name, Phone Number      |

---

## A. App

An **App** is a complete working environment in Salesforce that contains related objects, tabs, reports, dashboards, and other features.

Apps help users work efficiently by grouping all required functionalities together.

### Example:

### College Admission App

This app may contain:

* Student records
* Course details
* Admission management
* Faculty information
* Reports and dashboards

### Benefits of Apps

* Easy navigation
* Better organization
* Improved productivity
* Centralized access to features

---

## B. Object

An **Object** is used to store data in Salesforce. It works similarly to a table in a database.

Each object contains:

* Fields (columns)
* Records (rows)

### Example:

### Student Object

The Student Object stores information related to students.

### Fields in Student Object:

* Student Name
* Mobile Number
* Email
* Address
* Date of Birth

---

## C. Record

A **Record** is a single entry inside an object.

Each record stores complete information about one item.

### Example:

Inside the Student Object:

| Student Name | Phone Number | Course |
| ------------ | ------------ | ------ |
| Rahul Sharma | 9876543210   | BCA    |

This row represents one student record.

---

## D. Field

A **Field** stores a specific piece of information inside a record.

Fields are similar to columns in a database table.

### Examples of Fields:

* Name
* Phone Number
* Email
* Admission Status
* Course Fee

### Types of Fields in Salesforce

* Text Field
* Number Field
* Date Field
* Picklist Field
* Checkbox Field
* Formula Field

---

# 2. Standard Objects vs Custom Objects

Salesforce provides two types of objects:

1. Standard Objects
2. Custom Objects

---

## A. Standard Objects

Standard Objects are pre-built objects already provided by Salesforce for common business processes.

These objects cannot be deleted completely because they are part of the Salesforce system.

### Examples:

* Account
* Contact
* Opportunity
* Lead
* Case

### Purpose:

Used for common CRM activities such as:

* Customer management
* Sales tracking
* Support management

---

## B. Custom Objects

Custom Objects are objects created by users according to specific business requirements.

These objects are fully customizable.

### Examples:

* Student Object
* Course Object
* Admission Object
* Faculty Object

### Purpose:

Used for organization-specific processes such as:

* College management
* Hospital management
* Banking systems
* HR management

---

## Comparison Table

| Standard Objects                        | Custom Objects                  |
| --------------------------------------- | ------------------------------- |
| Already provided by Salesforce          | Created by users                |
| Used for common business data           | Used for business-specific data |
| Examples: Account, Contact, Opportunity | Examples: Student, Course       |
| Cannot be fully removed                 | Can be customized completely    |
| Limited customization                   | High customization possible     |

---

# 3. College Admission Data Model

A **Data Model** represents how objects are connected with each other inside a Salesforce application.

The College Admission Management System contains multiple objects and relationships.

---

# Objects Used

## 1. Student Object

Stores student information.

### Example Fields:

* Student Name
* Email
* Mobile Number
* Address

---

## 2. Course Object

Stores course-related information.

### Example Fields:

* Course Name
* Course Duration
* Fees
* Department

---

## 3. Admission Object

Stores admission details.

### Example Fields:

* Admission Number
* Admission Date
* Admission Status

---

## 4. Faculty Object

Stores faculty information.

### Example Fields:

* Faculty Name
* Department
* Qualification
* Contact Number

---

# Relationships Between Objects

Relationships help connect objects and share related data.

---

## A. Student and Admission Relationship

### Relationship:

One student can apply for many admissions.

### Example:

A student may apply for:

* BCA
* BBA
* MBA

This is called a:

### One-to-Many Relationship

---

## B. Course and Student Relationship

### Relationship:

One course can have many students.

### Example:

The BCA course may contain:

* Rahul
* Priya
* Amit
* Neha

---

## C. Faculty and Course Relationship

### Relationship:

One faculty member can manage multiple courses.

### Example:

Professor Sharma may teach:

* Database Management
* Computer Networks
* Operating Systems

---

# Simple Data Model Diagram

```text
Student ----< Admission >---- Course
                    |
                 Faculty
```

This model shows how objects are connected in the system.

---

# 4. Formula Fields

A **Formula Field** is a special field in Salesforce that automatically calculates values based on other fields.

Users do not need to manually enter values because Salesforce calculates them automatically.

---

# Advantages of Formula Fields

* Reduces manual work
* Improves accuracy
* Saves time
* Automatically updates values

---

# Example 1: Total Fee Calculation

Suppose:

* Course Fee = ₹50,000
* Discount = ₹5,000

The formula field calculates:

\text{Total Fee} = \text{Course Fee} - \text{Discount}

### Result:

₹45,000

---

# Example 2: Full Name Formula

The Full Name field combines:

* First Name
* Last Name

\text{Full Name} = \text{First Name} + \text{Last Name}

### Example:

Rahul + Sharma = Rahul Sharma

---

# Uses of Formula Fields

* Fee calculations
* Age calculations
* Percentage calculations
* Status display
* Full name generation

---

# 5. Validation Rules

Validation Rules are used to prevent users from entering incorrect or invalid data into Salesforce.

If the entered data does not satisfy the rule, Salesforce shows an error message.

---

# Advantages of Validation Rules

* Maintains data accuracy
* Prevents invalid records
* Improves data quality
* Reduces mistakes

---

# Example 1: Phone Number Validation

Condition:
Phone number must contain exactly 10 digits.

### Rule Logic:

If the phone number length is not 10, show an error message.

### Error Message:

“Phone number must contain 10 digits.”

---

# Example 2: Age Validation

Condition:
Student age must be greater than 17.

\text{Age} > 17

### Rule:

If age is less than 17, admission cannot be submitted.

### Error Message:

“Student must be older than 17 years.”

---

# Real-World Uses of Validation Rules

* Mandatory fields checking
* Email format validation
* Date restrictions
* Age restrictions
* Duplicate prevention

---

# 6. Reflection: Why Structured Enterprise Data Matters

In organizations such as colleges, hospitals, banks, and companies, a large amount of data is generated every day.

If this data is not organized properly, several problems can occur:

* Difficulty finding records
* Duplicate data
* Reporting issues
* Incorrect decision-making
* Increased manual work

Structured enterprise data helps organizations manage information in a systematic and efficient way.

---

# Importance of Structured Data

## A. Better Record Management

Structured data allows users to:

* Store records properly
* Search records quickly
* Update information easily

Example:
A college can quickly find a student’s admission details.

---

## B. Improved Reporting and Analytics

Structured data helps generate:

* Reports
* Dashboards
* Performance analysis

Example:
Management can view:

* Total admissions
* Course popularity
* Student performance

---

## C. Supports Automation

Organized data helps automate business processes such as:

* Admission approvals
* Email notifications
* Fee calculations
* Student status tracking

---

## D. Reduces Errors

Validation rules and structured storage reduce:

* Duplicate entries
* Incorrect information
* Missing data

---

## E. Better Decision-Making

Management can make informed decisions using accurate and organized data.

Example:
A college can decide:

* Which course has highest demand
* Which department needs more faculty
* Future admission planning

---

