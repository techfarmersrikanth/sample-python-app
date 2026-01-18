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

