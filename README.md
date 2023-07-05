# VMS Feasibility Report

(I converted my Notion page to Markdown code, here's the original Notion copy: [https://destiny-latency-f6f.notion.site/VMS-feasibility-report-d2b4928183a04269a5411448bb1469ad?pvs=4])

## Introduction

The purpose of this feasibility report is to assess the viability and potential implementation of a Visitor Management System (VMS) with AI features. The system aims to streamline and enhance the visitor management process using artificial intelligence technologies. 

The report will include a list of existing software solutions available in the market, an overview of their functionalities, and key features that can be incorporated into the proposed system.

### Existing Solutions: (3)

1. Envoy Visitors
2. VAMS
3. Condeco

### Need to have features

1. **Facial Recognition** of the visitor. We can tally the new entry with the existing repository of individuals logged into the database. 
   - If someone who is not present in the database shows up, then raise a flag and send notifications to everyone alerting about it.
   - Intelligent Visitor Profiling where one can access their historical data, visiting patterns, and preferences.
2. Integration with Access Control Systems.

## Good To Have Features

1. Suspicious behavior identification system - If any person is detected in possession of firearms, then the system can immediately raise a flag. 
2. Visitor Movement Tracking system - Either with the use of Geolocation or by strategically placing video cameras to implement real-time person tracking. 
3. Personalized Greetings, can be implemented, and customized welcome messages can be sent. 
4. As soon as a visitor signs in, the WiFi credentials are provisioned immediately, and guest network access is granted immediately. 
5. Visitor analytics - Key Data Points are added to the database. 
6. Visitor Pre-Registration - The user can pre-register before turning up for the scheduled appointment. This may lead to a decrease in waiting time in queue management at the reception and an expedited check-in. 
7. Multi-factor authentication - After Facial recognition, one can opt-in for biometric authentication as well. 
8. Dynamic Notification to hosts primarily when visitors arrive. 
9. Attendance tracking system that leverages facial recognition. 
10. Limiting Visitor Count. 
11. Customizing the theme for the product for each company individually. 
12. Booking of shared spaces and resources inside the company area for meetings and other purposes. 
13. Signing of legal documents using the iPad or whatever device we have at the gate. 
14. WhatsApp bot integration for communication. 
15. Alarm if the visit duration exceeds. 
16. Calendar Booking system. 

## User/ Software Journey

1. **Visitor Arrival:** The visitor arrives at the reception area and approaches the visitor management system.
2. **Facial recognition:** The iPad takes care of facial recognition and identification. 
3. Persona Type is assigned based on this request. Important to cross-reference for Blacklists and Watchlists and raise a flag if necessary.
4. **Validation of Employees:** If the visitor is an employee, their request is validated, and important details such as time logged in are recorded. 
5. If the visitor is new, their details are collected, including contact information and purpose of the visit. 
6. Badge Printing: Once all necessary information is gathered, the system generates a visitor badge containing the visitor's details, purpose, and any access restrictions or additional instructions.
7. Visitor Monitoring: The system continuously monitors the visitor's activities, including check-ins and check-outs, to ensure compliance with security protocols and track their location within the premises.
8. Check-out and Data Logging: When the visitor leaves, they go through a check-out process, either manually or automatically. The system records the visitor's departure time for future reference and analytics.
9. Feedback is collected from the visitor. 
10. Reports and Analytics are generated based on the collected data. 

### Access Levels of Persona Type

1. Admin(Super User) Pass
2. Security Pass 
3. Employee Pass 
4. Visitor Pass
5. VIP Pass
6. Special Pass - for emergency   
7. Watchlist
8. Blacklist Detection 

### Project Inspiration if built in React

GitHub Repository: [https://github.com/chinmaykude/atithi-visitor-management-system](https://github.com/chinmaykude/atithi-visitor-management-system)

## Important Test Cases

Note: All errors are shown to the user in the form of a prompt window.

### Visitor Form

- Email for the host and the visitor must not be the same.
- The host must be registered before the visitor can enter their details into the form.
- Already existing visitors are not allowed to re-register.
- Distinction is made based on the email. No two users with the same email can enter the premises at the same time.
- Both phone numbers must be 10-digit Indian phone numbers (beginning digit must be 5-9).

### Checkout Form
    
- Check out only the users that are checked in and have the email in the visitors’ list.
- Checkout is based on email, since it would be unique.

Reference GitHub Repository: [https://github.com/iamakshatjain/Innovacer_entry_management_system](https://github.com/iamakshatjain/Innovacer_entry_management_system)

## Implementation Level Documentation

The implementation level documentation includes competition features and UI. It can be found here: [Implementation Level Documentation](https://docs.google.com/document/d/1qz9gmwR5ELZh7UDKF9NSgxJv0WxzNzaFOjChUN4zUzM/edit)

## Tech Stack

The proposed tech stack for the VMS includes:

- Client Side: React.js, Material UI, Recharts (charting library), Axios (to handle HTTP requests)
- Backend: Node.js, Express.js, MongoDB (NoSQL database), Mongoose (for ODM)
- Authentication: Auth0
- Database: MongoDB (a NoSQL database)
- Integration Architecture: REST API-based communication, Twilio for SMS and notification system, bcrypt for hashing and password management
