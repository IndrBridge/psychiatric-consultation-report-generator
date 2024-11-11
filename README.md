#Psychiatric Consultation Report Generator

##Table of Contents

1.Overview
2.Features
3.Prerequisites
4.Installation
5.Configuration
6.Usage
7.Dependencies
8.Troubleshooting
9.Contributing
10.License
11.Contact
12.Quick Start Guide
13.Notes
14.Acknowledgements


Overview

The Psychiatric Consultation Report Generator is a Python application designed to automate the creation of structured psychiatric consultation reports. By utilizing OpenAI's GPT language models, the script reads patient data from an Excel file and generates professional reports in Microsoft Word format. This tool aims to streamline the documentation process for mental health professionals.

Features

-Automated Report Generation: Converts patient data into comprehensive consultation reports.
-Customizable Templates: Reports include standard sections such as Introduction, Patient History, Diagnosis, etc.
-Batch Processing: Handles multiple patient records efficiently.
-Secure API Integration: Interacts with OpenAI's API using environment variables for security.
-Easy Output Management: Saves generated reports in a designated reports directory with timestamped filenames.


Prerequisites

Before you begin, ensure you have met the following requirements:

-Operating System: Windows 10 or later, macOS, or Linux.
-Python: Version 3.7 or higher installed on your system.
-OpenAI Account: An account with OpenAI and a valid API key.
-Excel File: A patient_data.xlsx file containing patient information in the correct format.

Installation

1. Clone the Repository
Clone the repository to your local machine using the following command:

bash
Copy code

git clone https://github.com/IndrBridge/psychiatric-consultation-report-generator.git

Navigate to the project directory:

bash
Copy code

cd psychiatric-consultation-report-generator

2. Set Up a Virtual Environment (Recommended)

Create a virtual environment to manage project dependencies:

bash
Copy code

python -m venv venv

Activate the virtual environment:

Windows:

bash
Copy code

venv\Scripts\activate

macOS/Linux:

bash
Copy code

source venv/bin/activate

3. Install Dependencies
Install the required Python packages using pip:

bash
Copy code

pip install -r requirements.txt

If you don't have a requirements.txt file, install the packages individually:

bash
Copy code

pip install openai pandas python-docx openpyxl

Configuration

1. Set Up Your OpenAI API Key

For security, store your OpenAI API key in an environment variable.

On Windows (Command Prompt):

bash
Copy code

set OPENAI_API_KEY=your-api-key-here

On Windows (PowerShell):
powershell

Copy code

$env:OPENAI_API_KEY="your-api-key-here"

On macOS/Linux:

bash
Copy code

export OPENAI_API_KEY=your-api-key-here

Note: Replace your-api-key-here with your actual OpenAI API key.

2. Prepare the Excel File

Ensure your patient_data.xlsx file is in the project directory and follows this format:

Patient_ID	Name	Age	Gender	Symptoms	Medical_History	Diagnosis	Consultation_Notes
1001	John Doe	45	Male	Anxiety, Insomnia	Hypertension	General Anxiety Disorder	Notes here
1002	Jane Smith	30	Female	Depression	None	Major Depressive Disorder	Notes here

Usage

1. Run the Script

With your virtual environment activated and your API key set, run the script:

bash
Copy code

python generate_reports.py

2. Output

The script will generate Word documents for each patient in the reports directory.
Each file will be named in the format: report_<Patient_ID>_<timestamp>.docx

3. Example Output

bash
Copy code

Report generated for Patient ID: 1001
Report generated for Patient ID: 1002
...

Dependencies

The project uses the following Python libraries:

-openai: To interact with OpenAI's GPT models.
-pandas: For data manipulation and reading Excel files.
-python-docx: To create and manipulate Word documents.
-openpyxl: To read Excel .xlsx files.

Troubleshooting

Common Issues:

1. Missing OpenAI API Key

Error Message:

openai.error.AuthenticationError: No API key provided.

Solution:

Ensure your OPENAI_API_KEY environment variable is set.
Verify that there are no typos in your API key.

2. Insufficient Quota or Rate Limit Exceeded

Error Message:

openai.error.RateLimitError: You exceeded your current quota, please check your plan and billing details.

Solution:

Check your OpenAI account's usage limits.
Upgrade your plan or wait until the rate limit resets.

3. ModuleNotFoundError for Missing Packages

Error Message:

ModuleNotFoundError: No module named 'openai'

Solution:

Install the missing package using pip:

pip install openai

4. Excel File Issues

File Not Found: Ensure patient_data.xlsx is in the project directory.
Incorrect Format: Verify that the Excel file has all the required columns.

Contributing
Contributions are welcome! Please follow these steps:

Fork the Repository

Create a New Branch


git checkout -b feature/your-feature-name
Make Changes

Commit Changes


git commit -m "Add your commit message"
Push to Your Fork


git push origin feature/your-feature-name

Create a Pull Request

License
This project is licensed under the MIT License.

Contact
Author: IndrBridge
Email: indrbridge@gmail.com
For any questions or feedback, please open an issue on the repository or contact me directly.

Quick Start Guide
Clone the Repository

bash
Copy code
git clone https://github.com/IndrBridge/psychiatric-consultation-report-generator.git
cd psychiatric-consultation-report-generator

Set Up Virtual Environment

bash
Copy code

python -m venv venv
venv\Scripts\activate  # On Windows
source venv/bin/activate  # On macOS/Linux

Install Dependencies

bash
Copy code

pip install -r requirements.txt

Set OpenAI API Key

bash
Copy code

set OPENAI_API_KEY=your-api-key-here  # On Windows
export OPENAI_API_KEY=your-api-key-here  # On macOS/Linux

Run the Script

bash
Copy code

python generate_reports.py

Check the Reports

Navigate to the reports directory to find the generated Word documents.

Notes
API Key Security: Do not share your OpenAI API key publicly or commit it to version control.
Environment Variables: Using environment variables is a secure way to manage sensitive information.
OpenAI Costs: Be aware that using the OpenAI API may incur costs depending on your usage and plan.


Acknowledgements
OpenAI: For providing the language models that make this project possible.
Contributors: Thanks to everyone who has contributed to improving this project.
