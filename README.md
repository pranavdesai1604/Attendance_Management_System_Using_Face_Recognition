# Attendance_Management_System_Using_Face_Recognition

Welcome to the **Attendance Management System**, a comprehensive solution that leverages facial recognition to automate attendance marking. This project provides both smart (via facial recognition) and manual attendance recording features, along with an admin panel to manage student records efficiently.

---

## Table of Contents
1. [Features](#features)  
2. [Technologies Used](#technologies-used)  
3. [Installation Guide](#installation-guide)  
4. [Usage Guide](#usage-guide)  
5. [License](#license)  

---

## Features
- **Real-time Facial Recognition**: Use your webcam to automatically record attendance.  
- **GUI Interface**: User-friendly graphical interface for seamless interaction.  
- **Smart Attendance**: Automatically recognize and mark attendance based on stored facial data.  
- **Manual Attendance**: Enter attendance details manually for additional flexibility.  
- **Admin Panel**: Manage and view student data directly from the application.  

---

## Technologies Used
- **Python**: Core language for implementation.  
- **Tkinter**: For creating the graphical user interface.  
- **OpenCV**: For face detection and recognition.  
- **Pandas**: For handling CSV files and data analysis.  
- **Pillow**: For image processing.  

---

## Installation Guide

### Prerequisites
1. Install **Python** (version 3.8 or above) from the [official Python website](https://www.python.org/).  
2. Install **VS Code** for code editing and execution.  

---

### Setup Steps

#### 1. Clone the Repository
\`\`\`bash
git clone <repository_url>
cd <project_directory>
\`\`\`

#### 2. Set Up Virtual Environment
Open VS Code and launch the terminal using \`Ctrl + \` (backtick). Run the following commands:
\`\`\`bash
python -m venv venv
venv\Scripts\activate  # Use & .venv\Scripts\Activate.ps1 for PowerShell
\`\`\`

#### 3. Install Dependencies
Upgrade \`pip\` and install the required libraries:
\`\`\`bash
python -m pip install --upgrade pip
pip install opencv-contrib-python numpy pandas matplotlib ipywidgets ipython pillow
\`\`\`

#### 4. Configure Python Interpreter
Press \`Ctrl + Shift + P\` in VS Code, search for **Python: Select Interpreter**, and choose the interpreter from your \`venv\` folder.

---

## Usage Guide

### Launch the Application
Run the following command to start the application:
\`\`\`bash
python main.py
\`\`\`

### Application Workflow

#### 1. Take Images  
Capture images of students for training the model.  
![Take Images](path_to_image/take_images.png)

#### 2. Train Images  
Train the facial recognition model using the captured images.  
![Train Images](path_to_image/train_images.png)

#### 3. Smart Attendance  
Automatically record attendance by recognizing faces.  
![Smart Attendance](path_to_image/smart_attendance.png)

#### 4. Manual Attendance  
Manually enter attendance when necessary.  
![Manual Attendance](path_to_image/manual_attendance.png)

#### 5. Admin Panel  
View and manage registered student details.  
![Admin Panel](path_to_image/admin_panel.png)

### Closing the Application
The app supports a safe exit via the **Close Camera** button or the window close button.

---


# Face Recognition Attendance System

This project is a Face Recognition-based Attendance System that uses OpenCV, Tkinter, and an SQL database to manage student records and attendance. The system provides functionalities for adding, updating, deleting student details, training the face recognition model, and marking attendance through face recognition.

## Features
- **Student Details Management**: Add, update, or delete student details which are saved directly to the SQL database.
- **Face Training**: Capture images of students and train the face recognition model.
- **Attendance Marking**: Once the student's face is recognized, their attendance is marked and stored in a CSV file.
- **GUI**: Developed using Tkinter for a user-friendly interface.
  
## Technologies Used
- **Python 3.11** (Latest stable version of Python)
- **OpenCV** (for face detection and recognition)
- **Tkinter** (for creating the GUI)
- **SQL Database** (to store student details)
- **CSV** (to store attendance)

## Prerequisites
Before running the application, ensure that you have the following installed:
- Python 3.11 (latest stable version of Python)
- SQL database (for example, MySQL or SQLite)

### 1. Clone the repository:
```bash
git clone https://github.com/your-repo/Face-Attendance-Recognition-and-Management.git
cd Face-Attendance-Recognition-and-Management
```

### 2. Install the required Python libraries:
Use the `requirements.txt` file to install all the necessary dependencies. You can install them using pip:

```bash
pip install -r requirements.txt
```

Alternatively, you can manually install the following libraries:
- `opencv-python` for OpenCV
- `opencv-contrib-python` for additional OpenCV features (like `LBPH` face recognition)
- `tkinter` for the GUI
- `mysql-connector` or `sqlite3` for the SQL database connection

### 3. Database Setup:
- Set up a local SQL database (e.g., MySQL or SQLite).
- Create a database to store student details.
- Update the database connection settings in the `database.py` file with your database credentials.

Example of database setup for MySQL:
```sql
CREATE DATABASE attendance_db;

CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    roll_no VARCHAR(50),
    photo_path VARCHAR(255)
);
```

### 4. Running the Application:
1. **Start the app**: 
   Open the terminal and run the `main.py` file to launch the Tkinter-based GUI.
   ```bash
   python main.py
   ```

2. **Add Student Details**: 
   Use the "Student Details" page in the app to add, update, or delete student information. 
   
3. **Take Photos**: 
   Use the "Capture Photos" page to take pictures of students. These photos will be used to train the face recognition model.

4. **Train the Model**: 
   After capturing student images, use the "Train" button to train the face recognition model with the captured images.

5. **Mark Attendance**: 
   Use the "Recognize" page to recognize students based on the trained model. The attendance will be recorded in a CSV file (`attendance.csv`).

## File Structure
```
/face-recognition-attendance-system
│
├── Photos             # All the photos to be used
├── main.py                  # Main application logic (Tkinter GUI)
├── train.py                 # Script for training the face recognition model
├── recognize.py             # Script for recognizing faces and marking attendance
├── attendance.csv           # CSV file to store attendance records
├── student_data.db          # SQL database for student details
└── requirements.txt         # List of dependencies to install
# add the photos in a folder Face_attendance->Project_images(photos), others are to be kept unser the face_recog... folder
```

## Usage
- **Student Details Management**: Allows users to add, update, or delete student details from the system.
- **Face Training**: Allows users to take images of students and train the recognition model.
- **Attendance**: After the student is recognized, their attendance is marked in `attendance.csv`.

### Example Attendance CSV:
```csv
Name, Roll No, Date, Time
John Doe, 1234, 2024-12-08, 09:00
Jane Smith, 5678, 2024-12-08, 09:05
```

## Troubleshooting
- **Error: "No module named Tkinter"**: Ensure that Tkinter is installed. If using Python 3.x, Tkinter should be installed by default.
- **Error: "Could not connect to database"**: Verify that your database credentials are correct and that the database is running.

## Acknowledgments
- OpenCV for face detection and recognition.
- Tkinter for building the GUI.
- SQL for storing student details.
```
---

## License
This project is licensed under the **MIT License**. Feel free to use, modify, and distribute it as per the terms of the license.

---
