# Clubfoot Care Connect
### A Web-Based Awareness and Patient Follow-Up Management System

## 📌 About the Project

**Clubfoot Care Connect** is a web-based application designed to provide reliable information about clubfoot and help organize patient records, appointments, and follow-up reminders.

Clubfoot is a congenital condition in which one or both feet turn inward and downward. Treatment may require multiple visits to healthcare professionals and continued follow-up. Access to understandable information and organized appointment management can help families find relevant educational resources and help healthcare staff manage administrative tasks.

This project combines a public educational website with a patient follow-up management system for authorized staff. It is being developed as a final-year project for a Bachelor of Science in Information Technology (BSIT) degree.

The application is intended to support awareness and administrative organization. It does not diagnose medical conditions, prescribe treatment, or replace professional healthcare advice.

---

## 🎯 Project Objectives

The main objectives of Clubfoot Care Connect are:

- Provide reliable and easy-to-understand information about clubfoot.
- Make educational content available in English and Urdu.
- Help authorized healthcare staff manage patient records.
- Organize patient appointments, rescheduling, and cancellations.
- Track appointment and visit statuses.
- Support follow-up through appointment reminders.
- Provide an administrative dashboard for managing records and appointments.
- Develop a user-friendly, responsive, and secure web application.
- Evaluate the application through functional, validation, security, and usability testing.

---

## ❗ Problem Statement

Clubfoot requires appropriate medical assessment and treatment, which may involve repeated healthcare visits and long-term follow-up. Patients and their families need accessible information about the condition, while healthcare staff need an organized way to manage patient records and appointments.

Clubfoot Care Connect aims to address these information and administrative management needs through a single web-based platform. It brings together educational resources, patient record management, appointment scheduling, and follow-up reminder tracking.

The project focuses on developing and testing a functional software prototype rather than claiming to improve clinical outcomes.

---

## ✨ Main Features

### 1. Clubfoot Awareness and Education

The public section of the website is intended to provide general educational information about clubfoot.

Planned content includes:

- Introduction to clubfoot.
- Common signs and basic information about the condition.
- General information about professional assessment and treatment.
- The importance of attending scheduled follow-up appointments.
- Frequently asked questions (FAQs).
- Reliable healthcare information and useful resources.
- English and Urdu language options.

Educational content should be based on credible healthcare sources and reviewed before publication.

### 2. Patient Record Management

Authorized staff will be able to manage patient information through a structured interface.

Planned functions include:

- Registering patient records.
- Viewing and searching existing records.
- Updating patient information.
- Maintaining a unique patient identification code.
- Organizing relevant administrative visit information.
- Restricting access to patient records through staff authentication and permissions.

Only the information necessary for the application's functions should be stored.

### 3. Appointment Management

The appointment module is intended to help staff organize patient visits.

Planned functions include:

- Scheduling appointments.
- Viewing upcoming appointments.
- Rescheduling appointments.
- Cancelling appointments.
- Updating appointment status.
- Tracking scheduled and completed visits.
- Viewing appointment information through the administrative dashboard.

### 4. Follow-Up Reminders

The reminder module is intended to help staff track upcoming appointments.

Planned functions include:

- Identifying upcoming appointments.
- Creating reminder entries according to configured rules.
- Tracking reminder status.
- Displaying reminders in the administrative interface.

Actual SMS, email, or WhatsApp delivery will depend on the implementation and availability of the required services. External messaging integration is optional and is not guaranteed in the initial prototype.

### 5. Administrative Dashboard

The dashboard will provide authorized staff with a central place to manage the system.

Planned functions include:

- Viewing patient and appointment information.
- Accessing patient management features.
- Managing appointment schedules.
- Monitoring upcoming follow-up appointments.
- Viewing basic appointment statistics.
- Managing staff accounts and educational content, where implemented.

### 6. Authentication and Security

The staff-facing system will include security measures appropriate for a student prototype.

Planned measures include:

- Staff login and authentication.
- Role-based access control.
- Password hashing.
- Server-side input validation.
- Prepared SQL statements.
- Restricted access to protected pages and records.
- Appropriate handling of sensitive information.

These measures must be implemented and tested; their inclusion in this README does not imply that the application has already passed a security audit.

---

## 🛠️ Technologies Used

The project is planned around the following technologies:

| Technology | Purpose |
|---|---|
| HTML5 | Structures the website's pages and content. |
| CSS3 | Styles the interface and supports responsive layouts. |
| JavaScript | Adds client-side interactions and form feedback. |
| PHP | Handles server-side logic, authentication, and application functions. |
| MySQL | Stores user accounts, patient records, appointments, and related data. |
| XAMPP | Provides a local development environment with Apache, PHP, and MySQL/MariaDB components. |
| phpMyAdmin | Can be used to create and manage the database through a browser. |
| Figma | Used for interface planning and wireframes, where applicable. |
| Git and GitHub | Used for version control and project hosting. |

