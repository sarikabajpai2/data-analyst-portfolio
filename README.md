# Event Participation & Performance Analytics Dashboard

## Project Overview

This project analyzes event registration and attendance data to understand participation patterns and event performance.

The dashboard helps management identify which events attract more registrations, how participation varies across departments and cities, and how effectively registrations convert into actual attendance.

## Business Objective

The objective of this analysis is to provide an interactive view of event participation and attendance to support better decisions regarding event planning, employee engagement, and future event strategies.

## Dataset

The dataset contains 800 event registration records covering multiple professional and corporate events across different cities, departments, and employee levels.

### Key Fields

- Registration ID
- Event Name
- Event Category
- Event Date
- Registration Date
- City
- Department
- Employee Level
- Registration Status
- Attendance Status

## Data Preparation

The raw dataset was cleaned and prepared in Microsoft Excel before being imported into Power BI.

The cleaning process included:

- Checking for duplicate records
- Standardizing inconsistent city and department names
- Validating date fields
- Checking registration and attendance status consistency

## Tools & Technologies

- **Microsoft Excel** — Data cleaning and validation
- **Power BI** — Dashboard development and data visualization
- **DAX** — KPI calculations and analytical measures

## Key KPIs

| KPI | Value |
|---|---:|
| Total Registrations | 800 |
| Actual Attendees | 551 |
| Attendance Rate | 77.28% |

## Dashboard Features

- KPI cards for key performance indicators
- Registrations by Event
- Attendance by Event
- Registrations by Department
- Registrations by City
- Monthly Registration Trend
- Registration vs Attendance by Event
- Attendance Rate by Event
- Interactive slicers for Event Category, City, and Department

## DAX Measures

```DAX
Total Registrations = COUNTROWS(Cleaned_Data)

Confirmed Registrations =
CALCULATE(
    COUNTROWS(Cleaned_Data),
    Cleaned_Data[Registration_Status] = "Confirmed"
)

Actual Attendees =
CALCULATE(
    COUNTROWS(Cleaned_Data),
    Cleaned_Data[Attendance_Status] = "Attended"
)

Attendance Rate =
DIVIDE(
    [Actual Attendees],
    [Confirmed Registrations],
    0
)

Key Insights
The dataset contains 800 total registrations and 551 actual attendees.
The overall attendance rate was 77.28% of confirmed registrations.
Corporate Wellness Day recorded the highest number of registrations among the events.
Participation can be compared across events, departments, cities, and months.
Comparing registrations with actual attendance helps identify events with stronger or weaker participation.
Interactive slicers allow users to explore the dashboard based on Event Category, City, and Department.
Skills Demonstrated
Data Cleaning & Validation
Microsoft Excel
Power BI
DAX
Data Visualization
KPI Development
Interactive Dashboard Design
Business Analysis
Data Interpretation
Reporting & Presentation
Project Outcome

This project demonstrates the ability to transform raw business data into a structured, interactive dashboard and communicate meaningful insights through KPIs and visualizations.

