# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Student Name: DHARSHINIYAA KS (212223100004)

## Scenario Chosen:
University / Hospital (choose one)

## ER Diagram:

![ER ](https://github.com/user-attachments/assets/1ed29d51-9886-472a-9503-d6355ddacc90)


## Entities and Attributes:
Student: student_id (PK), name, email, phone, date_of_birth

Course: course_id (PK), course_name, credits, department

Professor: professor_id (PK), name, email, office_number

Department: dept_id (PK), dept_name, building

Enrollment: enrollment_id (PK), grade

Prerequisite: prereq_id (PK)

## Relationships and Constraints:
Student - Enrollment: (1:N, total participation of Enrollment)

Course - Enrollment: (1:N, total participation of Enrollment)

Professor - Course: (1:N, partial participation; a course must have a professor)

Department - Professor: (1:N, partial participation)

Department - Course: (1:N, total participation of Course)

Course - Prerequisite: (1:N, optional participation; a course may have zero or more prerequisites)

## Extension (Prerequisite):
Prerequisites: Modeled as a recursive relationship on the Course entity.
A course can have zero, one, or multiple prerequisite courses.
Example: "Data Structures" may require "Introduction to Programming" as a prerequisite.

## Design Choices:
Entities: Focused on academic structure and key stakeholders — students, professors, courses, and departments.

Relationships: Enrollment captures the many-to-many between Students and Courses. Prerequisites are handled through self-referencing Courses.

Constraints: Students must enroll in courses. Each course must belong to a department.

Assumptions: Each course is taught by one professor, and each professor can teach multiple courses. Departments manage multiple courses and professors.

## RESULT:
The ER diagram was drawn and explained successfully.
