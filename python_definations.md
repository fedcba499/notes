## What is decorator?
Decorate mean to enhance the appearance of something by adding something unessential.
- Painting building
- Adding lights, screens etc to event

> Decorator in Python implies - a function that takes another function as an argument and returns a new function with enhanced functionality.

## What is requirement of VIrtual Environments?
The more Python projects you have, the more likely it is that you need to work with different versions of Python libraries, or even different version of Python itself. Newer versions of libraries for one project can break compatibility in another project.

Virtual environments are used to create independent groups of Python libraries, one for each project. Packages installed for one project will not affect other projects or the operating system’s packages.

## Web Apps Python Library

Streamlit | For Single Page Web Apps ( Interactive)
--- | --- 
Gradio | Mainly used displaying ML Models
Flask | Multiple Web Pages, has routing feature 

## Python Library for OCR

pytesseractOCR | Light | Less Accurate
--- | --- | ---
EasyOCR | Medium | Good Accuracy
PaddleOCR | Heavy | Best Accurarcy

## Best Practises of Python
### Requirements File 
It is good method to use requirements file to use for listing dependency library. In future if we want to rerun program we can uses same set of library which were functional.

### Virtual Environment 
It is good practise to create separate Virtual environment for each project so that has its own dependent library in separate  folder can be added to gitignore.

### Version Control 
To test and add to Main Brach.

## What is IPython?
IPython stands for Interactive Python is an enhanced interactive Python shell designed for interactive computing and exploratory data analysis.

## What is pathlib?
Pathlib is python library introduced from python 3.4, replacing os.path. It is currently the recommended way to operate and use files and directory in python.

## What is pyenv? How does it differ from venv?
pyenv is a Python version management tool that lets you easily install, switch between, and manage multiple Python versions on your system.

venv is Python's built-in virtual environment tool that creates isolated environments for managing packages and dependencies.

