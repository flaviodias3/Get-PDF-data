## PDF Report Data Extraction

This program extracts data from a PDF report using OCR (Optical Character Recognition) and organizes it into a structured format using pandas DataFrame. The program utilizes the following libraries:

** pandas for data manipulation 
** fitz (PyMuPDF) for handling PDF files
** pytesseract for OCR
PIL (Pillow) for image processing
io and re for input/output and regular expressions
Prerequisites
Ensure you have the following installed:

Python 3.x
Tesseract OCR (Download and install from here)
Required Python libraries:
pip install pandas pymupdf pytesseract pillow
Setup
Set the path to the Tesseract executable in your script:

pytesseract.pytesseract.tesseract_cmd = r'C:\Users\e2023898\AppData\Local\Programs\Tesseract-OCR\tesseract.exe'
Specify the path to your PDF report:

pdf_path = r"V:\TEST CHILLER\PDF\00378721_TALF8NHHBX1T1U1R00_NUOVI_COMPRESSORI_20241108_133955.pdf"
Usage
Import the PDF Report:

Load the PDF and extract the first page.
Extract the image from the page.
Extract and Process the Image:

Remove specific parts of the image (e.g., company logo, text).
Split the image into two parts: upper (test info) and bottom (test data).
Enhance Image Quality:

Increase the size and contrast of the image for better OCR results.
Define Search Areas:

Define the areas on the image where text needs to be extracted.
Extract Text from Defined Areas:

Use OCR to extract text from the specified areas.
Preprocess the image to improve OCR accuracy.
Organize Extracted Text:

Convert the extracted text into a pandas DataFrame for further analysis.

Notes
Ensure the areas defined for text extraction match the layout of your PDF report.
Adjust the image enhancement parameters as needed to improve OCR accuracy.
The program currently processes only the first page of the PDF. Modify the code to handle multiple pages if necessary.
License
This project is licensed under the MIT License.
