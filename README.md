# QR-CODE-SCANNER
This is a simple Python application that uses your computer's webcam to scan and decode QR codes in real time. It uses the opencv-python library to access the camera and pyzbar library to decode the QR codes.

Features
Real-time QR code scanning using your webcam.
Displays the decoded QR code data on the screen.
Draws a rectangle around the QR code for easy identification.
Simple and easy to use.
Requirements
Python 3.x
OpenCV
pyzbar
Installation
Follow these steps to set up the QR code scanner on your machine.

1. Clone the Repository
If you haven't already, clone this repository to your local machine using:

bash
Copy code
git clone https://github.com/IkigaiAndra/QR-CODE-SCANNER-python.git
cd qr-code-scanner-python
2. Install Dependencies
You'll need to install the required Python libraries. You can do this by running the following command:

bash
Copy code
pip install opencv-python pyzbar
3. (Optional) Create a Virtual Environment
It's recommended to use a virtual environment to avoid conflicts with other Python projects. Here's how you can create and activate a virtual environment:

For Windows:

bash
Copy code
python -m venv venv
venv\Scripts\activate
For macOS/Linux:

bash
Copy code
python3 -m venv venv
source venv/bin/activate
After activation, you can install dependencies as mentioned in step 2.

4. Install Additional Libraries (Optional)
If you encounter any issues with numpy (a dependency of OpenCV), you can install it manually:

bash
Copy code
pip install numpy
Usage
Run the Scanner: After installing all dependencies, run the following Python script to start the QR code scanner:

bash
Copy code
python qr_code_scanner.py
Scan QR Codes: The application will open a camera window. Point your webcam at a QR code, and it will be automatically detected and decoded.

Exit the Scanner: Press the q key to exit the application.

Script Details
qr_code_scanner.py: This Python script initializes the camera, continuously captures frames, and uses the pyzbar library to detect and decode QR codes in real time. The decoded data is displayed on the screen.
How It Works
The program captures video from your webcam using OpenCV.
Each frame is processed to detect any QR codes.
If a QR code is detected, a green rectangle is drawn around it, and the decoded data is displayed above the QR code.
You can press q to stop the scanner and close the camera window.
Troubleshooting
Error with cv2.VideoCapture(0): If the camera is not recognized or an error occurs when accessing it, try using different integers (0, 1, etc.) in the cv2.VideoCapture() function to select the correct camera.

Issues with QR Code Detection: Make sure the QR code is clear and well-lit. If the camera resolution is too low, it might not be able to scan QR codes properly.
