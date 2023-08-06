# Volt Car Service

This document contains the details of Web API application `Volt Car Service`.
## Requirements

I want to create an online scheduler website for my car service agency. My agency has many service operators who must take in appointments for customers for a limited time.
A Service operator can take 1-hour appointments for all 24 hours, and they are available 24 x 7 x 365 days (sorry no vacation for them).
If a Service operator is booked for a specific time slot, he obviously cannot take any more customer appointments.

I want to be able to do the following:
- Ability to 'book' an appointment slot by specific Operator or any
- Ability to 'reschedule' or 'cancel' appointment
- Ability to show all booked appointments of an operator. This should display all individual appointments ie. 1-2, 2-3, 3-4
- Ability to show open slots of appointments for an operator. This should merge all consecutive open slots and show as 4-14 instead of 4-5, 5-6 .. 13-14.

Notes/Assumptions:
- number of service operators can be hardcoded to 3 - ServiceOperator0, ServiceOperator1, ServiceOperator2
- Please give an identifier to Appointment Id. This is crucial part of system which allows auditing
- Don't worry about the customer's aspect. Assume that you just have 1 customer who is booking multiple appointments at the same time or at different times of day/week
- I am not concerned with dates as well. Solve the problem for a single day (but ensure your solution can be expanded to work with say weekly schedule or yearly calendar)
- Don't worry about AM/PM. Use 24-hour format as it will greatly simplify your solution too.

## Solution Scope
The solution built have required functional APIs with limited Logging, Error Handling and Deployment steps.
The solution is built just to demonstrate the functions required and to work on localhost only.

## Solution
Built a Java Spring Boot Web API application `volt car service` which contains Web APIs to perform required functions such as book appointment based on available slots, etc.
Have Used MySQL DB as persistent data store.

## Pre-requisites
- Java v17 or above
- MySQL

## Steps to run
- Execute scripts in src/main/resources/schemaCreation.sql to create required schema and sample data.
- Update src/main/resources/application.properties, if required.
- Run Web API application in local.
- Execute APIs in attached postman collection in src/main/resources/VoltCarService.postman_collection.json for test run.


