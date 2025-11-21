Changes Made from PROGPOE Part 2 to PROGPOE Part 3

This section explains the upgrades, improvements, and new features that were implemented when moving from Part 2 to Part 3 of the PROG6212 Practical Assignment. These changes were based on lecturer feedback and the final POE checklist.

1. Login System Added (NEW)

Part 2:

No authentication system.

All pages were accessible without user restrictions.

Part 3:

A full custom login system was implemented.

Four user roles created:

Lecturer

Programme Coordinator

Academic Manager

HR (Super User)

Session-based authentication added.

Unauthorized users are prevented from accessing pages they should not access.

Benefit:
Secure, role-based workflow that matches real business rules.

 2. HR as Super User (NEW MODULE)

Part 2:

Lecturers and admins stored manually without a management view.

Part 3:

HR can now:

Add lecturers

Update lecturer details

Maintain hourly rates

View all users

Seeder added to automatically populate default lecturers in the database.

Benefit:
Centralized user management as required by the POE checklist.

 3. Auto-Fill Lecturer Information (ENHANCED)

Part 2:

Lecturer typed name, surname and hourly rate manually.

High chance of incorrect information.

Part 3:

Lecturer enters Lecturer ID only.

System auto-fills:

First name

Last name

Hourly rate

AJAX request fetches lecturer details in real time.

Benefit:
Eliminates human error and matches checklist requirement.

 4. Auto-Calculation of Claim Amount (NEW)

Part 2:

Lecturer manually calculated total amount.

Part 3:

Total amount auto-calculated using:
HoursWorked × HourlyRate.

Benefit:
Reduces mistakes and speeds up claim submission.

🔹 5. Validation Rules Enhanced

Part 2:

Limited or no validations.

Part 3:

Full validation added:
✔ 180-hour monthly limit
✔ Required document upload (PDF/DOCX/XLSX)
✔ File size limit (5MB)
✔ Lecturer must exist for auto-fill to work
✔ Model validation for all fields

Benefit:
Higher data accuracy and reduces invalid submissions.

🔹 6. Full Claim Approval Workflow Added (NEW)

Part 2:

No approval system.

Claims were created but not processed.

Part 3:

Coordinator View → Approve / Reject

Manager View → Final Approve / Reject

Lecturer can track claim status

HR can view all approved claims

Benefit:
Multi-step workflow meets professional approval processes.

 7. Proper Database Integration (IMPROVED)

Part 2:

No migrations.

Limited EF Core usage.

Part 3:

SQLite used as main DB

Tables include:

Users

Lecturers

Claims

SupportingDocuments

Seeder implemented for default users + lecturers

Database recreated cleanly when needed

Benefit:
Reliable persistent storage and stable EF Core environment.

 8. Improved UI & Navigation

Part 2:

Basic UI, not consistent.

Part 3:

Updated global layout with:
✔ Styled navigation bar
✔ Visible role indicator
✔ Cleaner forms (Bootstrap 5)
✔ Alerts for errors/success messages

Benefit:
User-friendly and clean design for all user roles.

 9. Security Increased

Part 2:

Users could access pages they shouldn’t.

Part 3:

Added session checks in every controller.

Added redirect to login for unauthorized access.

Menu dynamically updates based on role.

Benefit:
Fully secure and compliant with checklist requirement.


