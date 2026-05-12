
# 1. What is Salesforce Platform?

The Salesforce Platform is a cloud-based application development platform that allows businesses to create, manage, and customize applications without installing heavy hardware or software systems. Since it is cloud-based, users can access Salesforce from anywhere using the internet.

Salesforce is widely used in different industries such as:

* Education
* Healthcare
* Banking
* Sales and Marketing
* Customer Service
* Human Resource Management
* Retail and E-commerce

The platform helps organizations manage their business operations efficiently by providing tools for:

* Data storage and management
* Process automation
* Report generation
* User management and security
* Application development
* Customer relationship management (CRM)

One of the biggest advantages of Salesforce is that applications can be developed using both:

* **Configuration** (click-based development)
* **Coding** (programming-based development)

This makes Salesforce suitable for both beginners and advanced developers.

---

# 2. Important Salesforce Concepts

## A. App

An **App** in Salesforce is a collection of tabs, objects, features, and tools designed for a particular business process or department. Apps help users access related functionalities in one place.

Different departments in a company can have different apps according to their needs.

### Examples of Apps

* College Admission App
* Sales App
* HR Management App
* Customer Service App
* Banking Management App

### Purpose of an App

* Organizes business processes
* Provides easy navigation
* Improves user productivity
* Groups related features together

### Example

In a **College Admission App**, users can manage:

* Student details
* Course information
* Admission records
* Faculty information
* Reports and dashboards

---

## B. Object

An **Object** in Salesforce is similar to a database table. It is used to store and manage data.

Each object contains:

* Records (rows)
* Fields (columns)

Objects help organize business information in a structured manner.

### Types of Objects

1. Standard Objects
   Pre-built objects provided by Salesforce
   Examples:

   * Account
   * Contact
   * Opportunity

2. Custom Objects
   Objects created by users according to business requirements
   Examples:

   * Student Object
   * Course Object
   * Admission Object

---

### Examples of Objects in College Admission System

#### 1. Student Object

Stores student-related information.

##### Fields:

* Student Name
* Email
* Phone Number
* Address
* Date of Birth

---

#### 2. Course Object

Stores course-related information.

##### Fields:

* Course Name
* Course Duration
* Course Fees
* Department

---

#### 3. Admission Object

Stores admission details.

##### Fields:

* Admission Number
* Admission Date
* Status
* Selected Course

---

#### 4. Faculty Object

Stores faculty details.

##### Fields:

* Faculty Name
* Department
* Qualification
* Contact Number

---

## C. Tab

A **Tab** in Salesforce is used to open and access objects, records, dashboards, reports, or other features easily.

Tabs provide a user-friendly navigation system inside Salesforce applications.

### Examples of Tabs

* Students Tab
* Courses Tab
* Admissions Tab
* Faculty Tab
* Reports Tab

### Advantages of Tabs

* Easy access to records
* Better navigation
* Improved user experience
* Organized application structure

### Example

When a user clicks on the **Students Tab**, all student records become visible.

---

# 3. Difference Between Configuration and Coding in Salesforce

Salesforce development can be done in two ways:

1. Configuration
2. Coding

Both methods are used to customize applications based on business requirements.

---

## A. Configuration

Configuration means customizing Salesforce using clicks, settings, and built-in tools without writing code.

It is faster and easier to implement.

### Tools Used in Configuration

* Flow Builder
* Validation Rules
* Process Builder
* Page Layouts
* Approval Processes

### Advantages of Configuration

* Easy to learn
* Faster development
* Less maintenance
* No programming knowledge required

### Example

* Creating fields
* Creating reports
* Designing page layouts
* Creating workflows

---

## B. Coding

Coding means customizing Salesforce by writing program code.

Coding is used when business requirements are complex and cannot be achieved through configuration alone.

### Technologies Used

* Apex
* Lightning Web Components (LWC)
* Visualforce
* SOQL

### Advantages of Coding

* Advanced customization
* More flexibility
* Complex automation possible
* Better control over business logic

### Example

* Writing Apex Triggers
* Custom integrations
* Complex calculations
* Dynamic user interfaces

---

## Comparison Table

| Configuration                    | Coding                            |
| -------------------------------- | --------------------------------- |
| Done using clicks and settings   | Done by writing program code      |
| Easy and faster                  | Requires programming knowledge    |
| Uses Flow and Validation Rules   | Uses Apex and LWC                 |
| Less maintenance                 | More customization possible       |
| Suitable for simple requirements | Suitable for complex requirements |
| Example: Creating fields         | Example: Writing Apex Triggers    |

---

# 4. System Design – College Admission Management System

## Project Name

### College Admission Management System

This system is designed to manage the complete admission process of a college using Salesforce.

The application helps:

* Students
* Admin staff
* Faculty members

to manage admission-related activities efficiently.

---

# App Used

## College Admission App

The main app used in the system is the **College Admission App**.

This app contains:

* Student records
* Course details
* Admission information
* Faculty details
* Reports and dashboards

---

# Objects Used in the System

## 1. Student Object

Used to store student information.

### Data Stored:

* Student Name
* Mobile Number
* Email
* Address
* Previous Qualification

---

## 2. Course Object

Used to store course information.

### Data Stored:

* Course Name
* Duration
* Fees
* Available Seats

---

## 3. Admission Object

Used to manage student admissions.

### Data Stored:

* Admission Number
* Admission Status
* Admission Date
* Selected Course

---

## 4. Faculty Object

Used to manage faculty details.

### Data Stored:

* Faculty Name
* Department
* Experience
* Contact Information

---

# User Interaction Flow

The following steps explain how users interact with the system:

---

## Step 1: Student Admission Enquiry

A student visits the college and submits an admission enquiry.

The enquiry may include:

* Name
* Contact details
* Interested course

---

## Step 2: Admin Enters Student Details

The admin logs into Salesforce and creates a student record in the Student Object.

The admin stores:

* Personal details
* Educational information
* Contact information

---

## Step 3: Student Selects Course

The student chooses a course from the available course list.

The selected course is linked to the student admission record.

---

## Step 4: Admission Status Tracking

The admission process is tracked using different statuses such as:

* New
* Under Review
* Approved
* Rejected
* Confirmed

This helps the admin monitor the progress of each application.

---

## Step 5: Faculty and Admin Access Records

Faculty members and administrators can view:

* Student records
* Course details
* Admission information

Access is controlled using Salesforce security and user permissions.

---

## Step 6: Reports and Dashboards

Salesforce reports and dashboards are generated to analyze admission data.