The final technology list should reflect the tools actually used in the implementation.

---

## 🏗️ System Modules

The application is organized around the following main modules:

| Module | Description |
|---|---|
| Public Website | Displays general clubfoot awareness information. |
| Educational Content | Organizes health information in English and Urdu. |
| Staff Authentication | Controls access to protected staff functions. |
| Patient Management | Supports patient registration, searching, viewing, and updating. |
| Appointment Management | Supports appointment scheduling and status tracking. |
| Visit Management | Organizes administrative information about patient visits. |
| Reminder Management | Tracks upcoming appointments and reminder status. |
| Admin Dashboard | Provides access to management functions and basic statistics. |

These modules describe the intended system design. Their availability depends on the current implementation.

---

## 🗄️ Proposed Database Structure

The application is expected to use a MySQL database.

The proposed database may contain the following tables:

### 1. `users`

Stores staff account information.

Possible fields:

- `user_id`
- `name`
- `email`
- `password_hash`
- `role`
- `status`

### 2. `patients`

Stores the minimum patient information required by the application.

Possible fields:

- `patient_id`
- `patient_code`
- `date_of_birth`
- `guardian_contact`

### 3. `appointments`

Stores appointment scheduling information.

Possible fields:

- `appointment_id`
- `patient_id`
- `staff_id`
- `appointment_datetime`
- `status`

### 4. `visits`

Stores administrative information about patient visits.

Possible fields:

- `visit_id`
- `patient_id`
- `appointment_id`
- `visit_date`
- `administrative_notes`

### 5. `reminders`

Stores appointment reminder information.

Possible fields:

- `reminder_id`
- `appointment_id`
- `due_datetime`
- `channel`
- `delivery_status`

### 6. `education_content`

Stores educational content for the public website.

Possible fields:

- `content_id`
- `title`
- `language`
- `category`
- `content`
- `reviewed_date`

### 7. `clinics`

Can store verified clinic contact information, if this feature is implemented.

Possible fields:

- `clinic_id`
- `clinic_name`
- `address`
- `verified_contact`

**Note:** This is a proposed database structure. The actual tables and fields may differ depending on the final database design.

---

## 💻 Installation and Setup

Follow these steps to run the project locally if it uses the planned PHP, MySQL, and XAMPP stack.

### Prerequisites

Install the following software:

- XAMPP
- A modern web browser
- A code editor, such as Visual Studio Code
- Git, if you want to clone the repository

### Step 1: Clone the Repository

Open your terminal and run:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

Move into the project directory:

```bash
cd clubfoot-care-connect
```

Alternatively, download the repository as a ZIP file and extract it into your XAMPP `htdocs` directory.

### Step 2: Move the Project into XAMPP

If you downloaded the project separately, place its folder inside:

```text
C:\xampp\htdocs\
```

For example:

```text
C:\xampp\htdocs\clubfoot-care-connect\
```

The folder structure will depend on the files included in your project.

### Step 3: Start XAMPP Services

1. Open the XAMPP Control Panel.
2. Start Apache.
3. Start MySQL.
4. Confirm that both services are running.

### Step 4: Create the Database

1. Open your browser.
2. Visit `http://localhost/phpmyadmin/`.
3. Create a database named:

```text
clubfoot_care_connect
```

4. Import the project's SQL file if one is included.

If the project does not yet contain a database export, create the required tables using your database schema.

### Step 5: Configure the Database Connection

Locate the PHP database connection file in your project.

Configure the connection using your local database settings. For a typical XAMPP development environment, the settings may look like:

```php
$host = "localhost";
$username = "root";
$password = "";
$database = "clubfoot_care_connect";
```

These are example local-development settings, not universal credentials. Adjust them to match your environment.

Do not commit production database credentials or passwords to GitHub.

### Step 6: Open the Application

If the project folder is named `clubfoot-care-connect`, open:

```text
http://localhost/clubfoot-care-connect/
```

If your main PHP file is located in a subfolder, use the appropriate path.

The application should load if Apache, PHP, the database, and the project configuration are set up correctly.

---

## 📁 Suggested Project Structure

A possible folder structure for this project is:

