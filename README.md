
# Flask Application

Flask Event Calendar Application.
This repository contains a Flask web application that functions as a calendar for events. The application allows users to register their events, view their past events, and provides a page with all events. It also includes a user profile page and an event details page that provides additional information about specific events.

## Prerequisites

- Python 3.x installed on your machine
- Pip package manager

## Getting Started

1. Clone the repository to your local machine:

   ```shell
   $ git clone <repository-url>
   ```

2. Navigate to the project directory:

   ```shell
   $ cd Software-flask
   ```

3. Install the required dependencies:

   ```shell
   $ pip install flask
   ```

4. Set up the database:

Event Registration: 

- Users can register events on the platform. 
- The Event Table stores event information, including a unique ID, user ID (the person who created the event), name, date, location, time, information, player number      (playerNR), type of event, and timestamp of the last update.
- Each event is associated with a user who created it.

User Registration: 

- Users can create accounts on the platform. 
- The User Table stores user information, including a unique ID, name, last name, email, password, birthday, and photo name. 
- Users can authenticate using their email and password to access the platform. 
- A connection is established between the user and the event they create. 

Messaging: 
- Users can exchange messages related to events. 
- The Messages Table facilitates a many-to-many relationship between users and events.
- Each message is associated with a user who wrote it and an event it belongs to. 

Attendance: 
- Users can indicate their attendance at events. 
- The Attendance Table establishes a many-to-many relationship between users and events.
- For each event, multiple users can attend, and multiple events can have attendees. 
- The table records the user ID and event ID for attendance tracking.

To configure the project database, the project folder must first contain file.mwb. Open this file and the ERD diagram will appear. This diagram is made by the forward engineer and we expect all the steps to pass automatically.


5. Configuration:

   - Review the configuration file (`config.py`) and modify any necessary settings such as database connection details or API keys.

6. Running the Application:

   - Open a terminal and navigate to the project directory.
   - Execute the following command to start the Flask development server:

     ```shell
     $ flask run
     ```

7. Accessing the Application:

   - Once the server is running, open a web browser and enter the following URL:

     ```
     http://localhost:5000 or http://127.0.0.1:5000
     ```

   - The application should now be running locally on your machine.
