# PDF Watermarking Script Documentation

## Overview

This Python script utilizes the PyPDF2 library to add a watermark to each page of a PDF document. The watermark PDF is overlaid onto a template PDF, creating a watermarked output PDF file.

## Dependencies

- [PyPDF2](https://pythonhosted.org/PyPDF2/): A Python library for reading and manipulating PDF files.

## Usage

### 1. Installation

Ensure that the PyPDF2 library is installed in your Python environment. You can install it using:

```bash
pip install PyPDF2
```

### 2. Script Input

- **Template PDF (`super.pdf`):** The original PDF document on which the watermark will be applied.
- **Watermark PDF (`wtr.pdf`):** The PDF containing the watermark to be applied.

### 3. Script Output

- **Watermarked Output PDF (`watermarked_output.pdf`):** The resulting PDF file with the watermark applied to each page.

### 4. Code Explanation

The script performs the following steps:

- Reads the template PDF (`super.pdf`) and the watermark PDF (`wtr.pdf`) using PyPDF2.
- Creates a new PyPDF2 PdfFileWriter object to store the output.
- Iterates through each page of the template PDF:
  - Retrieves the current page from the template.
  - Merges the page with the first page of the watermark PDF.
  - Adds the merged page to the output PdfFileWriter.
- Writes the final watermarked output to a new PDF file (`watermarked_output.pdf`).

### 5. Running the Script

Execute the script using a Python interpreter. Ensure that the template PDF (`super.pdf`) and watermark PDF (`wtr.pdf`) are present in the script's working directory.

```bash
python watermark_script.py
```

## Note

- This script assumes that the watermark PDF (`wtr.pdf`) contains only one page. If the watermark PDF has multiple pages, additional logic may be required to handle them.