```text
clubfoot-care-connect/
│
├── index.php
├── README.md
├── config/
│   └── database.php
│
├── assets/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── script.js
│   └── images/
│
├── includes/
│   ├── header.php
│   ├── footer.php
│   └── functions.php
│
├── pages/
│   ├── about-clubfoot.php
│   ├── treatment-information.php
│   ├── faqs.php
│   └── contact.php
│
├── auth/
│   ├── login.php
│   └── logout.php
│
├── admin/
│   ├── dashboard.php
│   ├── patients.php
│   ├── appointments.php
│   └── reminders.php
│
├── database/
│   └── clubfoot_care_connect.sql
│
└── tests/
    └── test-cases.md
```

This is an example structure, not a description of files that already exist. Adapt it to your actual project and avoid creating empty folders just to match this example.

---

## 🔒 Privacy and Security

Because the project involves patient-related information, privacy and security are important considerations.

The following practices are recommended:

- Use synthetic or fictional patient records during development and demonstrations.
- Do not upload real patient records to GitHub.
- Do not publish patient photographs or identifiable medical information without appropriate authorization and informed consent.
- Store passwords using secure password-hashing functions.
- Use prepared SQL statements for database operations.
- Validate user input on the server.
- Restrict patient information to authorized staff.
- Check permissions on the server for every protected operation.
- Avoid exposing sensitive information in reminder messages.
- Keep database credentials and secret keys out of the public repository.
- Review educational content for accuracy before publishing it.

A public GitHub repository should contain only code, documentation, and safe example data.

---

## 🧪 Testing and Evaluation

The project is intended to be evaluated through software testing.

### Functional Testing

Check whether:

- Staff can log in and log out.
- Authorized staff can create and update patient records.
- Patient records can be searched.
- Appointments can be scheduled and updated.
- Appointment statuses are saved correctly.
- Reminder entries are generated according to configured rules.
- Dashboard information matches the database.

### Input Validation Testing

Check whether:

- Required fields cannot be left empty.
- Invalid dates are rejected.
- Incorrect input is handled safely.
- Duplicate or inconsistent records are handled appropriately.

### Access-Control Testing

Check whether:

- Invalid login attempts are rejected.
- Public visitors cannot access protected patient records.
- Staff permissions are enforced.
- Unauthorized users cannot perform restricted operations.

### Usability and Responsive Testing

Check whether:

- Navigation is understandable.
- Forms provide clear feedback.
- Pages work on different screen sizes.
- Users can complete common tasks without unnecessary difficulty.

Use fictional data for testing and document the actual results, issues, and limitations.

---

## 🚧 Project Scope and Limitations

### Included in the Proposed Scope

- Clubfoot awareness and educational information.
- English and Urdu educational content.
- Staff login and access control.
- Patient record management.
- Appointment scheduling and status tracking.
- Follow-up reminder tracking.
- Administrative dashboard.
- Software testing and evaluation.

### Outside the Initial Scope

- Automated medical diagnosis.
- AI-based medical recommendations.
- Prescribing medication or treatment.
- Replacing doctors or other healthcare professionals.
- Claims of preventing relapse or improving clinical outcomes.
- Large-scale deployment using real patient data.
- SMS or WhatsApp integration unless it is feasible and implemented as an extension.

The initial version is a student project prototype. Real-world clinical deployment would require additional privacy, security, operational, and healthcare review.

---

## 🔮 Future Enhancements

Possible future improvements include:

- Email or SMS appointment reminders.
- WhatsApp reminder integration, subject to availability and permissions.
- A dedicated parent or caregiver portal.
- Additional language support.
- Improved appointment reports and statistics.
- More advanced role and permission management.
- Online appointment requests.
- Improved accessibility features.
- Deployment on a secure hosting platform after appropriate review.

These are possible extensions, not guaranteed features of the initial version.

---

## 🎓 Project Purpose

Clubfoot Care Connect is being developed as a final-year project in Information Technology.

It combines web development, database management, user interface design, and healthcare information organization in one application.

The project aims to demonstrate how web technologies can be used to present educational information and support administrative workflows while recognizing the importance of privacy, security, and responsible healthcare communication.

---

## 👩‍💻 Developer

**Developer:** [Your Name]  
**Degree Program:** BS Information Technology  
**Project:** Clubfoot Care Connect  
**Project Type:** Final-Year Project  
**Technologies:** HTML, CSS, JavaScript, PHP, MySQL

---

## 📄 License

No license has been selected for this project yet.

If you plan to make the code open source, choose an appropriate license and add a `LICENSE` file. Until then, do not assume that others have permission to reuse or redistribute the project.

---

## ⚠️ Disclaimer

Clubfoot Care Connect is an educational and administrative software project. It is not a medical diagnostic system and does not provide personalized treatment recommendations.

Patients and caregivers should consult qualified healthcare professionals for diagnosis, treatment, and medical advice.