## 📌 What is Python?

**Python** is a high-level, easy-to-read programming language used for:
- Web applications
- Automation and scripting
- Data science and machine learning
- APIs and backend services

Python is popular because:
- It has simple and readable syntax
- It has a large ecosystem of libraries
- It works on all major operating systems
- It is widely used in industry and education

---

## 📌 Why is Python used?

Python is used because it:
- Allows fast development
- Requires less code compared to other languages
- Has strong community support
- Is ideal for beginners and professionals

---

## 📌 What is pip?

**pip (Python Package Installer)** is Python’s package management tool.

It is used to:
- Install external Python libraries
- Manage project dependencies
- Download packages from the Python Package Index (PyPI)

Example:
```bash
pip install flask

What is a Virtual Environment?

A virtual environment is an isolated Python workspace that keeps project dependencies separate from the system Python.

It creates a folder inside your project where all installed packages are stored.

This prevents conflicts between projects.

📌 Why use a Virtual Environment?

Using a virtual environment is recommended because it:

Avoids dependency conflicts between projects

Keeps your system Python clean

Makes project setup easy for others

Helps maintain consistent versions

# Sample Python Flask Application

This project demonstrates how to safely run a Python Flask application on Ubuntu using a **virtual environment**, which is the recommended approach on modern Linux systems.

---

## ✅ Correct & Recommended Setup (Virtual Environment)

Modern Ubuntu versions restrict system-wide `pip` installs.  
Using a virtual environment (`venv`) is **safe, clean, and recommended**.

---

## Step 1: Install Required Packages

Update the system and install Python venv support:

```bash
sudo apt update
sudo apt install python3-venv python3-full -y
Step 2: Create a Virtual Environment
From your project folder:

bash
Copy code
python3 -m venv venv
This will create a directory named venv/.

Step 3: Activate the Virtual Environment
bash
Copy code
source venv/bin/activate
You should see something like:

text
Copy code
(venv) ubuntu@ip-172-31-17-82:~/sample-python-app$
This means the virtual environment is active.

Step 4: Install Dependencies
With the virtual environment activated:

bash
Copy code
pip install -r requirements.txt
✅ No error
✅ Safe
✅ Recommended

Step 5: Run the Application
bash
Copy code
python app.py
The Flask server will start successfully.

🌐 Access the Application
Local Machine
Open your browser and visit:

arduino
Copy code
http://localhost:5000
If running on a remote server (e.g., EC2), use:

cpp
Copy code
http://<public-ip>:5000
Make sure port 5000 is allowed in your firewall or security group.

🛑 Stop the Application
Press:

mathematica
Copy code
Ctrl + C
🔚 Deactivate the Virtual Environment
When finished:

bash
Copy code
deactivate
📌 Key Notes
Always use a virtual environment for Python projects

Never install packages globally with pip on Ubuntu

This approach avoids breaking system Python

