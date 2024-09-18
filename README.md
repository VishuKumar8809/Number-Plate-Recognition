# Number-Plate-Recognition
Number Plate Recognition Using OCR
This project implements an Automatic Number Plate Recognition (ANPR) system using Optical Character Recognition (OCR) to extract license plate numbers from vehicle images. It integrates OpenCV for image processing and Pytesseract (Tesseract-OCR) for extracting characters from the license plate.

Project Overview
The aim of this project is to recognize vehicle license plates in real-time or from static images, typically used for traffic law enforcement and automated toll systems. By leveraging computer vision techniques and OCR, the system can accurately detect, extract, and read the text on a license plate.

This project focuses on the following tasks:

Image acquisition: Capturing or loading images of vehicles.
Image processing: Preprocessing the image to isolate the number plate.
Character extraction: Using Pytesseract to convert the isolated plate into text.
Post-processing: Refining the recognized text to match license plate formats.

Features
Detects and recognizes vehicle license plates from images.
Uses image processing techniques for better accuracy in detection and recognition.
Low-cost implementation with Raspberry Pi and Camera Module for real-time applications.
Python-based solution integrating OpenCV and Pytesseract.

System Architecture
Input: Image or video stream (captured using a camera or pre-recorded footage).
Preprocessing:
Grayscale conversion
Gaussian blur and bilateral filtering
Edge detection and contour detection
License Plate Detection: Localization of number plate using contour-based techniques.
OCR: Pytesseract extracts characters from the detected number plate region.
Output: The recognized license plate number as a string.

Installation
Prerequisites
Make sure you have Python 3 installed on your machine. Additionally, you'll need the following libraries:

OpenCV
Pytesseract
Numpy
Imutils (optional, for better contour manipulation)
Steps:

Install the required libraries:

pip install opencv-python pytesseract numpy imutils
Install Tesseract OCR:

For Windows: Download and install Tesseract.
For Linux: Install via package manager:

sudo apt-get install tesseract-ocr
Configure Pytesseract: Ensure the path to the Tesseract executable is correctly set in your script:


pytesseract.pytesseract.tesseract_cmd = r'path_to_tesseract.exe'
Usage
Run the script:
python number_plate_recognition.py

Input an image or video stream:

The system will prompt you to input an image file path or use a connected camera to capture the image.
Output:

The system will output the recognized license plate number in the terminal and display the processed image with the detected plate highlighted.
Example


python number_plate_recognition.py --image examples/car.jpg
This will load an image of a vehicle and display the extracted license plate number.

Future Enhancements
Improve detection accuracy in poor lighting and bad weather conditions.
Integrate machine learning models (e.g., YOLO) to enhance object detection.
Deploy the system on edge devices with IoT capabilities for real-time monitoring.
Add a dynamic camera adjustment mechanism to improve recognition in real-time applications.

References
OpenCV documentation: https://opencv.org/
Pytesseract documentation: https://pypi.org/project/pytesseract/
Tesseract-OCR GitHub: https://github.com/tesseract-ocr/tesseract
