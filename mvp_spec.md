MedLens MVP Specification

1. Goal

MedLens is a simple AI-powered application that turns patient information and medical reports into a structured, understandable, and reviewable record.

Important: MedLens organizes and explains information only. It does not diagnose conditions or provide treatment recommendations.

2. MVP Features

A. Patient Information

Capture:

Age

Sex

Symptoms

Existing conditions

Allergies

Medications

B. Medical Report Upload

Upload a medical report (PDF/image).

Extract basic laboratory information using AI:

Test name

Value

Unit

Reference range

Date

Observations

C. Structured Results

Display extracted results in a table:

Test

Value

Unit

Reference Range

Status

Hemoglobin

10.2

g/dL

12–15

Low

Status must be calculated only from the reference range present in the uploaded report.

If no reference range is available:
Status: Not determined

D. Provenance

Show where information came from:

User provided

Report extracted

AI generated

Human verified

E. AI Summary

Generate a short, patient-friendly summary of the available information.

The summary must:

Describe reported findings

Use the report's reference ranges

Avoid diagnosis

Avoid medication/dosage recommendations

Clearly mention when information is uncertain or missing

F. Verification

Allow the user to edit extracted values before accepting them.

3. Simple User Flow

Open MedLens

Enter patient information

Upload report

Click Process Report

AI extracts structured information

Review/edit extracted results

View Low / Normal / High status

Generate patient-friendly summary

4. MVP Screens

Home

MedLens name

Short description

Start button

Patient Intake

Patient information form

Continue button

Report Upload

File upload

Process Report button

Loading state

Error state

Patient Record

Patient details

Symptoms/medications

Lab results table

Provenance labels

Verification controls

AI summary

5. Safety Rules

MedLens must NOT:

Provide a definitive diagnosis

Prescribe medication

Recommend dosage changes

Present uncertain information as fact

Invent laboratory reference ranges

MedLens should display a disclaimer:

This information is for organizing and understanding medical records. It is not a medical diagnosis or treatment recommendation. Please consult a qualified healthcare professional for medical decisions.

6. Suggested Simple Tech Stack

Frontend: React

Backend: Node.js/Express or Replit backend

Database: SQLite or simple JSON storage for the demo

AI: Replit-supported AI/API

Deployment: Replit

Keep the architecture simple because this is a time-limited MVP.

7. MVP Demo Data

Use sample data if a real report is not available:

Patient: 45-year-old female

Symptoms: Fatigue, Mild Headache

Hemoglobin: 10.2 g/dL

Reference range: 12–15 g/dL

Status: Low

Do not infer a diagnosis from this result.

8. Definition of Done

The MVP is complete when a user can:

Enter patient information

Upload or use a sample medical report

Extract lab results

See values and source reference ranges

See Low/Normal/High status where a range exists

See provenance

Edit extracted information

Generate a safe patient-friendly summary

Run the complete flow successfully on Replit

9. Priority

If time is extremely limited, implement in this order:

Patient intake

Sample/upload report

Structured lab table

Reference-range status

AI summary

Provenance

Basic editing

Skip authentication, complex database design, advanced analytics, and PDF export unless the core flow is already working.
