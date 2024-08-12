# Data Flow Diagram (DFD) Documentation

## 0 DFD (Context Diagram)

### Purpose

![Dataflow Diagram 0](T3A2-A-Full-Stack-Project-Part-A-/images/DFD_0.png)

The 0 DFD provides a high-level overview of the system, showing the interactions between external entities and the web application.

### External Entities

1. **User**
   - **Interactions:**
     - Views property availability
     - Makes bookings
     - Submits reviews
     - Receives notifications

2. **Admin**
   - **Interactions:**
     - Manages property listings
     - Manages bookings
     - Manages reviews

### System

- **Web Application**
  - Handles user requests and admin functions.

### Data Flows

1. **User to Web Application:**
   - **Input Flows:**
     - Request for property availability
     - Booking requests
     - Review submissions
     - Authentication requests (registration, login)
   - **Output Flows:**
     - Display of available properties and dates
     - Booking confirmation
     - Review confirmation
     - User profile data

2. **Admin to Web Application:**
   - **Input Flows:**
     - Commands for managing properties, bookings, and reviews
   - **Output Flows:**
     - Updated listings, bookings, and reviews

## 1 DFD (Level 1 DFD)

![Dataflow Diagram 0](T3A2-A-Full-Stack-Project-Part-A-/images/DFD_1.png)

### Purpose

The 1 DFD provides a detailed view of the main processes within the system and their interactions with data stores and external entities.

### Processes

1. **1.1 Viewing Property Availability**
2. **1.2 Booking System**
3. **1.3 Review System**
4. **1.4 Notification System**
5. **1.5 Admin Functions**

### Data Stores

1. **D1: Property Data Store**
   - Stores property details (descriptions, images, availability).

2. **D2: Booking Data Store**
   - Stores booking information (dates, user details).

3. **D3: Review Data Store**
   - Stores user reviews and ratings.

4. **D4: User Data Store**
   - Stores user profiles and authentication details.

### Data Flows

1. **Viewing Property Availability (Process 1.1):**
   - **Input Flows:**
     - User request for property availability
   - **Output Flows:**
     - Display of available properties and dates
   - **Data Interactions:**
     - Fetch data from **Property Data Store** and **Booking Data Store**

2. **Booking System (Process 1.2):**
   - **Input Flows:**
     - User booking request
   - **Output Flows:**
     - Confirmation of booking and updated availability
   - **Data Interactions:**
     - Update **Booking Data Store**
     - Potentially modify **Property Data Store**

3. **Review System (Process 1.3):**
   - **Input Flows:**
     - User review submission
   - **Output Flows:**
     - Confirmation of review submission
   - **Data Interactions:**
     - Save reviews in **Review Data Store**

4. **Notification System (Process 1.4):**
   - **Input Flows:**
     - Triggers based on user actions (e.g., booking confirmation)
   - **Output Flows:**
     - Notification messages sent to users and admins
   - **Data Interactions:**
     - Use notification services for sending messages

5. **Admin Functions (Process 1.5):**
   - **Input Flows:**
     - Admin commands for managing properties, bookings, and reviews
   - **Output Flows:**
     - Updated listings, bookings, and reviews
   - **Data Interactions:**
     - Modify data in **Property Data Store**, **Booking Data Store**, and **Review Data Store**

### Diagram Overview

- **Processes:**
  - **1.1:** Retrieves and displays available properties.
  - **1.2:** Manages booking requests and updates availability.
  - **1.3:** Handles user review submissions.
  - **1.4:** Sends notifications based on user actions.
  - **1.5:** Manages property listings, bookings, and reviews.

- **Data Stores:**
  - **D1:** Contains property details.
  - **D2:** Contains booking information.
  - **D3:** Contains user reviews and ratings.
  - **D4:** Contains user profiles and authentication data.

- **External Entities:**
  - **User:** Interacts with the processes to view properties, make bookings, and leave reviews.
  - **Admin:** Interacts with processes for managing properties, bookings, and reviews.
