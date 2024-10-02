# AI PDF Filler

AI PDF Filler is an advanced Python application designed to automate the process of completing PDF forms using state-of-the-art AI-powered text generation. The software identifies unfilled fields within PDF documents and populates them with contextually appropriate responses based on provided information.

## Key Features

- Intuitive graphical user interface for streamlined file selection and processing
- Sophisticated empty form field detection
- Cutting-edge AI-driven text generation for form completion
- Robust handling of multi-cell input fields
- Comprehensive processing of question and answer sections
- High-fidelity PDF to image conversion for enhanced processing
- Seamless conversion of processed images back to PDF format

## System Requirements

- Python 3.7 or later
- Tesseract OCR engine

### Tesseract OCR Installation Guide

#### Windows
1. Obtain the installer from the [UB-Mannheim Tesseract repository](https://github.com/UB-Mannheim/tesseract/wiki)
2. Execute the installation package
3. Configure your system PATH to include the Tesseract installation directory
4. Update the Tesseract path in `testingcode.py`:
   ```python
   pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
   ```

#### macOS
```bash
brew install tesseract
```

#### Linux
```bash
sudo apt-get install tesseract-ocr
```

## Installation Process

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ai-pdf-filler.git
   cd ai-pdf-filler
   ```

2. Execute the installation script to set up required Python packages:
   ```bash
   python install.py
   ```

   This script will install the following dependencies:
   - opencv-python
   - numpy
   - PyMuPDF
   - pytesseract
   - Pillow
   - transformers
   - torch
   - setuptools

## Usage Instructions

1. Launch the GUI application:
   ```bash
   python gui.py
   ```

2. GUI Operation:
   - Select the input PDF file
   - Choose the context text file containing relevant information
   - Designate an output directory for processed files
   - Initiate processing by clicking "Start Processing"

## Project Architecture

- `gui.py`: Main graphical user interface application
- `testingcode.py`: Core processing logic implementation
- `install.py`: Dependency installation script

## Operational Workflow

1. Conversion of PDF pages to high-resolution images
2. Detection of empty form fields using advanced image processing techniques
3. For each identified empty field:
   - Field name identification
   - AI-powered generation of appropriate text
   - Population of the field with generated content
4. Similar processing applied to Q&A sections
5. Conversion of processed images back to PDF format

## Technical Requirements

Refer to `install.py` for a comprehensive list of Python package dependencies.

## Contribution Guidelines

1. Fork the repository
2. Create a new branch for your proposed feature
3. Commit your changes with clear, descriptive messages
4. Push to the newly created branch
5. Submit a detailed Pull Request for review

## Licensing

This project is distributed under the MIT License. Please see the LICENSE file for full details.

## Acknowledgements

- Tesseract OCR for advanced text recognition capabilities
- OpenCV for sophisticated image processing
- PyMuPDF for robust PDF handling and manipulation
