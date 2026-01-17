🐾 Animal Rescue Management System
The Animal Rescue Management System is a full-stack web application designed to help animal shelters manage their daily operations. It provides a centralized platform to track animal intakes, adoption records, shelter capacities, and volunteer contributions.

🚀 Features
Animal Tracking: Manage detailed profiles for rescued animals, including species, breed, age, gender, and medical/status tracking.

Adoption Management: Record adoptions and automatically update animal availability.

Shelter Partners: Monitor different shelter locations, their addresses, and current animal capacities.

Volunteer Portal: Maintain a database of volunteers and their contact information.

Data Integrity: Built-in logic to handle cascading deletes (e.g., removing an animal cleans up associated adoption and medical records).

Responsive Design: A clean, modern interface built with Bootstrap 5 that works on desktops and tablets.

🛠️ Tech Stack
Backend: Python & Flask

Database: MySQL

Frontend: Jinja2 Templates, HTML5, CSS3, Bootstrap 5

Database Connector: mysql-connector-python

📂 Project Structure
Plaintext

/
├── app.py                   # Main Flask application and routing
├── config.py                # Database and App configuration
├── requirements.txt         # List of Python dependencies
├── database/                # Database logic layer
│   ├── __init__.py          # Package initialization
│   ├── db_connection.py     # MySQL connection handler
│   ├── animal_queries.py    # CRUD for Animals
│   ├── adoption_queries.py  # CRUD for Adoptions
│   ├── shelter_queries.py   # CRUD for Shelters
│   └── volunteer_queries.py # CRUD for Volunteers
├── templates/               # HTML UI (Jinja2)
│   ├── base.html            # Global layout template
│   ├── index.html           # Dashboard
│   ├── animals.html         # Animals list view
│   └── ...                  # Add/Edit forms for all modules
└── static/
    └── style.css            # Custom UI styling
⚙️ Setup & Installation
1. Prerequisites
Python 3.8+

MySQL Server installed and running

2. Database Configuration
Create a MySQL database named animalrescue.

Open config.py and update the DB_CONFIG dictionary with your MySQL credentials:

Python

DB_CONFIG = {
    'host': 'localhost',
    'user': 'your_username',
    'password': 'your_password',
    'database': 'animalrescue'
}
3. Install Dependencies
Install the required Python packages using the provided requirements.txt:

Bash

pip install -r requirements.txt
4. Run the Application
Start the Flask server:

Bash

python app.py
Visit http://127.0.0.1:5000 in your web browser.

📋 Database Schema Overview
The system relies on the following key tables:

animal: Primary storage for all pet data.

adoption: Linked to animal via animalid.

shelter: Linked to animal to track current housing.

volunteer: Tracks personal details and join dates.

donation/volunteer_assignment: Dependent tables for financial and labor tracking.

🤝 Contributing
Fork the project.

Create your Feature Branch (git checkout -b feature/NewFeature).

Commit your changes (git commit -m 'Add some NewFeature').

Push to the branch (git push origin feature/NewFeature).

Open a Pull Request.

Developed with ❤️ for Animal Welfare.
