# Week 3 Day 4 - ERD Problems

This repository contains the logic, relationship mappings, and ERD diagrams for the following case studies:

* Event Management System
* Online Learning Platform
* Hotel Reservation System

The ERD diagrams for all three case studies are included in:

`Week 3 - Day 4 - ERD Problems.drawio.png`

---

# Case Study 1: Event Management System

## Entities

* Venue
* Event
* Attendee
* EventRegistration
* Staff
* EventStaff

---

## Primary Keys and Foreign Keys

### Venue

* venue_id (PK)

### Event

* event_id (PK)
* venue_id (FK)

### Attendee

* attendee_id (PK)

### EventRegistration

* registration_id (PK)
* attendee_id (FK)
* event_id (FK)

### Staff

* staff_id (PK)

### EventStaff

* event_staff_id (PK)
* staff_id (FK)
* event_id (FK)

---

## Relationship Mapping

* One Venue can host many Events → **1:N**
* Events and Attendees → **M:N** solved by `EventRegistration`
* Events and Staff → **M:N** solved by `EventStaff`

---

# Case Study 2: Online Learning Platform

## Entities

* Student
* Course
* Instructor
* Enrollment
* Assignment
* Submission

---

## Primary Keys and Foreign Keys

### Student

* student_id (PK)

### Course

* course_id (PK)
* instructor_id (FK)

### Instructor

* instructor_id (PK)

### Enrollment

* enrollment_id (PK)
* student_id (FK)
* course_id (FK)

### Assignment

* assignment_id (PK)
* course_id (FK)

### Submission

* submission_id (PK)
* student_id (FK)
* assignment_id (FK)

---

## Relationship Mapping

* One Instructor teaches many Courses → **1:N**
* Students and Courses → **M:N** solved by `Enrollment`
* One Course has many Assignments → **1:N**
* One Student has many Submissions → **1:N**
* One Assignment has many Submissions → **1:N**

---

# Case Study 3: Hotel Reservation System

## Entities

* Guest
* Room
* Reservation
* Services
* Services_used

---

## Primary Keys and Foreign Keys

### Guest

* guest_id (PK)

### Room

* room_id (PK)

### Reservation

* reservation_id (PK)
* guest_id (FK)
* room_id (FK)

### Services

* service_id (PK)

### Services_used

* services_used_id (PK)
* reservation_id (FK)
* service_id (FK)

---

## Relationship Mapping

* One Guest can make many Reservations → **1:N**
* One Room can have many Reservations → **1:N**
* Reservations and Services → **M:N** solved by `Services_used`

---

# Diagram Submission

All three ERD diagrams are included in:

`Week 3 - Day 4 - ERD Problems.drawio.png`
