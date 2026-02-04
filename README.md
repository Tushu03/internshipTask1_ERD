# internshipTask1_ERD
🏥 Doctor–Patient Appointment & Feedback ER Diagram Explanation

This ER diagram represents a simple medical appointment system where patients book appointments with doctors, and after the visit, they can share their experience or feedback.

👨‍⚕️ Doctor

The Doctor entity stores information about doctors available in the system.

Each doctor has:

a unique doctor_id

name and specialization

contact details (phone, email)

years of experience

👉 One doctor can attend many appointments, but each appointment is linked to only one doctor.

👤 Patient

The Patient entity stores details of people who book appointments.

Each patient has:

a unique patient_id

basic personal information like name, age, gender

contact details

👉 One patient can book multiple appointments, but each appointment belongs to only one patient.

📅 Appointment

The Appointment entity acts as a bridge between Doctor and Patient.

It contains:

appointment date and time

appointment status (Booked, Completed, Cancelled)

references to both doctor_id and patient_id

👉 This design ensures:

A doctor and patient are connected only through an appointment

No direct dependency between doctor and patient

⭐ Feedback / Experience

The Feedback entity stores the patient’s experience after an appointment.

It includes:

rating (for example: 1 to 5 stars)

comments or review text

feedback date

reference to appointment_id

👉 Feedback is linked to an appointment, not directly to a doctor or patient.
This ensures:

Only patients who actually attended an appointment can give feedback


👉 Each appointment can have at most one feedback, or none if the patient chooses not to review.
Entity RelationShip Diagram of Doctor And Patient
