## Citizens Complaints & FeedBacks Engagement System

### Project Overview

>This system will user to submit complaints or feedbacks on any sort of public services.

>The system should be able to receive, categorize, and route submissions to the appropriate government agency.
    
>It should also support basic tracking (e.g., ticket status) and allow institutions/government to respond.

### Core Features

* User Complaints Submission
    > * Having a Dashboard for the user to submit complaints and stores data in a database for review
    > * Have category for complaint based on the public services & provide a way for additional agencies of public services



* Categorization & Routing
    > * Having small description that meets their agency so it will be easier for the citizen to find their related complaint
    > * Then linkup or map those small description with their corresponding agency for better code efficiency
    > * Another Option is when the user doesn't find their corresponding complaint, they will have to submit complaint/feedback with their own description(and it will futher be categorized).

    
* Ticket Tracking
    > * Each complaint gets a ticket number.
    > * User can check status using the ticket ID. Same goes for the institution admins.
    > * Status options: “Submitted”, “In Progress”, “Resolved”, “Rejected”


* Admin Interface
    > * Simple login for agency staff
    > * View complaints assigned to them
    > * Change status
    > * Add responses/notes


### Database

    DB_name:
        > engagement_system

                Tables:
        . agencies
        . complaints
        . responses
        . citizen
        . admin

### Project Structure(MVC Style)

    citizen_engagement_system/
    ├── citizen/
    │   ├── signup.php
    │   ├── login.php
    │   ├── dashboard.php
    │   ├── submit.php          # Handles form submission
    │   └── status.php          # Citizen status checker 
    ├── admin/
    │   ├── login.php              # Admin login
    │   ├── dashboard.php          # View complaints
    │   └── respond.php            # Admin response handler
    ├── connection.php             # Database connection
    └── schema.sql                 # MySQL tables
