# PDF Processing Tool

This repository provides a Python script to extract text, tables, and images from specific pages of a PDF file using *PyMuPDF (fitz)* and *pdfplumber*. It also organizes the extracted images into a designated folder for easy access.

## Features
- Extract text from specified pages of a PDF.
- Identify and extract tables from pages using *pdfplumber*.
- Extract and save images from pages using *PyMuPDF (fitz)*.
- Handles multiple page queries in a user-friendly manner.

## Prerequisites
Make sure you have the following installed:
- Python 3.7 or higher
- pip (Python package manager)

## Installation
1. Clone the repository:
   bash
   git clone https://github.com/yourusername/pdf-processing-tool.git
   cd pdf-processing-tool
   

2. Install the required Python libraries:
   bash
   pip install --upgrade pymupdf pdfplumber
   

3. Create a static directory for output images:
   bash
   mkdir static
   

## Usage

1. Place your PDF file in the desired directory and update the pdf_path variable in the script with the path to your PDF file.

2. Run the script:
   bash
   python script_name.py
   

3. When prompted, enter your query in the format:
   
   page <page_number>
   
   You can specify multiple pages by separating them with commas (e.g., page 1, page 3).

4. The script will:
   - Extract text and tables from the specified pages.
   - Save extracted images in the designated output folder.

## Example
*Input:*

Enter your query: page 1, page 2


*Output:*

Data from page 1:
Text:
<Text extracted from page 1>
No tables found on this page.
Images extracted from this page:
 /content/output/page_1_img1.png

Data from page 2:
Text:
<Text extracted from page 2>
Tables found on this page:

Table 1:
Column1 | Column2 | Column3
Value1  | Value2  | Value3
Images extracted from this page:
 /content/output/page_2_img1.png
 /content/output/page_2_img2.png


## File Structure

.
├── script_name.py       # Main Python script
├── static               # Directory for storing extracted images
├── requirements.txt     # (Optional) List of dependencies
└── README.md            # This file


## Dependencies
- *PyMuPDF (fitz):* For extracting images from the PDF.
- *pdfplumber:* For extracting text and tables from the PDF.
- *os:* To manage directories and file paths.

## Notes
- Ensure the pdf_path and image_output_dir variables are updated with the correct paths before running the script.
- The script gracefully handles invalid queries or page numbers that do not exist in the PDF.

## Contributing
Feel free to submit issues or pull requests if you want to contribute or improve the script.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Author

Email: vasuchouhan1822@gmail.com  
GitHub: [korravasu](https://github.com/korravasu)
